# TuleBank Skill for Claude Code

Send Argentine pesos (ARS) to any bank account via CVU or ALIAS, swap USDC/wARS on Base, and manage beneficiaries — all from Claude Code.

## Install

```bash
npx skills add p2p-lanes/tulebank-skill
```

## Prerequisite

The TuleBank CLI must be installed globally:

```bash
npm i -g tulebank
```

Then run `tulebank signup --email <email> --phone <phone>` to create your account.

## What it does

- **Send ARS** — off-ramp crypto to any Argentine bank account via Ripio Ramps
- **Swap tokens** — convert between USDC and wARS on Base
- **Manage beneficiaries** — local address book with fuzzy search
- **Wallet management** — create and manage a CDP smart wallet on Base
- **Transaction history** — track sends and swaps with date/beneficiary filters

## Usage

Once installed, Claude Code can run TuleBank commands when you ask things like:

- "mandale 10k a Pili"
- "swap 5 USDC to wARS"
- "show my balance"
- "add franv98 as a beneficiary"

See the [CLI README](https://www.npmjs.com/package/tulebank) for full documentation.
