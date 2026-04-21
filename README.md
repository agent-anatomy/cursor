# Cursor — Starter Boilerplate

> Ready-to-use `.cursor/rules/` + `.cursorrules` for your project. Clone, copy, edit.

Part of [agent-anatomy](https://github.com/agent-anatomy) — boilerplates for every AI coding agent.

📊 **[View diagram →](https://agent-anatomy.github.io/graphics/cursor.html)**

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
.cursorrules                       ← global rules, always applied (legacy)
.cursor/
├── rules/
│   ├── code-style.mdc             ← always-on: coding conventions
│   ├── testing.mdc                ← always-on: test rules
│   ├── api-conventions.mdc        ← always-on: API patterns
│   └── react-components.mdc       ← auto: applies to *.tsx files only
└── mcp.json.example               → copy → mcp.json (gitignored if has secrets)
```

---

## What is .cursorrules?

`.cursorrules` is a plain text file at your project root that Cursor reads before every request. It gives Cursor context about your project — stack, conventions, rules.

It's the quickest way to get Cursor following your project's standards without repeating yourself.

---

## What is .cursor/rules/?

The modern replacement for a single `.cursorrules` file. Instead of one large file, you split rules into `.mdc` files with frontmatter that controls when each rule applies.

**Rule types:**

| Type | When it applies |
|------|----------------|
| `alwaysApply: true` | Every single request |
| `globs: ["**/*.tsx"]` | Only when matching files are in context |
| Agent-requested | Cursor decides based on the description |
| Manual (`@rule-name`) | Only when you reference it explicitly |

---

## .cursorrules vs .cursor/rules/ — which to use?

Use both. `.cursorrules` for quick global rules, `.cursor/rules/` for modular rules scoped to file types. Cursor reads both.

If migrating from a big `.cursorrules` file — split it into topic `.mdc` files in `.cursor/rules/`.

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

## FAQ

**Do Cursor rules apply to Cursor Tab (autocomplete)?**
No. Rules apply to Cursor Chat and Composer, not Tab autocomplete.

**How many rules files can I have?**
No hard limit. Keep always-on rules short — they consume context on every request.

**What is .mdc format?**
Markdown with YAML frontmatter. Cursor uses the frontmatter to decide when to load the rule.

**Can I use @rule-name in chat?**
Yes. Reference any rule file by name to pull it into context for that request only.

---

## Other agents

| Agent | Boilerplate |
|-------|-------------|
| Claude Code | [agent-anatomy/claude](https://github.com/agent-anatomy/claude) |
| OpenAI Codex | [agent-anatomy/codex](https://github.com/agent-anatomy/codex) |
| Windsurf | [agent-anatomy/windsurf](https://github.com/agent-anatomy/windsurf) |
| GitHub Copilot | [agent-anatomy/copilot](https://github.com/agent-anatomy/copilot) |
| Aider | [agent-anatomy/aider](https://github.com/agent-anatomy/aider) |
| Gemini CLI | [agent-anatomy/gemini](https://github.com/agent-anatomy/gemini) |
