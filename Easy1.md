
We are given:
- **Ciphertext**: `UFJKXQZQUNB`
- **Key**: `SOLVECRYPTO`
- A Vigenère cipher table to help with decryption.

The goal is to decrypt the ciphertext using the Vigenère cipher method.

## Solution Steps
1. **Align the Key with the Ciphertext**: Since the ciphertext and key are the same length, each letter in the ciphertext corresponds directly to a letter in the key.

2. **Decrypt Each Letter**:
   - For each letter in the ciphertext, locate the row in the Vigenère table corresponding to the key letter.
   - Find the column where the ciphertext letter appears in that row.
   - The top of that column gives the decrypted letter.

3. **Decryption**:
   Using the steps above, we find the following decrypted letters:

   - **U** (Ciphertext) with **S** (Key) -> **C**
   - **F** (Ciphertext) with **O** (Key) -> **R**
   - **J** (Ciphertext) with **L** (Key) -> **Y**
   - **K** (Ciphertext) with **V** (Key) -> **P**
   - **X** (Ciphertext) with **E** (Key) -> **T**
   - **Q** (Ciphertext) with **C** (Key) -> **O**
   - **Z** (Ciphertext) with **R** (Key) -> **I**
   - **Q** (Ciphertext) with **Y** (Key) -> **S**
   - **U** (Ciphertext) with **P** (Key) -> **F**
   - **N** (Ciphertext) with **T** (Key) -> **U**
   - **B** (Ciphertext) with **O** (Key) -> **N**

4. **Final Decrypted Message**:
   The decrypted message (flag) is: `CRYPTOISFUN`
   thus the final flag is: `picoCTF{CRYPTOISFUN}`
`
