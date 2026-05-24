# containerd

[![Go Reference](https://pkg.go.dev/badge/github.com/containerd/containerd.svg)](https://pkg.go.dev/github.com/containerd/containerd)
[![Build Status](https://github.com/containerd/containerd/workflows/CI/badge.svg)](https://github.com/containerd/containerd/actions?query=workflow%3ACI)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

A fork of [containerd/containerd](https://github.com/containerd/containerd) — an industry-standard container runtime with an emphasis on simplicity, robustness, and portability.

## Overview

containerd is available as a daemon for Linux and Windows. It manages the complete container lifecycle of its host system, from image transfer and storage to container execution and supervision to low-level storage to network attachments and beyond.

## Features

- **OCI Image Spec** support
- **OCI Runtime Spec** support (via runc and other OCI-compatible runtimes)
- **Image push and pull** support
- **Container lifecycle** management
- **Network primitives** for creation, attachment, and management of network interfaces
- **Multi-tenant** support with namespaces
- **Snapshotters** for overlay, btrfs, and more
- **Content-addressable** storage
- **Metadata persistence** with bolt

## Getting Started

### Prerequisites

- Go 1.21 or later
- Linux kernel 4.x or later (for full feature support)
- `runc` or another OCI-compatible runtime

### Development Environment

This repository includes a [Dev Container](.devcontainer/) configuration for a consistent development environment.

1. Open in VS Code with the Dev Containers extension installed.
2. Select **Reopen in Container** when prompted.
3. The environment will be set up automatically.

### Building from Source

```bash
# Clone the repository
git clone https://github.com/containerd/containerd.git
cd containerd

# Build containerd
make

# Build and install
make install
```

### Running Tests

```bash
# Run unit tests
make test

# Run integration tests (requires root)
sudo make integration
```

## Documentation

- [Architecture Overview](docs/architecture.md)
- [Getting Started Guide](docs/getting-started.md)
- [CRI Plugin](docs/cri/)
- [Snapshotters](docs/snapshotters/)
- [Plugins](docs/PLUGINS.md)

## Contributing

We welcome contributions! Please read our [Contributing Guide](CONTRIBUTING.md) before submitting a pull request.

### Reporting Issues

Use the [GitHub issue tracker](https://github.com/containerd/containerd/issues) to report bugs or request features. Please use the provided issue templates.

## Community

- **Slack**: [#containerd](https://cloud-native.slack.com/messages/containerd) on the CNCF Slack
- **Mailing List**: [containerd-dev](https://groups.google.com/forum/#!forum/containerd-dev)
- **Community Meetings**: See the [CNCF calendar](https://www.cncf.io/community/calendar/)

## License

This project is licensed under the Apache License 2.0 — see the [LICENSE](LICENSE) file for details.

## Acknowledgements

This project is a fork of the [containerd/containerd](https://github.com/containerd/containerd) project, maintained by the containerd authors and contributors.
