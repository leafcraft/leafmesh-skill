# LeafMesh Skill for Claude Code

The LeafMesh agent skill — what Claude Code reads to build LeafMesh agencies
correctly: agent types, `can_call` routing, decorators, YAML config, fan-in,
human-in-the-loop, MCP servers as tools, and the gotchas that cost people an
afternoon.

It ships inside every project created with `create-leafmesh`. This repository
is the same skill on its own, for adding to an existing project or reading
without installing anything.

## Install

Drop it into the project you're working in:

```bash
git clone https://github.com/leafcraft/leafmesh-skill.git
mkdir -p .claude/skills
cp -r leafmesh-skill/leafmesh .claude/skills/
```

Claude Code picks it up on the next session. To confirm, ask it something only
the skill knows — *"what are the three parameters of an llm agent function?"*

New projects don't need any of this:

```bash
pip install create-leafmesh
create-leafmesh create my-agency
```

## What's inside

| File | What it's for |
|------|---------------|
| `SKILL.md` | The entry point. Mesh design rules, agent types, config, the action table |
| `nuances-and-gotchas.md` | **Read first.** The mistakes that are quiet rather than loud |
| `agent-config-fields.md` | Every agent field, with types and defaults |
| `reference.md` | Config blocks, providers, listeners, deployment |
| `examples.md` | Working agencies, end to end |
| `agency-development.md` | Building a new agency from nothing |

## Keeping it current

The skill tracks the SDK, so it moves when the SDK does. Pull before starting
anything substantial. It is generated from the `create-leafmesh` templates —
raise issues and fixes there, and they land here on the next release.

## About LeafMesh

LeafMesh is an agent operations SDK: you describe a team of agents in YAML,
and it handles routing, handoffs, session state, human approval, cost control
and observability.

- Docs — https://leafcraft.ai
- `pip install leafmesh`

## Licence

The skill content is documentation for the LeafMesh SDK, published so people
building on LeafMesh can use it. LeafMesh itself is commercial software — see
https://leafcraft.ai for terms, or contact info@leafcraftstudios.com.
