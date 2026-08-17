# INFINITY USD (IUSD) — TRC-20

## Overview

**INFINITY USD (IUSD)** is a TRC-20 token implemented on the TRON network.

The supplied smart contract defines a fixed initial supply of **10,000,000,000 IUSD** with **6 decimal places**. The complete initial supply is assigned to the deploying address at deployment.

INFINITY USD is an independent token project and should not be represented as an official, issued, backed, endorsed, or authorized token of any other company or token issuer unless separate authorization exists.

---

## Token Information

| Property     | Value               |
| ------------ | ------------------- |
| Name         | INFINITY USD        |
| Symbol       | IUSD                |
| Network      | TRON                |
| Standard     | TRC-20              |
| Decimals     | 6                   |
| Total Supply | 10,000,000,000 IUSD |
| Supply Model | Fixed               |
| Public Mint  | No                  |
| Public Burn  | No                  |
| Transfer Tax | None                |
| Transfer Fee | None                |

The supplied contract establishes the token name, symbol, 6 decimals, and 10-billion-token supply.

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

The contract source contains the corresponding functions and events.

---

## Supply

The total supply is:

**10,000,000,000 IUSD**

With 6 decimals:

**1 IUSD = 1,000,000 base units**

Therefore:

**10,000,000,000 IUSD = 10,000,000,000,000,000 base units**

The contract assigns the complete initial supply to the deployer during deployment.

---

## Contract Architecture

INFINITY USD uses a fixed-supply architecture.

There is no public mint function after deployment, and the supplied contract does not expose a public burn function.

Transfers are performed through the standard TRC-20 accounting model, with balances deducted from the sender and credited to the recipient.

The contract does not include transfer taxes or transfer fees according to the supplied implementation.

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

The project's public resources may include:

```text
/
├── info.json
├── logo.png
├── whitepaper.pdf
└── README.md
```

The metadata can provide additional information such as the INFINITY USD description, logo, official website, documentation, and whitepaper.

Wallets and other applications may use their own token-list and verification systems, so publishing metadata does not guarantee that every platform will automatically display it.

---

## Whitepaper

The INFINITY USD whitepaper provides a more detailed description of:

* Token specifications
* Fixed supply
* TRC-20 functionality
* Initial distribution
* Ownership
* Metadata
* Security considerations
* Risk disclosures
* Project architecture

See:

`whitepaper.pdf`

---

## Security

Users should verify the exact INFINITY USD contract address before interacting with the token.

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

Users should independently review the verified contract source and conduct appropriate due diligence before interacting with the token.

---

## Verification

The deployed INFINITY USD contract source should be verified on TRONSCAN using the exact source code and compiler configuration used for deployment.

Verification allows users to inspect the published source corresponding to the deployed bytecode.

Contract verification does not by itself constitute an endorsement, investment recommendation, or guarantee of security.

---

## TRON Ecosystem

INFINITY USD is designed to use the TRC-20 interface on TRON.

Compatibility with wallets, explorers, decentralized exchanges, and other applications depends on each platform's individual support and listing or verification procedures.

Deployment of a token on TRON does not automatically guarantee listing, liquidity, or visibility on every wallet, exchange, or application.

---

## Repository Files

### `info.json`

Machine-readable metadata for INFINITY USD.

### `logo.png`

INFINITY USD project/token logo.

### `whitepaper.pdf`

Detailed INFINITY USD project documentation.

### `README.md`

Repository overview and technical information.

---

## Project Identity

**INFINITY USD (IUSD)** is an independent digital-token project operating on the TRON network.

The name, symbol, logo, website, metadata, or other branding associated with INFINITY USD should not be interpreted as evidence of affiliation with another token issuer, financial institution, company, or organization unless such affiliation is explicitly documented and independently verifiable.

Users should always identify the token by its exact blockchain contract address rather than relying solely on its name or symbol.

---

## Disclaimer

This repository describes the supplied INFINITY USD smart-contract implementation and its technical characteristics.

Nothing in this documentation constitutes a promise of market value, exchange rate, liquidity, financial return, or investment performance.

Users should independently verify the contract address, source code, token information, metadata, and project documentation before interacting with INFINITY USD.

Digital assets involve significant risks, and users are responsible for conducting their own due diligence.

---

## License

The supplied contract specifies the **MIT License**.

See the source code for the applicable license notice.
