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
- You should still remember not to sign arbitrary messages from other people ever or give the results of decrypted messages for others.
- To fix the issues of attacks, different keys can be used for each operation, or various algorithms can be used for each operation. Another solution is to use timestamps, which make incoming and outgoing messages different. Digital signatures with one-way hash functions also help in addressing the problem.
- Easiest wayt to get a public key of someone is to get it from the secure database somewhere. It must be public, so that everybody can get it.
- But even if the public keys are in a secure database, someone can still substitute one to another in transmission.
- To prevent that, the signer can sign public key with his own private key, which is often called a Key Serfificate Authority or Key Distribution Center.

## Random and pseudo-random-sequence generation

- There is a random-number generator built into every compiler, but they are not secure enough for cryptography.
- Random number generators are not random because they don't have to be. Their problem is, that they don't produce a random sequence.
- When using poor random-number generator, there can be wierd correlations and results that are strange.
- Computers are predictable, and therefore they cannot be random.
- A real random-number generator demands some random input and a computer cannot provide that.
- A pseudo-random-sequence generator is the best that computer can produce.
- The sequence's length should be sufficiently long to ensure that a practical sequence —one that is actually used— is not repetitive or predictable within a finite span.
- There has been a lot of effort in producing good pseudo-random sequences on computer, but the problem is still the producing those weird correlations and strange results.
- Cryptographically Secure Pseudo-Random Sequence must be unbredictable.
- They should not be compressible unless the key is known
- These cryptographically secure pseudo-random-sequence generators are subject for attacks just like any cryptographic algorithm.
- It is all about making generators resistant for attacks.
- Quantum mechanics tells us there is honest to goodness randomness in the real world.
- A sequence generator is real random if it has an additional third property: It cannot be reliably reproduced.
- For one time pad, the output of a generator s
- If a generator meets the three conditions, its output will work well for a one-time pad, key generation, and any other cryptographic applications that need a genuinely random sequence.
- The difficultness is when determining, is a sequence really a random. 

## Cryptographic hash functions and digital signatures

- Step 1. Preparation 
- Step 2. Signing
- Step 3. Verifying

- Digital signature improves security
- The processes of the signing and verification are based on a key pair, a private and a public key. It's done by generating first a private key and the claculating the public key from the private key. A random number generator can be used to generate the random number as a private key.
- The key pair must be created by making first the private key, which is huge, secret number.
- Then the public key is claculated from the private key.
- Bitcoin uses the digital signatures like above explained above for most payments today, but it is not the only way of doing it.

## PGP 

- I installed and updated the required tools and made it to the point, where I created a keypair. (https://terokarvinen.com/2023/pgp-encrypt-sign-verify/)

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/077682c5-4be3-48e0-b0aa-ed661f4ac895)

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/cece0443-692b-41d7-9b6c-4d7ac925ad2a)

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/7b7220b2-5ec7-4eeb-87d3-3aec311f90a6)

- I did as told (https://terokarvinen.com/2023/pgp-encrypt-sign-verify/), but I put my own email address there since I started the task by my own address, but there was an error..? No data and when I try to put command "micro message.txt" the command not found?
- I already thought that I start the whole task from the beginning, but since I already started like this, I try to continue...

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/72121dc8-b5a3-4021-8cd5-f70950085cdf)

- This is where I ended up:

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/62f756c4-b8d8-455e-a7c2-ace78545f83f)

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/dc35a4ad-55a5-4d8b-afc1-2608cef34cd3)

- I wanted to solve the problem, so I created a new folder eeva.pub

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/6bf792bd-a9dc-4750-ac58-6ac715a88984)

- I was able to get to this point, where Eeva needs Alices key to know it's her:

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/e830c4cc-3c93-44ff-a9ee-04a92010e81c)

- This is where I stucked last time also.. there comes "command not found"

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/ce49d4d6-b46f-4f10-ae09-2ada94e804d1)

- Then I just proceed to the end and "killall"

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/698f5fb9-d86f-4a2b-b416-465ef1149206)

- And here is my main keyring:

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/4f1875e9-3010-4293-bd49-0717951ade84)

- Here is Alices keyring:

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/a6d763c0-837e-4718-b3cc-1981370c53cf)
![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/cf9df575-f608-4e54-af69-5144a5d2ecb9)

## a) Pubkey today.

