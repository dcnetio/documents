# DCChain

DCChain is a public blockchain developed on the Substrate framework, adopting a unified account system that integrates the accounts and signatures (i.e., public and private keys) of both the Ethereum EVM and Substrate systems. This integration facilitates compatibility with Ethereum wallets and DApp integrations. As the central operational component of DC, it establishes a highly trustworthy, fair, reliable, and transparent consensus mechanism for all participants in the DC ecosystem. The following are the key consensus capabilities provided by DCChain for the entire DC network:

#### 1. Maintaining the Account System for DC

* **Identity Consensus**: Provides identity consensus for users across the network ecosystem, offering user identification and labeling for all business operations within DC.
* **Account and Password System**: Supports a unique account and password system in the DC network ecosystem, aligning user experience with existing internet application logins.
* **Account Sovereignty**: Users own the sovereignty of their accounts in DC, which can be freely transferred. Accounts used for password logins in the DC network are referred to as NFT accounts to distinguish from ERC20 format accounts.
* **Login and Authentication**: When users log in using their DC NFT account and password, DCChain provides an index from the NFT account to the user's basic information storage and backup nodes, directing login requests to the corresponding DC node to provide login responses. Upon successful login, the private key of the corresponding DCChain application signature account is extracted, enabling users to conduct subsequent business operations.

#### 2. Serving as the Incentive Layer for DC

* **Reward Distribution**: DC rewards participants based on their contributions with DCT tokens.
  * **Contributors**: Includes cloud service space providers, DCChain validators, nominators, and developers of DApps based on DC.
  * **Sources of Rewards**: DCT tokens are issued by DC based on the inflation rate and are awarded to blockchain validators, cloud service space providers, and spent by DApp users to exchange for cloud service space. Rewards are proportionately awarded to DApp developers and cloud service space providers.
  * **Fairness and Transparency**: DC records data such as network contributors, contribution levels, issuance rules, and user DCT token consumption information on the blockchain, ensuring the openness, fairness, reliability, and free participation of the DC economic ecosystem.
  * **Punishment Mechanisms**: DC can track and penalize malicious behavior within the network, primarily including disruptions to chain consensus and damage to stored data.

#### 3. Serving as the Data Indexing Layer for the DC Network

* **Data Storage Location Indexing**: DApps can quickly locate the list of cloud service nodes that store file or database information based on the CID of the file or database, enabling rapid data retrieval.
* **Cloud Service Node Indexing**: DApps can quickly obtain basic information about cloud service nodes from DCChain, including network status, storage capacity, and accessible internet addresses.
* **User Information Indexing**: DApps can quickly locate the cloud service node containing user information based on the NFT account, providing fast guidance services for user NFT account password login logic.

#### 4. Serving as the Smart Contract Layer for DC

* **Smart Contract Support**: DCChain supports the development and deployment of smart contracts, providing robust support for DC's DApps. DCChain is fully compatible with EVM, allowing any DApp running on Ethereum to be seamlessly migrated to DC.

