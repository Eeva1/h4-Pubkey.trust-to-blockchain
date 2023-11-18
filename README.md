## Communications using public-key cryptography

- symmetric algorithm is like a safe and the key is the combination
- Diffie and Hellman in 1976 described public-key cryptgraphy.
- They used two kinds of keys, a public and a private key
- Computationally it's hard to deduce the private and public key
- Everybody can encrypt the message but only a person who have the private key can decrypt it.
- Mathematically encryption is the easy direction, anyone can encrypt the message with the public key.
- For the decrytion you need a secret, the private key, which makes the decrytion as easy as encrypting.
- Every network user has it's own public key and private key, and public keys are published in some database.

## Hybrid Cryptosystem

- Public-key algorithms are not a substitute for symmetric algorithms.
- Public keys are not used encrypting messages, but are used to to encrypt keys, and there are two reasons for that:
  1. Algorithms that uses public keys are slow. Generally symmetric algorithms are thousand times faster than public-key algorithms.
  2. They are vulnerable to chosen-plainttext attacks.
- Symmetric cryptosystems are not vulnerable for chosen-plaintext attacks. A cryptoanalyst can't perfrom encryptions as trial with an unknown key.
- 
 
