# Cursor — Starter Boilerplate

> Ready-to-use `.cursor/rules/` folder + `.cursorrules` for your project. Clone, copy, edit.

Part of [agent-anatomy](https://github.com/agent-anatomy) — boilerplates for every AI coding agent.

---

## Usage

```bash
git clone https://github.com/agent-anatomy/cursor.git .cursor-boilerplate

cp .cursor-boilerplate/.cursorrules ./.cursorrules
cp -r .cursor-boilerplate/.cursor ./.cursor

rm -rf .cursor-boilerplate
```

Then edit `.cursorrules` and `.cursor/rules/` to match your project.

---

## What's included

```
.cursorrules                       ← legacy global rules (always applied)
.cursor/
├── rules/
│   ├── code-style.mdc             ← always-on: coding conventions
│   ├── testing.mdc                ← always-on: test rules
│   ├── api-conventions.mdc        ← always-on: API patterns
│   └── react-components.mdc       ← auto: applies to *.tsx files only
└── mcp.json.example               → copy → mcp.json (gitignored if has secrets)
```

---

## What to commit vs gitignore

| File | Commit? |
|------|---------|
| `.cursorrules` | ✅ Yes |
| `.cursor/rules/` | ✅ Yes |
| `.cursor/mcp.json` | ⚠️ Only if no secrets |

Add to your `.gitignore`:
```
.cursor/mcp.json
```

---

## Other agents

| Agent | Boilerplate |
|-------|-------------|
| Claude Code | [agent-anatomy/claude](https://github.com/agent-anatomy/claude) |
| OpenAI Codex | [agent-anatomy/codex](https://github.com/agent-anatomy/codex) |
| Windsurf | [agent-anatomy/windsurf](https://github.com/agent-anatomy/windsurf) |
| More... | [agent-anatomy](https://github.com/agent-anatomy) |
