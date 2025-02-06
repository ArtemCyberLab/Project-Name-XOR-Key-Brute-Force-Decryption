In this project, I analyzed XOR encryption and its vulnerability to brute-force attacks. I was given an encrypted text in hexadecimal format, which I decoded into bytes. Using pwntools and the xor() function, I attempted to decrypt the first few characters, knowing that the encrypted text started with THM{. This allowed me to determine part of the key.

Next, using nc, I connected to a remote server that asked me for the encryption key. By applying XOR to the ciphertext and the known part of the plaintext, I was able to recover the full key: 4M4U2. After entering this key on the server, I successfully passed the verification and received the second flag: THM{BrUt3_ForC1nG_XOR_cAn_B3_FuN_nO?}.

During the analysis, I also examined the provided server-side code, which confirmed that the encryption used a repeating 5-character key and applied XOR to each character of the flag. This helped me understand how the mechanism worked and perform an attack on the encryption using simple XOR math.

This project allowed me to deepen my understanding of XOR encryption, attack methods, and the practical use of pwntools and network interactions with netcat.
