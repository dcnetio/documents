# Upgrade of DCNode

Here’s a streamlined and coherent summary of the upgrade process for DCNode based on the TEE (Trusted Execution Environment) within the context of using the Substrate framework:

#### Upgrade Process for DCNode Leveraging TEE

**Background:** The Substrate framework offers a robust non-forking upgrade mechanism. However, since DCNode primarily operates within a TEE environment, this standard mechanism is not directly applicable. The DC team has adapted the Substrate's non-forking upgrade approach for DCChain updates, while DCNode upgrades are managed through a TEE-specific mechanism.

**Introduction of DCUpgrade Application:** The DCUpgrade application, which also runs in the TEE, facilitates the upgrade process. Its main function is to securely transfer cryptographic keys from the old version of DCNode to the new version, ensuring that the new version can decrypt and access data managed by the old version.

**Detailed Upgrade Steps:**

1. **Monitoring and Downloading:**
   * The DCUpgrade application continuously monitors DCChain for any new versions of the DCNode program that are verified by the DC network signature.
   * Upon detecting a new version, it automatically downloads this version for installation.
2. **Key Request and Verification:**
   * DCUpgrade requests the application keys from the currently active DCNode.
   * The existing DCNode then sends a TEE local proof challenge to DCUpgrade, which includes a random number.
3. **Proof Generation and Key Transfer:**
   * DCUpgrade responds by generating a TEE local proof using the provided random number and the DC-signed EnclaveID, and sends this proof back to DCNode.
   * After verifying the proof and the signature on the EnclaveID, DCNode sends the application keys to DCUpgrade.
4. **Application Key Encapsulation and Node Shutdown:**
   * DCUpgrade safely encapsulates the application keys within the TEE and shuts down the current DCNode program.
5. **Launching New Version:**
   * DCUpgrade initiates the new version of the DCNode program.
   * The new DCNode then requests the application keys from DCUpgrade.
6. **Final Verification and Handover:**
   * DCUpgrade issues another TEE local proof challenge to the new DCNode.
   * Upon successful verification of the proof by the new DCNode and confirmation of DCNode’s signature by DC, DCUpgrade transfers the application keys to the new DCNode.
   * The new version of DCNode then seamlessly takes over from the old version, completing the upgrade process.

This process ensures a secure and efficient transition between software versions, maintaining data integrity and continuity in the TEE environment.
