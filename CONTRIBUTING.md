# Contributing

Thanks for your interest in improving this project! This document explains how
to set up a development environment and get your changes merged.

## Development setup

```bash
git clone https://github.com/opao-max/e2b-go-sdk.git
cd e2b-go-sdk
go version   # requires Go 1.24+
go mod download
```

## Workflow

1. Fork the repository and create a branch from `main`:
   `git checkout -b feat/short-description`
2. Make your change, keeping commits focused and using
   [Conventional Commits](https://www.conventionalcommits.org/):
   `feat:`, `fix:`, `docs:`, `test:`, `refactor:`, `chore:`.
3. Before pushing, run the same checks as CI:

```bash
go vet ./...
go build ./...
go test ./...
gofmt -l .   # must print nothing
```

4. Push your branch and open a Pull Request, filling in the PR template.

## Code style

- Run `gofmt`/`goimports` before every commit.
- Exported identifiers must have doc comments.
- Prefer table-driven tests; cover error paths, not just the happy path.
- Keep public API changes backward compatible where possible; document
  breaking changes in the PR description and `CHANGELOG.md`.

## Reporting bugs

Please use the Bug Report issue template and include a minimal reproduction.

## License

By contributing, you agree that your contributions will be licensed under the
repository's MIT License.

