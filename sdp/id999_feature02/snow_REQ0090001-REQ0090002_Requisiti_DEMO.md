# Requisiti — REQ0090001 / REQ0090002

> **Sorgente:** Export da Sistema di Requirement Management (fittizio)
> **Progetto (Parent):** PRJ0012345
> **Rilascio:** Gestione presenza WalletPay e SaveLink sui conti e depositi coinvolti nella vendita in bundle di Opzione Risparmio Plus

---

## Riepilogo comparativo

| Campo | REQ0090001 | REQ0090002 |
|---|---|---|
| **Numero** | REQ0090001 | REQ0090002 |
| **Parent** | PRJ0012345 | PRJ0012345 |
| **Priorità** | 3 – Moderate | 3 – Moderate |
| **Categoria** | Business | Business |
| **Tipologia** | Funzionale | Funzionale |
| **Requisito coperto** | Sì | Sì |
| **Fast Lane** | No | No |
| **Stato Fast Lane** | NA | NA |
| **AP1** | AP-02010 - WEBDESK DEPOSITI - Front End Depositi | AP-02010 - WEBDESK DEPOSITI - Front End Depositi |
| **AP2** | AP-02455 - DOCUFORGE | AP-02455 - DOCUFORGE |
| **AP3** | AP-03120 - Product Hub | AP-03120 - Product Hub |
| **Altri AP impattati** | — | — |
| **Soluzione** | come da requisito | come da requisito |

---

## REQ0090001

### Metadati

| Campo | Valore |
|---|---|
| **Numero** | REQ0090001 |
| **Parent** | PRJ0012345 |
| **Priorità** | 3 – Moderate |
| **Categoria** | Business |
| **Tipologia** | Funzionale |
| **Categoria Requisiti IA** | — |
| **Requisito coperto** | Sì |
| **Fast Lane** | No |
| **Stato Fast Lane** | NA |
| **Rilascio** | Gestione presenza WalletPay e SaveLink sui conti e depositi coinvolti nella vendita in bundle di Opzione Risparmio Plus |
| **AP1** | AP-02010 - WEBDESK DEPOSITI - Front End Depositi |
| **AP2** | AP-02455 - DOCUFORGE |
| **AP3** | AP-03120 - Product Hub |
| **Altri AP impattati** | — |
| **Soluzione** | come da requisito |

### Classificazione processo

| Livello | Valore |
|---|---|
| **Libreria** | BPM Wealth Management |
| **I Livello** | Commerciale |
| **II Livello** | Vendita |
| **III Livello** | Contrattualizzazione |
| **IV Livello** | Apertura e trasformazione deposito a risparmio |
| **V Livello** | — |
| **Processo Operativo L2** | — |
| **Processo Operativo L3** | — |
| **Processo Operativo L4** | — |
| **Processo Operativo L5** | — |
| **Processo Operativo New** | — |

### Short Description

> Bundle Integrato\_Apertura Deposito Plus e collegamento CC Wallet: requisito attivazione WalletPay (Wave 2.1)

### Description

Di seguito il requisito rivisto, relativo all'attivazione di WalletPay, nella funzionalità di **Apertura Deposito Plus in WebDesk con collegamento Conto Wallet** per attivazione Opzione Risparmio Plus (Wave 2.1 – Bundle Integrato):

- In fase di vendita deposito con aggancio di un conto corrente occorre verificare se sul conto ci sia **WalletPay attivo**
- Se WalletPay **non è attivo**, viene completata l'attivazione dell'Opzione e nella schermata di riepilogo l'Operatore visualizza un messaggio che lo invita a chiedere al cliente se desidera attivare WalletPay.
- Cliccando sul tasto "prosegui" della pagina di riepilogo sarà avviato lo step di **onboarding del deposito** appena aperto (as is)
- Se il cliente parlando con l'operatore ha espresso la volontà di attivare WalletPay, l'Operatore potrà avviare l'apposita **funzionalità di postvendita** per attivare WalletPay e gestire eventuale retry con il motore di processo
- Nessuna modifica prevista per documenti contrattuali

### Descrizione Estesa

_Non compilata._

---

## REQ0090002

### Metadati

| Campo | Valore |
|---|---|
| **Numero** | REQ0090002 |
| **Parent** | PRJ0012345 |
| **Priorità** | 3 – Moderate |
| **Categoria** | Business |
| **Tipologia** | Funzionale |
| **Categoria Requisiti IA** | — |
| **Requisito coperto** | Sì |
| **Fast Lane** | No |
| **Stato Fast Lane** | NA |
| **Rilascio** | Gestione presenza WalletPay e SaveLink sui conti e depositi coinvolti nella vendita in bundle di Opzione Risparmio Plus |
| **AP1** | AP-02010 - WEBDESK DEPOSITI - Front End Depositi |
| **AP2** | AP-02455 - DOCUFORGE |
| **AP3** | AP-03120 - Product Hub |
| **Altri AP impattati** | — |
| **Soluzione** | come da requisito |

