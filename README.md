# TETHER USD (USDT) — TRC-20

## Overview

TETHER USD (USDT) is a TRC-20 token implemented on the TRON network.

The supplied smart contract defines a fixed initial supply of **10,000,000,000 USDT** with **6 decimal places**. The complete initial supply is assigned to the deploying address at deployment.

> **Important:** This project should not be represented as official Tether USD, or as issued, backed, endorsed, or authorized by Tether Limited, unless separate authorization exists.

---

## Token Information

| Property     | Value               |
| ------------ | ------------------- |
| Name         | TETHER USD          |
| Symbol       | USDT                |
| Network      | TRON                |
| Standard     | TRC-20              |
| Decimals     | 6                   |
| Total Supply | 10,000,000,000 USDT |
| Supply Model | Fixed               |
| Public Mint  | No                  |
| Public Burn  | No                  |
| Transfer Tax | None                |
| Transfer Fee | None                |

The uploaded contract establishes the token name, symbol, 6 decimals, and 10-billion-token supply.

---

## Features

The contract supports standard TRC-20 functionality:

* `totalSupply()`
* `balanceOf()`
* `transfer()`
* `approve()`
* `allowance()`
* `transferFrom()`
* `increaseAllowance()`
* `decreaseAllowance()`

It also provides:

* Ownership management
* Token metadata URI
* Logo URI
* Standard `Transfer` events
* Standard `Approval` events

## The contract source contains the corresponding functions and events.

## Supply

The total supply is:

**10,000,000,000 USDT**

With 6 decimals:

**1 USDT = 1,000,000 base units**

Therefore:

**10,000,000,000 USDT = 10,000,000,000,000,000 base units**

The contract assigns the complete initial supply to the deployer during deployment.

---

## Contract Architecture

The token uses a fixed-supply architecture.

There is no public mint function after deployment, and the supplied contract does not expose a public burn function.

Transfers are performed through the standard TRC-20 accounting model, with balances deducted from the sender and credited to the recipient.

---

## Ownership

The deploying address becomes the initial contract owner.

Ownership can subsequently be transferred through a two-step process:

1. The current owner nominates a new owner.
2. The nominated owner accepts ownership.

Ownership functionality is separate from token supply management in the supplied implementation.

---

## Metadata

The contract includes functions for retrieving project metadata and the token logo:

```text
metadataURI()
logoURI()
```

The supplied contract currently references GitHub-hosted resources for these URLs.

A project repository can contain:

```text
/
├── info.json
├── logo.png
├── whitepaper.pdf
└── README.md
```

The metadata can provide additional information such as the token description, logo, website, and whitepaper.

Wallets and other applications may use their own token-list and verification systems, so publishing metadata does not guarantee that every platform will automatically display it.

---

## Whitepaper

The project whitepaper provides a more detailed description of:

* Token specifications
* Supply
* TRC-20 functionality
* Distribution
* Ownership
* Metadata
* Security considerations
* Risk disclosures

See:

`whitepaper.pdf`

---

## Security

Users should verify the token's exact contract address before interacting with it.

Smart-contract and digital-asset activity involves risks including:

* Smart-contract vulnerabilities
* Private-key compromise
* Incorrect transactions
* Network issues
* Wallet compatibility problems
* Liquidity limitations
* Market volatility
* Phishing and impersonation

This repository documentation is not an independent security audit.

---

## Verification

The deployed contract source should be verified on TRONSCAN using the exact source code and compiler configuration used for deployment.

Verification allows users to inspect the published source corresponding to the deployed bytecode.

---

## TRON Ecosystem

The token is designed to use the TRC-20 interface on TRON.

Compatibility with wallets, explorers, decentralized exchanges, and other applications depends on each platform's individual support and listing/verification procedures.

A token contract being deployed on TRON does not automatically guarantee listing or visibility on every wallet, exchange, or application.

---

## Repository Files

### `info.json`

Machine-readable token metadata.

### `logo.png`

Project/token logo.

### `whitepaper.pdf`

Detailed project documentation.

### `README.md`

Repository overview and technical information.

---

## Disclaimer

This repository describes the supplied smart-contract implementation and its technical characteristics.

The use of the name **TETHER USD** and symbol **USDT** in the contract does not, by itself, establish any relationship with Tether Limited.

This project should not claim to be official Tether USD, Tether-issued USDT, or Tether-authorized unless appropriate authorization and evidence exist.

Users should independently verify the contract address, source code, token information, and project documentation before interacting with the token.

---

## License

The supplied contract specifies the **MIT License**.

See the source code for the applicable license notice.
