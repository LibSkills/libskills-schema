# libskills-schema

**JSON Schema definitions for LibSkills skill files.**

## Schemas

- [`skill.json`](./schemas/skill.json) — Skill metadata and knowledge files
- [`index.json`](./schemas/index.json) — Registry index

## Skill Format Overview

Every skill is a directory:

```
{language}/{author}/{name}/
├── skill.json                    ← Metadata only (this schema)
├── tier1/                        ← Official knowledge
│   ├── overview.md
│   ├── api.md
│   ├── pitfalls.md               ← Required
│   ├── threading.md
│   ├── lifecycle.md
│   ├── memory.md
│   ├── safety.md                  ← Required
│   ├── performance.md
│   └── examples/
└── tier2/                        ← Community knowledge
```

## Versioning

The current schema version is `libskills/v1`.

## License

Apache 2.0
