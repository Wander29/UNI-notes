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

**Service Level Agreement (SLA)**
Viene scritto da 3 tipi di *mammiferi* diversi: 

- uomo di business (che definisce gli obiettivi dell'azienda)
- uomo giuridico (riempie di cavilli il contratto, col fine (si spera) di favorire il cliente)
- informatico (informa riguardo le *vere* caratteristiche del servizio)

Tutti i tipi di storage online offrono un'affibilità di almeno il 90%. 
Ma come è definita questa affidabilitá?

**Amazon Web Services 3, AWS3**

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

**SLA Microsoft**
Ancora più esplicitamente ci fa notare il problema: 
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210217104818430.png" alt="image-20210217104818430" />

![image-20210217131531393](/home/ludo/.config/Typora/typora-user-images/image-20210217131531393.png)

![image-20210217131552155](/home/ludo/.config/Typora/typora-user-images/image-20210217131552155.png)

Tutte le applicazioni informatiche moderne sono basate sull'idea di partizionare i servizi per poter scalare al numero di richieste.

## Iaas (Infrastructure as a Service)

## PaaS (Platform as a Service)


## FaaS (Function as a Service)

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

