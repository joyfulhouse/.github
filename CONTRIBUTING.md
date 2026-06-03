# Contributing

Thanks for your interest in contributing to JoyfulHouse's open-source projects.
This guide applies across all `joyfulhouse` repositories.

## Reporting Issues

- Search existing issues first to avoid duplicates.
- Use the issue templates where provided.
- Include clear reproduction steps, expected vs. actual behavior, relevant
  versions (the integration/library version, and the Home Assistant version
  where applicable), and any relevant logs.

## Proposing Changes

1. Fork the repository and create a topic branch from the default branch.
2. Make your change in small, focused commits.
3. Add or update tests and documentation for any behavior change.
4. Run the test suite and linters locally (see below) and confirm they pass.
5. Open a pull request describing what changed and why. Link any related issue.

## Development Setup

Each project documents its own setup in `docs/DEVELOPMENT.md`. In general:

- **Python** projects use [`uv`](https://docs.astral.sh/uv/): `uv sync`, then
  `uv run pytest`, `uv run ruff check`, and `uv run mypy`.
- **JavaScript/TypeScript** projects use [`bun`](https://bun.sh): `bun install`,
  then `bun test` and `bun run lint`.

## Commit Messages

Write clear, imperative commit subjects ("Add reconnect backoff", not "added
backoff"). [Conventional Commits](https://www.conventionalcommits.org) prefixes
(`feat:`, `fix:`, `docs:`, `chore:`) are encouraged.

## Code Style

Follow the conventions already present in the codebase. Do not disable linters or
type checks to work around a finding — fix the root cause.

## License

By contributing, you agree that your contributions are licensed under the same
license as the project (see `LICENSE`).
