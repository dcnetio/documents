# Account Security Design

Given that the node list storing user account information is accessible via the NFT account, securing the user data within DCNode is crucial. To safeguard this information, DC employs several robust security measures:

1. **Encryption of Blockchain Account Private Keys Using AES256**:
   * The NFT account and password are combined in a series of encryption processes to generate a unique AES256 key. This key is exclusively linked to the blockchain account private key, ensuring that only individuals with knowledge of both the NFT account and password can decrypt the associated application account private key.
2. **Storage of Encrypted Keys**:
   * Encrypted blockchain account private keys are stored solely in networked DCNodes. The client SDK ensures that these keys are maintained only in networked and online DCNodes. Each networked DCNode undergoes certification through TEE-based remote attestation technology, verifying that the programs running on the nodes are unaltered, legitimate, and function within a TEE environment. This guarantees the security, privacy, and reliability of the data stored on these nodes.
3. **TEE Encapsulation**:
   * DCNode employs TEE encapsulation technology to secure the encrypted blockchain private keys stored on the nodes. This method ensures that even the physical device owners of DCNode cannot access the encrypted blockchain private keys.
4. **Secure Key Parameter Extraction**:
   * The key used in the login process encryption does not contain complete account password information. Instead, the key parameter extraction algorithm for the NFT account in the request information is securely designed by hashing the account and part of the password separately, then splitting and recombining them. Multiple hashing ensures that reverse-engineering the account password from the key is impossible. Part of the key is used in the calculation, and after hashing, part of it is taken for a second hash to ensure it cannot be brute-forced to obtain the exact NFT account and password.
5. **Encrypted Communication**:
   * The entire login process is encrypted to ensure communication security. When the client sends a login request to DCNode, the communication process is encrypted using the public key of DCNode, meaning only the requested DCNode program can decrypt it. Feedback data is also encrypted using the key negotiated during the login request process, ensuring that only the requester can decrypt it.
6. **Control of Failed Login Attempts**:
   * DCNode manages the number of failed login attempts within a specific time window, rejecting login requests that exceed this limit. This control prevents hackers from extracting the encrypted blockchain private key through brute force methods.
7. **Use of Bcrypt Algorithm**:
   * To slow down the generation speed of the AES256 key and prevent offline brute force attacks on the request key, the Bcrypt algorithm is introduced during the AES256 key generation process with the NFT account and password. Bcrypt modifies the encryption salt derived from the NFT account password using a specific algorithm. Utilizing the slow hashing principle of Bcrypt (cost set to 12, which can be adjusted as device performance improves), ensures that hackers cannot perform offline brute force attacks even if they obtain the encrypted blockchain private key.

These comprehensive measures are designed to ensure the utmost security of user information within the DCNode framework.
