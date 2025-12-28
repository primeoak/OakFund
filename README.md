# OakFund

Desktop app built to set up and fund Solana wallets you control, with secure local key generation.

Full info (download, pricing, docs): https://oakfund.app

<p align="center">
  <img src="https://www.oakfund.app/_next/image?q=75&url=%2Fimage.png&w=3840" alt="OakFund interface preview" width="900" />
</p>

<p align="center">
  <video src="https://www.oakfund.app/demo.mp4" width="900" controls muted playsinline></video>
</p>

## Quick links

- Site / Download / Pricing: https://oakfund.app
- Demo/screens: https://imgur.com/a/VardAc9
- Discord: https://discord.gg/E3nfuS2U3r
- Telegram: https://t.me/oakfund
- Contact: dreamyoaky@gmail.com

<details>
  <summary><strong>What it is</strong></summary>

OakFund is a native desktop app (C++) built for Solana wallet workflows with desktop polish.

- Purpose-built for Solana wallet setup + funding workflows (not a generic script)
- Local key generation
- Live monitoring and stats while running
- Simple licensing (1 device activation)

</details>

<details>
  <summary><strong>What it does</strong></summary>

- **BIP39 generation**
  - Generates random 12-word BIP39 seed phrases using an embedded `english.txt` wordlist
- **Derivation pipeline**
  - PBKDF2-HMAC-SHA512 (2048) → seed
  - Ed25519 key derivation
  - base58 output (Solana-ready)
- **Performance**
  - Multi-threaded engine with configurable thread count
  - Real-time wallets/second + running totals
- **Live monitoring**
  - Color-coded terminal output with timestamps
  - Valid/invalid indicators
  - Auto-scroll toggle
  - Configurable line cap
- **Stats + history**
  - Stat cards for wallets checked, speed, runtime, results found, and totals across sessions
  - Lifetime dashboard aggregates runs (wallets checked, results, runtime, session count)
- **Controls**
  - START/STOP with clean transitions
  - Copy-last-key button on results
- **Alerts**
  - System tray toasts + dialogs on results
  - Optional auto-copy to clipboard
- **Optional**
  - Solana RPC balance checking (for your own addresses / test environments)

</details>

<details>
  <summary><strong>How it works (high level)</strong></summary>

1) Generate a 12-word BIP39 mnemonic  
2) Derive the BIP39 seed with PBKDF2-HMAC-SHA512 (2048 iterations)  
3) Derive an Ed25519 keypair  
4) Encode output as base58 for Solana-friendly usage  
5) (Optional) Check balances through Solana RPC if enabled

</details>

<details>
  <summary><strong>Privacy</strong></summary>

Privacy by design.

- Local-only keys (generated and stored on-device)
- No ads, no trackers, no third-party analytics
- Minimal data: only what’s needed for licensing and support

Read more: https://oakfund.app

</details>

<details>
  <summary><strong>Licensing and plans</strong></summary>

- 1 device activation
- Week / month / lifetime options
- Local validation with expiry tracking
- Obfuscated storage under `HKCU\Software\Tnagie`

Pricing and plan details: https://oakfund.app

</details>

<details>
  <summary><strong>Technical specs</strong></summary>

- BIP39 12-word seed phrase generation
- PBKDF2 + Ed25519 key derivation
- Base58 private key output (64 bytes)
- Optional Solana RPC balance checking
- Custom GDI+ dark theme UI
- Obfuscated registry storage (HKCU)

</details>

<details>
  <summary><strong>Notes</strong></summary>

Seed phrases are sensitive. Treat them like cash:
- keep them offline
- don’t paste them into random tools/sites
- don’t generate keys on machines you don’t trust

Everything else (download/pricing/docs): https://oakfund.app

</details>
