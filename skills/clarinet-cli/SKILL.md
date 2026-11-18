---
name: clarinet-cli
description: Use the clarinet CLI to create and manage Clarity smart contract projects on Stacks.
---

# Clarinet CLI

You have access to the `clarinet` CLI — the primary tool for building, testing, and deploying Clarity smart contracts on the Stacks blockchain.

## Core commands

### Project management
- `clarinet new <project-name>` — Create a new Clarinet project with the standard directory structure
- `clarinet contracts new <contract-name>` — Create a new contract within an existing project (generates the `.clar` file and test file)
- `clarinet requirements add <contract-address>` — Add a contract dependency (e.g. a trait or deployed contract your project depends on)

### Testing
- Unit tests are written in TypeScript — use the package manager matching the project's lockfile (`package-lock.json`, `pnpm-lock.yaml`, `yarn.lock`, `bun.lockb`), defaulting to `npm` if none is present

### Discovering more commands
- Run `clarinet --help` to see all available commands
- Run `clarinet <command> --help` to see detailed usage for any specific command

## Usage guidelines

- Always run clarinet commands from the **project root** (the directory containing `Clarinet.toml`)
- **Never manually edit `Clarinet.toml` to add contracts or requirements** — always use `clarinet contracts new` and `clarinet requirements add` instead, which handle all necessary scaffolding
- Boot contracts (`SP000000000000000000002Q6VF78.*`, e.g. the `pox-*` contracts) and the sBTC contracts `sbtc-registry`, `sbtc-token` and `sbtc-deposit` are built into Clarinet — never add them as requirements; add every other contract dependency with `clarinet requirements add <CONTRACT_ID>`
- When creating a new project with `clarinet new`, cd into the new directory before running further commands
