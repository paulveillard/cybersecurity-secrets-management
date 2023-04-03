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

1.2 The Challenge

A non-human user with access to a secret automatically gains real-time access and permissions to any resources belonging to the owner of the secret. Cyber attackers understand this and target secrets to gain unauthorized access to additional secrets and hosts to complete their mission. A cyber attack targeting secrets can often spread far beyond the scope of the initial breach.

[Secrets are widespread](https://www.hashicorp.com/resources/what-is-secret-sprawl-why-is-it-harmful). They include embedded hard-coded credentials in containerized applications (e.g., Red Hat OpenShift, Kubernetes or Pivotal); automation processes (e.g., Ansible Playbooks, Puppet or Chef); business-critical applications, including both internally developed and commercial off-the-shelf solutions (COTS); security software, such as vulnerability scanners; application servers and IT management software, Robotic Process Automation (RPA) platforms and the Continuous Integration/Continuous Deployment (CI/CD) tool chain.

- Hard-Coded Secrets – Teams store sensitive data in source code.‍

- Configuration Files – Teams consolidate sensitive data in configuration files. Generally, these files contain only material required by a single application or service, however, teams occasionally maintain “master config” files. These files possess secrets for multiple services and allow teams to maintain only a single manifest.‍

- Encrypted Secrets – Teams frequently check-in source code or configuration files which contain encrypted secrets. These secrets must be “unpacked” by either an encryption service or with a decryption key provided to the application.
