# Concept

## What this repository is

`_project-index` is a Project Registry: a shared machine-readable map of software projects.

It is deliberately separate from the projects themselves.

A project repository contains implementation. The registry contains metadata needed to discover, identify, relate, and manage projects.

## Consumers

The same registry can be consumed by:

- Humans
- Coding agents
- Research agents
- Project-management agents
- Local autonomous agents
- Scripts and applications
- Multi-agent systems

## Three information classes

### Identity

Stable identification of a project and its source repository.

### Human-defined metadata

Meaning that requires an owner's decision, such as purpose, role, importance, and relationships.

### Machine-observed metadata

Facts that can be refreshed from GitHub or other configured sources, such as visibility, default branch, latest commit, languages, and archive state.

This separation is important because automated synchronization should not silently change project intent.

## Repository privacy

The registry may contain references to private repositories. A reference does not grant access to the private repository.

No credentials, secrets, private source code, or sensitive personal data belong in this public registry.

## Extensibility

The schema is intentionally small in version 1.0. Future versions may add owners, teams, capabilities, interfaces, lifecycle states, external resources, agent compatibility, provenance, and event history without requiring consumers to understand every future field.