### Classificazione processo

| Livello | Valore |
|---|---|
| **Libreria** | BPM Wealth Management |
| **I Livello** | Commerciale |
| **II Livello** | Vendita |
| **III Livello** | Contrattualizzazione |
| **IV Livello** | Apertura e trasformazione deposito a risparmio |
| **V Livello** | — |
| **Processo Operativo L2** | — |
| **Processo Operativo L3** | — |
| **Processo Operativo L4** | — |
| **Processo Operativo L5** | — |
| **Processo Operativo New** | — |

### Short Description

> Bundle Integrato\_Collegamento stock CC\_Card vs Deposito Plus: requisito attivazione WalletPay SaveLink (Wave 2.2)

### Description

Di seguito il requisito rivisto, relativo all'attivazione di WalletPay e SaveLink, nella funzionalità di **postvendita che consente il collegamento di Deposito Plus e Conto Wallet** per attivazione Opzione Risparmio Plus (Wave 2.2 – Bundle Integrato):

- In fase di aggancio di un deposito e di un conto corrente se uno dei due prodotti non ha **SaveLink/WalletPay attivi**:
  - **Se SaveLink non è attivo:**
    - Non verrà mostrata nel funnel la pagina di securizzazione del cellulare sul deposito
    - Completata l'attivazione dell'Opzione, in una nuova schermata successiva a quella di riepilogo l'Operatore visualizzerà un messaggio per richiedere al cliente se desidera attivare/non attivare SaveLink
    - Se il cliente sceglie di attivare SaveLink l'Operatore verrà reindirizzato alla fase di postvendita per attivare SaveLink; la securizzazione del cellulare sul deposito sarà effettuata contestualmente e verrà gestito il relativo modulo come da processi as is
  - **Se WalletPay non è attivo:**
    - Completata l'attivazione dell'Opzione, in una nuova schermata successiva a quella di riepilogo l'Operatore visualizzerà un messaggio per richiedere al cliente se desidera attivare/non attivare WalletPay
    - Se il cliente sceglie di attivare WalletPay l'Operatore verrà reindirizzato alla fase di postvendita per attivare WalletPay e gestire eventuale retry con il motore di processo
  - **Se entrambi SaveLink e WalletPay non sono attivi:**
    - Non verrà mostrata nel funnel la pagina di securizzazione del cellulare sul deposito
    - Completata l'attivazione dell'Opzione, in una nuova schermata successiva a quella di riepilogo l'Operatore visualizzerà un messaggio per richiedere al cliente se desidera attivare/non attivare SaveLink e WalletPay
    - Se il cliente sceglie di attivarli l'Operatore verrà reindirizzato alla fase di postvendita per attivare SaveLink; la securizzazione del cellulare sul deposito sarà effettuata contestualmente e verrà gestito il relativo modulo come da processi as is
    - Sarà l'operatore che al termine dell'attivazione di SaveLink dovrà avviare l'apposita funzionalità di postvendita per attivare WalletPay e gestire eventuale retry con il motore di processo
    - Viene gestita in coerenza con il nuovo requisito anche la gestione della securizzazione del cellulare non visibile nel caso di stock deposito senza SaveLink e Carta Prepagata, ed il messaggio post-riepilogo che invita ad attivare SaveLink
    - **Prevista eliminazione della sola parte statica del modulo di connessione** (quella riferita all'attivazione di WalletPay e SaveLink inserita nella versione precedente).

### Descrizione Estesa

_Non compilata._

---

## Note

- I campi **Processo Operativo L2–L5** e **Processo Operativo New** non sono valorizzati per entrambi i requisiti.
- Il campo **Descrizione Estesa** non è valorizzato per entrambi i requisiti.
- Il campo **Altri AP impattati** non è valorizzato: gli AP impattati sono solo AP1 (AP-02010 - WEBDESK DEPOSITI - Front End Depositi), AP2 (AP-02455 - DOCUFORGE) e AP3 (AP-03120 - Product Hub).
- I due requisiti fanno parte dello stesso rilascio e progetto; si distinguono per la **Wave** di riferimento (2.1 vs 2.2) e per il **perimetro funzionale** (apertura deposito vs collegamento stock CC/Card).
