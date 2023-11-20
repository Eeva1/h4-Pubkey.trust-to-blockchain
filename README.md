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

I installed and updated the required tools and made it to the point, where I created a keypair.

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/077682c5-4be3-48e0-b0aa-ed661f4ac895)

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/cece0443-692b-41d7-9b6c-4d7ac925ad2a)

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/7b7220b2-5ec7-4eeb-87d3-3aec311f90a6)

I did as told, but I put my own email address there since I started the task by my own address, but there was an error..? No data and when I try to put command "micro message.txt" the command not found?
I already thought that I start the whole task from the beginning, but since I already started like this, I try to continue...

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/72121dc8-b5a3-4021-8cd5-f70950085cdf)

THis is where I ended up:

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/62f756c4-b8d8-455e-a7c2-ace78545f83f)

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/dc35a4ad-55a5-4d8b-afc1-2608cef34cd3)

I wanted to solve the problem, so I created a new folder eeva.pub

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/6bf792bd-a9dc-4750-ac58-6ac715a88984)

I was able to get to this point, where Eeva needs Alices key to know it's her:

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/e830c4cc-3c93-44ff-a9ee-04a92010e81c)

This is where I stucked last time also.. there comes "command not found"

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/ce49d4d6-b46f-4f10-ae09-2ada94e804d1)

Then I just proceed to the end and "killall"


![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/698f5fb9-d86f-4a2b-b416-465ef1149206)

And here is my main keyring:

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/4f1875e9-3010-4293-bd49-0717951ade84)

Here is Alices keyring:

![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/a6d763c0-837e-4718-b3cc-1981370c53cf)
![image](https://github.com/Eeva1/h4-Pubkey.trust-to-blockchain/assets/149093822/cf9df575-f608-4e54-af69-5144a5d2ecb9)

## a) Pubkey today. Explain how you have used public key cryptography today or yesterday, outside of this homework. In addition to naming the system, identify how different parties use keys in different steps of the system. (Answering this question likely requries finding sources on your own. This subtask does not require tests with a computer.)

- I use IKEv2/IPsec network protocol to my VPN connection, or as a SASE (secure access service edge) security framework.
- IKEv2/IPsec is a mix of a key management protocol (IKEv2) and a tunneling and data-transporting tunnel (IPSec).
- IKEv2/IPsec uses the AES-256-GCM cipher to encryption, which is coupled with SHA2-384 for integrity. In addition, IKEv2/IPSec uses Perfect Forward Secrecy (PFS) with 3072-bit Diffie-Hellman keys.
- PFS is a process in which an encryption system changes its encryption keys regurlarly, so only a small bit of data can be compromised in any single breach. It switches keys after every call, message or page load. 

## b) Messaging. Send an encrypted and signed message using PGP, then verify and decrypt it. (You can use folders to simulate users, or use two computers or two different OS users. Don't use Tero as a name of any party, unless that's your given name.)


c) Other tool. Encrypt a message using a tool other than PGP. Explain how different parties use different keys at different stages of operation. Evaluate the security of the tool you've chosen.


d) Eve and Mallory. In many crypto stories, Eve is a passive eavesdropper, listening on the wire. Mallory malliciously modifies the messages. Explain how PGP protects against Mallory and Eve. Be specific what features, which use of keys and which flags in the command are related to this protection. (This subtasks does not require tests with a computer)


f) Password management. Demonstrate use of a password manager. What kind of attacks take advantage of people not using password managers? (You can use any password manager, some examples include pass and KeePassXC.)


g) Refer to sources. Verify each homework report (this and the earlier ones) refers to sources. Every homework report should refer to this task page. It should also have references to any other source used, such as web pages, LLMs, man pages, other reports... References are mandatory, and must be present in every report. (This subtask does not need a report, you can just do it and write "Done." as the answer for this subtask.)



