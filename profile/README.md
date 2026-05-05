<div align="center">

# Meow Labs

**Open-source developer tools. Built for engineers who ship fast.**

</div>

---

## MeowPass

**CLI-first, E2E encrypted secret manager for developers. Zero-knowledge. AI-native.**

One command to encrypt your .env, share with your team, and inject into any process. Works with Claude Code, Cursor, and your CI/CD.

```bash
brew install meowrithm/tap/meowpass
meowpass init       # scan .env → create vault → encrypt → push
meowpass run -- npm start   # inject secrets into process (in-memory)
```

### Encryption

```
Master Password → Argon2id (time=3, mem=64MB) → Master Key
                → AES-256-GCM → Encrypted Vault
Team Sharing    → X25519 key exchange (per-member encrypted vault key)
```

---

## Open Source Projects

| Repo | Description | Install |
|------|-------------|---------|
| [`meowpass-cli`](https://github.com/meowrithm/meowpass-cli) | Go CLI — 22 commands, offline cache | `brew install meowrithm/tap/meowpass` |
| [`meowpass-app`](https://github.com/meowrithm/meowpass-app) | Web dashboard — vault manager | [app.meowpass.dev](https://app.meowpass.dev) |
| [`meowpass-extension`](https://github.com/meowrithm/meowpass-extension) | Chrome extension (MV3) | [Download](https://github.com/meowrithm/meowpass-extension/releases/latest) |
| [`meowpass-action`](https://github.com/meowrithm/meowpass-action) | GitHub Action for CI/CD | `uses: meowrithm/meowpass-action@v1` |
| [`meowpass-skill`](https://github.com/meowrithm/meowpass-skill) | Claude Code skill | `npx skills@latest add meowrithm/meowpass-skill` |

### npm Packages

| Package | Description | Install |
|---------|-------------|---------|
| [`@meowlabs/meowpass-mcp`](https://www.npmjs.com/package/@meowlabs/meowpass-mcp) | MCP server (14 tools) for Claude, Cursor, Windsurf | `npx @meowlabs/meowpass-mcp` |
| [`@meowlabs/meowpass`](https://www.npmjs.com/package/@meowlabs/meowpass) | Node.js SDK with full E2E encryption | `npm install @meowlabs/meowpass` |

---

## CLI Commands (v0.2.0)

| Command | What it does |
|---------|-------------|
| `meowpass init` | Scan .env, create vault, encrypt & push |
| `meowpass run -- cmd` | Inject secrets into process (in-memory) |
| `meowpass diff` | Compare local .env vs vault |
| `meowpass history KEY` | Per-secret version timeline |
| `meowpass rollback KEY` | Restore previous version |
| `meowpass rotate` | Full vault key rotation |
| `meowpass doctor` | Diagnose health |
| `meowpass set/get/list/delete` | CRUD secrets |
| `meowpass pull/push` | Sync .env files |
| `meowpass share` | Share vault with team (X25519) |
| `meowpass git-hook install` | Pre-commit drift detection |

---

## Pricing

| | Developer | Pro | Team |
|---|---|---|---|
| **Price** | Free | $3/mo | $6/user/mo |
| **Status** | **All features unlocked during early access** | Coming soon | Coming soon |

---

## Links

- **Website**: [meowpass.dev](https://meowpass.dev)
- **Web App**: [app.meowpass.dev](https://app.meowpass.dev)
- **Docs**: [meowpass.dev/docs](https://meowpass.dev/docs)
- **Security**: [meowpass.dev/security](https://meowpass.dev/security)
- **Discord**: [Join our community](https://discord.gg/GTZcZKRQu7)
- **Contact**: hello@meowpass.dev

---

<div align="center">

**Built with** Go · Next.js · TypeScript · AWS Lambda · Neon Postgres · Argon2id · AES-256-GCM · X25519

**Open source** · MIT License

</div>
