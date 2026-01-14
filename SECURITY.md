# Security Policy

## Supported Versions

Use this section to tell people about which versions of your project are currently being supported with security updates.

| Version | Supported          |
| ------- | ------------------ |
| 1.x     | :white_check_mark: |
| < 1.0   | :x:                |

## Reporting a Vulnerability

We take security seriously. If you discover a vulnerability, please follow these steps:

1. **Do NOT open a public issue.** Publicly reporting a vulnerability can put the entire community at risk.
2. **Email the maintainers** directly (e.g., at `security@example.com` - *replace with actual email*) or use the GitHub "Report a vulnerability" tab if enabled.
3. **Provide details**: specific steps to reproduce the issue, potential impact, and proof-of-concept code if possible.

## Response Timeline

- We will acknowledge your report within **48 hours**.
- We will provide a status update every **5 days** until resolved.
- Once fixed, we will release a patch and publish a security advisory.

## Security Best Practices for Users

- Always keep your dependencies updated.
- Use environment variables for all secrets (API keys, DB URLs).
- Do not commit `.env` files to the repository.
