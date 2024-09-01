# Uses-of-Encryption-Techniques
This project explores encryption techniques using Python. It implements two common ciphers, Kamasutra and Caesar, and demonstrates the Diffie-Hellman Key Exchange (DHKE) protocol.
 <h2>Description</h2>
  <p>This README file provides an overview of a cryptography project implemented in Python. The project explores two encryption techniques, Kamasutra and Caesar ciphers, and demonstrates the Diffie-Hellman Key Exchange (DHKE) protocol.</p>

  <h3>Libraries Used</h3>
  <ul>
    <li>NumPy: For numerical operations.</li>
    <li>Matplotlib: For data visualization.</li>
  </ul>

  <h3>Key Features</h3>
  <ul>
    <li>Kamasutra Cipher: Encrypts plaintext using a fixed key.</li>
    <li>Caesar Cipher: Encrypts plaintext using a shift operation.</li>
    <li>Frequency Analysis: Analyzes the frequency distribution of letters in ciphertext.</li>
    <li>DHKE: Implements the Diffie-Hellman Key Exchange protocol.</li>
  </ul>

  <h2>Code Structure</h2>
  <p>The code is structured into Python classes for modularity and reusability. The classes include:</p>
  <ul>
    <li>KamasutraCipher: Handles Kamasutra encryption.</li>
    <li>CaesarCipher: Handles Caesar cipher encryption.</li>
    <li>FrequencyAnalyzer: Calculates letter frequencies and creates histograms.</li>
    <li>DHKE: Implements the Diffie-Hellman Key Exchange protocol.</li>
  </ul>

  <h2>Usage</h2>
  <ol>
    <li><strong>Import necessary libraries:</strong>
      ```python
      import numpy as np
      import matplotlib.pyplot as plt
      from cryptography.ciphers import KamasutraCipher, CaesarCipher
      from cryptography.dhke import DHKE
      ```
    </li>
    <li><strong>Create cipher objects and perform encryption:</strong>
      ```python
      plaintext = "Your Full Name"
      ka_cipher = KamasutraCipher()
      ca_cipher = CaesarCipher(shift=11)

      ka_ciphertext = ka_cipher.encrypt(plaintext)
      ca_ciphertext = ca_cipher.encrypt(plaintext)
      ```
    </li>
    <li><strong>Analyze letter frequencies and create a histogram:</strong>
      ```python
      analyzer = FrequencyAnalyzer(ca_ciphertext)
      analyzer.analyze()
      analyzer.plot_histogram()
      ```
    </li>
    <li><strong>Implement DHKE:</strong>
      ```python
      dhke = DHKE()
      dhke.generate_parameters()
      tim_private_key, tim_public_key = dhke.generate_keys()
      stephen_private_key, stephen_public_key = dhke.generate_keys()
      shared_key = dhke.compute_shared_key(tim_private_key, stephen_public_key)
      ```
    </li>
  </ol>

  <h2>Additional Notes</h2>
  <ul>
    <li><strong>Key Length:</strong> For the Kamasutra cipher, ensure that the key length matches the alphabet size.</li>
    <li><strong>Prime Number and Primitive Root:</strong> In DHKE, the generated prime number should be sufficiently large for security.</li>
    <li><strong>Error Handling:</strong> Consider adding error handling for invalid inputs or unexpected scenarios.</li>
  </ul>
