<div align="center">

# Meow Labs

**Open-source developer tools. Built for engineers who ship fast.**

We build tools that make developers' lives easier — starting with secret management.

</div>

---

## MeowPass

**CLI-first, E2E encrypted secret management for developers.**

Stop losing API keys in Slack DMs. MeowPass is an encrypted vault for your secrets — API keys, database credentials, .env files — with a CLI, Chrome extension, and AI agent integrations.

### How it works

```
Master Password → Argon2id → Master Key → AES-256-GCM → Encrypted Vault
```

Your secrets are encrypted on your device before they touch the server. Zero-knowledge architecture — we can't read your data.

### Get started

```bash
brew install chpecson/tap/meowpass
meowpass login
meowpass vault create my-project
meowpass set STRIPE_KEY sk_live_... --vault <id>
```

### Ecosystem

| Tool | Install | Description |
|------|---------|-------------|
| **CLI** | `brew install chpecson/tap/meowpass` | Terminal-first secret management |
| **Chrome Extension** | [Download](https://github.com/meowrithm/meowpass-extension/releases/latest) | Manage secrets from your browser |
| **MCP Server** | `npx @meowlabs/meowpass-mcp` | AI agent integration (Claude Code, Cursor, Windsurf) |
| **Claude Code Skill** | `npx skills@latest add meowrithm/meowpass-skill` | Natural language secret management |

### Plans

| | Developer | Pro | Team |
|---|---|---|---|
| **Price** | Free | $5/mo | $9/user/mo |
| **Vaults** | 1 | Unlimited | Unlimited |
| **Secrets** | 50 | Unlimited | Unlimited |
| **Features** | CLI, Extension | + .env sync, API access | + Shared vaults, RBAC, Audit logs |

### Links

- **Website**: [meowpass.dev](https://meowpass.dev)
- **Integrations**: [meowpass.dev/integrations](https://meowpass.dev/integrations)
- **npm**: [@meowlabs/meowpass-mcp](https://www.npmjs.com/package/@meowlabs/meowpass-mcp)
- **Contact**: hello@meowpass.dev

---

<div align="center">

**Built with** Go, Next.js, AWS Lambda, Neon Postgres, WebCrypto

</div>
