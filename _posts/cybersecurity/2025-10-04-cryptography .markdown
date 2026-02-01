---
layout: post
date:   2025-10-04
categories: [cryptography, cybersecurity, encryption]
tags: [cryptography, Cybersecurity, Encryption]
---

<div class="image-container">
  <img src="{{ site.baseurl }}/assets/images/encryption.webp" alt="White Hat Hacker">
</div>
<style>
.image-container {
  text-align: center;
  margin: 2rem 0;
}

.image-container img {
  width: 100%; /* Set a fixed width */
  height: auto;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
  transition: transform 0.3s ease;
}
</style>

### Cryptography vs Encryption


Cryptography is the broader field for encryption, digital signatures, hash functions, and more in order to protect data from unauthorized access or modification. Encryption, on the other hand, is a specific cryptographic technique that involves converting plaintext into ciphertext using an encryption algorithm and a secret key. In short, cryptography is the science behind securing information, while encryption is one of the tools or techniques used within cryptography to achieve that goal.

### Encryption in Short

Symmetric encryption uses a shared key for encryption and decryption, providing fast and efficient data protection, while asymmetric encryption uses a pair of keys—a public key for encryption and a private key for decryption. Asymmetric encryption, like RSA, enables secure key exchange and features such as digital signatures (such as SSL/TLS for web). Public keys encrypt data, while private keys decrypt it. SSL/TLS and IPsec are protocols that leverage both symmetric and asymmetric encryption algorithms to ensure secure communication over the internet, with SSL/TLS focusing on web security and IPsec securing IP communications at the packet level. AES is a widely used symmetric encryption algorithm known for its speed and security, used for example in Wi-Fi (WPA) and encrypting files on systems in ransomware attacks.

### Symmetric Encryption

Also called private key cryptography or symmetric key cryptography, symmetric encryption is used to encrypt data. Symmetric encryption uses the same key to encrypt and decrypt data, meaning there is only a single key that is used for both operations. Therefore, the key must be stored in a safe place.

Symmetric encryption is faster, more efficient, and a great choice for encrypting large amounts of data, such as data in storage, disk encryption, VPNs, and financial transactions. However, since symmetric encryption uses the same key (only one key) to encrypt and decrypt data, it is challenging to securely transmit the key.

Another drawback of symmetric encryption is that it does not provide non-repudiation. These drawbacks can be complemented by using asymmetric encryption with digital signatures together with symmetric encryption. For example, we can encrypt the actual data with symmetric encryption and then encrypt the symmetric key with asymmetric encryption to securely perform key exchange.

### Cipher (Encryption Algorithm)

In cryptography, a cipher is an encryption algorithm for performing encryption or decryption—a series of well-defined steps that can be followed as a procedure. There are two types of cipher that symmetric encryption can use, namely stream cipher and block cipher.

#### Stream Cipher

Encrypts data bit by bit (or byte by byte) and is generally faster but less secure. It would normally go through every bit of data and encrypt it and then decrypt it on the other end.

#### Block Cipher

Breaks data into fixed-size blocks (such as 64 bits, 128 bits, etc.) and then encrypts each block separately. Block cipher is more secure and slower since it requires more computational power.

### Encryption Modes

Also known as modes of operation, determine how data is encrypted by a cipher. A block cipher requires an encryption mode such as ECB to encrypt data. While the encryption algorithm (cipher) encrypts the data, the encryption mode specifies how the algorithm processes and encrypts the data (if the data is longer than a block, then the encryption algorithm must use an encryption mode). Different modes can be chosen based on our preferences, such as whether we want increased security which requires more computational power and leaves more overhead, or faster encryption which is less secure. Here are some common encryption modes for block ciphers:

1. **ECB (Electronic Codebook)**: Encrypts each block of data independently but is less secure due to pattern vulnerability.
2. **CBC (Cipher Block Chaining)**: Uses an initialization vector (IV) and chains blocks together, providing better security by ensuring identical plaintext blocks encrypt differently.
3. **CTR (Counter)**: Converts a block cipher into a stream cipher by encrypting successive values of a counter, allowing parallel processing and improved performance.

