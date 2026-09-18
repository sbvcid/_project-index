# Contributing

## Adding a project

A project entry should contain:

1. A stable `id`.
2. Repository identity.
3. Human-defined purpose and role when known.
4. Machine-observed repository metadata when available.
5. Explicit relationships only when supported by evidence.

## Agent-generated changes

Agents may synchronize observable repository facts.

Agents should not silently rewrite human-defined semantic fields.

Every automated update should be small, reviewable, and attributable to a clear synchronization or maintenance action.

## Validation

Before committing:

- Validate JSON syntax.
- Validate registry structure against the schemas.
- Check that repository identifiers are well formed.
- Check for duplicate project IDs.
- Check that relationship targets refer to known project IDs when relationships are present.
- Do not include secrets or private source contents.

## Compatibility

Changes to the schema should increment the schema version when they introduce incompatible requirements.

Prefer additive changes for minor revisions.
