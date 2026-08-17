# INFINITY USD (IUSD)

## TRC-20 Token — TRON Network

### Whitepaper

**Version:** 1.0
**Blockchain:** TRON
**Token Standard:** TRC-20
**Token Name:** INFINITY USD
**Token Symbol:** IUSD
**Decimals:** 6
**Maximum / Fixed Supply:** 10,000,000,000 IUSD

---

# 1. Abstract

**INFINITY USD (IUSD)** is a fixed-supply TRC-20 token designed to operate on the TRON network.

The token is designed to provide standard TRC-20 functionality, including token transfers, balances, approvals, allowances, and delegated transfers through `transferFrom`.

The token establishes a fixed initial supply of **10 billion IUSD**, with the initial supply assigned to the deploying address at deployment, according to the supplied contract specification.

The contract does not provide a public minting mechanism after deployment and does not provide a public burning mechanism, according to the supplied implementation.

INFINITY USD is intended to provide a straightforward and transparent digital-token architecture for users and applications that support TRC-20 assets.

---

# 2. Token Specification

| Parameter            | Specification       |
| -------------------- | ------------------- |
| Token Name           | INFINITY USD        |
| Symbol               | IUSD                |
| Network              | TRON                |
| Standard             | TRC-20              |
| Decimals             | 6                   |
| Total Supply         | 10,000,000,000 IUSD |
| Initial Distribution | 100% to deployer    |
| Public Minting       | No                  |
| Public Burning       | No                  |
| Transfer Tax         | None                |
| Transfer Fee         | None                |
| Blacklist            | None                |
| Pause Mechanism      | None                |
| Freeze Mechanism     | None                |
| Upgrade Mechanism    | None                |

The token's name, symbol, decimal precision, and supply are defined by the deployed smart contract.

---

# 3. TRON and TRC-20

INFINITY USD is designed for the **TRON blockchain** using the TRC-20 token standard.

The contract provides standard token functionality including:

* `totalSupply()`
* `balanceOf()`
* `transfer()`
* `allowance()`
* `approve()`
* `transferFrom()`

The contract also emits standard:

* `Transfer`
* `Approval`

events.

This standard interface allows compatible TRON wallets, decentralized applications, and other blockchain services to interact with the token.

---

# 4. Token Supply

The total supply of INFINITY USD is:

**10,000,000,000 IUSD**

The token uses **6 decimal places**.

Therefore, one whole IUSD corresponds to:

**1,000,000 base units**

The blockchain-level representation of the total supply is:

**10,000,000,000 × 1,000,000 = 10,000,000,000,000,000 base units**

The supply is established at deployment according to the supplied contract architecture.

---

# 5. Initial Distribution

At deployment, the initial token supply is assigned to the deploying address.

The entire supply can subsequently be distributed through ordinary token transfers.

The contract does not define predetermined allocations for investors, team members, treasury wallets, or other parties.

Any future distribution is therefore performed through standard blockchain transactions from addresses holding IUSD.

---

# 6. Token Transfers

INFINITY USD supports standard TRC-20 token transfers.

A holder can call:

`transfer(recipient, amount)`

to transfer IUSD from their own balance to another address.

The transfer mechanism verifies that:

* The sender is not the zero address.
* The recipient is not the zero address.
* The sender has sufficient balance.

Following a successful transfer, the sender's balance is reduced and the recipient's balance is increased by the specified amount.

A standard `Transfer` event is emitted for successful transfers.

---

# 7. Allowances and Delegated Transfers

INFINITY USD supports the standard allowance mechanism.

A token holder can approve another address to spend a specified amount using:

`approve(spender, amount)`

The approved address can subsequently call:

`transferFrom(sender, recipient, amount)`

subject to the available allowance.

The contract also supports:

* `increaseAllowance()`
* `decreaseAllowance()`

where implemented in the supplied contract.

This functionality enables compatible decentralized applications and smart contracts to interact with IUSD on behalf of token holders.

---

# 8. Fixed-Supply Architecture

INFINITY USD follows a fixed-supply architecture.

The contract does not expose a public minting function.

The initial supply is established during deployment and cannot be increased through a public minting mechanism according to the supplied implementation.

The contract also does not expose a public burn function.

The resulting architecture is intended to provide predictable token-supply characteristics.

---

# 9. Ownership

The supplied contract contains an ownership mechanism.

The deploying address becomes the initial owner.

Ownership can be transferred through the contract's ownership-transfer process.

Ownership itself does not provide the owner with a public minting, blacklist, freeze, pause, or upgrade mechanism according to the supplied implementation.

Users should independently verify the deployed source code and ownership status on the relevant blockchain explorer.

---

# 10. Token Metadata

INFINITY USD may provide public metadata through:

* `metadataURI()`
* `logoURI()`

These resources can contain information such as token details, project documentation, branding, and logo assets.

