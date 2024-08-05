![Format Developer](https://github.com/user-attachments/assets/07295330-a2a3-430a-8ae6-4e4fd1edeb5f)

> Develop custom code and data formats.

#

[Format Developer](https://chatgpt.com/g/g-Joa1YMscU-format-developer) was developed to specialize in developing tailored code and information formats to meet specific user requirements. Its primary function is to understand the user's needs in detail, considering the context in which the format will be used, such as documentation, software development, or reporting. By identifying key elements or data types that need formatting, the GPT ensures that the custom formats are optimized for clarity, consistency, and usability.

Once the requirements are clear, this GPT creates custom formats that can include code templates, unique data structures, or specialized layouts for presenting information. These formats are designed to enhance readability, maintainability, and overall efficiency in the user's projects. The GPT also provides guidelines for consistent application across teams or projects, ensuring that the new formats are seamlessly integrated into existing workflows.

Beyond just creating formats, this GPT assists in implementing and refining them through testing and gathering feedback. It ensures compatibility with existing systems and provides documentation and training to help users adopt the new formats effectively. By supporting the entire lifecycle from design to implementation, this GPT ensures that the custom formats are not only effective but also adaptable and sustainable for future needs.

#
### Example Usage

<details><summary>Unique Communication Encryption Format Example</summary>
<br>

### Hybrid Encryption Communication Format

**Overview**: This format combines the strengths of both symmetric and asymmetric encryption. Asymmetric encryption is used to securely exchange a symmetric key, which is then used to encrypt the actual message.

#### Components:

1. **Asymmetric Encryption**:
   - Algorithm: RSA (Rivest–Shamir–Adleman)
   - Key Size: 2048 bits
   - Used for: Secure key exchange

2. **Symmetric Encryption**:
   - Algorithm: AES (Advanced Encryption Standard)
   - Key Size: 256 bits
   - Used for: Message encryption

3. **Message Structure**:
   - **Header**: Contains metadata about the message, including version, timestamp, and the encrypted symmetric key.
   - **Body**: The actual encrypted message data.
   - **Signature**: Optional, provides integrity and authenticity.

### Detailed Format:

#### 1. **Header**:

- **Version (2 bytes)**: Identifies the version of the encryption format.
- **Timestamp (8 bytes)**: UNIX timestamp indicating when the message was created.
- **Sender ID (Variable)**: Unique identifier for the sender (e.g., public key fingerprint).
- **Encrypted Symmetric Key (256 bytes)**: The AES key encrypted using the recipient's RSA public key.

#### 2. **Body**:

- **IV (Initialization Vector) (16 bytes)**: Randomly generated for each message, used with AES encryption.
- **Encrypted Data (Variable)**: The actual message data encrypted using the AES symmetric key.

#### 3. **Signature (Optional)**:

- **Signature (Variable)**: The message body signed with the sender's RSA private key, ensuring integrity and authenticity.

### Message Flow Example:

1. **Message Creation**:
   - The sender generates a 256-bit AES symmetric key.
   - The sender encrypts the AES key using the recipient's RSA public key.
   - The sender encrypts the message body using AES encryption with the generated key.
   - The sender creates a message header, including metadata and the encrypted AES key.
   - Optionally, the sender signs the message body using their RSA private key.

2. **Message Transmission**:
   - The complete message, including header, body, and optional signature, is transmitted to the recipient.

3. **Message Decryption**:
   - The recipient extracts the encrypted AES key from the header and decrypts it using their RSA private key.
   - The recipient uses the decrypted AES key to decrypt the message body.
   - Optionally, the recipient verifies the signature using the sender's public key.

### Example Message Structure (in Bytes):

```
| Header |

Version: 0x01 0x00
Timestamp: 0x5F3B5E7B
Sender ID: 0xA1B2C3D4E5F6G7H8
Encrypted AES Key: 0x123456789ABCDEF...

| Body |

IV: 0x1A2B3C4D5E6F7081
Encrypted Data: 0x9F8E7D6C5B4A3B2C...

| Signature (Optional) |

Signature: 0xABCDEF0123456789...
```

### Advantages of This Format:

- **Security**: Combines the security of RSA for key exchange with the efficiency of AES for data encryption.
- **Flexibility**: The format is adaptable and can be extended with additional metadata or security features.
- **Integrity and Authenticity**: Optional signature ensures the message has not been tampered with and verifies the sender's identity.

This format provides a solid foundation for secure communication, suitable for scenarios where both security and performance are important.

<br>
</details>

#
### Related Links

[ChatGPT](https://github.com/sourceduty/ChatGPT)
<br>
[Serial Format](https://github.com/sourceduty/Serial_Format)
<br>
[Format Analyzer](https://github.com/sourceduty/Format_Analyzer)
<br>
[Encryption Specialist](https://chatgpt.com/g/g-AClVroVDs-encryption-specialist)
<br>
[Encryption](https://github.com/sourceduty/Encryption)
<br>
[Programming Language Writer](https://github.com/sourceduty/Programming_Language_Writer)

***
Copyright (C) 2024, Sourceduty - All Rights Reserved.
