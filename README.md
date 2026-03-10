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
