# Copilot Instructions for miniature-fishstick

## Project Overview
This is a new project repository. As the codebase develops, update this file with specific architectural decisions, patterns, and conventions.

## Repository Structure

```
.
├── .github/
│   ├── workflows/         # GitHub Actions workflows
│   │   └── ci.yml        # Main CI pipeline
│   ├── dependabot.yml    # Automated dependency updates
│   └── copilot-instructions.md
├── src/                  # Source code directory
│   └── README.md         # Source structure documentation
├── README.md             # Project documentation
├── SECURITY.md           # Security policy
├── .gitignore           # Git ignore patterns
└── .editorconfig        # Editor configuration for consistent style
```

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

### Build/Test Commands
Currently, the repository uses GitHub Actions for CI/CD:
- **CI Workflow**: `.github/workflows/ci.yml` - Validates repository structure
- Run locally: Check file structure with `ls -la` and verify essential files exist

To validate changes locally:
```bash
# Check repository structure
ls -la

# Verify essential files
test -f README.md && echo "✓ README.md found"
test -f .gitignore && echo "✓ .gitignore found"
test -f .editorconfig && echo "✓ .editorconfig found"
```

## Pipeline & Automation
The repository is configured with:
- **GitHub Actions**: Automated CI/CD workflows in `.github/workflows/`
- **Dependabot**: Automated dependency updates for npm, pip, and GitHub Actions
- **EditorConfig**: Consistent code style across different editors

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
