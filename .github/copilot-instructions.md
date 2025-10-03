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

## Resources

- [GitHub Security Features](https://docs.github.com/en/code-security)
- [CodeQL Documentation](https://codeql.github.com/docs/)
- [Dependabot Documentation](https://docs.github.com/en/code-security/dependabot)
- [BSD-3-Clause License](https://opensource.org/licenses/BSD-3-Clause)
