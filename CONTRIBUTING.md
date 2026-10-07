# Contributing to UTILITY-FORGE

<p align="center"><a href="#english">🇬🇧 English</a> · <a href="#italiano">🇮🇹 Italiano</a></p>

## English

UTILITY-FORGE is a collection of standalone, privacy-first document and file utilities. Contributions should preserve that model: tools remain understandable, narrowly scoped, local/self-hosted where practical and explicit about their security limits.

### Before you start
1. Read `README.md`, `SECURITY.md` and the README inside the tool you are changing.
2. Search existing issues and keep each pull request focused on one tool or one cross-cutting concern.
3. Never commit real personal documents, customer files, credentials, metadata samples containing private information or copyrighted fixtures you cannot redistribute.
4. Use synthetic fixtures for PDFs, Office files, images, CSV/Excel inputs and filenames.
5. Report vulnerabilities privately.

### Development
Most tools are intentionally self-contained. Run the changed tool in the environment documented by its own README. For PHP-based tools, validate syntax and exercise uploads/conversions in an isolated local server. For browser tools, test with local synthetic files in supported browsers.

### Security checks
For every changed tool verify, as applicable:
- file-count and size limits;
- MIME/extension/content validation;
- safe filenames and path handling;
- no unsafe `innerHTML` rendering of untrusted data;
- Content Security Policy assumptions;
- true redaction/sanitization claims, not cosmetic masking;
- local-only processing claims and any external network dependency;
- failure behaviour for malformed, oversized or unsupported inputs.

### Adding a new tool
A new utility must have its own folder and README, a clear privacy/data-flow statement, explicit limitations, safe sample data, and an entry in the root README. New dependencies need a specific purpose, compatible licence and reasonable maintenance posture.

### Pull requests
Describe the user problem, implementation, supported environments, sample data used, tests performed, security/privacy impact and known limitations. Update English documentation first and keep Italian documentation semantically aligned.

Participation follows `CODE_OF_CONDUCT.md`.

## Italiano

UTILITY-FORGE raccoglie strumenti standalone e privacy-first per documenti e file. I contributi devono mantenere questo modello: strumenti comprensibili, circoscritti, locali/self-hosted quando possibile e chiari sui propri limiti di sicurezza.

### Prima di iniziare
1. Leggi `README.md`, `SECURITY.md` e il README dello strumento interessato.
2. Controlla le issue esistenti e mantieni ogni pull request focalizzata.
3. Non committare documenti personali reali, file cliente, credenziali, metadati privati o fixture non redistribuibili.
4. Usa fixture sintetiche per PDF, Office, immagini, CSV/Excel e nomi file.
5. Segnala privatamente le vulnerabilità.

### Sviluppo e sicurezza
Esegui lo strumento nell'ambiente documentato e verifica, quando applicabile: limiti di numero/dimensione file, validazione di contenuto e tipo, nomi file sicuri, protezione da path traversal e injection, assenza di rendering HTML non sicuro, CSP, autenticità delle operazioni di redazione/sanitizzazione, elaborazione locale dichiarata e gestione corretta degli input malformati.

### Nuovi strumenti
Ogni nuovo tool deve avere cartella e README propri, data-flow/privacy chiari, limiti espliciti, esempi sicuri e una voce nel README principale. Le nuove dipendenze devono essere motivate, compatibili con MIT e ragionevolmente mantenute.

### Pull request
Descrivi problema, implementazione, ambienti supportati, dati di test, controlli eseguiti, impatto sicurezza/privacy e limiti noti. Aggiorna prima la documentazione inglese e mantieni quella italiana equivalente.

Si applica `CODE_OF_CONDUCT.md`.
