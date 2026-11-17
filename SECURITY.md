# Security Policy

## Supported versions
Security fixes target the latest revision on the default branch. Individual tools are supported as part of that current repository state rather than as independent historical releases.

## Scope
This policy covers every utility in this monorepo, including file parsing, browser APIs, PHP upload/conversion paths, document/image metadata handling, redaction/sanitization, archive generation, filenames, local filesystem access, third-party libraries and repository CI/build configuration.

## Reporting a vulnerability
Do not open a public issue for an unpatched vulnerability. Use GitHub private vulnerability reporting / Security Advisories when available. Include the affected tool and commit, impact, minimal reproducible steps or proof of concept, browser/runtime assumptions and suggested mitigations. Use synthetic files and strip unrelated private data.

## Data and privacy
The project is privacy-first. A tool must not silently upload user files or metadata to third parties. Any network dependency must be documented. Do not commit real documents, credentials, GPS data, personal metadata or customer information.

## File-processing security
Treat every filename and file as hostile until validated. Enforce count/size bounds, validate format and structure, sanitize output names, prevent path traversal, avoid unsafe DOM insertion and isolate server-side conversion tools. Redaction features must remove underlying information rather than merely cover it visually.

## Supply chain
Review dependency and vendor changes, licence compatibility and remote resources. Prefer self-contained or pinned components and keep CSP assumptions consistent with the actual assets loaded.

## Private reporting process

Use **Report a vulnerability** in the repository Security tab if private reporting is available. Otherwise use a verified private contact published by the repository owner. If no private contact is available, open a public issue asking only for a private contact, without vulnerability details. Do not publish exploit details, credentials, personal data or sensitive logs in public issues.

Include the affected revision, environment, impact and minimal synthetic reproduction. Coordinate disclosure with the maintainer. Acknowledgement and remediation depend on availability and severity; no fixed response deadline is guaranteed.
