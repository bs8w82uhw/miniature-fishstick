# Contributing to miniature-fishstick

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to this project.

## Getting Started

1. Fork the repository
2. Clone your fork locally
3. Create a new branch for your changes
4. Make your changes
5. Test your changes
6. Submit a pull request

## Development Workflow

### Branch Naming Convention

Use descriptive branch names with prefixes:
- `feature/` - New features
- `bugfix/` - Bug fixes
- `hotfix/` - Urgent fixes for production
- `docs/` - Documentation changes
- `refactor/` - Code refactoring
- `test/` - Test additions or modifications

Example: `feature/add-user-authentication`

### Commit Messages

Write clear, concise commit messages following this format:
```
<type>(<scope>): <subject>

<body>

<footer>
```

Types:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `test`: Adding or modifying tests
- `chore`: Maintenance tasks
- `perf`: Performance improvements

Example:
```
feat(auth): add user login endpoint

Implement POST /api/login endpoint with email/password authentication.
Includes JWT token generation and validation.

Closes #123
```

### Pull Request Process

1. **Update Documentation**: Ensure any new features or changes are documented
2. **Add Tests**: Include appropriate tests for your changes
3. **Update Changelog**: Add a note about your changes (if applicable)
4. **Follow Code Style**: Ensure your code follows the project's style guidelines
5. **Fill PR Template**: Complete all relevant sections of the PR template
6. **Request Review**: Request review from maintainers
7. **Address Feedback**: Respond to and address all review comments

### Code Quality Standards

- Write clean, readable, and maintainable code
- Follow language-specific best practices
- Add comments for complex logic
- Keep functions small and focused
- Use meaningful variable and function names
- Avoid code duplication

### Testing

- Write tests for new features
- Ensure all tests pass before submitting PR
- Maintain or improve code coverage
- Include both positive and negative test cases

## CI/CD Workflows

This project uses GitHub Actions for continuous integration. All PRs must pass:
- ✅ CI validation checks
- ✅ Code quality/linting checks
- ✅ Security scans
- ✅ PR validation checks

You can run checks locally before pushing:
```bash
# Run linters (examples - adjust based on your project)
# npm run lint
# flake8 .
# golangci-lint run
```

## Reporting Issues

When reporting issues, please:
- Use the appropriate issue template
- Provide a clear description
- Include steps to reproduce
- Specify your environment details
- Add relevant logs or screenshots

## Questions?

If you have questions, please:
- Check existing issues and discussions
- Open a new issue with the "question" label
- Reach out to maintainers

## Code of Conduct

Be respectful and professional in all interactions. We aim to maintain a welcoming and inclusive environment for everyone.

---

Thank you for contributing! 🎉
