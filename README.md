# Matrix Documentation

**Matrix** is the cognition and UX layer on [Paxeer Network](https://paxeer.app). It turns natural-language requests into typed, inspectable, replayable agent execution across two rails:

- **Neo** — the default conversational tool-calling agent for reversible work
- **MCL** — the rigorous rail for monetary or irreversible work (NL → Intent IR → Plan → Walk)

This repository contains the official documentation for Matrix, hosted at [docs.matrixmcl.com](https://docs.matrixmcl.com).

## What's Inside

### Core Modules

Matrix is a polyglot monorepo of independently buildable Go modules plus MCP tool servers:

| Module | Role |
|--------|------|
| **mcl** | Compiler turning natural language into typed Intent IR |
| **cortex** | Per-actor typed memory graph on Pebble DB |
| **executor** | Plan walker, lifecycle machine, MCP tool dispatch |
| **neo** | Default conversational agent with paged cortex memory |
| **gateway** | Metered LLM proxy + PAX credit ledger |
| **router** | Per-user Fly Machine provisioning + reverse proxy |
| **deus** | Agent-service marketplace with EIP-712 receipts |
| **layerx** | Settlement fabric and custody spine |
| **chronos** | Agent scheduler and wake system |
| **tachyon** | Agent-native Solidity/EVM engine |
| **uwac** | Universal Web Agent Connector (OAuth vault → MCP tools) |

### Documentation Structure

- **Get Started** — Introduction, quickstart, core concepts, glossary
- **User Guide** — Chat interface, skills, wallet management
- **Developer** — Architecture, module deep-dives, build/test/lint, contributing
- **API Reference** — HTTP/SSE endpoints for all services
- **MCP** — Model Context Protocol tool servers and agent manifests
- **Reference** — Deep subsystem documentation (cortex, mcl, neo, chronos, tachyon, deus, layerx, skills, standards)
- **FAQ** — Common questions for users, developers, ops, billing, security

## Building the Docs

This documentation is built with [Jamdesk](https://jamdesk.com), a modern documentation platform.

```bash
# Install Jamdesk CLI
npm install -g jamdesk

# Build the site
jamdesk build

# Preview locally
jamdesk dev

# Deploy to production
jamdesk deploy
```

## For AI Agents

This repository includes agent-friendly artifacts:

- **`llms.txt`** — Structured index with descriptions for LLM consumption
- **`sitemap.txt`** — Flat list of all documentation paths
- **`agent.txt`** — Agent manifest describing structure, navigation, and known issues

When consuming these docs programmatically:
1. Start with `/introduction`, `/concepts`, `/glossary` for the mental model
2. Strip MDX components (`<Columns>`, `<Card>`, `<Tip>`, etc.) to extract plain text
3. All code examples are in standard markdown code blocks
4. Cross-references use absolute paths from root (`/path/to/page`)

## Contributing

See [developer/contributing.mdx](developer/contributing.mdx) for ground rules, commit format, and PR workflow.

## License

See [LICENSE](LICENSE) for details.

## Links

- **Documentation**: [docs.matrixmcl.com](https://docs.matrixmcl.com)
- **Source Code**: [github.com/paxlabs-inc/matrix-core](https://github.com/paxlabs-inc/matrix-core)
- **Paxeer Network**: [paxeer.app](https://paxeer.app)
