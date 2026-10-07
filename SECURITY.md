# Security Policy

<p align="center"><a href="#english">🇬🇧 English</a> · <a href="#italiano">🇮🇹 Italiano</a></p>

## English

### Supported versions
Security fixes target the latest revision on the default branch. Individual tools are supported as part of that current repository state rather than as independent historical releases.

### Scope
This policy covers every utility in this monorepo, including file parsing, browser APIs, PHP upload/conversion paths, document/image metadata handling, redaction/sanitization, archive generation, filenames, local filesystem access, third-party libraries and repository CI/build configuration.

### Reporting a vulnerability
Do not open a public issue for an unpatched vulnerability. Use GitHub private vulnerability reporting / Security Advisories when available. Include the affected tool and commit, impact, minimal reproducible steps or proof of concept, browser/runtime assumptions and suggested mitigations. Use synthetic files and strip unrelated private data.

### Data and privacy
The project is privacy-first. A tool must not silently upload user files or metadata to third parties. Any network dependency must be documented. Do not commit real documents, credentials, GPS data, personal metadata or customer information.

### File-processing security
Treat every filename and file as hostile until validated. Enforce count/size bounds, validate format and structure, sanitize output names, prevent path traversal, avoid unsafe DOM insertion and isolate server-side conversion tools. Redaction features must remove underlying information rather than merely cover it visually.

### Supply chain
Review dependency and vendor changes, licence compatibility and remote resources. Prefer self-contained or pinned components and keep CSP assumptions consistent with the actual assets loaded.

## Italiano

### Versioni supportate
Le correzioni di sicurezza riguardano la revisione più recente del branch predefinito. I singoli strumenti sono supportati come parte dello stato corrente del repository.

### Ambito
La policy copre tutti i tool del monorepo: parsing dei file, API browser, upload/conversione PHP, metadati di documenti/immagini, redazione/sanitizzazione, archivi, nomi file, accesso al filesystem locale, librerie di terze parti e CI/build.

### Segnalazione
Non aprire issue pubbliche per vulnerabilità non corrette. Usa la segnalazione privata / Security Advisories quando disponibile. Indica tool e commit interessati, impatto, passaggi minimi riproducibili o PoC, assunzioni su browser/runtime e mitigazioni. Usa file sintetici e rimuovi dati privati non necessari.

### Dati e privacy
Il progetto è privacy-first. Nessun tool deve inviare silenziosamente file o metadati a terzi. Ogni dipendenza di rete va documentata. Non committare documenti reali, credenziali, coordinate GPS, metadati personali o dati cliente.

### Sicurezza nell'elaborazione file
Considera ostili file e nomi file fino alla validazione. Applica limiti di numero/dimensione, valida formato e struttura, sanifica i nomi di output, previeni path traversal, evita inserimenti DOM non sicuri e isola gli strumenti di conversione server-side. Le funzioni di redazione devono rimuovere davvero l'informazione, non solo coprirla visivamente.

### Supply chain
Controlla dipendenze e vendor, compatibilità delle licenze e risorse remote. Preferisci componenti self-contained o pinnati e mantieni la CSP coerente con gli asset realmente caricati.
