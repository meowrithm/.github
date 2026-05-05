<div align="center">

# Meow Labs

**Open-source developer tools. Built for engineers who ship fast.**

We build tools that make developers' lives easier — starting with secret management.

</div>

---

## MeowPass

**The first AI-native, E2E encrypted secret manager for developers.**

Stop losing API keys in Slack DMs. MeowPass is an encrypted vault for your secrets — API keys, database credentials, .env files — with a CLI, web app, Chrome extension, and built-in AI agent integration.

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

---

## Open Source Projects

| Repo | Description | Install |
|------|-------------|---------|
| [`meowpass-cli`](https://github.com/meowrithm/meowpass-cli) | CLI for secret management (Go, Cobra) | `brew install chpecson/tap/meowpass` |
| [`meowpass-app`](https://github.com/meowrithm/meowpass-app) | Web app — vault manager in the browser | [app.meowpass.dev](https://app.meowpass.dev) |
| [`meowpass-extension`](https://github.com/meowrithm/meowpass-extension) | Chrome extension | [Download](https://github.com/meowrithm/meowpass-extension/releases/latest) |
| [`meowpass-skill`](https://github.com/meowrithm/meowpass-skill) | Claude Code skill | `npx skills@latest add meowrithm/meowpass-skill` |

### Also on npm

| Package | Description | Install |
|---------|-------------|---------|
| [`@meowlabs/meowpass-mcp`](https://www.npmjs.com/package/@meowlabs/meowpass-mcp) | MCP server for AI agents (Claude Code, Cursor, Windsurf) | `npx @meowlabs/meowpass-mcp` |

---

## Pricing

| | Developer | Pro | Team |
|---|---|---|---|
| **Price** | Free | $3/mo | $6/user/mo |
| **Vaults** | 1 | Unlimited | Unlimited |
| **Secrets** | 50 | Unlimited | Unlimited |
| **Features** | CLI, Extension, Web App | + .env sync, MCP, API keys | + Shared vaults, RBAC, Audit logs |

---

## Links

- **Website**: [meowpass.dev](https://meowpass.dev)
- **Web App**: [app.meowpass.dev](https://app.meowpass.dev)
- **Integrations**: [meowpass.dev/integrations](https://meowpass.dev/integrations)
- **npm**: [@meowlabs/meowpass-mcp](https://www.npmjs.com/package/@meowlabs/meowpass-mcp)
- **Discord**: [Join our community](https://discord.gg/GTZcZKRQu7)
- **Contact**: hello@meowpass.dev

---

<div align="center">

**Built with** Go · Next.js · TypeScript · AWS Lambda · Neon Postgres · WebCrypto · Argon2id

**Open source** · MIT License

</div>
