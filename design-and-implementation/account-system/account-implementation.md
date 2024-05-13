# &#x20;Account Implementation

DC users' NFT accounts and passwords are linked to their application signing private keys, meaning each DC NFT account and password pair corresponds to a specific signing private key or mnemonic phrase. To facilitate cross-terminal login for Web3.0 applications, DC implements the following procedures:

1. **Private Key Storage**:
   * The private key information associated with the NFT account and password is stored within DC. This information, along with basic user data, is kept completely private and can only be decrypted by the user.
2. **Secure Login**:
   * When logging in using an NFT account and password, users can securely and swiftly retrieve the corresponding application private key information from DC.
3. **Extraction Security**:
   * The application private key information stored in DC can only be accessed by users who possess both the NFT account and password. The entire login and information extraction process is fully encrypted.

The implementation details of the DC account system are as follows:

**Steps Consistent with Existing Web3.0**:

1. Users locally generate an application account, which includes a private key or derived mnemonic phrase.
2. Users are guided to record the mnemonic phrase.
3. Completion of the creation of a decentralized chain-based application account occurs, simultaneously deriving an ERC20 format chain account through the mnemonic phrase.

**DC Network NFT Account-Specific Steps**:

4. Users are guided to enter basic information such as their NFT account and password.
5. In DC, a check is performed to determine if the NFT account has been registered. If it is already registered, users are guided to choose another NFT account.
6. The user's chain account is checked for balance. If there is no balance, users are guided to deposit funds into the chain account. It is advisable for application developers to establish a faucet service during the early stages of application promotion to automatically transfer funds needed to bind the account for new registered users.
7. The chain account subscribes to cloud service space for the user's application account on DCChain.
8. The binding relationship between the application private key or mnemonic phrase and the NFT account is submitted to DC. If during the submission process, the account is bound by someone else or there is insufficient balance, the process returns to step 2.
9. Users can directly log in on any terminal using the NFT account and password.
10. Users can modify their login password as needed.
