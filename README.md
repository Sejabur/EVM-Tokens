# EVM-Tokens: Historical Taxed Token Smart Contracts

A curated archive of EVM-compatible taxed token smart contracts developed for various client projects during the peak of the 2021 meme coin era. 

---

## Backstory & Context

Having served **100+ clients** across **Fiverr and Upwork** since 2021, these files represent a historical archive of custom-tailored Solidity smart contracts. After unfortunately losing access to the primary development drive, these few files were successfully recovered from secondary backups.

 **Disclaimer & Archival Notice**
> Because these files are recovered from legacy backups, they may not represent the absolute final, production-ready, or bug-free versions deployed on mainnet. They are provided "as-is" for educational, reference, and archival purposes. Use them in production environments at your own risk.

---

## 🛠️ Included Smart Contracts

This repository contains a variety of custom ERC-20 / BEP-20 implementations utilizing advanced tokenomics features (taxes, liquidity generation, reflection, and buybacks):

| Contract File / Directory | Key Mechanisms & Tokenomics Included |
| :--- | :--- |
| `LP Fee.sol` | Standard Liquidity Pool auto-yield/taxation mechanics. |
| `LP, Marketing Fee.sol` | Dual-split taxation routing funds to LP and a marketing wallet. |
| `LP, Redistribution in BUSD.sol` | Token reflection rewards distributed to holders in a stablecoin ($BUSD). |
| `Redistribution, Gaming Fee.sol` | Custom fee allocation reserved for gaming ecosystems or prize pools. |
| `Burn, Redistribution, LP, Charity Fee.sol` | Multi-split taxation supporting deflationary burns and charity allocation. |
| `Redistribution, LP, Burn, Wallet, Buyback Fee.sol` | Advanced tokenomics featuring auto-buybacks, burns, and holder rewards. |

---

## Security & Best Practices

If you intend to reference or redeploy any portion of these contracts, please ensure you implement modern Web3 security protocols:

1. **Compiler Compatibility**: These legacy contracts likely target Solidity version `^0.8.0` or `^0.6.0` (common in 2021). Update them to a modern stable compiler version (e.g., `>=0.8.20`) and resolve any resulting compiler warnings or deprecated keyword errors.
2. **Reentrancy Protection**: Ensure state-changing functions that route fees (especially those converting native gas tokens or stablecoins) utilize OpenZeppelin's `ReentrancyGuard`.
3. **Safe ERC-20 Transfers**: Always utilize `SafeERC20` or safe transfer patterns when routing reward tokens like $BUSD to avoid silent transfer failures.
4. **Third-Party Audits**: Taxed tokens are highly susceptible to economic exploits, sandwich attacks, and unexpected slippage errors. Ensure any modified code undergoes a thorough independent audit before mainnet deployment.

---

## License

This repository is provided as an open-source archive. Please check individual Solidity files for specific SPDX License Identifiers.
