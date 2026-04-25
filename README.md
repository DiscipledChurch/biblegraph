# Bible Graph Data

Structured data for [biblegraph.ai](https://biblegraph.ai) — an interactive site for exploring biblical proper names and their relationships.

## Structure

```
people/    # Individual persons (Adam, Eve, Abraham, etc.)
places/    # Geographic locations (Eden, Bethlehem, etc.)
clans/     # Tribal/clan groupings
groups/    # Named groups (Pharisees, Apostles, etc.)
events/    # Named events (Exodus, Crucifixion, etc.)
schema/    # JSON Schema for validation
```

## Data Format

Each unit is a Markdown file with YAML frontmatter. See `schema/unit.schema.json` for the full schema.

## Relationships

Relationships are gender-specific and bidirectional. Both sides must be explicitly defined. See `schema/relationships.json` for the canonical list.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

This data is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
