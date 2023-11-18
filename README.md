## Communications using public-key cryptography

- symmetric algorithm is like a safe and the key is the combination
- Diffie and Hellman in 1976 described public-key cryptgraphy.
- They used two kinds of keys, a public and a private key
- Computationally it's hard to deduce the private and public key
- Everybody can encrypt the message but only a person who have the private key can decrypt it.
- Mathematically encryption is the easy direction, anyone can encrypt the message with the public key.
- For the decrytion you need a secret, the private key, which makes the decrytion as easy as encrypting.
- Every network user has it's own public key and private key, and public keys are published in some database.

_Hybrid Cryptosystem_

- Public-key algorithms are not a substitute for symmetric algorithms.
- Public keys are not used encrypting messages, but are used to to encrypt keys, and there are two reasons for that:
  1. Algorithms that uses public keys are slow. Generally symmetric algorithms are thousand times faster than public-key algorithms.
  2. They are vulnerable to chosen-plainttext attacks.
- Symmetric cryptosystems are not vulnerable for chosen-plaintext attacks. A cryptoanalyst can't perfrom encryptions as trial with an unknown key.
- Public-key cryptography is used to secure and distribute _session keys_. Session keys are used to secure message traffic with symmetric keys, sometimes called a _hybrid cryptosystem_.
- Key-management problem is solved by the usage of public-key cryptographic for key distribution.
- With symmetric cryptography, the key used to encrypt data is around until it's needed.
- The session key is created when it's needed and destroyed when no needed anymore.

## Digital signatures

- Signatures can be faked and there is a possibility to copy/paste them by several tecniques.
- digital signatures have problems on computers: the computer files are trivial to copy and they are easy to modify without leaving any trace or evidence of the modification.
- Merkle suggested a way to sign digital documents using a secret-key method. This involves creating countless unique signatures through a tree-like structure.
- The idea is to place the root in some public file. The root signs a message and authenticates the sub-nodes in tree.

- Public-key algorithms can be used for digital signatures
- For example RSA, both public or private key can be used for encryption.
- DSA is separet algorithm for digital signatures and can't be used in encryption.

- Digital signatures often have timestamps, and the signatures date & time are attached to the message. That way no one cannot go and use the digital signatures for the second time.
  
- Public-key algorithms are inefficient to sign long documents
- Digital signature protocols are often implemented with one-way hash functions to save time
- Instead of signing the document, the hash of the document is signed.
- Signing documents with public-key cryptography and one-way hash have benefits: the signature can be kept separate from document and the requirements of the recipient's storage and signature are smaller.

- There is lots of Digital signature algorithms and all of them are public-key algorithms with secret information signing documents public information veryfying signatures.

- You can always cheat with digital signatures although timestamps can limit the impact of cheating.

## Digital signatures with encryption

- When blending digital signatures with public-key cryptography, we create a process that merges the safety of encryption with the trustworthiness of digital signatures.
- Timestamps should be used also with this protocol to prevent the reusage of the messages.

- Implementing the protocol, you should consider to put additional feature for confirmating the message.





 
