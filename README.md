# _project-index

A machine-readable project registry for humans and AI agents.

## Purpose

_project-index provides a shared, structured map of a project ecosystem. It is designed to be readable by:

- Humans
- Individual AI agents
- Multi-agent systems
- Automation and project-management tools

The registry describes projects, their purpose, observable repository metadata, and relationships between projects.

## Design principles

1. Machine-readable first, human-readable second.
2. Human-defined semantic metadata must not be silently overwritten by automation.
3. Machine-observed metadata may be refreshed from source repositories.
4. Project relationships should be explicit rather than inferred as facts.
5. Private repositories may be referenced without exposing private source code or secrets.
6. The schema is intended to remain generic so this registry can be reused by other people, agents, and organizations.

## Structure

- `registry/projects.json` — current project registry.
- `schema/registry.schema.json` — registry-level JSON Schema.
- `schema/project.schema.json` — project-entry JSON Schema.
- `agents/AGENTS.md` — instructions for AI agents operating on this registry.
- `docs/CONCEPT.md` — conceptual model and field ownership.
- `docs/CONTRIBUTING.md` — contribution and synchronization rules.

## Updating the registry

An agent may synchronize machine-observed metadata from the repositories listed in the registry and detect newly created repositories.

Human-defined fields such as project purpose, role, importance, and relationships should only be changed when explicitly confirmed or when the change is clearly documented in project metadata.

A synchronization should validate the JSON files before committing changes.

## Scope

This registry is intentionally independent from any single agent implementation. It can be consumed by future agents, scripts, applications, or humans without requiring the `ai-agent-v3` project.

## License

No license is currently specified for this repository.
