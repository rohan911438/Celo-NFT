# ImpactNFT — Impart NFT

This repository contains the Solidity source for the "Impart NFT" (symbol: `IMPCT`). Two deployments were created and successfully verified via Sourcify. Below are the deployed contract addresses, verification links, transaction details, and a short description of the idea behind the project.

## Deployed Contracts

- Name: Impart NFT (symbol: IMPCT)
  - Contract address: `0x55e074dc4846bf13a4475137211a8c83c60867b4`
  - Transaction hash: `0xc98903148ddf59f3292dac8c60688e5e72c29f71b82b01f19992e2a3d4b966f1`
  - Block number: `8529420`
  - Sourcify: https://repo.sourcify.dev/11142220/0x55e074DC4846bf13a4475137211A8C83C60867b4/

- Name: Impart NFT (symbol: IMPCT)
  - Contract address: `0x49304f6b3bf5053ed5bce8b72d08ac12be65348e`
  - Transaction hash: `0x3e2dba35888c29dc31423c5c60ca31339f1129f07233b69c36b71ae8dc51f00a`
  - Block number: `8529454`
  - Sourcify: https://repo.sourcify.dev/11142220/0x49304F6b3BF5053eD5BcE8B72D08aC12be65348E/

## Idea / Purpose

Impart NFT is an NFT contract intended to represent verifiable impact (social, environmental, or charitable). Typical usage patterns:

- Mint NFTs tied to verified impact events (reports, receipts, off-chain attestations).
- Use token metadata to store or reference proof documents, IPFS hashes, and third-party attestations.
- Transfer or retire tokens to represent ownership or completed impact cycles.

The contract name and symbol used at deployment were:

- Name: "Impart NFT"
- Symbol: `IMPCT`

## Repository layout

- `contract/ImpactNFT.sol` — Solidity source used to compile/deploy the contracts above.

## Verification

Both deployments were verified with Sourcify (links above). That means the published sources match the bytecode produced at deployment for the corresponding network/chain ID used.

## Quick interaction example (ethers.js)

Below is a minimal example to call the contract from Node.js / a frontend (replace PROVIDER_URL and the contract address as needed).

```js
// Minimal example (node or browser with ethers available)
const { ethers } = require('ethers');
const provider = new ethers.providers.JsonRpcProvider(PROVIDER_URL);
const signer = provider.getSigner(); // or use a wallet
const contractAddress = '0x55e074dc4846bf13a4475137211a8c83c60867b4';
const abi = [ /* paste generated ABI from compilation/artifacts here */ ];
const contract = new ethers.Contract(contractAddress, abi, signer);
// Example: call a read-only function
// await contract.name();
// await contract.symbol();
```

## Next steps / Notes

- Add the compiled ABI (e.g., export artifacts) to `artifacts/` or include in the frontend.
- Add a small frontend or script to mint and view metadata.
- Consider adding README sections for minting policy, ownership, and upgradeability if applicable.

If you want, I can:

- add the ABI file(s) to the repo,
- create a tiny frontend demo to mint/view NFTs,
- or add a `DEPLOYMENTS.md` with more metadata and network tags.

---
Generated automatically from the Remix deployment output; contract source: `contract/ImpactNFT.sol`.
