# TETHER USD (USDT)

## TRC-20 Token — TRON Network

### Whitepaper

**Version:** 1.0
**Blockchain:** TRON
**Token Standard:** TRC-20
**Token Name:** TETHER USD
**Token Symbol:** USDT
**Decimals:** 6
**Maximum / Fixed Supply:** 10,000,000,000 USDT

---

# 1. Abstract

TETHER USD (USDT) is a fixed-supply TRC-20 token implemented as a smart contract on the TRON network.

The token is designed to provide standard TRC-20 functionality, including token transfers, balances, approvals, allowances, and delegated transfers through `transferFrom`.

The deployed contract defines a fixed initial supply of **10 billion tokens**, with all initial tokens assigned to the deploying address at deployment.

The contract does not provide a public minting mechanism after deployment and does not provide a public burning mechanism.

This document describes the technical characteristics and functionality of the token contract.

---

# 2. Token Specification

| Parameter            | Specification       |
| -------------------- | ------------------- |
| Token Name           | TETHER USD          |
| Symbol               | USDT                |
| Network              | TRON                |
| Standard             | TRC-20              |
| Decimals             | 6                   |
| Total Supply         | 10,000,000,000 USDT |
| Initial Distribution | 100% to deployer    |
| Public Minting       | No                  |
| Public Burning       | No                  |
| Transfer Tax         | None                |
| Transfer Fee         | None                |
| Blacklist            | None                |
| Pause Mechanism      | None                |
| Freeze Mechanism     | None                |
| Upgrade Mechanism    | None                |

The contract source explicitly defines the token's name, symbol, decimals, and 10-billion-token initial supply.

---

# 3. TRON and TRC-20

The token is designed for the TRON network using the TRC-20 token interface.

The contract implements the standard functions required for token accounting and transfers:

* `totalSupply()`
* `balanceOf()`
* `transfer()`
* `allowance()`
* `approve()`
* `transferFrom()`

It also emits the standard:

* `Transfer`
* `Approval`

events.

These functions and events are defined directly in the uploaded contract source.

---

# 4. Token Supply

The contract establishes a fixed initial supply of:

**10,000,000,000 USDT**

Because the token uses 6 decimals, one whole token corresponds to:

**1,000,000 base units**

Therefore the blockchain-level representation of the total supply is:

**10,000,000,000 × 1,000,000 = 10,000,000,000,000,000 base units**

## The contract stores this amount as its immutable total supply and assigns the entire amount to the deployer's address during construction.

# 5. Initial Distribution

At deployment, the complete supply is assigned to the address that deploys the contract.

The constructor initializes the owner, establishes the total supply, assigns the entire balance to `msg.sender`, and emits the corresponding transfer and ownership events.

There is no allocation mechanism in the contract for investors, team members, treasury wallets, or other predefined addresses.

Any subsequent distribution therefore occurs through ordinary token transfers.

---

# 6. Token Transfers

The contract supports standard token transfers.

A holder can call:

`transfer(recipient, amount)`

to transfer tokens from their own balance to another address.

The internal transfer mechanism checks that:

* The sender is not the zero address.
* The recipient is not the zero address.
* The sender has sufficient balance.

## The sender's balance is reduced and the recipient's balance is increased by the specified amount. A `Transfer` event is emitted for each successful transfer.

# 7. Allowances and Delegated Transfers

The token supports the standard ERC-20/TRC-20 allowance model.

A token holder can approve another address to spend a specified amount of tokens using:

`approve(spender, amount)`

The approved spender can subsequently use:

`transferFrom(sender, recipient, amount)`

subject to the available allowance.

The contract also provides:

* `increaseAllowance()`
* `decreaseAllowance()`

for managing existing allowances.

---

# 8. Fixed-Supply Architecture

The contract does not expose a public or external mint function.

The initial supply is established during contract deployment and stored as an immutable value.

The contract also does not expose a public burn function.

Consequently, according to the uploaded source, the token's supply cannot be increased through a public contract function after deployment.

---

# 9. Ownership

The contract contains an ownership mechanism.

The deploying address becomes the initial owner.

Ownership can be transferred using a two-step process:

1. The current owner calls `transferOwnership()`.
2. The nominated address calls `acceptOwnership()`.

