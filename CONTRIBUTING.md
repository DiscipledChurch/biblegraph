# Contributing to Bible Graph Data

## Adding a New Unit

1. Choose the correct category folder (`people/`, `places/`, `clans/`, `groups/`, `events/`)
2. Create a Markdown file named after the unit (e.g., `Abraham.md`)
3. Include valid YAML frontmatter matching `schema/unit.schema.json`
4. Generate a new UUID v4 for the `id` field
5. Add relationships to related units — **both sides must be explicit**

## Frontmatter Requirements

- `id`: UUID v4 (globally unique)
- `name`: Display name
- `type`: Must match the folder (`person`, `place`, `clan`, `group`, `event`)
- `relationships`: Each relationship must have a matching inverse in the target file

## Relationship Rules

- Relationships are gender-specific: use `father_of`/`mother_of`, not generic `parent_of`
- Relationship names must contain verbs: `is_member_of`, not `member`
- Both directions must be present: if A `father_of` B, then B must have `son_of` or `daughter_of` A

## Validation

Run the validation tool before submitting:

```bash
cd tools && python -m src.validate.runner --data-dir ../data
```

## Style Guide

- File names: PascalCase matching the display name (e.g., `Adam.md`, `GardenOfEden.md`)
- Markdown body: freeform content displayed on the unit's detail page
- References: use book name, chapter, and verse ranges
