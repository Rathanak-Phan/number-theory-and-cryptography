<template>
  <div class="max-w-xl mx-auto bg-white dark:bg-gray-900 text-gray-800 dark:text-gray-200 border rounded-2xl shadow-lg p-6">
    <h2 class="text-2xl font-bold text-blue-600 dark:text-blue-400 mb-4">🔐 RSA Message Encryptor</h2>

    <!-- Key Inputs -->
    <div class="grid grid-cols-2 gap-4 mb-4">
      <div>
        <label class="block text-sm font-medium">Prime p:</label>
        <input type="number" v-model.number="p" />
      </div>
      <div>
        <label class="block text-sm font-medium">Prime q:</label>
        <input type="number" v-model.number="q" />
      </div>
      <div>
        <label class="block text-sm font-medium">Public exponent e:</label>
        <input type="number" v-model.number="e" />
      </div>
      <div>
        <label class="block text-sm font-medium">Message to Encrypt (A–Z):</label>
        <input type="text" v-model="userInput" class="uppercase" />
      </div>
    </div>

    <!-- Key + Encryption Buttons -->
    <div class="flex gap-2 mb-4">
      <button @click="generateKeys" class="flex-1 bg-yellow-500 text-white py-2 rounded-lg hover:bg-yellow-600">🔑 Generate Keys</button>
      <button @click="encryptMessage" class="flex-1 bg-green-500 text-white py-2 rounded-lg hover:bg-green-600">Encrypt</button>
      <button @click="decryptMessage" class="flex-1 bg-purple-500 text-white py-2 rounded-lg hover:bg-purple-600">Decrypt</button>
    </div>

    <!-- Manual Decrypt Input -->
    <div class="mb-4">
      <label class="block text-sm font-medium">🔐 Ciphertext Blocks (space-separated):</label>
      <input v-model="manualCiphertext" placeholder="e.g. 2081 2182" class="w-full px-2 py-1 mt-1 border rounded-md dark:bg-gray-700 dark:text-white" />
      <button @click="decryptManual" class="mt-2 w-full bg-indigo-500 text-white py-2 rounded-lg hover:bg-indigo-600">🔓 Decrypt Manual Input</button>
    </div>

    <!-- Result Display -->
    <div class="text-sm space-y-1">
      <p><strong>n:</strong> {{ n }}</p>
      <p><strong>φ(n):</strong> {{ phi }}</p>
      <p><strong>d (private exponent):</strong> {{ d }}</p>
      <p><strong>Encrypted blocks:</strong> {{ ciphertextBlocks.join(' ') }}</p>
      <p><strong>Decrypted message:</strong> {{ decryptedMessage }}</p>
    </div>

    <pre class="mt-4 p-3 bg-gray-100 dark:bg-gray-800 rounded-lg border border-gray-300 dark:border-gray-700 whitespace-pre-wrap text-sm font-mono">{{ result }}</pre>
  </div>
</template>

<script setup>
import { ref } from 'vue'

// Key inputs
const p = ref(43)
const q = ref(59)
const e = ref(13)

// RSA values
const n = ref(0)
const phi = ref(0)
const d = ref(0)

// Message state
const userInput = ref('STOP')
const ciphertextBlocks = ref([])
const decryptedMessage = ref('')
const result = ref('')

// Manual input for ciphertext
const manualCiphertext = ref('')

// Math helpers
function gcd(a, b) {
  while (b !== 0) [a, b] = [b, a % b]
  return a
}

function modInverse(a, m) {
  let m0 = m, x0 = 0, x1 = 1
  while (a > 1) {
    const q = Math.floor(a / m)
    ;[a, m] = [m, a % m]
    ;[x0, x1] = [x1 - q * x0, x0]
  }
  return x1 < 0 ? x1 + m0 : x1
}

function modPow(base, exponent, modulus) {
  base = BigInt(base) % BigInt(modulus)
  let result = 1n
  exponent = BigInt(exponent)
  while (exponent > 0n) {
    if (exponent % 2n === 1n) result = (result * base) % BigInt(modulus)
    exponent /= 2n
    base = (base * base) % BigInt(modulus)
  }
  return result
}

// Encode A-Z → 00–25
function letterToNumber(text) {
  return text.toUpperCase().split('').map(char => {
    const code = char.charCodeAt(0) - 65
    return code < 10 ? `0${code}` : `${code}`
  }).join('')
}

// Decode 00–25 → A-Z
function numberToLetters(digits) {
  const chars = []
  for (let i = 0; i < digits.length; i += 2) {
    const num = parseInt(digits.slice(i, i + 2))
    chars.push(String.fromCharCode(65 + num))
  }
  return chars.join('')
}

// Generate RSA keys
function generateKeys() {
  n.value = p.value * q.value
  phi.value = (p.value - 1) * (q.value - 1)
  if (gcd(e.value, phi.value) !== 1) {
    result.value = '❌ e must be coprime with φ(n)'
    return
  }
  d.value = modInverse(e.value, phi.value)
  result.value = `✅ Keys generated! Public key: (${e.value}, ${n.value}) | Private key: (${d.value}, ${n.value})`
  ciphertextBlocks.value = []
  decryptedMessage.value = ''
}

// Encrypt
function encryptMessage() {
  if (!n.value || !e.value) {
    result.value = '⚠️ Please generate keys first.'
    return
  }

  let digits = letterToNumber(userInput.value)
  if (digits.length % 4 !== 0) digits += '23' // pad with 'X' → 23

  const blocks = []
  for (let i = 0; i < digits.length; i += 4) {
    const block = digits.slice(i, i + 4)
    const m = BigInt(block)
    const c = modPow(m, BigInt(e.value), BigInt(n.value))
    blocks.push(c.toString())
  }

  ciphertextBlocks.value = blocks
  result.value = `🔐 Encrypted: ${blocks.join(' ')}`
}

// Decrypt encryptedBlocks
function decryptMessage() {
  if (!d.value || !n.value) {
    result.value = '⚠️ Please generate keys first.'
    return
  }

  const decryptedDigits = ciphertextBlocks.value.map(c => {
    const m = modPow(BigInt(c), BigInt(d.value), BigInt(n.value))
    return m.toString().padStart(4, '0')
  }).join('')

  decryptedMessage.value = numberToLetters(decryptedDigits)
  result.value = `🔓 Decrypted: ${decryptedMessage.value}`
}

// Manual decrypt from user-input ciphertext
function decryptManual() {
  if (!d.value || !n.value) {
    result.value = '⚠️ Please generate keys first.'
    return
  }

  const inputBlocks = manualCiphertext.value.trim().split(/\s+/)
  let fullDigits = ''

  for (const block of inputBlocks) {
    const m = modPow(BigInt(block), BigInt(d.value), BigInt(n.value))
    fullDigits += m.toString().padStart(4, '0') // Ensure each block is 4 digits
  }

  decryptedMessage.value = numberToLetters(fullDigits)
  result.value = `🔓 Manual Decrypt: ${decryptedMessage.value}`
}
</script>
