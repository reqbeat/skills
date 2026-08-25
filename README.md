# Reqbeat Hiring Signals — agent skill

Find companies hiring for a role and geo, qualify them, and watch them for changes.

## Community, built on the public API

Community, not an official Reqbeat product. It is built on the same public API any reader
can call, and it carries no support commitment — no ticket queue stands behind it, and no
response time is promised.

That is a choice rather than a disclaimer. Reqbeat is self-serve the whole way down;
nobody is in the loop on an account. A pack that implied a support desk would be
advertising something that does not exist.

## Install

```bash
npx skills add reqbeat/skills
```

Installs `com-reqbeat-hiring-signals/SKILL.md`, which teaches an agent when to reach for
Reqbeat, how to try it with no key, and how to connect `com.reqbeat/hiring-signals`
(v1.0.0, streamable-http) once it needs the full index.

## No key? Try it right now

```bash
curl -s 'https://jobs.signalsapi.com/v1/sandbox/reqs/search?role=backend+engineer&geo=United+States'
```

Real rows, capped at 25 companies, billed to nobody.

## Generated, not hand-written

Every file here is rendered from the live `server.json` that
`https://mcp.reqbeat.com/mcp` serves, on each generation cycle. Edit
`static-site/skills_publisher.py` in reqbeat.git, never these files — a hand-edit is
overwritten on the next cycle, silently.

Tool descriptions are served live and are deliberately absent from `SKILL.md`; an agent
reads them with `tools/list`.