The ownership mechanism does not provide the owner with a minting function, blacklist function, freeze function, or pause function in the uploaded implementation.

---

# 10. Token Metadata

The contract contains two fixed metadata-related URLs:

* `metadataURI()`
* `logoURI()`

The uploaded source currently points these to files hosted in the project's GitHub repository.
The metadata can be used to provide publicly accessible project information, including token information and a logo, where supported by third-party wallets, explorers, applications, or token-list systems.

Metadata availability does not by itself constitute verification or endorsement by any wallet, exchange, explorer, blockchain organization, or token issuer.

---

# 11. Wallet and Application Compatibility

Because the contract implements standard TRC-20 functions and events, compatible TRON wallets and decentralized applications can interact with the token through its contract address.

Compatibility depends on the individual wallet or application.

A wallet may require the token to be manually added or may use its own token-list and verification system before displaying a token logo or additional metadata.

---

# 12. Decentralized Exchange Compatibility

The contract contains standard transfer and allowance functionality required for interaction with compatible decentralized applications.

A decentralized exchange can interact with the token through the standard token interface, subject to the exchange's own listing requirements, token verification policies, liquidity requirements, and risk controls.

Deployment of a TRC-20 contract does not automatically create a trading market or guarantee exchange listing.

---

# 13. Security Model

The contract implements basic checks intended to prevent invalid token accounting operations.

Transfer operations verify sufficient balances and reject zero-address transfers.

Allowance operations reject the zero address as a spender.

The contract uses Solidity 0.8.20, which provides built-in arithmetic overflow and underflow checks except where explicitly bypassed with `unchecked`.

The source should nevertheless undergo independent security review before being relied upon for significant financial value.

This document is a technical description of the supplied source and is not an independent smart-contract audit.

---

# 14. Transparency

The project's contract source code, token metadata, logo, and documentation may be made publicly accessible through appropriate repositories and blockchain explorers.

Users should independently verify the official contract address before interacting with the token.

The token's contract address is the authoritative blockchain identifier for the deployed token.

Names, symbols, logos, websites, and metadata should not be treated as proof of token authenticity.

---

# 15. Risk Disclosure

Digital assets and smart contracts involve technical, financial, operational, and market risks.

Potential risks include:

* Smart-contract vulnerabilities.
* Loss or compromise of private keys.
* Incorrect transactions.
* Network congestion or outages.
* Wallet compatibility issues.
* Liquidity limitations.
* Market-price volatility.
* Third-party application failures.
* Phishing and impersonation.
* Incorrect contract-address selection.

Users should verify the contract address and transaction details before interacting with the token.

No statement in this document guarantees a particular market value, exchange rate, liquidity level, or financial return.

---

# 16. Important Identity and Issuer Disclosure

The token described in this document uses the name **TETHER USD** and symbol **USDT** as specified by the supplied smart-contract source.

Unless separately demonstrated through official documentation or authorization, this document does **not** establish that the token is issued by, backed by, endorsed by, or affiliated with Tether Limited or the official Tether USD token.

Users should distinguish this token from officially issued Tether USD tokens by checking the blockchain network and exact contract address.

---

# 17. Technical Summary

The supplied contract provides:

**Token**

* TETHER USD
* USDT
* TRC-20
* TRON
* 6 decimals

**Supply**

* 10,000,000,000 USDT
* Fixed at deployment
* Entire initial supply assigned to deployer

**Standard functionality**

* Transfer
* TransferFrom
* Approve
* Allowance
* Increase allowance
* Decrease allowance
* Balance tracking
* Total supply tracking

**Additional functionality**

* Ownership transfer
* Metadata URI
* Logo URI

**Not included**

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

# 18. Conclusion

TETHER USD (USDT), as described by the supplied smart contract, is a fixed-supply TRC-20 token implemented on the TRON network.

The contract establishes a total supply of **10 billion tokens with 6 decimal places**, assigns the initial supply to the deployer, and provides standard TRC-20 transfer and allowance functionality.

The project can provide additional public information through metadata, a logo, a website, and a whitepaper. Wallet and explorer visibility, however, depends on the individual platform's token-listing and verification systems.

Users should always verify the token's exact contract address before interacting with it.
