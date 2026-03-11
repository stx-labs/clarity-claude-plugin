Give Claude the ability to use the Clarity LSP.

# Installation

Add the Stacks Labs marketplace, then install the plugin:

```sh
/plugin marketplace add stx-labs/claude-marketplace
/plugin install clarity-plugin@stx-labs
```

Then start Claude from a Clarinet project and the plugin will provide LSP diagnostics automatically.

# Dev Usage (no installation)

Clone this repository, then start Claude from a Clarinet project:

```sh
git clone https://github.com/stx-labs/clarity-claude-plugin.git
git clone https://github.com/stx-labs/clarity-starter # if you need a basic Clarity project
cd clarity-starter

# the important part:
claude --plugin-dir ../clarity-claude-plugin
# from there, Claude will get the diagnostics as it interacts with the LSP
```

## See it in action

![Clarity LSP in Claude Code](./screenshot-clarity-lsp.png "Clarity LSP in Claude Code")

## Disclaimer

This plugin and its associated skills are provided as developer tools only. Any smart contract code generated, modified, or suggested through the use of this plugin **must be thoroughly reviewed, tested, and independently audited** before deployment to any adversarial environment such as a blockchain. Blockchain transactions are irreversible, and vulnerabilities in smart contracts can lead to permanent loss of funds.

Stacks Labs makes no representations or warranties regarding the correctness, security, or fitness for purpose of any code produced using this plugin. **Stacks Labs assumes no responsibility or liability** for any losses, damages, or other consequences arising from the use or deployment of code generated with the assistance of this plugin. Use at your own risk.
