# Contributing to containerd

Welcome! We're glad you're interested in contributing to this fork of containerd.
This document outlines the process for contributing to this project.

## Code of Conduct

This project follows the [CNCF Code of Conduct](https://github.com/cncf/foundation/blob/main/code-of-conduct.md).
By participating, you are expected to uphold this code.

## Getting Started

### Prerequisites

- Go 1.21 or later
- Linux environment (or use the provided devcontainer)
- Docker or containerd installed for integration tests

### Setting Up Your Development Environment

The easiest way to get started is using the provided devcontainer:

1. Install [VS Code](https://code.visualstudio.com/) and the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
2. Open this repository in VS Code
3. When prompted, click "Reopen in Container"
4. The container will automatically set up all required dependencies

Alternatively, you can set up manually:

```bash
# Clone the repository
git clone https://github.com/your-org/containerd.git
cd containerd

# Install dependencies
go mod download

# Build the project
make build
```

## How to Contribute

### Reporting Bugs

Before filing a bug report, please check the [existing issues](../../issues) to avoid duplicates.
Use the bug report template when creating a new issue.

### Requesting Features

Feature requests are welcome! Please use the feature request template and provide
as much context as possible about your use case.

### Submitting Pull Requests

1. Fork the repository and create a new branch from `main`
2. Make your changes with appropriate tests
3. Ensure all tests pass: `make test`
4. Ensure code is properly formatted: `make fmt`
5. Run linting: `make lint`
6. Submit a pull request with a clear description of the changes

### Commit Message Format

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

Types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

Examples:
- `feat(snapshots): add overlay snapshot driver support`
- `fix(runtime): resolve race condition in task manager`
- `docs: update contributing guidelines`

## Development Workflow

### Running Tests

```bash
# Unit tests
make test

# Integration tests (requires root)
sudo make integration

# Specific package tests
go test ./pkg/...
```

### Code Style

- Follow standard Go conventions and idioms
- Run `gofmt` or `goimports` before committing
- Add comments for all exported functions and types
- Keep functions focused and reasonably sized

## Review Process

All submissions require review. We use GitHub pull requests for this purpose.
Reviewers will look for:

- Correctness and test coverage
- Code quality and consistency with existing patterns
- Documentation updates where necessary
- Backward compatibility considerations

## License

By contributing, you agree that your contributions will be licensed under the
[Apache 2.0 License](LICENSE).
