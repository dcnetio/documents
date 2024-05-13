# Utilization Mechanism

DC operates on a user-pay model, where services are paid for using DCT tokens. The payment methods vary based on how users interact with the DC network, primarily divided into two main approaches:

#### 1. **Direct Blockchain Interaction for Business Operations**

In this approach, users directly utilize DCT tokens for business-related transactions. This includes direct interactions with DCChain for transferring DCT tokens or employing on-chain smart contract functionalities. This method represents a straightforward blockchain operation, where users engage directly with the blockchain to execute and confirm transactions.

#### 2. **Interaction with Cloud Service Nodes via DApps**

Under this model, users interact indirectly with DCChain through cloud service nodes, which handle the business operations. For transactions that require blockchain recording, cloud service nodes prepare and submit the requests on users’ behalf after generating an Ed25519 signature. This setup eliminates direct blockchain interaction fees for users. However, users must first subscribe to DC cloud service space using DCT tokens for a specified period, such as on a monthly or annual basis. This subscription ensures real-time and deterministic interactions with DCNode, bypassing the delays associated with blockchain confirmation times and interaction fees.

(Note: In most cases, DCNodes interacting online with DCChain also do not incur transaction fees.)

The introduction of the second method addresses the limitations of current blockchain networks, where all operations are executed on-chain. This traditional model is not always practical for developing extensive applications due to even minimal gas fees, which can add up. By only charging for operations that deliver tangible value, DC circumvents the inefficiencies of on-chain processing for every action, which could stifle the realization of many business logics.

DC supports both deterministic and non-value-generating business logic through services akin to those provided by centralized cloud service nodes. Moreover, blockchain's inherent transaction ordering and block confirmation processes remain unchanged, regardless of specific business needs, which can introduce delays in DApp responses. To mitigate this and enhance user experience, DC delegates non-essential blockchain interactions to DCNode, ensuring seamless continuity and accuracy in data recording on the blockchain. This method significantly improves the responsiveness and user experience of DApps operating within the DC ecosystem.

\
