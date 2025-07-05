<template>
  <main
    class="min-h-screen bg-white dark:bg-gray-900 text-gray-800 dark:text-gray-200 transition-colors duration-300 ease-in-out"
  >
    <!-- Header Section -->
    <!-- <UniversityHero /> -->

    <!-- Welcome Section -->
    <section
      class="text-center py-16 px-4 sm:px-6 md:px-20 bg-none bg-gray-50 dark:bg-[#0F172A] duration-300 ease-in-out"
    >
      <!-- Background Video -->
      <video
        autoplay
        muted
        loop
        playsinline
        class="absolute top-0 left-0 w-full h-full object-cover z-0 opacity-85 dark:opacity-15"
      >
        <source
          src="https://media.istockphoto.com/id/1027718724/video/handwritten-formulas-spinning-in-3d-space-on-a-bright-background.mp4?s=mp4-640x640-is&k=20&c=OZhq1lBjCn5IOD_h79W3NqOtVFgpP54Ia6_fT3y3mN0="
          type="video/mp4"
        />
        Your browser does not support the video tag. 
      </video>

      <!-- Content Layer -->
      <div
        data-aos="fade-zoom-in"
        data-aos-easing="ease-in-back"
        data-aos-delay="300"
        data-aos-offset="0"
        class="max-w-7xl mx-auto"
      >
        <h1
          class="text-4xl sm:text-5xl md:text-6xl font-bold text-white dark:text-blue-300 mb-6"
        >
          Welcome to Number Theory & Cryptography
        </h1>
        <p
          class="text-md md:text-xl sm:text-lg max-w-4xl mx-auto text-white dark:text-gray-300 leading-relaxed mb-8"
        >
          Explore the fascinating intersection where mathematical elegance meets
          digital security. Number theory, the mother of modern cryptography,
          provides the mathematical foundation that protects our digital world
          through secure communication, data privacy, and authentication
          systems.
          <a
            class="text-red-400 hover:underline hover:text-red-700 hover:opacity-100 duration-300 ease-in-out opacity-70"
            href="https://www.geeksforgeeks.org/maths/number-theory-used-in-cryptography/"
            target="blank"
            >Learn More</a
          >
        </p>
        <p
          class="text-2xl sm:text-3xl md:text-4xl font-semibold text-green-500 dark:text-blue-300 mb-4"
        >
          Example: About
          <span class="text-red-400 hover:underline hover:text-red-700 hover:opacity-100"
            ><a
              cla4s="hover:underline hover:text-red-700 hover:opacity-100"
              href="https://www.geeksforgeeks.org/computer-networks/rsa-algorithm-cryptography/"
              target="_blank"
              >RSA</a
            ></span
          >
          Algorithm in Cryptography
        </p>
      </div>
      <Carousel data-aos="zoom-in" />
    </section>

    <!-- About Number Theory -->
    <section
      class="py-16 px-4 sm:px-6 md:px-20 bg-white dark:bg-gray-900 duration-300 ease-in-out"
    >
      <div class="max-w-7xl mx-auto grid md:grid-cols-2 gap-12 items-center">
        <div data-aos="fade-right">
          <h2
            class="text-3xl sm:text-4xl font-medium text-gray-800 dark:text-gray-50 mb-4"
          >
            Number Theory: The Foundation of Cryptography
          </h2>
          <p
            class="text-gray-700 dark:text-gray-300 text-base sm:text-lg leading-relaxed mb-6"
          >
            Number theory is the branch of mathematics relating to numbers and
            the rules governing them. It serves as the foundation for modern
            cryptographic algorithms that ensure data privacy, integrity, and
            authenticity in digital communications. Key mathematical concepts
            include:
            <a
              class="text-red-400 hover:underline hover:text-red-700 hover:opacity-100 duration-300 ease-in-out opacity-80"
              href="https://www.geeksforgeeks.org/number-theory/"
              target="blank"
              >Learn More</a
            >
          </p>
          <ul
            class="list-disc ml-6 mt-4 text-gray-700 dark:text-gray-300 space-y-2"
          >
            <li>
              <strong>Prime Numbers:</strong> Used in RSA encryption and key
              generation algorithms
            </li>
            <li>
              <strong>Modular Arithmetic:</strong> Essential for secure
              encryption and decryption processes
            </li>
            <li>
              <strong>Discrete Logarithms:</strong> Foundation for elliptic
              curve cryptography and digital signatures
            </li>
            <li>
              <strong>Greatest Common Divisors (GCD):</strong> Critical for key
              exchange protocols
            </li>
            <li>
              <strong>Euler's Theorem:</strong> Powers RSA algorithm and
              public-key cryptography
            </li>
          </ul>
        </div>
        <img
          data-aos="fade-up"
          src="/src/assets/number.png"
          alt="Mathematical concepts used in cryptography"
          class="rounded-lg shadow-md w-full h-auto"
          loading="lazy"
        />
      </div>
    </section>

    <!-- Real-World Applications -->
    <section
      class="py-16 px-4 sm:px-6 md:px-20 bg-gray-50 dark:bg-gray-900 duration-300 ease-in-out"
    >
      <div class="max-w-7xl mx-auto">
        <h2
          class="text-3xl sm:text-4xl font-semibold text-gray-800 dark:text-gray-50 mb-12 text-center"
        >
          Real-Life Applications of Number Theory in Cryptography
        </h2>

        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          <!-- Secure Online Transactions -->
          <div
            data-aos="zoom-in-right"
            data-aos-delay="300"
            data-aos-duration="500"
            class="bg-white dark:bg-gray-700 p-6 rounded-lg shadow-md hover:shadow-2xl hover:scale-105 transition-transform duration-300 border border-transparent hover:border-gray-300 dark:hover:border-gray-500"
          >
            <div
              class="w-12 h-12 bg-green-500 rounded-full flex items-center justify-center mb-4"
            >
              <span class="text-white text-xl">🛒</span>
            </div>
            <h3
              class="text-xl font-semibold mb-3 text-gray-800 dark:text-white"
            >
              Secure Online Transactions
            </h3>
            <p class="text-gray-600 dark:text-gray-300 text-sm leading-relaxed">
              SSL/TLS protocols use number theory-based cryptographic algorithms
              to protect e-commerce transactions, keeping credit card
              information and personal details safe from unauthorized access
              during online purchases.
              <a
                class="text-red-400 hover:underline hover:text-red-700 hover:opacity-100 duration-300 ease-in-out opacity-80"
                href="https://thelaw.institute/cyberspace-technology-and-social-issues/securing-online-transactions-encryption-protocols-best-practices/"
                target="blank"
                >Learn More</a
              >
            </p>
          </div>

          <!-- Digital Identity Verification -->
          <div
            data-aos="zoom-in"
            data-aos-delay="300"
            data-aos-duration="500"
            class="bg-white dark:bg-gray-700 p-6 rounded-lg shadow-md hover:shadow-2xl hover:scale-105 transition-transform duration-300 border border-transparent hover:border-gray-300 dark:hover:border-gray-500"
          >
            <div
              class="w-12 h-12 bg-blue-500 rounded-full flex items-center justify-center mb-4"
            >
              <span class="text-white text-xl">🔐</span>
            </div>
            <h3
              class="text-xl font-semibold mb-3 text-gray-800 dark:text-white"
            >
              Digital Identity Verification
            </h3>
            <p class="text-gray-600 dark:text-gray-300 text-sm leading-relaxed">
              Digital signatures and Public Key Infrastructure (PKI) systems use
              number theory to verify digital identities, ensuring document
              authenticity and preventing tampering in electronic contracts and
              transactions.
              <a
                class="text-red-400 hover:underline hover:text-red-700 hover:opacity-100 duration-300 ease-in-out opacity-80"
                href="https://www.wallstreetmojo.com/digital-identity-verification/"
                target="blank"
                >Learn More</a
              >
            </p>
          </div>

          <!-- Secure Messaging -->
          <div
            data-aos="zoom-in-left"
            data-aos-delay="300"
            data-aos-duration="500"
            class="bg-white dark:bg-gray-700 p-6 rounded-lg shadow-md hover:shadow-2xl hover:scale-105 transition-transform duration-300 border border-transparent hover:border-gray-300 dark:hover:border-gray-500"
          >
            <div
              class="w-12 h-12 bg-purple-500 rounded-full flex items-center justify-center mb-4"
            >
              <span class="text-white text-xl">💬</span>
            </div>
            <h3
              class="text-xl font-semibold mb-3 text-gray-800 dark:text-white"
            >
              Secure Messaging
            </h3>
            <p class="text-gray-600 dark:text-gray-300 text-sm leading-relaxed">
              End-to-end encryption protocols like Signal and WhatsApp use
              number theory-based algorithms to ensure private communication,
              protecting conversations from unauthorized access by third
              parties.
              <a
                class="text-red-400 hover:underline hover:text-red-700 hover:opacity-100 duration-300 ease-in-out opacity-80"
                href="https://proprivacy.com/privacy-service/comparison/5-secure-private-messengers"
                target="blank"
                >Learn More</a
              >
            </p>
          </div>

          <!-- Data Integrity -->
          <div
            data-aos="zoom-in-right"
            data-aos-delay="300"
            data-aos-duration="500"
            class="bg-white dark:bg-gray-700 p-6 rounded-lg shadow-md hover:shadow-2xl hover:scale-105 transition-transform duration-300 border border-transparent hover:border-gray-300 dark:hover:border-gray-500"
          >
            <div
              class="w-12 h-12 bg-orange-500 rounded-full flex items-center justify-center mb-4"
            >
              <span class="text-white text-xl">⛓️</span>
            </div>
            <h3
              class="text-xl font-semibold mb-3 text-gray-800 dark:text-white"
            >
              Data Integrity & Blockchain
            </h3>
            <p class="text-gray-600 dark:text-gray-300 text-sm leading-relaxed">
              Cryptographic hash functions based on number theory principles
              ensure data integrity in blockchain transactions, creating
              immutable records for cryptocurrencies like Bitcoin and Ethereum.
              <a
                class="text-red-400 hover:underline hover:text-red-700 hover:opacity-100 duration-300 ease-in-out opacity-80"
                href="https://dataautomation.com/how-blockchain-technology-enhances-data-integrity/"
                target="blank"
                >Learn More</a
              >
            </p>
          </div>

          <!-- Password Security -->
          <div
            data-aos="zoom-in"
            data-aos-delay="300"
            data-aos-duration="500"
            class="bg-white dark:bg-gray-700 p-6 rounded-lg shadow-md hover:shadow-2xl hover:scale-105 transition-transform duration-300 border border-transparent hover:border-gray-300 dark:hover:border-gray-500"
          >
            <div
              class="w-12 h-12 bg-red-500 rounded-full flex items-center justify-center mb-4"
            >
              <span class="text-white text-xl">🔑</span>
            </div>
            <h3
              class="text-xl font-semibold mb-3 text-gray-800 dark:text-white"
            >
              Password Security
            </h3>
            <p class="text-gray-600 dark:text-gray-300 text-sm leading-relaxed">
              Advanced password hashing algorithms like bcrypt and Argon2 use
              number theory concepts to protect against brute force attacks and
              secure user authentication systems across web platforms.
              <a
                class="text-red-400 hover:underline hover:text-red-700 hover:opacity-100 duration-300 ease-in-out opacity-80"
                href="https://mellow-sorbet-fcba86.netlify.app/security/hashing.html?utm_source=chatgpt.com"
                target="blank"
                >Learn More</a
              >
            </p>
          </div>

          <!-- Access Control -->
          <div
            data-aos="zoom-in-left"
            data-aos-delay="300"
            data-aos-duration="500"
            class="bg-white dark:bg-gray-700 p-6 rounded-lg shadow-md hover:shadow-2xl hover:scale-105 transition-transform duration-300 border border-transparent hover:border-gray-300 dark:hover:border-gray-500"
          >
            <div
              class="w-12 h-12 bg-indigo-500 rounded-full flex items-center justify-center mb-4"
            >
              <span class="text-white text-xl">🏢</span>
            </div>
            <h3
              class="text-xl font-semibold mb-3 text-gray-800 dark:text-white"
            >
              Secure Access Control
            </h3>
            <p class="text-gray-600 dark:text-gray-300 text-sm leading-relaxed">
              Biometric systems and smart card authentication use number
              theory-based cryptography to secure physical and digital access to
              buildings, networks, and confidential information systems.
              <a
                class="text-red-400 hover:underline hover:text-red-700 hover:opacity-100 duration-300 ease-in-out opacity-80"
                href="https://www.fortinet.com/resources/cyberglossary/access-control"
                target="blank"
                >Learn More</a
              >
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- About Cryptography -->
    <section
      class="py-16 px-4 sm:px-6 md:px-20 bg-white dark:bg-gray-900 duration-300 ease-in-out"
    >
      <div class="max-w-7xl mx-auto grid md:grid-cols-2 gap-12 items-center">
        <!-- Text first on mobile, second on desktop -->
        <div data-aos="fade-up-left" class="order-1 md:order-1">
          <h2
            class="text-3xl sm:text-4xl font-semibold text-gray-800 dark:text-gray-50 mb-4"
          >
            Modern Cryptography in Practice
          </h2>
          <p
            class="text-gray-700 dark:text-gray-300 text-base sm:text-lg leading-relaxed mb-6"
          >
            Cryptography protects digital communication through sophisticated
            mathematical techniques rooted in number theory. Modern
            cryptographic systems secure everything from online banking to
            government communications through:
            <a
              class="text-red-400 hover:underline hover:text-red-700 hover:opacity-100 duration-300 ease-in-out opacity-80"
              href="https://www.geeksforgeeks.org/computer-networks/cryptography-and-its-types/"
              target="blank"
              >Learn More</a
            >
          </p>
          <ul
            class="list-disc ml-6 mt-4 text-gray-700 dark:text-gray-300 space-y-2"
          >
            <li>
              <strong>RSA Encryption:</strong> Uses large prime numbers for
              secure key exchange and digital signatures
            </li>
            <li>
              <strong>Elliptic Curve Cryptography (ECC):</strong> Provides
              strong security with smaller key sizes
            </li>
            <li>
              <strong>Advanced Encryption Standard (AES):</strong> Symmetric
              encryption for high-speed data protection
            </li>
            <li>
              <strong>Hash Functions:</strong> Ensure data integrity and digital
              fingerprinting
            </li>
            <li>
              <strong>Digital Certificates:</strong> Authenticate identities in
              secure communications
            </li>
          </ul>
        </div>

        <!-- Image second on mobile, first on desktop -->
        <img
          data-aos="fade-down-right"
          src="/src/assets/cryptography.png"
          alt="Modern cryptographic systems and algorithms"
          class="order-2 md:order-first rounded-lg shadow-md w-full h-auto"
          loading="lazy"
        />
      </div>
    </section>

    <!-- Key Algorithms Section -->
    <section
      class="py-16 px-4 sm:px-6 md:px-20 bg-gray-50 dark:bg-gray-900 duration-300 ease-in-out"
    >
      <div class="max-w-7xl mx-auto">
        <h2
          class="text-3xl sm:text-4xl font-semibold text-gray-800 dark:text-gray-50 mb-12 text-center"
        >
          Core Cryptographic Algorithms
        </h2>
        <div class="grid md:grid-cols-3 gap-8">
          <!-- RSA Algorithm -->
          <div
            data-aos="flip-left"
            class="bg-gradient-to-br from-blue-50 to-indigo-100 dark:from-gray-700 dark:to-gray-600 p-8 rounded-2xl shadow-lg hover:shadow-2xl transition-all duration-300 transform hover:-translate-y-2"
          >
            <div
              class="w-16 h-16 bg-blue-600 rounded-full flex items-center justify-center mb-6 mx-auto"
            >
              <span class="text-white font-bold text-2xl">RSA</span>
            </div>
            <h3
              class="text-2xl font-semibold text-center mb-4 text-gray-800 dark:text-white"
            >
              RSA Algorithm
            </h3>
            <p
              class="text-gray-700 dark:text-gray-300 text-center leading-relaxed"
            >
              Uses the mathematical difficulty of factoring large prime numbers
              to create secure public-key encryption, forming the backbone of
              internet security and digital signatures.
              <a
                class="text-red-400 hover:underline hover:text-red-700 hover:opacity-100 duration-300 ease-in-out opacity-80"
                href="https://www.geeksforgeeks.org/computer-networks/rsa-algorithm-cryptography/"
                target="blank"
                >Learn More</a
              >
            </p>
          </div>

          <!-- Elliptic Curve Cryptography -->
          <div
            data-aos="zoom-in-up"
            class="bg-gradient-to-br from-purple-50 to-pink-100 dark:from-gray-700 dark:to-gray-600 p-8 rounded-2xl shadow-lg hover:shadow-2xl transition-all duration-300 transform hover:-translate-y-2"
          >
            <div
              class="w-16 h-16 bg-purple-600 rounded-full flex items-center justify-center mb-6 mx-auto"
            >
              <span class="text-white font-bold text-2xl">ECC</span>
            </div>
            <h3
              class="text-2xl font-semibold text-center mb-4 text-gray-800 dark:text-white"
            >
              Elliptic Curve Cryptography
            </h3>
            <p
              class="text-gray-700 dark:text-gray-300 text-center leading-relaxed"
            >
              Leverages discrete logarithms on elliptic curves to provide
              equivalent security with smaller key sizes, making it perfect for
              mobile devices and IoT applications.
              <a
                class="text-red-400 hover:underline hover:text-red-700 hover:opacity-100 duration-300 ease-in-out opacity-80"
                href="https://www.geeksforgeeks.org/ethical-hacking/blockchain-elliptic-curve-cryptography/"
                target="blank"
                >Learn More</a
              >
            </p>
          </div>

          <!-- Diffie-Hellman Key Exchange -->
          <div
            data-aos="flip-right"
            class="bg-gradient-to-br from-green-50 to-emerald-100 dark:from-gray-700 dark:to-gray-600 p-8 rounded-2xl shadow-lg hover:shadow-2xl transition-all duration-300 transform hover:-translate-y-2"
          >
            <div
              class="w-16 h-16 bg-green-600 rounded-full flex items-center justify-center mb-6 mx-auto"
            >
              <span class="text-white font-bold text-2xl">DH</span>
            </div>
            <h3
              class="text-2xl font-semibold text-center mb-4 text-gray-800 dark:text-white"
            >
              Diffie-Hellman Key Exchange
            </h3>
            <p
              class="text-gray-700 dark:text-gray-300 text-center leading-relaxed"
            >
              Uses modular arithmetic and discrete logarithms to enable secure
              key exchange over insecure channels, fundamental to modern secure
              communication protocols.
              <a
                class="text-red-400 hover:underline hover:text-red-700 hover:opacity-100 duration-300 ease-in-out opacity-80"
                href="https://www.geeksforgeeks.org/computer-networks/implementation-diffie-hellman-algorithm/"
                target="blank"
                >Learn More</a
              >
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Call to Action -->
    <section
      class="text-center py-16 px-4 sm:px-6 md:px-20 bg-white dark:bg-gray-900 duration-300 ease-in-out"
    >
      <h2
        class="text-3xl sm:text-4xl font-bold text-gray-800 dark:text-gray-50 mb-6"
      >
        Start The Journey into Mathematical Security
      </h2>
      <p
        class="text-gray-600 dark:text-gray-300 max-w-2xl mx-auto mb-8 text-base sm:text-lg leading-relaxed"
      >
        Whether you're a student, developer, or security professional,
        understanding the mathematical foundations of cryptography is essential
        in our digital age. Explore how number theory protects everything from
        your online banking to social media messages.
      </p>
      <div class="flex justify-center flex-wrap gap-4">
        <router-link
          to="/number-theory"
          @click="scrollToTop"
          class="bg-blue-600 hover:bg-blue-700 text-white px-8 py-4 rounded-lg shadow-md transition-colors duration-300 font-semibold"
          aria-label="Learn about number theory foundations"
        >
          Explore Number Theory
        </router-link>
        <router-link
          to="/cryptography"
          @click="scrollToTop"
          class="bg-green-600 hover:bg-green-700 text-white px-8 py-4 rounded-lg shadow-md transition-colors duration-300 font-semibold"
          aria-label="Discover cryptographic applications"
        >
          Discover Cryptography
        </router-link>
        <router-link
          to="/demos"
          @click="scrollToTop"
          class="bg-purple-600 hover:bg-purple-700 text-white px-8 py-4 rounded-lg shadow-md transition-colors duration-300 font-semibold"
          aria-label="Try interactive demonstrations"
        >
          Interactive Demos
        </router-link>
      </div>
    </section>
    
  </main>
</template>

<script>
import Carousel from "../components/Carousel.vue";
import UniversityHero from "../components/UniversityHero.vue";

export default {
  name: "Home",
  components: {
    Carousel,
    UniversityHero,
  },
  mounted() {
    document.title =
      "Number Theory & Cryptography | Mathematical Foundations of Digital Security";
  },
  methods: {
    scrollToTop() {
      window.scrollTo({
        top: 0,
        // behavior: "smooth",
      });
    },
  },
};
</script>
