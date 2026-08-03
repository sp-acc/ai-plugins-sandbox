# Animal in Latin

A lightweight educational AI plugin that provides the scientific (Latin) name of animals, along with a brief description and classification context.

## What it does

When the user invokes the skill, the plugin responds with:

- the common English name
- the scientific name in Latin form
- the animal family
- whether the animal is extant or extinct
- a brief educational description

The plugin supports the `/in-latin` command and is designed for quick lookup and classroom-style learning.

## Skill command

- Command: `/in-latin`
- Argument hint: `[animal name]`

## Example prompts

- `/in-latin lion`
- `/in-latin shark`
- `/in-latin`
- What is the Latin name of a dolphin?

## Behavior

The skill follows a consistent response pattern:

- accepts English-only input
- asks the user to re-enter names in English when another language is supplied
- handles missing input by returning a few example animals
- treats fictional or unrecognized creatures as unsupported
- includes extinct-species details with approximate time periods when relevant

## Plugin metadata

- Name: `in-latin`
- Version: `1.0.3`
- Author: `Srdjan Perovic`
- Category: `Education`
- Tags: `education`, `animals`, `latin`

## Repository layout

```text
plugins/animal/
├── README.md
└── skills/
    └── in-latin/
        ├── SKILL.md
        └── .claude-plugin/
            └── plugin.json
```

## Files

- [skills/in-latin/.claude-plugin/plugin.json](skills/in-latin/.claude-plugin/plugin.json) — plugin manifest and metadata
- [skills/in-latin/SKILL.md](skills/in-latin/SKILL.md) — skill logic and instruction rules

## Example response format

```text
Common Name: Tiger
Scientific Name: Panthera tigris (Family: Felidae)
Status: Extant
Description: Tigers are large carnivorous mammals known for their powerful build, striped coat, and role as apex predators in Asian habitats.
```

This plugin is intended as a clear educational example of a concise AI skill that can be packaged and listed in a minimal marketplace catalog.
