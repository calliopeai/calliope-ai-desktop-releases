# Security Policy

## Reporting a Vulnerability

At Calliope Labs, we take security seriously. If you discover a security vulnerability in any of our desktop applications, please help us by reporting it responsibly.

### How to Report

**DO NOT** create a public GitHub issue for security vulnerabilities.

Instead, please report security issues via email to:

**security@calliope.ai**

### What to Include

Please include the following information in your report:

- **Application**: Which application (Calliope AI IDE or Calliope AI Lab)
- **Version**: The version number where you found the vulnerability
- **Platform**: Operating system and architecture
- **Description**: A clear description of the vulnerability
- **Steps to Reproduce**: Detailed steps to reproduce the issue
- **Impact**: The potential impact of the vulnerability
- **Proof of Concept**: If applicable, include a proof of concept
- **Suggested Fix**: If you have suggestions for fixing the issue

### Response Timeline

- We will acknowledge receipt of your vulnerability report within **48 hours**
- We will provide a more detailed response within **5 business days**
- We will work to validate and address confirmed vulnerabilities as quickly as possible
- We will keep you informed of our progress

### Disclosure Policy

- Please give us reasonable time to address the vulnerability before making it public
- We will coordinate with you on the disclosure timeline
- We will credit you (if desired) when we publicly disclose the vulnerability

## Supported Versions

Security updates are provided for the following versions:

| Application | Version | Supported          |
| ----------- | ------- | ------------------ |
| Calliope AI IDE | 1.0.x | :white_check_mark: |
| Calliope AI Lab | 1.0.x | :white_check_mark: |

Older versions may not receive security updates. We recommend always using the latest version.

## Security Best Practices

When using Calliope AI desktop applications:

### API Key Security

- **Never share** your API keys for AI providers
- **Never commit** API keys to version control
- Store API keys securely using the built-in SecretStorage
- Rotate your API keys regularly
- Use separate API keys for different applications/environments

### Local Data Security

- Calliope AI Lab stores data in a local PostgreSQL database
- This data is stored unencrypted on your local machine
- Ensure your operating system user account is password protected
- Consider encrypting your hard drive (FileVault, BitLocker, LUKS)
- Be cautious when sharing notebooks or exporting data

### Network Security

- AI features communicate with external API providers
- Ensure you trust the AI provider you're using
- Be aware that code and data sent to AI providers may be used for training
- For sensitive work, consider using local models via Ollama
- Use HTTPS connections when available

### Extension Security (IDE)

- Only install extensions from trusted sources
- Review extension permissions before installation
- Keep extensions updated
- Be cautious with extensions that request network access

### Update Security

- Keep your applications updated to receive security patches
- Enable automatic update notifications
- Verify downloads are from official Calliope AI sources
- Check file hashes if provided in release notes

## Known Security Considerations

### Unsigned Binaries

Current releases are **unsigned**, which means:

- **macOS**: Gatekeeper will show warnings on first launch
  - Solution: Go to System Settings → Privacy & Security → "Open Anyway"
  - Terminal alternative: `xattr -dr com.apple.quarantine /Applications/Calliope\ AI\ IDE.app`
- **Windows**: SmartScreen may show warnings
  - Solution: Click "More info" → "Run anyway"
  - PowerShell alternative: `Unblock-File -Path "C:\path\to\Calliope AI IDE Setup.exe"`

This is a known limitation and **not a security vulnerability**. Future releases will include code signing.

### Third-Party Dependencies

Both applications include numerous third-party open-source components:

- We monitor dependencies for known vulnerabilities
- We update dependencies regularly
- See `LICENSES` directory in each application for full dependency list

### Data Privacy

**Important Privacy Notes:**

- **Local Processing**: Both applications run entirely on your local machine
- **AI Provider Communication**: When using AI features, your code/data is sent to the configured AI provider
- **No Telemetry**: We do not collect usage analytics or telemetry by default
- **Your Responsibility**: You are responsible for compliance with data protection regulations when using AI features

## Security Features

### Built-in Security

- **Sandboxed Execution**: Application runs in OS-level sandbox
- **Secure Storage**: API keys stored using platform SecretStorage APIs
- **HTTPS**: All external API calls use HTTPS
- **No Remote Code Execution**: No remote code execution capabilities by default

### What We Don't Do

- We do **not** collect or transmit your code or data (except to AI providers you configure)
- We do **not** have backdoors or remote access
- We do **not** share your information with third parties
- We do **not** require account creation or authentication

## Bug Bounty Program

We currently do not have a formal bug bounty program. However:

- We deeply appreciate responsible disclosure
- We will acknowledge security researchers in our release notes (if desired)
- We may provide swag or other recognition for significant findings

## Questions?

If you have questions about security that don't involve reporting a vulnerability, you can:

- Email: security@calliope.ai
- Join our Discord: https://discord.gg/Z9bbbE6hJv (use #security channel)

---

**Last Updated**: November 14, 2025

Thank you for helping keep Calliope AI and our users safe!
