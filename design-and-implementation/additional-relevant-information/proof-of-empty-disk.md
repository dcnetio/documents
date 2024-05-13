# Proof of Empty Disk

To accurately gauge the storage capacity offered by nodes in the network, a unique method called the empty disk encapsulation mechanism has been established. This mechanism is designed to ensure the authenticity and veracity of the storage space that nodes claim to provide . Here’s how the process works:

#### Overview of the Empty Disk Encapsulation Mechanism:

1. **File generation rule:** All filenames are generated in numerical order.
2. **Hash Process**: Following encryption, the node performs a series of HASH operations on the encrypted filename. This process generates a 256-length seed that is uniquely associated with the filename of the encapsulation file.
3. **File Generation**: Using the generated seed, the node then creates a 1GB encapsulation file. This file is constructed in a chained manner, starting from the seed, ensuring that each part of the file is derived from the initial seed.
4. **Integrity Verification**: The integrity of this 1GB encapsulation file can be verified at any position within the file through random sampling. This method ensures that the storage space reported by the node is genuine and not fabricated.

#### Significance of the Encapsulation Mechanism:

* **Authenticity**: This mechanism ensures that the declared storage capacity of a node is authentic. Since each encapsulation file is generated from a unique seed derived from a secure hash process, it is nearly impossible to falsely represent storage capacity.
* **Verifiability**: The ability to verify the integrity of the storage at any point in the encapsulation file adds an additional layer of security and trust. Stakeholders can perform random checks to confirm that the storage space is not only genuine but also functioning as expected.
* **Security**: Encrypting the filename within the TEE and generating a secure seed for file creation helps protect against potential security threats, ensuring that the storage space cannot be tampered with or compromised.

This encapsulation mechanism is a critical component in maintaining the reliability and security of the storage solutions offered by nodes in the network, thereby enhancing overall trust in the system’s infrastructure.
