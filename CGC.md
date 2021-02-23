CGC: **Cloud & Green Computing**
CdL Informatica, a.a. 2020/21
*prof. Antonio Brogi*

---

[toc]

---

# Introduzione

*Introdurre vari aspetti tecnologoci, sviluppo e operatività di microservizi e containers, caratteristiche di business models.*
*Introduzione alle conoscenze tecniche per l'uso del cloud.*
*Introduzione ai concetti di sostenibilità ambientale per la tecnologia informatica.*

Il guadagno con infrastrutture cloud nel Q2 2019 è pari a **$23 mld**, 
con Amazon 33%, Microsoft 16%, Google 8%.

Sostenibilità ICT: *green computing* vs *denaro*
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210217125634180.png" alt="image-20210217125634180" style="zoom:33%;" />

# Servizi

**Tutto come un servizio.**
L'economia è passato dai beni ai servizi. Ad esempio: dal comprare una bicicletta all'abbonamento *CicloPi*, oppure i servizi *Car as a Service*. 
Nel mondo dell'informatica vi è il passaggio dal giradischi/radio a *Spotify* oppure il mondo dei servizi di memorizzazione di terze parti (AWS3, DropBox) anche con modelli *freemium*.

**Contratto dei servizi**
I clienti non sanno e spesso non vogliono sapere come è implementato il servizio che usano. Prendendo un aereo non si vuol sapere la vita del pilota, quanti anni ha, quante ore ha dormito ecc.. ci fidiamo della compagnia basandoci sul *contratto*.
Un fornitore espone *un contratto* (o almeno dovrebbe farlo), e i clienti dovrebbero scegliere un servizio in base ad essi.
*Problema: i clienti leggono i contratti?*

*I soldi non sono tutto.* Nei servizi di storage vorremmo poter accedere ai nostri dati anche tra 10/20 anni o più, vorremmo privacy ecc... I soldi non sono tutto per poter effettuare una scelta.

## **Service Level Agreement (SLA)**
Viene scritto da 3 tipi di *mammiferi* diversi: 

- uomo di business (che definisce gli obiettivi dell'azienda)
- uomo giuridico (riempie di cavilli il contratto, col fine (si spera) di favorire il cliente)
- informatico (informa riguardo le *vere* caratteristiche del servizio)

Tutti i tipi di storage online offrono un'affibilità di almeno il 90%. 
Ma come è definita questa affidabilitá?

### **Amazon Web Services 3, AWS3**

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210217104106505.png" alt="image-20210217104106505" style="zoom: 67%;" />

Le cose scritte in maiuscolo in un contratto prevedono delle definizioni in genere.
![image-20210217104433175](/home/ludo/.config/Typora/typora-user-images/image-20210217104433175.png)

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210217104115417.png" alt="image-20210217104115417" style="zoom:50%;" />![image-20210217104412307](/home/ludo/.config/Typora/typora-user-images/image-20210217104412307.png)

*?Quanto “service credit” otterrete se il servizio non è disponibile per due giorni consecutive (per
esempio 1 e 2 Aprile)?*
La risposta non è immediata come potrebbe sembrare. Ciò dipende non soltanto dalla disponibilità del servizio ma anche dalle richieste effettuate dall'utente.
Ad esempio, provando ad accedere a AWS3 alle 9, alle 11, alle 13 e alle 15 di entrambi i giorni, ottenendo un errore “ServiceUnavailable” ogni volta allora avrei:

- *8 “five minute periods” con “Error Rate” = 100%*
- Rimanenti (12 x 24 x 30) – 8 “five minute periods” con “Error Rate” al 100% (12 viene da 60minuti/intervalliDi5minuti = 12 intervalli per ogni ora)
- *“monthly Uptime Percentage”* = 100% - (8/(12 x 24 x 30) x 100%) = **99,9**0740741%
- per avere uno sconto del 25% dovrei raggiungere una percentuale minore del 99% pertanto dovrei avere $\frac{x}{12\cdot24\cdot30}\cdot100 > 1 = x \cdot 0.011574 > 1 = x > 86.4$
  Quindi dovremmo effettuare almeno **87** richieste in intervalli di 5 minuti differenti in un mese con Errore rate al 100% 

### **Microsoft**
Ancora più esplicitamente ci fa notare il problema: 
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210217104818430.png" alt="image-20210217104818430" />

![image-20210217131531393](/home/ludo/.config/Typora/typora-user-images/image-20210217131531393.png)

![image-20210217131552155](/home/ludo/.config/Typora/typora-user-images/image-20210217131552155.png)

Tutte le applicazioni informatiche moderne sono basate sull'idea di partizionare i servizi per poter scalare al numero di richieste.

### Facebook

*?è vero che se pubblico un'immagine su fb non ne ho più i diritti?*
É scritto nel SLA di facebbok:
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210219113638567.png" alt="image-20210219113638567" style="zoom:67%;" />

Una volta pubblicata una foto si concede una licenza a facebook, che può dare quella foto ad un'agenzia pubblicitaria che stampa cartelloni pubblicitari con quella foto.

Anche nei *colloqui d'assunzione* le foto possono assumere importanza per le Human Resource delle aziende, che cercano di inquadrare i candidati.
Un tempo le domande erano del tipo *"quali libri salverebbe per l'umanità in futuro potendone scegliere solo 2?"*.

Sondaggio a lezione:

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210219114354039.png" alt="image-20210219114354039" style="zoom: 80%;" />



# Cloud Computing 101

La *richiesta* di un servizio varia nel tempo, nessuno sa come.

**Overpoisoning**
Partendo da pattern giornalieri, stagionali o picchi inattesi si cerca di soddisfare sempre i picchi attesi. Ciò porta a *sprecare* risorse (anche se la stima è corretta, peggio se la richiesta è sovrastimata).

**Underprovisioning**
Se la richiesta è sottostimata si possono *respingere* utenti. Probabilmente si perdono i clienti, oltre che le entrate perse delle richieste non servite.

Il cloud fornisce una qunatità di risorse apparentemente *infinite*. Ne fornisce all'utente una quantità maggiore di quante ne possa mai usare (e questo fornisce l'illusione che siano infinite). Le risorse sono disponibili *su richiesta*. 

