# Scheda HW

> Torna a [Solution](./README.md)

### Risorse on Prem

<!-- ISTRUZIONE: Specificare nella colonna Ambiente se si tratta di ambienti di Sviluppo, Collaudo, Certificazione, Disaster Recovery e Produzione. -->

<br>

**Tabella per Risorse on Prem (HW dedicato o Private Cloud)** 

| AP\PK         | Ambiente |Server Fisico/Virtuale|Layer|Tipologia|Data Center|Cluster|RAM|Storage|CPU|Core|SO|SW|
|-----------------|------------|------------------------------------|------------------|--------|----|----|----|----|----|----|----|----|
|   || |		||||||||||

**Tabella Mainframe**

|Componente        | Ambiente |MIPS|Tipologia elaborazione|Capacità di storage|Storage Tape|
|-----------------|------------|------------------------------------|------------------|--------|----|
|   || |		|||

**Tabella HW Periferico**

|Tipologia       | Marca |Modello|Caratteristica tecnica 1|Caratteristica tecnica 2|Caratteristica tecnica 3|Caratteristica tecnica 4|
|-----------------|------------|------------------------------------|------------------|--------|----|----|
|   || |		|||



### Backup Risorse on Prem

<!-- ISTRUZIONE: Definire per ciascuna delle risorse elencate nel paragrafo precedente i parametri essenziali per garantire una strategia di backup efficace. Selezionare una delle opzioni operative: BASELINE BACKUP, POLICY CUSTOM, NO BACKUP. -->

* BASELINE BACKUP
*	POLICY CUSTOM
* NO BACKUP

•	Confermare la BASELINE BACKUP

L'adozione della Baseline di backup consente l'applicazione immediata di una serie di policy predefinite, validate e operative sin dal rilascio in esercizio della risorsa. Questa opzione è indicata quando le impostazioni suggerite risultano adeguate e sufficienti per garantire la protezione dei dati.
Verificare se i parametri di backup (Tipologia, Oggetto del Backup, Frequenza e Retention) indicati siano adeguati. 
La Baseline è una configurazione standard non modificabile. Qualora fosse necessario adottare parametri diversi, occorrerà selezionare l’opzione per la definizione di una Policy Custom.


•	Definire POLICY CUSTOM 

Qualora la Baseline non risulti idonea, oppure nel caso in cui sia parziale e non copra tutti gli oggetti necessari, è possibile configurare una policy personalizzata. 
In tal caso, è fondamentale compilare con attenzione i seguenti parametri:

  Tipologia di Dato: File System, SO, MSsql Server,Oracle, DB2, SAP, SAP Hana,mysql,Informix, NAS
  Oggetto del Backup: Es. Elenco FS, drive, istanza DB, etc…
  Frequenza: Giornaliera, settimanale, mensile, oraria
  Retention: Periodo di conservazione del backup
  GB Frontend: Volume dei dati da proteggere
  Num Copie: Copie simultanee di backup da mantenere
  Immutabilità: Specificare se le copie devono essere rese immutabili
  DR:  Indicare se la risorsa rientra nel piano di Disaster Recovery
  DORA: Indicare se la risorsa è soggetta alla normativa DORA
  NOTE: Indicare eventuali vincoli o dipendenze applicative

•	NO BACKUP

Se si ritiene che una o più risorse non debbano essere soggette a backup, selezionare questa opzione. 
È necessario indicare esplicitamente quali risorse escludere dalla strategia di protezione.
Attenzione: La selezione della sola checkbox, senza specificare il dettaglio, comporterà l’esclusione dal backup di tutte le risorse elencate nel paragrafo precedente.

### BASELINE BACKUP

**Baseline Backup on Prem**

> [!NOTE]
> Per tutti i workload applicativi installati sulle VM, qualora fosse necessario un backup differente dal FULL VM, è necessario compilare area POLICY CUSTOM.

| Ambiente      | Server Fisico\Virtuale |Tiplogia|Data Center|Cluster|SO|SW|Tipologia Dato|Oggetto del Backup|Frequenza|Retention|
|-----------------|------------|------------------------------------|------------------|--------|----|----|----|----|----|----|
|   || |		|||||||||


### POLICY CUSTOM

**Policy Backup Custom**

> [!NOTE]
> Per tutti i dati su sistemi in DR e/o DORA verrà applicata l'immutabilità per le copie di backup e 2 copie di backup.

| Ambiente      | Server Fisico\Virtuale |Tiplogia|Data Center|Cluster|SO|SW|Tipologia Dato|Oggetto del Backup|Frequenza|Retention|GB Frontend| N° Copie|Immutabilità|DR|DORA|NOTE|
|-----------------|------------|------------------------------------|------------------|--------|----|----|----|----|----|----|-----|-|---|---|---|--|
|   || |		||||||||||||||


### NO BACKUP

**No Backup**
| Ambiente      | Server Fisico\Virtuale |Tiplogia|Data Center|Cluster|SO|SW|
|-----------------|------------|------------------------------------|------------------|--------|----|----|
|   || |		||||

