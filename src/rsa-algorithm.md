Here's a **rewritten, step-by-step version of the RSA algorithm** for both encryption and decryption, using clear, structured language, suitable for understanding and teaching purposes.

---

## 🔐 **RSA Cryptosystem Algorithm**

*RSA is a public key cryptosystem used for secure communication.*

---

### 🧠 **RSA Key Generation Steps**

1. **Choose two distinct large prime numbers**:
   Let’s call them `p` and `q`.

2. **Compute n** (the modulus):

   $$
   n = p \times q
   $$

3. **Compute Euler's totient function ϕ(n)**:

   $$
   \phi(n) = (p - 1) \times (q - 1)
   $$

4. **Choose a public exponent e**:

   * e must satisfy:

     $$
     1 < e < \phi(n) \quad \text{and} \quad \gcd(e, \phi(n)) = 1
     $$
   * Common choice: `e = 65537`

5. **Compute the private key exponent d**:

   * `d` is the modular inverse of `e` modulo `ϕ(n)`:

     $$
     d \equiv e^{-1} \mod \phi(n)
     $$

✅ **Public key** = `(n, e)`
🔐 **Private key** = `d`

---

### ✉️ **RSA Encryption Algorithm**

Given a **plaintext message `M`**:

1. **Convert the message to numbers**:

   * Translate letters to two-digit numbers (A=00, B=01, ..., Z=25).
   * Combine digits into blocks such that each block number < `n`.

2. **Encrypt each block `m` using the formula**:

   $$
   c = m^e \mod n
   $$

3. **Send the ciphertext `c` to the recipient**.

---

### 🔓 **RSA Decryption Algorithm**

To recover the original message from ciphertext `c`:

1. **Use the private exponent `d`**:

   $$
   m = c^d \mod n
   $$

2. **Convert decrypted numbers back to letters** using the 2-digit encoding.

---

## 🔢 **RSA Example Walkthrough**

### 📌 Example 8: Encrypt “STOP” using (n=2537, e=13)

1. Translate:

   * S = 18, T = 19, O = 14, P = 15
     → Combined: `1819 1415`

2. Encrypt:

   * $c_1 = 1819^{13} \mod 2537 = 2081$
   * $c_2 = 1415^{13} \mod 2537 = 2182$

✅ Encrypted message: `2081 2182`

---

### 📌 Example 9: Decrypt “0981 0461” using d = 937

1. Compute:

   * $m_1 = 0981^{937} \mod 2537 = 0704$
   * $m_2 = 0461^{937} \mod 2537 = 1115$

2. Translate back:

   * 07 = H, 04 = E, 11 = L, 15 = P
     ✅ Message: **HELP**

---

## ⚖️ RSA Summary Table

| Step           | Description                        | Formula                                          |
| -------------- | ---------------------------------- | ------------------------------------------------ |
| Key Generation | Choose p, q, compute n, φ(n), e, d | `n = p×q`, `ϕ(n)=(p−1)(q−1)`, `d ≡ e⁻¹ mod ϕ(n)` |
| Encryption     | `c = m^e mod n`                    |                                                  |
| Decryption     | `m = c^d mod n`                    |                                                  |

---

Would you like me to write this into a Markdown file for your lesson or GitHub repo (`rsa-algorithm.md`)?
