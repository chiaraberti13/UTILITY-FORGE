# Contributing to UTILITY-FORGE

UTILITY-FORGE is a collection of standalone, privacy-first document and file utilities. Contributions should preserve that model: tools remain understandable, narrowly scoped, local/self-hosted where practical and explicit about their security limits.

## Before you start
1. Read `README.md`, `SECURITY.md` and the README inside the tool you are changing.
2. Search existing issues and keep each pull request focused on one tool or one cross-cutting concern.
3. Never commit real personal documents, customer files, credentials, metadata samples containing private information or copyrighted fixtures you cannot redistribute.
4. Use synthetic fixtures for PDFs, Office files, images, CSV/Excel inputs and filenames.
5. Report vulnerabilities privately.

## Development
Most tools are intentionally self-contained. Run the changed tool in the environment documented by its own README. For PHP-based tools, validate syntax and exercise uploads/conversions in an isolated local server. For browser tools, test with local synthetic files in supported browsers.

## Security checks
For every changed tool verify, as applicable:
- file-count and size limits;
- MIME/extension/content validation;
- safe filenames and path handling;
- no unsafe `innerHTML` rendering of untrusted data;
- Content Security Policy assumptions;
- true redaction/sanitization claims, not cosmetic masking;
- local-only processing claims and any external network dependency;
- failure behaviour for malformed, oversized or unsupported inputs.

## Adding a new tool
A new utility must have its own folder and README, a clear privacy/data-flow statement, explicit limitations, safe sample data, and an entry in the root README. New dependencies need a specific purpose, compatible licence and reasonable maintenance posture.

## Pull requests
Describe the user problem, implementation, supported environments, sample data used, tests performed, security/privacy impact and known limitations. Write documentation in English and keep README.md and README.it.md semantically aligned.

Participation follows `CODE_OF_CONDUCT.md`.

## Reporting and contribution checks

Use the [issue templates](https://github.com/chiaraberti13/UTILITY-FORGE/issues/new/choose) and check for duplicates first. Useful context: Utility name, browser or PHP version, file format and synthetic sample.

Write community and technical documentation in English; maintain equivalent English and Italian READMEs. Preserve existing application translations. Fill in the pull request template with commands, results and checks not performed, including the reason. Use synthetic examples without secrets or personal data.

See [the code of conduct](CODE_OF_CONDUCT.md), [security policy](SECURITY.md) and [accessibility statement](ACCESSIBILITY.md). Report vulnerabilities only through the security policy process.
