# Teaching material: Blockchain, Decentralized IAM and Federated Learning

Course slides and lab subjects for a master-level teaching activity on blockchain, decentralized identity and access control (D-IAM), and federated learning (FL).

This repository contains **only the material I developed**. All content is written in **French**.

## Contents

### Courses

| Course | File | Topics |
|---|---|---|
| Decentralized identity and access control (D-IAM) | `cours/DIAM.pdf` | DIDs, Verifiable Credentials, SSI, privacy, access control (RBAC/ABAC), Hyperledger Besu |
| Introduction to blockchain | `cours/Blockchain.pdf` | Cryptographic foundations, consensus, smart contracts, security, scalability |
| Federated learning | `cours/FL.pdf` | FedAvg, non-IID data, privacy, poisoning and backdoors, robust aggregation, decentralized FL |

Each course is organized in 10 modules and ends with exercises, discussion questions and references.

### Labs and project (HTML)

| Reference | Subject |
|---|---|
| TP1 | Introduction to blockchain (Besu, QBFT, Solidity, Remix) |
| TP2 + tutorial | DApp development: NFT with Hardhat, IPFS, Web3.js, MetaMask |
| TP3 | Decentralized access control with smart contracts (RBAC and ABAC) |
| TD | Federated learning with Flower, PyTorch and FashionMNIST |
| TP4 | Robust FL: poisoning attacks and defenses |
| TP5 | Blockchain-based federated learning (BFL) |
| Project | FL and BFL on FashionMNIST |

Open `TPs/index.html` in a browser for the overview. Suggested order: TP1 → TP2 → TP3 and TD → TP4 → TP5 → Project.

## Repository structure

```
.
├── README.md
├── courses/
│   ├── DIAM.pdf
│   ├── Blockchain.pdf
│   └── FL.pdf
└── TPs/
    ├── index.html
    ├── style.css
    ├── TP1_Introduction_Blockchain.html
    ├── TP2_Introduction_DApps.html
    ├── Tuto_DApp_NFT.html
    ├── TP3_Introduction_DIAM.html
    ├── TD_Introduction_FL.html
    ├── TP4_Robust_FL.html
    ├── TP5_BFL.html
    └── Projet_FL.html
```


## Tools used in the labs

- Hyperledger Besu, Docker or a Linux VM (TP1, TP2, TP3, TP5)
- Node.js, Hardhat, MetaMask, IPFS (Kubo) (TP2, TP3)
- Python, PyTorch, Flower (TD, TP4, TP5, Project)

Some versions of these tools evolve quickly: check the commands against the current documentation before running.

