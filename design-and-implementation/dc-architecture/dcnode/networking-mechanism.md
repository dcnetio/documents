# Networking Mechanism

The DCNode system is designed to operate within a decentralized cloud service infrastructure, where each node is self-organizing and functions within a Trusted Execution Environment (TEE). This setup ensures the security and integrity of data across the network. Here’s a detailed overview of the onboarding and offboarding mechanisms for DCNodes:

#### 5.1 Node Onboarding Mechanism

1. **Initialization and Account Setup:**
   * Operators start the DCNode node program, which generates a PeerId for the node and an Erc20 account. The private key for this account is encrypted and securely stored within the node's TEE, making it inaccessible to anyone else.
2. **Funding for Transaction Fees:**
   * Operators must transfer a small amount of DCT (the native token of DCChain) to the node’s Erc20 account via the DC portal or an Ethereum-compatible wallet. These funds cover transaction fees for activities on the DCChain.
3. **Staking and Binding:**
   * The node's PeerId is bound to an Erc20 account owned by the user specifically for staking purposes. The required amount of DCT for staking is then transferred to this account.
4. **Onboarding Application and Verification:**
   * Upon successful staking, the node program automatically initiates an onboarding application that includes TEE remote attestation. This application must be confirmed through the consensus mechanism of DCChain.
   * A randomly selected group of existing networked DCNodes verifies the TEE remote attestation of the new node. If the attestation fails, they submit a report request to the blockchain.
   * After waiting for 300 blocks, the new applicant DCNode re-submits its onboarding application. DCChain then evaluates whether the application has cleared the TEE remote attestation verification conducted by other networked nodes. If the verification is successful, the new node is integrated into the network; if it fails, a corresponding amount of staked DCT tokens is deducted as a penalty.
5. **Integration into the Network:**
   * Once integrated, the new DCNode begins providing cloud services and takes on roles such as initiating verification tasks that include TEE remote attestations.

#### 5.2 Node Offboarding Mechanism

1. **Initiation of Offboarding:**
   * Node operators can initiate an offboarding request anytime through the DC portal. Upon receiving this request, DC starts a data backup task on the node, allowing it to go offline since the network maintains multiple backups.
2. **Penalties for Non-compliance:**
   * If a node operator stops the DCNode program and fails to initiate an offboarding request within 7 days, DC will impose a penalty by deducting a certain amount of the staked DCT tokens.

This structured approach to node management within the DC network ensures that each node’s entry and exit are controlled and secure, maintaining the overall integrity and consistency of the network’s data.
