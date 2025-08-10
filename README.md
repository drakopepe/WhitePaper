# Drakopepe ($DPEP) — Whitepaper & Technical Overview

**Date:** 2025-08-10  
**Website:** https://drakopepe.org/  
**Symbol:** DPEP · **Unit:** Drako

---

## Abstract
Drakopepe ($DPEP) is a community‑first, Proof‑of‑Work (PoW) meme cryptocurrency built for fairness, transparency, and culture. Network rules are simple and public; emission follows a fixed halving schedule; there are no protocol‑level dev taxes. This document provides the core parameters, tokenomics, mining guidance, and roadmap.

---

## Table of Contents
1. [Quick Facts](#quick-facts)  
2. [Protocol Overview](#protocol-overview)  
3. [Network Parameters](#network-parameters)  
4. [Tokenomics](#tokenomics)  
5. [Mining](#mining)  
6. [Wallets & Releases](#wallets--releases)  
7. [Explorer](#explorer)  
8. [Governance & Community](#governance--community)  
9. [Roadmap](#roadmap)  
10. [Security](#security)  
11. [Brand Kit](#brand-kit)  
12. [Team](#team)  
13. [License](#license)  
14. [How to Publish on GitHub](#how-to-publish-on-github)

---

## Quick Facts
| Item | Value |
|---|---|
| **Algorithm** | Scrypt (Proof of Work) |
| **Block Reward (initial)** | 50 DPEP |
| **Halving** | Every 210,000 blocks |
| **Max Supply** | 21,000,000 DPEP |
| **Target Spacing** | 5 minutes (300 s) |
| **Difficulty Timespan** | 10 minutes |
| **Coinbase Maturity** | 20 blocks (spendable after 21 confirmations) |
| **TX Confirmations (recommended)** | 6 blocks |
| **P2P Port** | 24442 |
| **RPC Port** | 24441 |
| **Address Prefix** | Mainnet P2PKH starts with **"1"**; Testnet P2PKH starts with **"M"** |
| **Coin Name** | DrakoPepe |
| **Abbreviation** | DPEP |
| **Smallest Unit** | Drako |

> Source: project specifications shared by the core team.

---

## Protocol Overview
- **Consensus:** Proof‑of‑Work (Scrypt).  
- **Transactions:** Bitcoin‑like UTXO model (version, inputs, outputs, locktime).  
- **Fees:** Market‑based miner fees; no protocol‑level dev tax.  
- **Finality:** Probabilistic; **6 confirmations** recommended for high‑value transactions.  

**Notes:** Genesis date/hash, address types beyond P2PKH (e.g., Bech32), and exact difficulty formula constants should be published alongside the reference client when finalized.

---

## Network Parameters
| Parameter | Value |
|---|---|
| Algorithm | Scrypt (PoW) |
| Block time target | 300 s (5 min) |
| Difficulty adjustment window | 10 minutes |
| Initial block reward | 50 DPEP |
| Halving interval | 210,000 blocks |
| Max supply | 21,000,000 DPEP |
| Coinbase maturity | 20 blocks (spendable after 21 confirmations) |
| Transaction confirmations | 6 blocks |
| RPC default port | 24441 |
| P2P default port | 24442 |
| Address prefixes | Mainnet "1"; Testnet "M" |

---

## Tokenomics
Drakopepe follows a classic PoW emission with periodic halvings until the 21,000,000 cap.

```text
Initial reward: 50 DPEP
Halving schedule: every 210,000 blocks (~2 years at 5 min blocks)
Max supply: 21,000,000 DPEP
Coinbase maturity: 20 blocks (spendable after 21 confirmations)
```

- **No Premine / No Dev Tax:** Newly minted coins are earned solely by miners who contribute hashpower.  
- **Fees:** Paid by users to miners; adjustable by mempool conditions.

---

## Mining
Both **solo** and **pool** mining are supported.

### Hardware
- **Beginner:** GPU miners supporting Scrypt.  
- **Advanced:** Scrypt ASICs for higher hashrate and efficiency.

### Example Pool Config (generic)
```ini
url=stratum+tcp://<pool-host>:<port>
user=<YOUR_WALLET_ADDRESS>.<WORKER>
pass=x
algo=scrypt
```

### Example Solo Mining
> The CLI names below are placeholders; replace with your client binary names.

```bash
# 1) Start the daemon
./dpepcoind -daemon

# 2) Generate a block to a specific address (testing)
./dpep-cli generatetoaddress <YOUR_ADDRESS> --max-blocks 1

# 3) Check balance and mining info
./dpep-cli getbalance
./dpep-cli getmininginfo
```

**Best Practices:** Verify binaries via SHA256; keep nodes and miners up to date; back up `wallet.dat` and seed phrases securely.

---

## Wallets & Releases
- **Desktop Wallets:** Windows & Linux.  
- **Checksums:** Provide SHA256 for each downloadable binary.  
- **Reproducible Builds:** Recommended; publish build scripts where possible.

### Example Checksums (fill in on release)
| File | SHA256 |
|---|---|
| `dpep-qt-windows.zip` | `TBD` |
| `dpep-qt-linux.tar.gz` | `TBD` |

> Add direct URLs when publishing releases.

---

## Explorer
Add the official explorer URL when finalized, e.g.:  
https://explorer.drakopepe.org/

---

## Governance & Community
- **Development:** Open issues/PRs on GitHub.  
- **Community Input:** Proposals via GitHub Discussions and social channels (Telegram/X).  
- **Treasury:** If established, must be a transparent multisig with on‑chain reporting; there is **no protocol‑level tax**.

---

## Roadmap
- **Q3–Q4 2025:** Public wallets (Win/Linux), explorer launch, mining docs, first community campaigns.  
- **Q1–Q2 2026:** Listings (DEX/CEX where appropriate), meme‑game prototypes, curated NFT drops.  
- **H2 2026:** Dev grants and ecosystem bounties; improved tooling and docs.  
- **2027+:** Scaling community utilities and governance experiments.

---

## Security
- **51% Risks:** Mitigated by diversified hashrate; support multiple pools and honest‑miner majority.  
- **Operational Hygiene:** Verify downloads, validate checksums, keep cold backups.  
- **Responsible Disclosure:** Report vulnerabilities privately to the core team first.

---

## Brand Kit
Use these cues for consistent visuals (site/hero art, media kits):
- **Body:** `#4CC055` (bright green)  
- **Belly:** `#A8E6A1` (mint)  
- **Horns:** beige  
- **Outline/Glow:** teal  
- **Accent:** small red bow tie  
- **Background (hero):** dark‑to‑purple radial gradient (black → deep violet/blue)

---

## Team
- **Lena “MemeQueen” — Creative Director**  
  Visual identity (logos, memes, NFTs); drives viral look & feel.
- **Alex “HashMaster” — Lead Developer**  
  PoW architect; core client, networking, emission schedule.
- **Max “ShillDragon” — Community & Marketing Lead**  
  Socials, campaigns, partnerships, and community growth.

---

## License
Unless otherwise noted, documentation is provided under the **MIT License**.  
You may also add a `LICENSE` file in the repository root.
