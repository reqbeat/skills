# Reqbeat Hiring Signals — agent skill

Find companies hiring for a role and geo, qualify them, and watch them for changes.

## What this is

The Reqbeat agent skill, rendered from the live `server.json` the hosted server publishes.
Issues → [support@reqbeat.com](mailto:support@reqbeat.com).

The docs repo — install guides, per-client configs, the tool table — is
[reqbeat/mcp-server](https://github.com/reqbeat/mcp-server).

## Install

```bash
npx skills add reqbeat/skills
```

Installs `com-reqbeat-hiring-signals/SKILL.md`, which teaches an agent when to reach for
Reqbeat, how to try it with no key, and how to connect `com.reqbeat/hiring-signals`
(v1.0.1, streamable-http) once it needs the full index.

## No key? Try it right now

```bash
curl -s 'https://api.reqbeat.com/v1/sandbox/reqs/search?role=backend+engineer&geo=United+States'
```

Real rows, capped at 25 companies, billed to nobody.

## Generated, not hand-written

Every file here is rendered from the live `server.json` that
`https://mcp.reqbeat.com/mcp` serves, on each generation cycle. Edit
`static-site/skills_publisher.py` in reqbeat.git, never these files — a hand-edit is
overwritten on the next cycle, silently.

Tool descriptions are served live and are deliberately absent from `SKILL.md`; an agent
reads them with `tools/list`.
