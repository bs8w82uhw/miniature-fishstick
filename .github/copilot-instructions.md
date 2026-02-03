# Copilot Instructions for miniature-fishstick

## Project Overview
This is a new project repository. As the codebase develops, update this file with specific architectural decisions, patterns, and conventions.

## Repository Structure
Currently minimal - contains only [README.md](../README.md). Structure will be documented as components are added.

## Development Workflow

### Getting Started
- Repository: `bs8w82uhw/miniature-fishstick`
- Default branch: `main`
- Environment: Dev container running Ubuntu 24.04.3 LTS

### Key Considerations for AI Agents
- This is an early-stage project - establish clear patterns from the start
- Document architectural decisions as they're made
- Follow consistent naming conventions once established
- Add build/test commands to this file as they're configured

## CI/CD Workflows

### GitHub Actions
The repository uses GitHub Actions for continuous integration and automation:

- **CI Workflow** (`.github/workflows/ci.yml`): Runs on push to main and pull requests
  - Validates repository structure
  - Verifies essential files exist
  - Status: [![CI](https://github.com/bs8w82uhw/miniature-fishstick/actions/workflows/ci.yml/badge.svg)](https://github.com/bs8w82uhw/miniature-fishstick/actions/workflows/ci.yml)

- **PR Checks** (`.github/workflows/pr-checks.yml`): Automated pull request validation
  - Validates PR title format
  - Checks for merge conflicts
  - Lists files changed
  - Status: [![PR Checks](https://github.com/bs8w82uhw/miniature-fishstick/actions/workflows/pr-checks.yml/badge.svg)](https://github.com/bs8w82uhw/miniature-fishstick/actions/workflows/pr-checks.yml)

### Adding New Workflows
When adding language-specific or framework-specific workflows:
1. Create workflow files in `.github/workflows/`
2. Follow the naming convention: `<purpose>.yml`
3. Add status badges to README.md
4. Document the workflow purpose in this file

## To Be Documented
As the project grows, add sections for:
- **Architecture**: Major components and their interactions
- **Coding Patterns**: Project-specific conventions and idioms
- **Dependencies**: External libraries and integration points
- **Testing Strategy**: Test framework and coverage expectations

## Notes for Contributors
- Update this file when introducing new architectural patterns
- Keep instructions concise and actionable
- Focus on project-specific knowledge, not general best practices
