# libskills-schema

**JSON Schema definitions for LibSkills skill files.**

Part of the [LibSkills](https://github.com/LibSkills) ecosystem — the Behavioral Knowledge Layer for open-source libraries.

## Schemas

| Schema | File | Description |
|--------|------|-------------|
| Skill metadata | [`skill.json`](./schemas/skill.json) | Defines the structure of a skill directory |
| Registry index | [`index.json`](./schemas/index.json) | Defines the registry index format |

## Skill Format Overview

Every skill is a directory:

```
{language}/{author}/{name}/
├── skill.json                    ← Metadata (this schema)
├── tier1/                        ← Official knowledge
│   ├── overview.md
│   ├── pitfalls.md               ← Required (high-cost knowledge)
│   ├── lifecycle.md
│   ├── threading.md
│   ├── safety.md                  ← Required (risk awareness)
│   ├── performance.md
│   └── examples/
└── tier2/                        ← Community knowledge
```

## Versioning

The current schema version is `libskills/v1`.

## How JSON Schema works

The `skill.json` schema enforces:
- Required fields: name, repo, language, tier, group, version, skill_version, schema, trust_score, tags
- Trust score (0-100)
- Completeness score (0-100)
- Compatibility metadata
- Dependency declarations

## License

Apache 2.0
