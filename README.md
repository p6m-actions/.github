# YBOR P6M Github Actions

A collection of reusable, composable GitHub Actions for streamlining your
software development lifecycle across multiple language ecosystems.

While generally useful, these actions are designed around the Ybor Platform,
and got hand-in-hand with project's generated from Ybor's catalog of
[Archetect](https://github.com/archetect/archetect) Archetypes.

## Overview

`p6m-actions` provides standardized GitHub Actions that can be easily
integrated into your workflows. Our actions follow consistent patterns across
language ecosystems, making it simple to implement similar CI/CD processes
regardless of your tech stack.

## Available Actions

Our actions are organized by language ecosystem and common functionality,
implementing steps commonly required in a typical SDLC. Thise include:

- Building
- Testing
- Version Bumping and Cutting Tags
- Logging into Artifact Management Repositories
- Publishing Artifacts
- Code Quality Assessments
- Security Scans
- Releases and Changelogs

## Usage

Each action is contained in its own repository within this organization. To use an action, reference it in your workflow file:

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: p6m-actions/rust-registry-login@v1
        with:
          registry-url: "https://registry.example.com"
          registry-token: ${{ secrets.REGISTRY_TOKEN }}
      - uses: p6m-actions/rust-build@v1
        with:
          cargo-args: "--release"
```

## Contributing

We welcome contributions! Please see our [contribution guidelines](CONTRIBUTING.md) for details on how to submit improvements.
