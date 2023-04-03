# Understanding Secrets Management - Hashicorp Vault

> Note: A large portion of text in this design document is borrowed from other sources (mainly from Hashicorp's product documentation). Furthermore, a lot of of images have been borrowed and reused as necessary within the scope of this document.

## 1 - Introduction to Secrets Management

Secrets management is the process of managing secrets in a secure and centralized manner, throughout the secrets lifecycle or is the use of tools and methods to securely store, access and centrally manage the lifecycle of digital authentication credentials.

 

With increasing complexity and modernization, DevOps or Security Engineers need a standard method for managing and maintaining secrets within modern environments. Frequently, engineering teams produce proof-of-concept level applications by hard-coding secrets into source code, or enterprises will create complex secret management ecosystems. The most common strategies are listed below:

1.1 The Secret

These non-human privileged credentials are often called “secrets” and refer to a private piece of information that acts as a key to unlock protected resources or sensitive information in tools, applications, containers, DevOps and cloud-native environments.

Some of the most common types of secrets include:

- Privileged account credentials

- Passwords

- Certificates

- SSH keys

- API keys

- Encryption keys
