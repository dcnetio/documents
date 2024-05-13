# Core Services&#x20;

The DC network, comprised of numerous self-organizing DCNodes, offers a robust framework for providing decentralized cloud services to users. Each node within this network operates within a Trusted Execution Environment (TEE), which is pivotal for ensuring the absolute privacy and security of user data. Below, we delve deeper into the main functionalities and supporting mechanisms that enable DCNodes to deliver these services effectively:

#### Core Services of DCNodes

1. **Basic Data Storage:**
   * **Technology Used:** DCNodes leverage the InterPlanetary File System (IPFS) to provide file data storage services.
   * **User Interaction:** Users interact with this storage via DC's decentralized applications (DApps).
   * **Data Reliability:** To ensure reliability and availability, DCNode maintains no fewer than three copies of data backups for each file stored.
2. **Database Storage:**
   * **Service Type:** This is a multi-threaded distributed database storage service, which supports applications requiring multi-terminal concurrent access.
   * **Capacity Provisioning:** Storage space is allocated based on user demands, similar to the basic data storage service.
   * **Data Backup:** Each database is backed up in at least three locations to ensure data integrity and availability.
   * **Data Security:** All data is stored encrypted, and only the user can decrypt and access it.
3. **Social Routing:**
   * **Purpose:** This service enables DApps to encrypt and store users' basic information, social relationships, and social process data.
   * **Application:** It is particularly useful for developers aiming to create social networking DApps, offering functionalities similar to popular platforms like Facebook, Twitter, and LinkedIn.
   * **Privacy and Security:** The use of encryption and storage within the secure TEE environment enhances privacy and security for user data.
4. **Message Caching:**
   * **Service Duration:** Offers caching of messages for up to 10 days.
   * **Functionality:** Ensures that users do not miss messages from other users or platforms when they are offline, enhancing communication reliability.

DCNodes form a critical part of the DC cloud service network, providing robust, secure, and scalable cloud services to users. The use of TEEs across all nodes ensures that data privacy and security are maintained at the highest standards. The variety of services offered—from basic data storage to specialized services like social routing—demonstrates the network's flexibility and its potential to support a wide range of applications and use cases.

These services are integrated through an account system, incentive mechanisms, and data indexing mechanisms provided by DCChain, which likely serves as the underlying blockchain technology enabling decentralized consensus and transaction verification within the network. This integration not only enhances the functionality of individual nodes but also ensures that the network operates efficiently and remains resilient against various types of failures or attacks.
