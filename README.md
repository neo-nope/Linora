# Linora Cipher

*A modular neighbor-chain cipher by **modify***  
**Created: 2025**  
**License: Linora License v1.0**

---

## 🔍 Overview

The **Linora Cipher** is a symmetric encryption algorithm developed by `modify` in 2025. It transforms characters using modular arithmetic and chained differences, making each output character reliant on both the input and the previous result.

---

## 🔐 Algorithm Description

### Step 1: Character Conversion

- Convert all characters to numbers:  
  `a = 0, b = 1, ..., z = 25`

### Step 2: Encryption

1. **First character**:  
   Add the first key element to it, modulo 26.

2. **Each subsequent character**:
   - Compute the difference from the previous **plaintext** character (mod 26).
   - Multiply the result by the corresponding key element (cycled).
   - Take the result modulo 26.

### Step 3: Decryption

1. **First character**:  
   Subtract the first key element from it (modulo 26).

2. **Subsequent characters**:
   - Multiply the ciphered character by the modular inverse of the corresponding key element (mod 26).
   - Add the result to the previous **plaintext** character, modulo 26.

---

## 📘 Example

- **Plaintext**: `hello`  
- **Key**: `[3, 5, 7]`  
- Each character is transformed step-by-step using the above algorithm.
- The cipher chaining ensures that a small change in input cascades through the rest of the output.

---

## ⚠️ Security Notes

The Linora Cipher introduces chaining similar to Cipher Block Chaining (CBC) mode in block ciphers, but operates at the character level.

- Not intended for industrial cryptographic security.
- Suitable for obfuscation, experimentation, games, puzzles, and learning.
- Resistant to simple frequency analysis due to chaining.

---

## 📜 License

```text
Linora Cipher License v1.0
Copyright © 2025 modify

Permission is hereby granted to any person or organization to use, reproduce, modify, and distribute the Linora Cipher and associated documentation (the "Cipher"), subject to the following conditions:

1. Attribution Requirement
   - Proper credit must be given to the original author (“modify”) in any distributed or published work that uses or adapts the Cipher.

2. Exceptions to Attribution
   - Attribution is not required when the Cipher is used as part of an alternate reality game (ARG), immersive fiction, escape room, or interactive experience where visible attribution would break narrative immersion or reduce the effectiveness of the experience.

3. No Warranty
   - The Cipher is provided "as is", without warranty of any kind, express or implied. The author is not liable for any damage or misuse resulting from its use.

4. Integrity of Design
   - Modified versions may be created, but must not be falsely presented as the original design by modify.

By using the Cipher, you agree to the terms above.

— modify
