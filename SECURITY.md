# Security Policy

At Classgrid, the security of educational institutions, student data, and administrative records is our highest priority. We take vulnerabilities seriously and are committed to maintaining a robust, enterprise-grade security posture across our entire infrastructure.

## Supported Versions

Since Classgrid is a unified, cloud-hosted SaaS platform, we actively maintain and secure the latest production deployment on our servers. 

| Component | Status |
| --- | --- |
| Classgrid Core Platform (Web/API) | ✅ Supported |
| Classgrid Marketing Engine (Next.js) | ✅ Supported |
| Legacy/Archived Branches | ❌ Not Supported |

## Reporting a Vulnerability

We deeply appreciate the efforts of security researchers and developers who help us keep our platform safe. 

If you discover a security vulnerability in our codebase, infrastructure, APIs, or database architecture (MongoDB/Supabase), please **DO NOT** disclose it publicly or create a public GitHub issue. 

Instead, please report it privately:

1. **Email:** Send a detailed report to **[security@classgrid.in](mailto:security@classgrid.in)**.
2. **Details:** Include a description of the vulnerability, steps to reproduce, and any potential impact (e.g., unauthorized data access, RBAC bypass).
3. **Response:** Our security team will acknowledge receipt of your vulnerability report within 48 hours and provide an estimated timeline for remediation.

We will work closely with you to understand the issue and resolve it securely. 

## Best Practices
As a contributor, please ensure:
- **No Secrets in Code:** Never commit API keys, database credentials, or `.env` files. (We use GitGuardian to enforce this).
- **Dependency Updates:** Keep `package.json` dependencies updated. We run automated checks using `npm audit`.
- **Data Privacy:** Ensure strict adherence to our RBAC (Role-Based Access Control) policies in any new API route added to the Express or Next.js backend.
