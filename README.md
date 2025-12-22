# Cursor Rules Repository

## Purpose

Shared cursor rules for LLM-assisted development. Clone and symlink to any project.

## Setup

Clone at the same level as project repositories:

```
projects/
├── fep-cursor-rules/    # This repo
├── my-project/
└── another-project/
```

## Usage

From project root, create relative symlink:

```bash
ln -s ../fep-cursor-rules/cursor-rules .cursor/rules
```

Verify:

```bash
ls -la .cursor/rules
```

## Structure

```
cursor-rules/
├── 000-master.mdc           # Root index (alwaysApply)
├── 001-rules-maintenance.mdc # Maintenance procedures
├── common/                   # Cross-cutting rules (3xx)
│   ├── 300-common-master.mdc
│   ├── 301-cursor-rules-development.mdc
│   ├── 302-llm-oriented-writing.mdc
│   ├── 303-observability.mdc
│   └── 304-secret-leak-detection.mdc
├── ops/                      # Infrastructure rules (4xx)
│   └── 401-ansible.mdc
├── python/                   # Python rules (5xx)
│   ├── 500-python-master.mdc
│   ├── 501-python-development.mdc
│   ├── 502-python-quality.mdc
│   └── 503-python-uv.mdc
└── nextjs/                   # Next.js rules (6xx)
    ├── 600-nextjs-master.mdc
    ├── 601-nextjs-development.mdc
    ├── 602-nextjs-components.mdc
    └── 603-nextjs-api-testing.mdc
```

## Rule Categories

| Prefix | Category | Scope |
|--------|----------|-------|
| 3xx | Common | All projects |
| 4xx | Ops | Infrastructure, deployment |
| 5xx | Python | Python development |
| 6xx | Next.js | Next.js development |

## AlwaysApply Rules

Active in all contexts:

- `000-master.mdc` — root navigation
- `common/300-common-master.mdc` — common navigation
- `common/302-llm-oriented-writing.mdc` — LLM writing style
- `common/304-secret-leak-detection.mdc` — secret handling
- `python/500-python-master.mdc` — Python navigation
- `nextjs/600-nextjs-master.mdc` — Next.js navigation

## Adding Rules

See `cursor-rules/001-rules-maintenance.mdc`.
