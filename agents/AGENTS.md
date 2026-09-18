# Agent Instructions

## Role

You are operating on `_project-index`, a shared project registry intended for humans and AI agents.

## Before changing the registry

1. Read `README.md`.
2. Read the relevant schemas.
3. Inspect the current `registry/projects.json`.
4. Distinguish machine-observed facts from human-defined metadata.
5. Never invent a repository, dependency, relationship, status, or purpose.

## Synchronization

When asked to synchronize the registry:

1. Enumerate the repositories available to the configured GitHub account.
2. Compare them with `registry/projects.json`.
3. Add newly discovered repositories.
4. Detect repositories that disappeared, were archived, or were renamed.
5. Refresh machine-observed metadata.
6. Read project documentation when semantic metadata needs confirmation.
7. Preserve human-defined fields unless the user explicitly requests their modification.
8. Update `indexed_at` and `indexed_commit` after successfully inspecting a repository.
9. Validate the resulting JSON against the schemas.
10. Commit the changes with a clear message.

## Multi-agent safety

Multiple agents may consume this registry. Agents should:

- Make minimal changes.
- Avoid rewriting unrelated entries.
- Preserve valid information written by other agents.
- Prefer explicit evidence over inference.
- Record uncertainty instead of inventing facts.
- Avoid storing secrets, credentials, tokens, or private source code.

## Relationship rules

A relationship such as `depends_on` or `used_by` should only be added when it is documented or explicitly confirmed.

Do not infer a dependency merely because two projects have similar names or technologies.
