# Contributing to Taxonomy V2 MDP

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to this project.

## Code of Conduct

Please review our [Code of Conduct](CODE_OF_CONDUCT.md) before participating.

## Getting Started

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/taxonomy_v2.mdp.git
   cd taxonomy_v2.mdp
   ```
3. **Add upstream remote**:
   ```bash
   git remote add upstream https://github.com/islam1494/taxonomy_v2.mdp.git
   ```

## Development Setup

### Using Dev Container
```bash
# Open in VS Code with Dev Containers extension
# Press F1 and select "Dev Containers: Open Folder in Container"
```

### Local Setup
```bash
# Install Rust: https://rustup.rs/
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

# Build the project
cargo build

# Run tests
cargo test
```

## Making Changes

1. **Create a feature branch**:
   ```bash
   git checkout -b feature/description-of-feature
   ```

2. **Make your changes** and test thoroughly:
   ```bash
   cargo test
   cargo fmt
   cargo clippy
   ```

3. **Commit with clear messages**:
   ```bash
   git commit -m "feat: description of what was added"
   git commit -m "fix: description of what was fixed"
   git commit -m "docs: description of documentation changes"
   ```

4. **Push to your fork**:
   ```bash
   git push origin feature/description-of-feature
   ```

5. **Create a Pull Request** on GitHub

## Commit Message Format

Follow the [Conventional Commits](https://www.conventionalcommits.org/) format:

- `feat:` A new feature
- `fix:` A bug fix
- `docs:` Documentation changes
- `style:` Code style changes (formatting, semicolons, etc.)
- `refactor:` Code changes that neither fix bugs nor add features
- `perf:` Performance improvements
- `test:` Adding or updating tests
- `chore:` Build process, dependencies, or tooling changes

Example:
```
feat: add taxonomy classification algorithm
fix: resolve memory leak in parser
docs: update installation instructions
```

## Code Standards

- Format code with `cargo fmt`
- Check with `cargo clippy` and fix warnings
- Write tests for new functionality
- Ensure all tests pass: `cargo test`
- Add documentation comments for public APIs

## Pull Request Process

1. Update documentation if needed
2. Add or update tests for your changes
3. Ensure all tests pass
4. Fill out the PR template completely
5. Be responsive to feedback and review comments

## Reporting Issues

### Bug Reports
Include:
- Clear description of the bug
- Steps to reproduce
- Expected behavior
- Actual behavior
- Environment (OS, Rust version, etc.)

### Feature Requests
Include:
- Clear description of the feature
- Use case and motivation
- Potential implementation approach (optional)

## Questions?

Feel free to:
- Open an issue with the `question` label
- Check existing issues and discussions
- Ask in pull request comments

Thank you for contributing! 🎉