### OpenShift on Prem

<!-- ISTRUZIONE: Specificare nella colonna Ambiente se si tratta di ambienti di Sviluppo, Collaudo, Certificazione, Disaster Recovery e Produzione. Specificare nella colonna Namespace e Nome Cluster nuovo o già esistenti (indicandolo). -->

**Tabella Openshift on Prem**

| AP\PK         | Ambiente |Nome Cluster|Tiplogia cluster|Namespace|Gen|Request Core  (millicore) |Request Ram (MB)|Limit Core(core) |Limit Ram (MB)|Pod|BlobStorage (GB)|
|-----------------|------------|------------------------------------|------------------|--------|----|----|----|----|----|----|----|
|   || |		|||||||||


### Backup risorse OpenShift (On Prem)

<!-- ISTRUZIONE: Definire per ciascuna delle risorse elencate nel paragrafo precedente i parametri essenziali per garantire una strategia di backup efficace. Selezionare una delle opzioni operative: BASELINE BACKUP, POLICY CUSTOM, NO BACKUP. -->

* BASELINE BACKUP
* 	POLICY CUSTOM
* NO BACKUP

•	Confermare la BASELINE BACKUP

L'adozione della Baseline di backup consente l'applicazione immediata di una serie di policy predefinite, validate e operative sin dal rilascio in esercizio della risorsa.
Questa opzione è indicata quando le impostazioni suggerite risultano adeguate e sufficienti per garantire la protezione dei dati.
Verificare se i parametri di backup (Tipologia, Oggetto del Backup, Frequenza e Retention) indicati siano adeguati. 
La Baseline è una configurazione standard non modificabile. Qualora fosse necessario adottare parametri diversi, occorrerà selezionare l’opzione per la definizione di una Policy Custom.


•	Definire POLICY CUSTOM

Qualora la Baseline non risulti idonea, oppure nel caso in cui sia parziale e non copra tutti gli oggetti necessari, è possibile configurare una policy personalizzata. 
In tal caso, è fondamentale compilare con attenzione i seguenti parametri:

Tipologia di Dato: Resources namespace, PVC , Workload applicativo
Oggetto del Backup: Name delle tipologie precedenti
Application Consistency: Indicare se necessaria la consistenza applicativa per workload specifici (fornire lo script adeguato)
Frequenza: Giornaliera, settimanale, mensile, oraria
Retention: Periodo di conservazione del backup
GB Frontend: Volume dei dati da proteggere
NOTE: Indicare eventuali vincoli o dipendenze applicative

•	NO BACKUP
Se si ritiene che una o più risorse non debbano essere soggette a backup, selezionare questa opzione. 
È necessario indicare esplicitamente quali risorse escludere dalla strategia di protezione.
Attenzione: La selezione della sola checkbox, senza specificare il dettaglio, comporterà l’esclusione dal backup di tutte le risorse elencate nel paragrafo precedente.

### BASELINE BACKUP ###

**Baseline Backup OCP - PROD** 

| Ambiente      |Nome Cluster |Name Space|Gen|Tipologia Dato|Frequenza|Retention|
|-----------------|------------|------------------------------------|------------------|--------|----|----|
|   || |		||||


### POLICY CUSTOM ###

**Policy Custom**

| Ambiente      | Nome Cluster |Name Space|Gen|Tipologia Dato|Oggetto del Backup|Application Consistency|Frequenza|Retention|GB Frontend|Note|
|-----------------|------------|------------------------------------|------------------|--------|----|----|----|----|----|----|
|   || |		||||||||


### NO BACKUP ### 

**No Backup**

| Ambiente      | Nome Cluster |Namespace|Gen|Tiplogia Dato|Oggetto del Backup|
|-----------------|------------|------------------------------------|------------------|--------|-----|
|   || |		|||



### Risorse Cloud

<!-- ISTRUZIONE: Specificare nella colonna Ambiente (Sviluppo, Collaudo, Certificazione, DR, Produzione) e nella colonna Tipologia (IaaS/PaaS/SaaS). Specificare nei Resource Group se sono nuovi o già esistenti. Allegare CALCULATOR AWS o AZURE CLOUD. Per IaaS valorizzare anche la tabella sottostante. -->


**Tabella Risorse Cloud IaaS**

| AP\PK         | Ambiente |Risorsa|Tipologia|Cloud Provider|Region|Resouce Group|FQDN Front Door|FQDN Backend|RAM|Storage|CPU|Core|SO|SW|
|-----------------|------------|------------------------------------|------------------|--------|----|----|----|----|----|----|----|----|--|--|
|   || |		||||||||||||

### Backup Risorse On Cloud

<!-- ISTRUZIONE: Definire per ciascuna delle risorse elencate nel paragrafo precedente i parametri essenziali per garantire una strategia di backup efficace. Selezionare una delle opzioni operative: BASELINE BACKUP, POLICY CUSTOM, NO BACKUP. -->

