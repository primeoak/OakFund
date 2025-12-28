# OakFund

OakFund is a native desktop app (C++) built for Solana wallet setup and funding workflows — with secure local key generation, live monitoring, and a clean desktop UI.

Download / pricing / full site: https://oakfund.app  
Demo/screens: https://imgur.com/a/VardAc9  
Discord: https://discord.gg/2amP69bfgV  
Telegram: https://t.me/oakfund  
Contact: dreamyoaky@gmail.com

## What OakFund is

Purpose-built desktop tooling for people who want a reliable, daily-use workflow around Solana wallets:
- generate wallets locally
- monitor progress live
- manage results cleanly
- optionally check balances via RPC (for wallets/addresses you control or for testing)

Not a generic “random script.” Not a browser toy.

## Core features

### BIP39 generation + Solana derivation
- Random 12-word BIP39 mnemonics using an embedded 2048-word english wordlist
- PBKDF2-HMAC-SHA512 derivation (2048 iterations) → seed
- Ed25519 key derivation
- base58 output (Solana-ready)

### Performance
- Multi-threaded engine
- Configurable thread count
- Real-time wallets/second + running totals

### Live monitoring
- Color-coded terminal output
- Timestamps
- Valid/invalid indicators
- Auto-scroll toggle
- Configurable line cap

### Stats + history
- Stat cards tracking:
  - wallets checked
  - generation speed
  - runtime
  - hits/results found
  - total balance across sessions (when balance checking is enabled)
- Lifetime/session history dashboard:
  - total wallets checked
  - results found
  - runtime
  - session count
  - aggregated totals

### UX / controls
- START / STOP controls with clean state transitions
- Copy-last-key button appears on results
- Clean dark UI (custom GDI+ theme)

### Alerts
- System tray notifications / on-screen dialogs on results
- Optional auto-copy to clipboard

### Settings
- Threads
- Max lines
- Notifications
- Save-results preferences
- Auto-update flag (if enabled in your build)
- Settings stored locally

### Licensing
- 1 device activation
- Week / month / lifetime licenses
- Local validation with expiry tracking
- Obfuscated local storage under `HKCU\Software\Tnagie`

## How it works (high-level)

1) Generate a 12-word BIP39 mnemonic (local)
2) Derive seed via PBKDF2-HMAC-SHA512 (2048)
3) Derive Ed25519 keypair
4) Encode output for Solana (base58)
5) Optionally check balances via Solana RPC (for your own wallets/addresses or test environments)

## Privacy promise

Privacy by design:
- Local-only key generation
- No ads, no trackers, no third-party analytics
- Minimal data: only what’s needed for licensing/support

Read more on the site: https://oakfund.app

## Plans

Pricing and plan details live here: https://oakfund.app

- 1 Week — $200
- 1 Month — $500
- Lifetime — $2000

## Technical specs (quick)

- BIP39 12-word seed phrase generation
- PBKDF2 + Ed25519 key derivation
- base58 private key output (64 bytes)
- Optional Solana RPC balance checking
- Custom GDI+ dark theme UI
- Obfuscated registry storage (HKCU)

## Notes

Seed phrases are sensitive. Treat them like cash:
- keep them offline
- don’t paste them into random tools/sites
- don’t generate keys on machines you don’t trust

For full docs, downloads, and updates: https://oakfund.app