**Definizione di Cloud del NIST** 
Il Cloud computing è un *modello* per permettere un accesso via rete diffuso, conveniente e su richiesta a un insieme condiviso di risorse di calcolo configurabili che possono essere rapidamente fornite e rilasciate con un minimo costo di gestione o di interazione col fornitore.

**Idee chiave**

- raggruppare in modo efficiente ed on-demand infrastrutture virtuali, offerte come *servizi*
- fornisce risorse *dinamicamente scalabili*, virtualizzate, a molti clienti tramite internet
- separare la fornitura di servizi di calcolo dalla tecnologia sottostante 

**Attrattiva economica**

- 
  Eliminazione di impegni *in anticipo* da parte degli utenti. Si possono realizzare ed offrire servizi interamente sul cloud. Si possono spostare le spese di capitale in spese di operazione (da *CapEx a OpEx*). 
- *Pay per use*: piace ai clienti, qualunque sia il servizio e qualunque sia il costo. Il costo è compensato dai benefici economici in termini di *elasticità* e 
- Trasferimento dei rischi. Se dovessimo fare noi il backup dei dati di un'azienda il rischio sarebbe nostro, appaltando il compito t*rasferiamo il rischio sul SLA del provider del servizio*.

**Modelli di servizio**
Vogliamo sviluppare un'applicazione e pubblicare il nostro servizio a quanti più utenti possibile.
Una metafora semplice per spiegare le differenze fra IaaS, PaaS e Saas è pensare a una Pizza as a Service. 
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210219121852841.png" alt="image-20210219121852841" style="zoom:67%;" />

**IaaS**: *Amazon EC2 (Elastic Cloude computing), S3(Storage)*, fornisce dei serivizi virtualizzati: server, memoria, rete. Il fornitore gestisce l'infrastruttura mentre il cliente è responsabile di tutti gli altri aspetti dello sviluppo (sistema operativo, applicazione).

**PaaS**: *Microsoft Azure, Heroku*, intero ambiente di sviluppo virtualizzato come un ambiente in rete. Gestisce non solo l'infrastruttura ma tiene su tutta la piattaforma. Infrastruttura + sistema operativo + enabling software. Il client è responsabile di installare e gestire l'applicazione.

**Saas:** *Salesforce.com*, fornisce software on-demand accedibile mediante API o thin client. Gestisce infrastruttura + sistema operativo + appliczione. Il cliente non è responsabile di nulla. 

 **Faas**: molto recente, serverless computing.

## Modelli di Deployment

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210219122626336.png" alt="image-20210219122626336" style="zoom:50%;" />

*?Cosa divido fra cloud pubblico e privato?* 
I dati sensibili preferisco averli nel cloud privato mentre dove ho bisogno di più elasticità cerco di usare il cloud pubblico.

## Ostacoli all'adozione del Cloud

- **Confidenzialità dei dati**: i dati dovrebbero essero visibili e comprensibili solo dai proprietari
  *?Dove verranno memorizzati concretamente i nostri dati concretamente*
  *?Come saranno garantite privacy e integrità dei dati?*
  *?Come sapremo se si verifica un problema?*
- **Disponibilità dei servizi** 
  *?Cosa succede se un cloud provider fallisce?*
  Mantra dell'informatica: *no single point of failure*
- **Vendor Lock-in**
  Rimanere bloccati in un servizio, si crea una dipendenza dal servizio di un'azienda

Nel caso del cloud non sono delle clausole nei contratti a bloccare al servizio, dato che essi si basano sul *pay-per-use*. 
Nella pratica, data la costosità di un'eventuale cambio di fornitore, vi è una dipendenza dal servizio.

La *costosità* deriva da uno degli aspetti a cui più bisogna prestare attenzione nei servizi cloud: alcune applicazioni non si possono passare *senza problemi* da un PaaS all'altro. 
Ci sono degli add-on che si possono usare su un PaaS ma che potrebbero essere proprietari.
Per potersi spostare allora diventa necessario cambiare plugin, il che vuol dire cambiare codice in fase di produzione e di conseguenza rivalidare e ritestare l'applicazione, cosa che si vuole sempre evitare. Oggi non si tiene in considerazione il *multicloud*, si assume che il cloud in uso ci assisterà sempre.

*Più l'API è di alto livello più si è allucchettati usandola.* 
<img src="https://i.pinimg.com/736x/7d/18/a2/7d18a2db086679c1c991cb7e871dabdc.jpg" alt="https://i.pinimg.com/736x/7d/18/a2/7d18a2db086679c1c991cb7e871dabdc.jpg" style="zoom:50%;" />
*Piccola nota su Windows:*

![image-20210219125631944](/home/ludo/.config/Typora/typora-user-images/image-20210219125631944.png)



## Iaas (Infrastructure as a Service)

## PaaS (Platform as a Service)


## SaaS (Software as a Service)

# Microservizi

## Lock-in e contromisure

## Container

*sfruttando la virtualizzazione*

# Business Models

# Cloud in Azienda

# Datacenters

# Green Computing

# Fog Computing

# Bibliografia consigliata

