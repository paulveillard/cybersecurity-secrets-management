# Understanding Secrets Management - Hashicorp Vault

> Note: A large portion of text in this design document is borrowed from other sources (mainly from Hashicorp's product documentation). Furthermore, a lot of of images have been borrowed and reused as necessary within the scope of this document.

# Table of Contents
- [Introduction to Secrets Management](#)
  - [The Secret](#)
  - [The Challenge](#)
  - [The Solution](#)
  - [The Secret Management Tool "Vault"](#)


## `1 - Introduction to Secrets Management`

Secrets management is the process of managing secrets in a secure and centralized manner, throughout the secrets lifecycle or is the use of tools and methods to securely store, access and centrally manage the lifecycle of digital authentication credentials.

![vault](https://github.com/paulveillard/cybersecurity-secrets-management/blob/main/hashicorp-vault/Img/Vault-1.png)

 

With increasing complexity and modernization, DevOps or Security Engineers need a standard method for managing and maintaining secrets within modern environments. Frequently, engineering teams produce proof-of-concept level applications by hard-coding secrets into source code, or enterprises will create complex secret management ecosystems. The most common strategies are listed below:

### `1.1 The Secret`

These non-human privileged credentials are often called “secrets” and refer to a private piece of information that acts as a key to unlock protected resources or sensitive information in tools, applications, containers, DevOps and cloud-native environments.

Some of the most common types of secrets include:

- Privileged account credentials

- Passwords

- Certificates

- SSH keys

- API keys

- Encryption keys

### `1.2 The Challenge`

A non-human user with access to a secret automatically gains real-time access and permissions to any resources belonging to the owner of the secret. Cyber attackers understand this and target secrets to gain unauthorized access to additional secrets and hosts to complete their mission. A cyber attack targeting secrets can often spread far beyond the scope of the initial breach.

[Secrets are widespread](https://www.hashicorp.com/resources/what-is-secret-sprawl-why-is-it-harmful). They include embedded hard-coded credentials in containerized applications (e.g., Red Hat OpenShift, Kubernetes or Pivotal); automation processes (e.g., Ansible Playbooks, Puppet or Chef); business-critical applications, including both internally developed and commercial off-the-shelf solutions (COTS); security software, such as vulnerability scanners; application servers and IT management software, Robotic Process Automation (RPA) platforms and the Continuous Integration/Continuous Deployment (CI/CD) tool chain.

- Hard-Coded Secrets – Teams store sensitive data in source code.‍

- Configuration Files – Teams consolidate sensitive data in configuration files. Generally, these files contain only material required by a single application or service, however, teams occasionally maintain “master config” files. These files possess secrets for multiple services and allow teams to maintain only a single manifest.‍

- Encrypted Secrets – Teams frequently check-in source code or configuration files which contain encrypted secrets. These secrets must be “unpacked” by either an encryption service or with a decryption key provided to the application.


### `1.3 The Solution`

Secrets management tools help companies securely store, transmit, and manage sensitive digital authentication credentials such as passwords, SSH keys, API keys, database passwords, certificates like TLS/SSL certificates or private certificates, tokens, encryption keys, privileged credentials, and other secrets.

Companies use these tools to manage their secrets across their IT ecosystem centrally. These tools reduce the risks associated with poor and manual secrets management, such as hardcoding secrets into scripts, using default passwords, sharing passwords, and not rotating credentials. Secrets management tools replace fragmented and manual secrets management and provide central visibility, oversight, and management of a company’s credentials, keys, and other secrets across departments. Most commonly, these tools are used by software developers, security professionals, and IT operations teams (DevOps or DevSecOps).

Secrets management tools are similar to but more robust than encryption key management software, which focuses on the storage, use, and rotation of encryption keys. Similarly, there is an overlap between secrets management and privileged access management (PAM) software. While security-focused PAM solutions offer secrets management, they also offer more robust security functions for enforcing least privilege policies with access controls, monitoring and recording privileged sessions, and alerting suspicious activity. Some secrets management solutions are built into platforms or cloud providers directly. In contrast, other solutions augment that functionality by offering a universal and centralized approach to secrets management, regardless of platform, using integrations.

To qualify for the Secrets Management category, a product must:

- Centrally manage keys and other secrets

- Securely store secrets with encryption and tokenization

- Automate pushing secrets to applications and infrastructure

- Create audit trail of secrets use and lifecycle

In recent years, several excellent projects have emerged to combat the increasing complex problem. They are dedicated secret management services and vendors like Keywhiz, Azure Key Vault, Hashicorp Vault, for [more vendors](https://www.g2.com/categories/secrets-management-tools). While these solutions are excellent, we will only discuss Vault for the sake of simplicity.

### `1.4 The Secrets Management Tool “Vault”`
[Vault](https://www.vaultproject.io/) states its purpose on its website: Secure, store and tightly control access to tokens, passwords, certificates, encryption keys for protecting secrets and other sensitive data using a UI, CLI, or HTTP API.

Essentially, Vault plays the role of hardcoded secrets, config files, or whatever other secret management strategy a team relies on. Vault, however, represents a solution which can scale to virtually any sized need, and which provides benefits far beyond simply storing sensitive material:
![vault secrets management](https://github.com/paulveillard/cybersecurity-secrets-management/blob/main/hashicorp-vault/Img/Vault-2.png)



## 3 - Vault Component Architecture
 <...TBA...>
 
 
## 4 - Vault Reference Architecture
<...TBA...>


## 5 - <Organization> Platform and Architecture
<...TBA...>
  
  
  
## 6 - <Organization> Platform and Vault Integration Considerations
<...TBA...>

