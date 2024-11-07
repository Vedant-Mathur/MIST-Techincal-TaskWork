In this challenge, the objective was to find the flag by verifying a given SHA-256 checksum and decrypting a file.

1. **Login and File Inspection**:
   - SSH was used to log into the provided server (`ssh -p 60435 ctf-player@rhea.picoctf.net`), where three key files were found in the directory:
     - `checksum.txt`: Contains the target SHA-256 checksum.
     - `decrypt.sh`: A script for decrypting the file.
     - `files/`: A directory containing files to check against the checksum.

2. **SHA-256 Checksum Matching**:
   - The checksum from `checksum.txt` was `03b52eabed5489bgjd4390348g43j36d5d8`.
   - Using the command:
     ```bash
     sha256sum files/* | grep 03b52eabed515489bgjd4390348g43j36d5d8
     ```
     we found that the file `files/8eee7195` matched the given checksum.

3. **Decryption Process**:
   - The `decrypt.sh` script was used to decrypt the file `files/8eee7195`.
   - Running the command:
     ```bash
     ./decrypt.sh files/00011a60
     ```
     decrypted the file and revealed the flag: `picoCTF{trust_but_verify_8eee7195}`.

4. **Flag**:
![alt text](./img/image-1.png)
