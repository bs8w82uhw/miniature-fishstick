# Quick Reference: CI/CD Infrastructure

## 🚀 Quick Start

### For New Contributors
1. Read `CONTRIBUTING.md` for contribution guidelines
2. Use issue templates when creating issues
3. Use PR template when submitting pull requests
4. All CI checks must pass before merge

### For Maintainers
1. Review `INITIALIZATION_SUMMARY.md` for complete setup details
2. Check `.github/CICD.md` for workflow documentation
3. Monitor Dependabot PRs weekly
4. Address security alerts promptly

## 📊 Workflows Overview

| Workflow | Runs On | Purpose | Status Check |
|----------|---------|---------|--------------|
| **CI** | Push, PR | Basic validation, structure checks | ✅ Required |
| **Code Quality** | Push, PR | Markdown/YAML linting | ✅ Required |
| **Security** | Push, PR, Weekly | Dependency & secret scanning | ⚠️ Monitor |
| **PR Validation** | PR only | Metadata, size, conflicts | ℹ️ Advisory |

## 🛠️ Common Tasks

### Run Linters Locally
```bash
# Markdown (requires markdownlint-cli2)
npx markdownlint-cli2 "**/*.md"

# YAML (requires yamllint)
yamllint .
```

### Test Workflow Locally
```bash
# Install act: https://github.com/nektos/act
act -l                    # List workflows
act push                  # Simulate push event
act pull_request          # Simulate PR event
```

### Add a New Language

**Example: Adding Python**

1. **Update `.github/workflows/ci.yml`**:
```yaml
# Uncomment and customize:
build:
  name: Build
  runs-on: ubuntu-latest
  permissions:
    contents: read
  steps:
    - uses: actions/checkout@v4
    - uses: actions/setup-python@v5
      with:
        python-version: '3.11'
    - name: Install dependencies
      run: pip install -r requirements.txt
    - name: Build
      run: python setup.py build
```

2. **Update `.github/workflows/code-quality.yml`**:
```yaml
# Uncomment Python linting section
```

3. **Update `.github/workflows/security.yml`**:
```yaml
# Add to CodeQL matrix:
language: ['python']
```

4. **Update `.github/dependabot.yml`**:
```yaml
# Uncomment pip section
```

## 🔒 Security Features

- ✅ Explicit workflow permissions (least privilege)
- ✅ Secret scanning (TruffleHog)
- ✅ Dependency vulnerability checks
- ✅ CodeQL analysis (ready for supported languages)
- ✅ Weekly security scans

## 📋 Checklist: Before First PR

- [ ] Review CONTRIBUTING.md
- [ ] Ensure CI workflows pass
- [ ] Add tests for new features
- [ ] Update documentation if needed
- [ ] Fill out PR template completely
- [ ] Request review from maintainers

## 📋 Checklist: Adding New Feature

- [ ] Create feature branch: `feature/your-feature-name`
- [ ] Add code and tests
- [ ] Update relevant documentation
- [ ] Run linters locally
- [ ] Commit using conventional commits
- [ ] Push and create PR using template
- [ ] Address CI feedback
- [ ] Respond to code review comments

## 🆘 Troubleshooting

### CI Failing?
1. Check workflow logs in Actions tab
2. Review the specific job that failed
3. Run the same checks locally
4. Fix issues and push updates

### Workflow Not Triggering?
1. Check trigger conditions in workflow file
2. Verify branch names match triggers
3. Ensure workflow file is in `main` or target branch
4. Check Actions tab for workflow runs

### Need Help?
1. Check `.github/CICD.md` for detailed documentation
2. Review existing issues and PRs
3. Create an issue using appropriate template
4. Tag maintainers if urgent

## 📚 Key Files

| File | Purpose |
|------|---------|
| `.github/workflows/*.yml` | GitHub Actions workflows |
| `.github/dependabot.yml` | Automated dependency updates |
| `.github/CICD.md` | Detailed CI/CD documentation |
| `.gitignore` | Files to exclude from git |
| `CONTRIBUTING.md` | Contribution guidelines |
| `INITIALIZATION_SUMMARY.md` | Setup documentation |

## 🔗 Useful Links

- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Semantic Versioning](https://semver.org/)
- [GitHub Flow](https://guides.github.com/introduction/flow/)

---

**Last Updated**: Repository Initialization
**For Questions**: Create an issue or contact maintainers