### Encryption Rounds

In encryption algorithms, a "round" refers to a single cycle of operations that transforms the plaintext into encrypted text. These rounds are the core of the algorithm's complexity and security. For example, DES encryption has 16 rounds, meaning 16 cycles of operation on the same text.

### Popular Types of Symmetric Encryption Algorithms

#### AES (Advanced Encryption Standard)

Is the de facto standard for modern-day encryption and is widely used across different domains. AES is more secure and a lot faster than other encryption algorithms and is therefore the standard for modern-day encryption. AES comes in different key sizes such as 128 bit, 192 bit, or 256 bit. Remember that larger key size means stronger encryption but may also result in increased overhead. AES is a replacement for all other encryption algorithms since AES is a lot faster both in software and hardware (CPUs) and is more secure than Triple DES or DES.

#### DES (Data Encryption Standard)

An old encryption algorithm which uses a 56-bit key and 16 rounds. DES is no longer used because it is not secure anymore.

#### Triple DES

This symmetric encryption algorithm is the same as DES but three times stronger and is therefore called Triple DES. It uses a 168-bit long encryption key and 48 rounds. It is three times stronger than DES because DES is a 56-bit key and 16 rounds, so 3×56 = 168-bit key and 3×16 = 48 rounds. 3DES is generally only used for legacy systems or compatibility reasons but is largely replaced by AES which is more secure and faster.

Other encryption protocols are RC4, which is no longer used because of less security and was originally used in Wi-Fi WEP. RC5 is better than RC4 but still less secure. RC6 is the latest cipher in the RC family and a good competitor for AES, but AES is still considered the better choice due to its widespread adoption, strong security track record, and hardware acceleration support.

There are even other block ciphers (encryption algorithms) such as Blowfish and Twofish which are also replaced by the industry standard AES encryption algorithm, which is faster and more secure.

### Other Encryption Protocols

Other encryption protocols are RC4, which is no longer used because of less security and was originally used in Wi-Fi WEP. RC5 is better than RC4 but still less secure. RC6 is the latest cipher in the RC family and a good competitor for AES, but AES is still considered the better choice due to its widespread adoption, strong security track record, and hardware acceleration support.

There are even other block ciphers (encryption algorithms) such as Blowfish and Twofish, which are also replaced by the industry standard AES encryption algorithm, which is faster and more secure.

### Hybrid Encryption

Hybrid encryption means using both symmetric and asymmetric encryption, where symmetric encryption is used for encrypting the actual data and asymmetric encryption is used to facilitate secure key exchange of the symmetric key. In real-world and practical scenarios, there is almost always hybrid encryption being implemented because symmetric is very fast and efficient for actual data encryption, and asymmetric is used for securely transmitting the key by encrypting it. Examples are SSL/TLS, S/MIME, IPsec, SSH, and more. In some rare cases where encryption speed (time) and efficiency are not important, such as in ransomware, then all encryption is done by asymmetric encryption because threat actors may not want to transmit the private key at all, even securely.

### Asymmetric Encryption

Also known as public key cryptography, asymmetric encryption is used for encrypting data that needs to travel over insecure networks such as the internet. In asymmetric encryption, a pair of keys (public and private) are created for encrypting and decrypting data. It is more secure than symmetric encryption but is slower and less efficient. Therefore, asymmetric encryption is almost always combined with symmetric encryption, where the actual data is encrypted with symmetric encryption, and the symmetric key (private key of symmetric encryption) is encrypted with asymmetric encryption for secure key exchange. In asymmetric encryption, the public key of the recipient is used to encrypt data, and the private key is used to decrypt it.


#### Example Scenario
{% highlight ruby %}
User A wants to send some data to User B using asymmetric encryption:

