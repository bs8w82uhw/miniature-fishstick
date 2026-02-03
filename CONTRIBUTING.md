# Contributing to miniature-fishstick

Thank you for your interest in contributing!

## Development Workflow

### Prerequisites
- Ensure you have the necessary development tools installed for your project stack
- Fork and clone the repository

### Making Changes

1. Create a new branch from `main`:
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. Make your changes following the project conventions

3. Run local checks:
   - Lint your code
   - Run tests
   - Build the project

4. Commit your changes with clear, descriptive messages

5. Push to your fork and create a pull request

## CI/CD Pipeline

### Continuous Integration
The CI workflow (`.github/workflows/ci.yml`) runs on:
- Push to `main` branch
- Pull requests to `main`
- Manual trigger via workflow_dispatch

**CI Steps:**
1. **Lint**: Code quality and style checks
2. **Test**: Automated test suite
3. **Build**: Project build verification

### Release Process
Releases are automated via the Release workflow (`.github/workflows/release.yml`):
- Triggered by pushing tags with format `v*` (e.g., `v1.0.0`)
- Can also be triggered manually via workflow_dispatch
- Automatically creates GitHub releases

**To create a release:**
```bash
git tag -a v1.0.0 -m "Release version 1.0.0"
git push origin v1.0.0
```

## Pull Request Guidelines

- Keep PRs focused on a single feature or fix
- Ensure all CI checks pass
- Update documentation as needed
- Add tests for new features

## Questions?

Feel free to open an issue for any questions or concerns.
