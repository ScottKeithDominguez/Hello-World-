# Copilot Instructions for Hello-World-

## Repository Overview

This is a test repository for learning and experimentation with GitHub features and workflows.

## Project Structure

```
/
├── .github/
│   └── workflows/
│       └── codeql.yml          # CodeQL security scanning workflow
├── LICENSE                     # BSD-3-Clause License
├── README.md                   # Project documentation
├── SECURITY.md                 # Security policy and vulnerability reporting
└── SECURITY_SETUP.md          # Security configuration instructions
```

## Security & Best Practices

### Security Features Implemented

1. **CodeQL Analysis**: Automated code scanning configured in `.github/workflows/codeql.yml`
   - The language matrix is currently empty and needs to be updated based on project languages
   - Runs on push to main, pull requests, and weekly schedule
   - Supported languages: `c-cpp`, `csharp`, `go`, `java-kotlin`, `javascript-typescript`, `python`, `ruby`, `swift`

2. **Security Policy**: Defined in `SECURITY.md`
   - Vulnerability reporting process
   - Response timeline expectations
   - Contact methods for security issues

3. **Manual Security Features**: As documented in `SECURITY_SETUP.md`, the following must be enabled manually:
   - Secret scanning
   - Dependabot alerts
   - Dependabot security updates
   - Private vulnerability reporting

### When Making Changes

- **Security First**: Always consider security implications when adding new code or dependencies
- **CodeQL Configuration**: When adding code in a new language, update the `language` matrix in `.github/workflows/codeql.yml` to include the appropriate language identifier
- **License Compliance**: This project uses BSD-3-Clause license - ensure any added code or dependencies are compatible
- **Documentation**: Update relevant documentation (README.md, SECURITY_SETUP.md) when adding new features or security measures

## Coding Guidelines

### General Principles

- Keep changes minimal and focused
- Maintain consistency with existing code style
- Document security-related changes thoroughly
- Test changes before committing

### Security Considerations

- Never commit secrets, API keys, or credentials
- Use environment variables for sensitive configuration
- Follow the security reporting process outlined in SECURITY.md
- Keep dependencies up to date and monitor for vulnerabilities

## Testing & Validation

- Ensure any code changes are compatible with the configured CodeQL scanning
- Validate that security workflows continue to run successfully
- Test locally before pushing changes

## Workflow & Contribution Guidelines

### Development Process

1. **Branch Naming**: Use descriptive branch names (e.g., `feature/add-authentication`, `fix/security-vulnerability`)
2. **Commit Messages**: Write clear, concise commit messages that explain the "why" behind changes
3. **Pull Requests**: 
   - Include a description of changes
   - Reference related issues
   - Ensure all checks pass before requesting review
4. **Code Review**: All changes should be reviewed before merging to main branch

### File Organization

- **Documentation**: Store all documentation files (`.md`) in the root directory
- **Workflows**: GitHub Actions workflows go in `.github/workflows/`
- **Configuration**: Project configuration files in `.github/` or root as appropriate
- **Security**: Security-related documentation in root with `SECURITY` prefix

## Common Patterns & Examples

### Documentation Style

When adding new documentation:
- Use clear headings and subheadings
- Include code examples where applicable
- Add links to external resources
- Keep formatting consistent with existing docs

### Security Practices

When working with sensitive data:
```yaml
# Good: Use GitHub Secrets
env:
  API_KEY: ${{ secrets.API_KEY }}

# Bad: Never hardcode secrets
env:
  API_KEY: "1234567890abcdef"
```

### Workflow Updates

When modifying GitHub Actions workflows:
- Test changes in a feature branch first
- Ensure proper permissions are set
- Use specific action versions (e.g., `@v4` not `@latest`)
- Add comments explaining complex steps

## Resources

- [GitHub Security Features](https://docs.github.com/en/code-security)
- [CodeQL Documentation](https://codeql.github.com/docs/)
- [Dependabot Documentation](https://docs.github.com/en/code-security/dependabot)
- [BSD-3-Clause License](https://opensource.org/licenses/BSD-3-Clause)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Markdown Guide](https://www.markdownguide.org/)
