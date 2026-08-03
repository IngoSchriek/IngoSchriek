## Ingo Schriek

Backend engineer working on digital signature and public key infrastructure. Certificate
issuance, signing protocols, cryptographic hardware, and the standards that tie them
together: ICP-Brasil, CSC, PKCS#11, KMIP.

Most of what I build lives in private repositories at [Rubrix.lat](https://rubrix.lat) and
[LabSEC/UFSC](http://www.labsec.ufsc.br/), so this page is a map of the work rather than the
code itself.

---

### Rubrix.lat, Backend Developer (2026 to present)

Digital signature platform with legal validity for Latin America, built around a single
promise: signing a document through Pix in under a minute.

| Feature | Description |
|---|---|
| **FinanceID** | Patented core technology that turns a Pix transaction into an identity for signing. The signer confirms a R$ 0.01 Pix, bank KYC validates who they are, and a single use certificate is issued to sign the document. No prior certificate, no installation. |
| **CSC broker** | Acts as CSC (Cloud Signature Consortium) client and server at the same time, routing a signature either to other CSC providers or to national ones such as gov.br. Positions the platform as a single interoperability point between the international standard and the Brazilian signature ecosystem. |
| **Rubrix Token** | Local signing agent for A3 certificates (tokens and smartcards over PKCS#11) and A1 certificates (PKCS#12 files), the case a browser alone has not handled since Java applets died. Ships as a GraalVM native binary, with no JRE or browser extension required. Pairs with the backend over OAuth2 for native apps (RFC 8252, public client, PKCE, loopback redirect) and holds a WebSocket channel through which the backend requests signatures, approved by the user in native OS dialogs. |
| **Platform** | Multi-tenant architecture with per tenant isolation and configurable restrictions, OAuth2 server and client, ICP-Brasil (ITI) integration and S3 compatible storage. |

---

### LabSEC/UFSC, Backend Developer (2024 to present)

| Project | Description |
|---|---|
| **Hawa** | Issuance and lifecycle management of digital certificates: validation, issuance and signing, CRL generation and an OCSP service. It backs the gov.br electronic signer, responsible for more than 500 thousand signatures a day. I had a central role in its migration to post-quantum cryptography, adding support for quantum resistant algorithms. |
| **Amanajé** | Java library for talking to Hardware Security Modules over KMIP, co-created from scratch. I worked on the protocol decoder, the component that reads the binary TTLV encoding and makes every HSM operation in the library possible. |
| **Urutau** | PKCS#11 interface in C++ for key management and digital signatures backed by HSMs, part of a Trusted Service Provider implementation under DOC ICP 17.01, in use at a private institution. I proposed the structural base and the design patterns it uses today. |
| **Ybyra** | Issuance and management of attribute certificates, assigning roles, permissions or qualifications to a digital identity. |

---

### Before that

Research assistant at UFSC (2023 to 2024), on Self-Sovereign Identity and blockchain applied
to forensic computing, specifically the management and traceability of forensic evidence.
Hyperledger Indy, Aries and AnonCreds.

---

### Public repositories

| Repository | What it does |
|---|---|
| [libprune-maven-plugin](https://github.com/IngoSchriek/libprune-maven-plugin) | Maven plugin that iteratively restores deleted classes until compilation succeeds. |
| [cross-ref-scanner](https://github.com/IngoSchriek/cross-ref-scanner) | Finds unused symbols across projects. Java, Python and others. |

---

### Stack

<code>Java</code> <code>Spring Boot</code> <code>Quarkus</code> <code>GraalVM native image</code> <code>Bouncy Castle</code>
<code>PKCS#11</code> <code>PKCS#12</code> <code>KMIP</code> <code>HSM</code> <code>PKI</code>
<code>ICP-Brasil</code> <code>CSC</code> <code>OAuth2</code> <code>PostgreSQL</code>
<code>Redis</code> <code>Docker</code> <code>Python</code> <code>C++</code>

### Reach me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ingo-schriek/)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ingoquina@gmail.com)