- User A encrypts the data with User B’s public key (recipient's key).
- When User B receives the data, they use their private key, associated with their public key, to decrypt the data.
- If User B needs to send data back to User A, they encrypt it with User A’s public key.

{% endhighlight %}
This ensures that only the intended recipient, who possesses the corresponding private key, can decrypt and access the data.

### Diffie-Hellman Key Exchange

As the name suggests, this is a key exchange algorithm created to address issues that arise with symmetric encryption, specifically the secure transmission of the private key. Diffie-Hellman is not an encryption algorithm (meaning it does not encrypt data) but rather a secure key exchange algorithm. However, the problem with Diffie-Hellman key exchange is that it does not authenticate any party, making it vulnerable to a man-in-the-middle attack. In such an attack, a threat actor could intercept the packets and then encrypt them again with the public key of the recipient, spoofing the communication. Diffie-Hellman provides forward secrecy, which means that even if the private keys are compromised in the future, past communications remain secure since each session generates its own private keys. So if a private key is compromised, then the minimal amount of data (one session) will be compromised instead of the entire communication. We can use digital signatures with Diffie-Hellman to authenticate the involved parties, eliminating the risk of man-in-the-middle attacks. Diffie-Hellman is part of public key cryptography.

### RSA (Rivest-Shamir-Adleman)

RSA is one of the most widely used public key encryption algorithms, which provides encryption, secure key exchange (for example, in the case of exchanging a symmetric key), and authentication through using digital signatures. However, RSA does not provide forward secrecy and is therefore sometimes used together with Diffie-Hellman to provide optimal security in terms of encryption, authentication, and forward secrecy. There are many protocols which use RSA such as SSH, IPsec, SSL/TLS, and more.

### Elliptic Curve Cryptography (ECC)

ECC is the fastest and most secure public key encryption algorithm known for its efficiency and strong security. It’s a lot faster and more secure than RSA. It offers encryption, authentication through digital signatures (ECDSA), and secure key exchange (ECDH). ECC achieves high security with smaller key sizes compared to RSA, making it faster and more resource-efficient. This efficiency is particularly valuable for resource-constrained devices like mobile phones and IoT devices as well. ECC is widely used by major organizations such as Google and Cloudflare due to its performance benefits and robust security.

### Data Integrity and Authentication

#### Message Authentication Code (MAC)

MAC is used to verify data integrity and authentication of the sender, meaning that the data has not been tampered with and is coming from the right sender. MAC is a little bit different than hash functions, which are also used for data integrity but cannot verify the sender. MAC is a cryptographic string that is attached to the message, and upon being received, is calculated. If the newly calculated MAC matches the one coming with the packet, then the data is not modified and is coming from the right sender. MAC is not an encryption algorithm, so it does not provide encryption (privacy) but rather data integrity and authentication. The concept of MAC is the same as digital signatures, but MAC does not provide non-repudiation, whereas digital signatures do.

#### Hash Message Authentication Code (HMAC)

One of the most popular types of MAC is HMAC, which is used to create a unique MAC value (hash) for every message being sent. HMAC uses a hash function such as SHA-256 to calculate a hash value for the data being sent and a secret key, which is required for the hash to be recalculated when the message is received. When creating an HMAC, the hash function processes a combination of the message and the secret key in a specific way. This combination generates a unique hash value (the HMAC) for the message. By using HMAC, we achieve data integrity through hash functions and authentication through the secret key, since only those who possess the secret will be able to recalculate the hash (HMAC) of the data. An example of HMAC would be HMAC-SHA256 if it is using SHA-256, and so on.

#### Digital Signatures

Digital signatures are encrypted hash values which provide data integrity, authentication, and non-repudiation. Digital signatures are an important part of the PKI framework and are used in different scenarios such as signing SSL/TLS certificates with a hash function, digitally signing a document, and more. Digital signatures do not provide encryption but rather, just like real handwritten signatures, verify that the data has not been modified, the involved party has been authenticated, and that the sender cannot deny the action (non-repudiation). Digital signatures and message authentication code concepts are the same, but MAC does not provide non-repudiation. When non-repudiation is needed, we must use digital signatures. MAC is easier to implement since there is only one key involved, whereas in digital signatures, two keys (public and private) are involved.


How digital signatures work: let’s say two parties are communicating and using digital signatures. 

Sender: Before sending the data, the sender calculates the hash of the data using a hash function (such as SHA-256). They then encrypt this hash with their private key to create a digital signature (encrypted hash). 

Recipient: Upon receiving the message along with the digital signature (encrypted hash), the recipient separates the digital signature and decrypts it using the sender’s public key. The recipient then calculates the hash of the received data using the same hash function (also called signature algorithm). By comparing this newly computed hash with the decrypted hash from the signature, they can verify that the data has not been altered. This process confirms that the message was indeed sent by the authenticated sender and ensures that the sender cannot deny having sent the message if verification is needed. 

Example of digital signature with Elliptic Curve encryption algorithm: 
ECDSA Signature with SHA-256  

ECDSA stands for Elliptic Curve Digital Signature Algorithm. 

  

Summary of how keys are used for encryption and digital signatures: 

{% highlight ruby %}
- You encrypt a message with the recipient’s public key. 
- You decrypt a message with your own private key. 
- You digitally sign a message with your own private key. (encrypt the hash of the data being sent with your private key) 
- You verify the signature of a message with the sender’s public key 
{% endhighlight%}

### Email Security
 Most popular email encryption protocols are Secure Multipurpose Internet Mail Extension (S/MIME) and Pretty Good Privacy (PGP). These protocols follow the concept of public key encryption meaning they use public and private keys for encryption and decryption. These protocols provide encryption, data integrity, authentication and non-repudiation for email message so that emails can be securely transmitted over the network. Just like SSL/TLS is used for web security (including emails via web browsers), S/MIME and PGP is used for email security. S/MIME configuration is centralized via a certificate authority whereas PGP is decentralized and requires more complex configuration.  

 

### Public Key Infrastructure (PKI):  

PKI is the framework or software, hardware and policies for creating and managing digital certificates. PKI is all about creating and managing encryption key pairs, creating digital signatures and managing key exchange methods. Components of PKI are digital certificates, public and private encryption keys, Certificate authority, key exchange, trust hierarchy, certificate revocation list, digital signatures, Hardware Security Modules (HSM) and so on. In short PKI is the tools and tooling for implementing and managing public key cryptography.  

Hardware Security Module (HSM): HSM is a physical device which is used to create, manage and store encryption keys and certificates in order to avoid unauthorized access to the encryption keys. Most data sensitive enterprise networks use some of HSM devices to store encryption keys. Trusted Platform Model or TPM is a small chip which is attached to motherboard of a computer and stores encryption keys such as bitLocker keys for the device it is using.  

### Digital Certificates
 are like ID cards for devices and applications which contains public key and is digitally signed by a trusted party just like a real ID card is signed by the owner. The certificate also includes CA information, expiration data and signature from CA.   Since the certificate is signed by a trusted third party so it proves the identity (public key) of the certificate. When a device sends data it needs to encrypt that data or (private key if using hybrid encryption) with the recipient’s public key and the only way the sender gets that public key is through the recipient’s certificate. In short, when sending data the sender looks at the recipient’s certificate to get its public key and then encrypts data with it and sends it. Trusted parties that can issue digital certificates are digitcert, Microsoft, cloudflare and more. You can also create self-signed certificate by using OpenSSL but that would not be as much trusted and secure as a certificate issued by Digicert for example. You may wanna create self-signed certificates using openSSl  for testing or internal projects. We can also identify people by using digital certificates in that case there is no data transmission so we only need authentication and signature and that can be provided by a creating digital signature certificate for a person from CA.  