- I use IKEv2/IPsec network protocol to my VPN connection, which is a SASE (secure access service edge) security framework.
- IKEv2/IPsec is a mix of a key management protocol (IKEv2) and a tunneling and data-transporting tunnel (IPSec).
- IKEv2/IPsec uses the AES-256-GCM cipher to encryption, which is coupled with SHA2-384 for integrity. In addition, IKEv2/IPSec uses Perfect Forward Secrecy (PFS) with 3072-bit Diffie-Hellman keys.
- PFS is a process in which an encryption system changes its encryption keys regurlarly, so only a small bit of data can be compromised in any single breach. It switches keys after every call, message or page load.
(https://nordvpn.com/fi/blog/ikev2ipsec/)
(https://nordvpn.com/fi/blog/perfect-forward-secrecy/)

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/de4c4da4-10f4-4462-82e6-471a7ccfad51)

## b) Messaging. 

- Started from the beginnig with the updates and this time also with this: $ sudo apt-get install gpg micro psmisc
I created a new key pair:
  
![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/57cfdd27-389e-4dfe-a13f-9c959541ec99)
![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/44340f6e-7a5d-4668-8e4a-66b82be00ccc)

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/602e6871-e4d8-4a7a-843b-00192bbac960)

- And now I have lots of different keys:

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/94fb2d2b-0ef1-4d00-8445-cdea5f54961d)

- I manage to write the secret message...

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/75ec1f72-6398-40e0-bbcb-4177593ea295)

- I got this far..

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/85811660-67f9-458b-927c-402cc907cf98)

- But in the end, I couldn't decrypt the message...:/

- ![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/4b7567de-c761-474c-9a75-0ba1c7c700a8)

- ![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/f2726a17-6a15-4d98-936a-8a3aa997853b)

c) Other tool. Encrypt a message using a tool other than PGP. Explain how different parties use different keys at different stages of operation. 

- I can send encrypted email from my Outlook:

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/05701420-5c42-4ada-915e-d6b26f7c28ee)

- Then I get the secret message notification:

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/5e20b029-506a-464e-8af0-54f2c1de9250)

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/7ccc04e8-6158-47dc-a698-859985354189)

- To open up the message I must sign in or get the one-time code:

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/70e73b08-a907-47de-b0dc-6c03b4977cea)

- And then I got to read the message: 

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/4fa15e15-0052-42ba-a083-513b5f4f47b4)

- I think Outlook encrypted messaging is reliable. Only bad thing is, that it cannot encrypt attachments such as pdf files and that way somebody can intercept the pdf file.
- Sometimes decrypting has turned out to be more difficult than it should be, if receiving person don't remember her passwords or there is something with the email addresses. 

d) Eve and Mallory. In many crypto stories, Eve is a passive eavesdropper, listening on the wire. Mallory malliciously modifies the messages. Explain how PGP protects against Mallory and Eve. 

PGP (Pretty Good Privacy)

- PGP uses SBE (Symmetric Bloc Encryption) for confidentiality, which includes the usage of the same key for encrypt and decrypt message. The key is generated randomly every time when message is encrypted, which makes it difficult to decode the content of stolen message.
https://www.includehelp.com/computer-networks/pgp-authentication-and-confidentiality.aspx#:~:text=PGP%20uses%20Symmetric%20Block%20Encryption%20%28SBE%29%20for%20confidentiality%2C,attackers%20to%20decipher%20the%20content%20of%20intercepted%20messages.
https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec006

f) Password management. 

- I use Google Password manager to secure all my passwords. That way I don't need to remember all my passwords to sign in to different pages/portals, but only one. 
That way hackers cannot get the passwords, because they are encrypted and can decrypt only with my main pin code. The pin code is also changing almost every month so it would be very hard to decrypt my Google passwords.
https://passwords.google/

g) References: 

- https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02
- https://terokarvinen.com/2023/pgp-encrypt-sign-verify/
- https://terokarvinen.com/2023/trust-to-blockchain/
- https://www.microsoft.com/en-us/security/business/security-101/what-is-sase
- https://nordvpn.com/fi/blog/perfect-forward-secrecy/
- https://www.includehelp.com/computer-networks/pgp-authentication-and-confidentiality.aspx#:~:text=PGP%20uses%20Symmetric%20Block%20Encryption%20%28SBE%29%20for%20confidentiality%2C,attackers%20to%20decipher%20the%20content%20of%20intercepted%20messages.
- https://passwords.google/ 
