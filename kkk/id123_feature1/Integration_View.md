# Integration View

> Torna a [Solution](./README.md)

---

## Information System Architecture

<!-- ISTRUZIONE: Descrivere l'insieme degli applicativi/moduli coinvolti e le loro principali interazioni a livello di flussi dati. Questa sezione copre il "chi parla con chi"; le logiche di dettaglio (come, con quale sequenza, con quali condizioni) vanno nella Specifica di Integrazione. qui la mia modifica -->

_[Inserire qui il diagramma ISA]_

> [!TIP]
> Per il grafico vedere [FAQ — Come inserire diagrammi e grafici?](./Template_FAQ.md#come-inserire-diagrammi-e-grafici)

| Flusso Dati | Descrizione | Impatto |
|---|---|---|
| _[da compilare]_ | _[Oggetti di business scambiati, input/output, vincoli di comunicazione o tipologia di canale]_ | _[`Nuovo` \| `Modificato` \| `Invariato`]_ |

---

## Specifica di Integrazione

<!-- ISTRUZIONE: Descrivere le logiche con cui i sistemi che compongono la solution si integrano tra loro end-to-end. Aggiungere una sotto-sezione per ogni scenario, flusso o dominio rilevante, replicando il blocco seguente. Intestare ogni sotto-sezione con il criterio scelto: "Scenario — Checkout utente", "Flusso — Notifica ordine verso CRM", "Dominio — Gestione pagamenti", ecc. -->

> [!TIP]
> Se le logiche di integrazione diventano numerose o sono gestite da team separati, estrarle in file dedicati (es. `Specifica_Integrazione_Pagamenti.md`). Vedere [FAQ — Cosa fare quando una sezione diventa troppo lunga?](./Template_FAQ.md#cosa-fare-quando-una-sezione-diventa-troppo-lunga)

---

### _[Scenario / Flusso / Dominio — Titolo]_

**Riferimenti**

> [!TIP]
> Sezione facoltativa. Documenti di riferimento specifici per questa integrazione: user story JIRA, IFA (Interfacce Applicative), contratti API, specifiche di protocollo. Non duplicare qui ciò che è già nei Riferimenti generali del README.

- _[US-NNN — Titolo user story](LINK)_
- _[IFA-NNN — Nome interfaccia](LINK)_

**Descrizione**

<!-- ISTRUZIONE: Contesto di business e obiettivo dell'integrazione. Cosa deve accadere end-to-end e perché. -->

_[Descrizione — da compilare]_

**Logica di integrazione**

<!-- ISTRUZIONE: Sequenza di chiamate, trasformazioni dati, condizioni, gestione degli errori e delle retry, vincoli di ordine o temporali. Essere espliciti su chi chiama chi, con quale protocollo, in quale contesto. -->

_[Logica di integrazione — da compilare]_

**Diagramma**

> [!NOTE]
> Preferire Mermaid inline per sequenze semplici; per diagrammi complessi usare `![Titolo](./assets/nome_file.png)` con il file sorgente in `assets/`.

_[Inserire qui il diagramma]_

---

### _[Scenario / Flusso / Dominio — Titolo]_

<!-- ISTRUZIONE: Replicare la struttura della sotto-sezione precedente. Aggiungere tutte le sotto-sezioni necessarie. -->
