# Architectural View

> Torna a [Solution](./README.md)

---

## Architecture Decision Records

> [!NOTE]
> Un file per ogni decisione nella cartella `adr/`. Convenzione di naming: `adr/NNN_titolo_decisione.md`. Usare il [template ADR](./adr/000_template.md) fornito. Aggiornare l'elenco sotto ad ogni nuova decisione.

<!-- ISTRUZIONE: Aggiungere una riga per ogni ADR. Rimuovere la riga di esempio sotto prima di pubblicare. -->

- [000 — Template](./adr/000_template.md) — `—`
- _[001 — Titolo decisione](./adr/001_titolo.md) — `Accettata` (esempio — rimuovere)_

---

## Application Technical Architecture

<!-- ISTRUZIONE: Descrivere l'insieme delle piattaforme applicative coinvolte nel progetto e le loro interazioni. -->

> [!NOTE]
> **Convenzione grafici** — usare la seguente priorità:
> 1. **Mermaid inline** per diagrammi semplici (flowchart, component): versionato col testo, renderizzato nativamente da GitHub, nessun file esterno.
> 2. **PNG o SVG in `assets/`** per diagrammi complessi (draw.io, Visio, ecc.): `![Titolo](./assets/nome_file.png)`. Conservare anche il file sorgente (`.drawio`, `.vsdx`) nella stessa cartella.
> 3. **Link esterno** (Confluence, Figma, Miro...) solo come riferimento complementare, mai come unica fonte.

_[Inserire qui il diagramma di Application Technical Architecture — Mermaid inline oppure `![ATA](./assets/Diagramma_ATA.png)`]_

---

### Dettaglio applicativi

| Pacchetto Applicativo | Software | Versione | Layer applicativo | Applicativo esistente o nuovo |
|---|---|---|---|---|
| _[da compilare]_ | | | | |

---

### Dettaglio flusso dati

| Flusso dati | Protocollo | Contratto | Origine Layer | Destinazione Layer | Tipologia | Frequenza | Frequenza di Picco | Dimensione media msg | Dimensione massima msg | Flusso nuovo o esist. |
|---|---|---|---|---|---|---|---|---|---|---|
| _[da compilare]_ | _[es. REST over HTTPS]_ | _[es. [OpenAPI 3.1](LINK)]_ | _[es. Microfrontend]_ | _[es. Backend-lists]_ | _[es. Real time]_ | | | | | _[Nuovo/Esistente]_ |

---

### Capacità elaborativa

> [!TIP]
> Sezione facoltativa. Dimensionamento flussi dati mainframe per stima CPU. Compilare solo se pertinente.

| Flusso dati | Protocollo | Tipologia | Stato Flusso | Frequenza media | Frequenza di Picco | Numero Record (Solo Batch) |
|---|---|---|---|---|---|---|
| _[da compilare]_ | | | | | | |

---

### Spazio disco

> [!TIP]
> Sezione facoltativa. Dimensionamento spazio disco mainframe. Compilare solo se pertinente.

| Tipo Repository | Stato Repository | Dimensioni | Numero record | Lunghezza record |
|---|---|---|---|---|
| _[da compilare]_ | | | | |
