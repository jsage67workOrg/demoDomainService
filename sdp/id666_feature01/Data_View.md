# Data View

> Torna a [Solution](./README.md)

> [!NOTE]
> Sezione modulare: compilare solo le sotto-sezioni pertinenti alla soluzione. Ogni sotto-sezione è facoltativa e indipendente. QUi faccio la modifica

<!-- ISTRUZIONE: Questa view descrive la relazione tra la solution e i Data Product coinvolti — quali vengono consumati, creati o modificati e quali impatti architetturali ne derivano. Non duplicare qui informazioni che vivono nel catalogo dati aziendale: elenco completo degli attributi, definizione dei campi, regole di qualità dettagliate, lineage completo. -->

---

## Data Product consumati

> [!TIP]
> Sezione facoltativa. Elencare i Data Product che la solution legge o da cui dipende. Per ogni DP indicare il motivo dell'utilizzo a livello logico (non campo per campo), la versione o SLA da rispettare e l'impatto architetturale in caso di breaking change.

| Data Product | Utilizzo nella solution | Versione / SLA | Impatto se cambia |
|---|---|---|---|
| _[da compilare]_ | _[perché viene usato — descrizione logica]_ | _[versione o SLA]_ | _[impatto architetturale]_ |

---

## Data Product creati

> [!TIP]
> Sezione facoltativa. Elencare i Data Product che la solution produce ex novo. Indicare lo scope dei dati esposti e l'eventuale necessità di backfill o migrazione dati iniziale.

| Data Product | Scope dei dati esposti | Backfill / Migrazione |
|---|---|---|
| _[da compilare]_ | _[descrizione dei dati esposti]_ | _[necessità di backfill o note su migrazione iniziale]_ |

---

## Data Product modificati

> [!TIP]
> Sezione facoltativa. Elencare i Data Product esistenti che la solution arricchisce o altera. Indicare la natura della modifica e l'impatto sulle versioni e sui consumer esistenti.

| Data Product | Natura della modifica | Impatto su versioni / consumer esistenti |
|---|---|---|
| _[da compilare]_ | _[es. aggiunta campi, cambio semantica, rimozione attributi]_ | _[impatto sui consumer attuali del DP]_ |

---

## Mapping dati

> [!TIP]
> Sezione facoltativa. Adatta a solution integratrici (portali 360°, dashboard, aggregatori) che espongono dati provenienti da più sorgenti senza produrre un proprio DP. Per ogni dato logico mostrata dalla solution, indicare da dove proviene e come viene recuperata.

| Campo logico | Sorgente | Consumer / Esposizione | API / Endpoint | Modalità accesso | Note |
|---|---|---|---|---|---|
| _[es. Saldo disponibile]_ | _[es. DP Conti Correnti]_ | _[es. Scheda cliente — sezione Prodotti]_ | _[es. GET /accounts/{id}/balance]_ | _[`real-time` \| `cache` \| `batch`]_ | _[es. aggregazione multi-sorgente]_ |

---

## Impatti architetturali e di governance

> [!TIP]
> Sezione facoltativa. Vincoli trasversali che condizionano la progettazione della solution in relazione ai dati: version pinning dei data contract, politiche PII o retention che impattano il design, dipendenze con SLA critici, decisioni di ownership. Per le decisioni architetturali strutturate, rimandare agli ADR in [`adr/`](./adr/).

_[Impatti architetturali e di governance — da compilare, oppure eliminare la sezione se non applicabile]_