Wallets, explorers, decentralized applications, and token-list services may use this information where supported.

Metadata visibility is dependent on the individual platform and does not constitute independent verification or endorsement.

---

# 11. Wallet and Application Compatibility

Because INFINITY USD follows the TRC-20 token interface, compatible TRON wallets and decentralized applications can interact with the token through its contract address.

Individual platforms may have their own requirements for displaying tokens, logos, symbols, and metadata.

Users should always verify the **official IUSD contract address** before adding or transferring tokens.

---

# 12. Decentralized Exchange Compatibility

INFINITY USD provides standard transfer and allowance functionality intended to allow interaction with compatible decentralized applications.

A decentralized exchange may interact with IUSD through its standard token interface.

However, deployment of a TRC-20 token does not automatically establish liquidity, create a trading pair, or guarantee exchange listing.

Any exchange listing, liquidity pool, or trading market is subject to the policies and requirements of the relevant platform.

---

# 13. Security Model

The contract implements basic checks intended to protect token accounting and prevent invalid operations.

Transfer operations verify sufficient balances and reject zero-address transfers.

Allowance operations include checks against invalid spender addresses.

The contract uses Solidity 0.8.20, which provides built-in arithmetic overflow and underflow protection except where explicitly bypassed.

As with any smart contract, independent security review is recommended before significant financial value is placed into the system.

This whitepaper describes the supplied contract architecture and should not be considered an independent smart-contract audit.

---

# 14. Transparency

The INFINITY USD project may make its smart-contract source code, metadata, documentation, and other project information publicly accessible.

The **contract address** is the authoritative blockchain identifier for the token.

Users should independently verify:

* Contract address
* Contract source code
* Token symbol
* Token decimals
* Total supply
* Ownership status
* Transaction details

Names, symbols, logos, and websites alone should not be treated as proof of authenticity.

---

# 15. Risk Disclosure

Digital assets and blockchain-based applications involve technical, financial, operational, and market risks.

Potential risks include:

* Smart-contract vulnerabilities.
* Loss or compromise of private keys.
* Incorrect blockchain transactions.
* Network congestion or outages.
* Wallet compatibility limitations.
* Liquidity limitations.
* Market-price volatility.
* Third-party application failures.
* Phishing and impersonation.
* Fraudulent websites or contracts.
* Incorrect contract-address selection.

Users should carefully verify transaction details and the official contract address before interacting with IUSD.

Nothing in this document guarantees a particular market price, exchange rate, liquidity level, or financial return.

---

# 16. Identity and Project Disclosure

**INFINITY USD (IUSD)** is a separate token project using its own name, symbol, smart contract, and contract address.

INFINITY USD should not be represented as **Tether USD**, **USDT**, or as being issued, backed, endorsed, or affiliated with **Tether Limited** unless there is separate official authorization establishing such a relationship.

The name "INFINITY USD" and symbol "IUSD" identify this project and should be distinguished from other digital assets using similar names or symbols.

Users should verify the exact contract address when identifying the authentic INFINITY USD token.

---

# 17. Technical Summary

### Token

* INFINITY USD
* IUSD
* TRC-20
* TRON
* 6 decimals

### Supply

* 10,000,000,000 IUSD
* Fixed initial supply
* Initial supply assigned to deployer

### Standard Functionality

* Transfer
* TransferFrom
* Approve
* Allowance
* Increase allowance
* Decrease allowance
* Balance tracking
* Total supply tracking

### Additional Functionality

* Ownership transfer
* Metadata URI
* Logo URI

### Not Included

* Public minting
* Public burning
* Blacklist
* Whitelist
* Pause
* Freeze
* Transfer tax
* Transfer fee
* Upgrade mechanism

---

# 18. Vision

INFINITY USD is designed around a simple principle: provide a transparent, predictable, and accessible digital token on the TRON network.

The project aims to combine standard blockchain infrastructure with a recognizable identity and an ecosystem that can support future applications, integrations, communities, and decentralized services.

As the project develops, additional infrastructure and ecosystem initiatives may be introduced independently of the core token contract.

The smart contract remains the foundation of the token, while the broader INFINITY USD ecosystem can evolve through community participation, integrations, and future development.

---

# 19. Conclusion

INFINITY USD (IUSD) is a fixed-supply TRC-20 token designed for the TRON network.

The supplied contract establishes a total supply of **10 billion IUSD with 6 decimal places**, assigns the initial supply to the deployer, and provides standard TRC-20 transfer and allowance functionality.

The project can provide additional public information through documentation, metadata, a logo, and other official resources.

Wallet visibility, explorer recognition, decentralized-exchange availability, and token-list inclusion depend on the policies and verification procedures of individual platforms.

Users should always verify the official **INFINITY USD contract address** before interacting with the token.

**INFINITY USD — Built on TRON. Designed for the future.**
