# Security Policy

**Project:** wolfXspotify-API  
**Maintainer:** Silent Wolf · WOLF TECH  
**GitHub:** [https://github.com/WOLFTECH-254](https://github.com/WOLFTECH-254)  
**Live API:** [https://spotify.xwolf.space](https://spotify.xwolf.space)

---

## Supported Versions

| Version | Supported |
|---------|-----------|
| 2.x (current) | ✅ Active |
| 1.x | ⚠️ Security fixes only |

---

## Reporting a Vulnerability

If you discover a security vulnerability in **wolfXspotify-API**, please **do not** open a public GitHub issue. Instead, report it responsibly using one of the following methods:

1. **GitHub Private Advisory** — Open a [Security Advisory](https://github.com/WOLFTECH-254/wolfXspotify-API/security/advisories/new) on this repository
2. **GitHub Issues** — Create an issue with the label `security` (will be kept private / handled discreetly)

Please include:
- A clear description of the vulnerability
- Steps to reproduce
- Potential impact
- Any suggested fix if available

---

## Response Timeline

| Stage | Timeframe |
|-------|-----------|
| Acknowledgement | Within 48 hours |
| Initial assessment | Within 5 days |
| Fix or mitigation | Within 14 days (depending on severity) |
| Public disclosure | After fix is deployed |

---

## Scope

### In scope
- Authentication or token exposure vulnerabilities
- Server-side injection issues
- Denial of service vulnerabilities
- Information disclosure issues
- CORS misconfigurations
- Environment variable leakage

### Out of scope
- Vulnerabilities in Spotify's own platform
- Issues related to data accuracy or availability
- Rate limiting bypass (this API intentionally has no rate limits)
- Client-side usage vulnerabilities (users are responsible for their own implementations)

---

## Responsible Disclosure

We appreciate responsible disclosure and will acknowledge your contribution in the release notes if you agree. We do not currently offer a bug bounty programme, but we sincerely value the security community's efforts.

---

## Security Best Practices for Users

When using **wolfXspotify-API** in your applications:

1. **Do not expose tokens** — Never log or expose the access token returned by `/api/token` to end users if you're using it as a backend proxy
2. **Cache responsibly** — Implement proper token caching as shown in the README
3. **Use HTTPS** — Always communicate with the API over HTTPS (enforced on the live deployment)
4. **Validate inputs** — Sanitize any user inputs before passing them to the API

---

## Environment Variables (Self-Hosted)

If self-hosting, ensure the following are properly secured:

| Variable | Security Notes |
|----------|----------------|
| `GITHUB_TOKEN` | Keep private — store in `.env` and never commit to version control |
| `GITHUB_REPO` | Only necessary if using GitHub token persistence |
| `PORT` | No special security considerations |

---

## Contact

For security-related inquiries only:
- **GitHub Security Advisory** (preferred)
- **GitHub Issues** with `security` label

---

© 2026 WOLF TECH · Silent Wolf — All rights reserved.
