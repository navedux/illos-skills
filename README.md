# Illos skills

Animated SVG illustrations for your website or app, added by your coding agent. This repo has a free skill and the Illos MCP server, packaged for Claude Code, Cursor, Codex and any agent that reads `SKILL.md` folders.

[Illos.dev](https://illos.dev) has 158 animated illustrations in four themes (Shader, HUD, Isometric and Interface), each in light and dark. 65 are free for commercial use, with no account and no credit.

## What it does

Ask your agent for a picture where a page needs one:

> Add an illustration to the empty notifications screen.
> Use Illos Isometric illustrations for the feature sections on the home page.

The `illos-library` skill picks one theme for the whole site, finds the illustration that explains each section, and adds it: with one `npx shadcn` command in a React project, or as an SVG file anywhere else.

## Install

**Claude Code** (the skill and the MCP server):

```
/plugin marketplace add navedux/illos-skills
/plugin install illos@illos-dev
```

**Any agent, with the skills CLI** ([skills.sh](https://skills.sh)):

```bash
npx skills add navedux/illos-skills
```

**Cursor:** open Customize, From GitHub Repository, and paste this repo's URL. Or copy `skills/illos-library` into `.cursor/skills/`.

**Codex:** copy `skills/illos-library` into `.agents/skills/` in your project, or `~/.agents/skills/` for every project.

### The MCP server on its own

`https://illos.dev/mcp` (Streamable HTTP, no sign-in) gives any MCP client three tools: `find_illustrations`, `get_illustration` and `list_themes`.

```bash
claude mcp add --transport http illos https://illos.dev/mcp
```

Cursor (`~/.cursor/mcp.json`):

```json
{ "mcpServers": { "illos": { "url": "https://illos.dev/mcp" } } }
```

## New illustrations in the same style

When the library doesn't have what a page needs, the Illos Pro skills teach your agent a theme's rules, so it can draw new illustrations that match and check each one. They come with [Illos Pro](https://illos.dev/pro).

## Licence

The skill and the files in this repo: MIT. The illustrations: [illos.dev/license](https://illos.dev/license). Free ones need no credit.