•	Confermare la BASELINE BACKUP

L'adozione della Baseline di backup consente l'applicazione immediata di una serie di policy predefinite, validate e operative sin dal rilascio in esercizio della 
risorsa. Questa opzione è indicata quando le impostazioni suggerite risultano adeguate e sufficienti per garantire la protezione dei dati.
Verificare se i parametri di backup (Tipologia, Oggetto del Backup, Frequenza e Retention) indicati siano adeguati. 
La Baseline è una configurazione standard non modificabile. Qualora fosse necessario adottare parametri diversi, occorrerà selezionare l’opzione per la definizione di una Policy Custom.

•	Definire POLICY CUSTOM
Qualora la Baseline non risulti idonea, oppure nel caso in cui sia parziale e non copra tutti gli oggetti necessari, è possibile configurare una policy personalizzata. 
In tal caso, è fondamentale compilare con attenzione i seguenti parametri:

Oggetto del Backup: Database, bucket, directory, etc…
Frequenza: Giornaliera, settimanale, mensile, oraria
Retention: Periodo di conservazione del backup
GB Frontend: Volume dei dati da proteggere
Num Copie: Copie simultanee di backup da mantenere
Immutabilità: Specificare se le copie devono essere rese immutabili
NOTE: Indicare eventuali vincoli o dipendenze applicative

•	NO BACKUP
Se si ritiene che una o più risorse non debbano essere soggette a backup, selezionare questa opzione. 
È necessario indicare esplicitamente quali risorse escludere dalla strategia di protezione.
Attenzione: La selezione della sola checkbox, senza specificare il dettaglio, comporterà l’esclusione dal backup di tutte le risorse elencate nel paragrafo precedente.

### BASELINE BACKUP

**Baseline Backup Cloud – Prod**

> [!NOTE]
> Per tutti i workload applicativi installati sulle EC2/IaaS, qualora fosse necessario un backup differente dal FULL VM, è necessario compilare area POLICY CUSTOM.

| Ambiente      |Cloud Provider |Risorsa|Tipologia|Region|Subscription\Account|Oggetto del Backup|Frequenza|Retation|GB Frontend|N°Copie|Immutabilità|
|-----------------|------------|------------------------------------|------------------|--------|----|----|--|--|--|--|-|
|   || |		|||||||||


### POLICY CUSTOM ###

**Policy Custom**

| Ambiente      |Cloud Provider |Risorsa|Tipologia|Region|Subscription\Account|Oggetto del Backup|Frequenza|Retation|GB Frontend|N°Copie|Immutabilità|Note|
|-----------------|------------|------------------------------------|------------------|--------|----|----|--|--|--|--|-|-|
|   || |		||||||||||


### NO BACKUP ### 

**No Backup**

| Ambiente      |Cloud Provider|Risorsa|Tipologia|Region|Subscription\Account|
|-----------------|------------|------------------------------------|------------------|--------|-----|
|   || |		|||




### OpenShift Cloud

<!-- ISTRUZIONE: Specificare nella colonna Ambiente (Sviluppo, Collaudo, Certificazione, DR, Produzione) e nella colonna Namespace se nuovo o già esistente (indicandolo). -->

**Tabella Openshift Cloud** 

| AP\PK         | Ambiente |Nome Cluster|Tiplogia cluster|Namespace|Gen|Request Core  (millicore) |Request Ram (MB)|Limit Core(core) |Limit Ram (MB)|Pod|BlobStorage (GB)|
|-----------------|------------|------------------------------------|------------------|--------|----|----|----|----|----|----|----|
|   || |		|||||||||

### Backup risorse OpenShift (On Cloud)

<!-- ISTRUZIONE: Definire per ciascuna delle risorse elencate nel paragrafo precedente i parametri essenziali per garantire una strategia di backup efficace. Selezionare una delle opzioni operative: BASELINE BACKUP, POLICY CUSTOM, NO BACKUP. -->

*	BASELINE BACKUP
*	POLICY CUSTOM
*	NO BACKUP

### BASELINE BACKUP ###

**Baseline Backup OCP - PROD** 

| Ambiente      |Nome Cluster |Name Space|Gen|Tipologia Dato|Frequenza|Retention|
|-----------------|------------|------------------------------------|------------------|--------|----|----|
|   || |		||||


### POLICY CUSTOM ###

**Policy Custom**

| Ambiente      | Nome Cluster |Name Space|Gen|Tipologia Dato|Oggetto del Backup|Application Consistency|Frequenza|Retention|GB Frontend|Note|
|-----------------|------------|------------------------------------|------------------|--------|----|----|----|----|----|----|
|   || |		||||||||


### NO BACKUP ### 

**No Backup**

| Ambiente      | Nome Cluster |Namespace|Gen|Tiplogia Dato|Oggetto del Backup|
|-----------------|------------|------------------------------------|------------------|--------|-----|
|   || |		|||


### ALLEGATI


