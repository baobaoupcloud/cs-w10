---
title : "Hashing and Encryption"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---
When passwords are stored, they should never be saved as plain text. **Hashing** and **encryption** are two essential techniques that protect sensitive data.
### Hashing
Hashing converts a password into a unique, irreversible string. When you log in, the entered password is hashed, and the system compares it with the stored hash.

One-way hashing allows online services to actually never store the original password typed by the user. Only the hashed value of these passwords. Accordingly, if there is a breach, only the hashed value will be known.

Rainbow tables are huge dictionaries that adversaries use to attempt to pre-hash possible passwords as a means by which to attempt to break the hash algorithm.

As an additional process to heightened security, programmers may sometimes introduce salting where it becomes unlikely that multiple users may have the same hash value to represent their passwords. 

### Encryption
Encryption converts data into an unreadable format that can only be decrypted by someone with the correct decryption key. Two key types are used:
- **Public key**: Used to encrypt data, can be shared openly.
- **Private key**: Kept secure, used to decrypt data.

Encryption is essential for protecting sensitive data and communications from unauthorized access. 

**End-to-end encryption** (used by apps like iMessage and WhatsApp) ensures only the sender and receiver can read messages, preventing third parties from intercepting data.

