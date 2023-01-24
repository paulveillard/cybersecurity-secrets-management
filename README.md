#  Software Security - Secrets Management

An ongoing & curated collection of awesome software best practices and techniques, libraries and frameworks, E-books and videos, websites, blog posts, links to github Repositories, technical guidelines and important resources about  Secrets Management Process in Cybersecurity.
> Thanks to all contributors, you're awesome and wouldn't be possible without you! Our goal is to build a categorized community-driven collection of very well-known resources.

## Table of Contents
- [What Are Secrets](#)
  - [Why store secrets?](#)
  - [How do you store secrets?](#)
  - [Where do you store secrets?](#)
- [What Are Secrets Management](#)
  - [Why is Secrets Management is important](#)
- [Secrets Management Tools](#)
  - [Top 20 Best Secrets Management Tools](#)

## What Are Secrets?

Secrets are environment dependent configurations that need to be kept secret and should be read only by subjects with a need-to-know. Secrets are digital authentication credentials such as:
- Passwords, 
- SSH keys, 
- API keys, 
- AWS IAM/STS Credentials, 
- Database passwords (SQL/NoSQL), 
- X.509 certificates like TLS/SSL certificates or private certificates, 
- Tokens, 
- Locks (encryption keys), 
- Privileged credentials, and other secrets.


### Why Store Secrets?
- 
 
### How do you store Secrets
Passwords, API keys, secure Tokens, and confidential data fall into the category of secrets. That’s data which shouldn’t lie around. It mustn’t be available in plaintext in easy to guess locations. In fact, it must not be stored in plaintext in any location.

### Where do you store Secrets?

The care taken to protect our secrets applies both to how we get and store them, but also to how we use them.

    - Don't log secrets
    - Don't put them in reporting
    - Don't send them to other applications, as part of URLs, forms, or in any other way other than to make a request to the service that requires that secret


## What Are Secrets Management?

- Secrets Management refers to the way in which we protect configuration settings and other sensitive data which, if made public, would allow unauthorized access to resources. Examples of secrets are usernames, passwords, api keys, SAS tokens etc. Secrets Management centrally Manage Secrets to Reduce Secrets Sprawl.

### Why Is Secrets Management Important?

- Users need to use authentication methods to access sensitive information or company resources. Whenever these secrets or credentials are transmitted across the company, there is a risk of data leakage or lost passwords. Because of this risk, there is a critical need for organizations to protect secrets. 


## Secret Management Tools
- Secrets management tools replace fragmented and manual secrets management and provide central visibility, oversight, and management of a company’s credentials, keys, and other secrets across departments. Most commonly, these tools are used by software developers, security professionals, and IT operations teams (DevOps or DevSecOps).


> [Secrets Management Tools](https://www.g2.com/categories/secrets-management-tools)  are similar to but more robust than encryption key management software, which focuses on the storage, use, and rotation of encryption keys. Similarly, there is an overlap between secrets management and privileged access management (PAM) software. While security-focused PAM solutions offer secrets management, they also offer more robust security functions for enforcing least privilege policies with access controls, monitoring and recording privileged sessions, and alerting suspicious activity. Some secrets management solutions are built into platforms or cloud providers directly. In contrast, other solutions augment that functionality by offering a universal and centralized approach to secrets management, regardless of platform, using integrations.

To qualify for the Secrets Management category, a product must:
- Centrally manage keys and other secrets
- Securely store secrets with encryption and tokenization
- Automate pushing secrets to applications and infrastructure
- Create audit trail of secrets use and lifecycle

## Top 20 Best Secrets Management Tools Vendors (By Alphabetical Order)
### 1 Password
### Akeyless Vault Platform
### AWS Secrets Manager
### Azure Key Vault
### BeyondTrust Cloud Vault
### BeyondTrust DevOps Secrets Safe
### Confidant
### CyberArk Conjur
### Delinea Secret Server
### Delinea DevOps Secrets Vault
### EnvKey
### Google Cloud Key Management Service (KMS)
### Hashicorp Vault
### Keywhiz
### Knox
### Onboardbase
### SpectralOps


## What Are the Challenges of Secrets Management?

## What Are Some Secrets Management Best Practices?
- While it is possible to manually perform secrets management, doing so introduces the possibility of human error and can be incredibly inefficient. Generally, a password management tool is a first step. However, you should consider a more holistic approach for a large organization.

> Some secrets management tools go beyond handling standard user accounts and will also support other types of secrets such as the ones listed previously. Having a secure, centralized place to store your secrets is the only way to achieve a truly streamlined experience. 

Other secrets management best practices include:

#### General password strategies. 

> Employee passwords are often a weak point in the security of a business. Encourage passwords with high enough length and complexity. Try to change passwords regularly as well, especially for sensitive accounts. Avoid common and easily guessed passwords.

#### Centralized management. 

> With so many different types of secrets, having them all in one place for your IT department to manage is the best way to avoid leaks and mitigate risks.


#### Privileged session monitoring. 

> Software that helps manage a secrets vault can also integrate well with privileged access management (PAM) platforms, adding an extra layer of security and ensuring that access is restricted to only the users who need it. DevOps teams should be able to monitor privileged user activity and terminate sessions if necessary.


##### Threat analytics. 

> An effect of centralized secret management is the ability to analyze your secrets easily. Finding and reporting on risks is faster and more comprehensive this way.

**[`^        back to top        ^`](#)**

## License
MIT License & [cc](https://creativecommons.org/licenses/by/4.0/) license

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

To the extent possible under law, [Paul Veillard](https://github.com/paulveillard/) has waived all copyright and related or neighboring rights to this work.
