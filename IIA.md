IIA: **Introduzione all'intelligenza artificiale**
CdL Informatica, a.a. 2020/21
*Prof. Alessio Micheli & Maria Simi*

---

[toc]

---

# Introduzione

*Lo scopo del corso è di far apprendere i concetti principali e i metodi che stanno alla base della progettazione e sviluppo di sistemi intelligenti.*
*Il corso introduce le tecniche di base per la realizzazione di agenti intelligenti e in particolare il paradigma di risoluzione dei problemi  come ricerca in uno spazio di stati, la rappresentazione della  conoscenza e il ragionamento automatico, i metodi e modelli di base  dell’apprendimento automatico.*

AI: nuovo strumento per l'uomo, affiancare la nostra intelligenza a quella artificiale.
Obiettivo dell'ia: fornire all'uomo strumenti potenti per ampliare la conoscenza.

L'IA si occupa di costruire entità intelligenti;si occupa di una doppia sfida: 

- comprensione  
- riproduzione 

del comportamento intelligente.

Due tipi di approcci:

- **Intelligenza artificiale forte**: assume che tutta l'intelligenza possa essere meccanizzata
  - analisi e comprensione di un fenomeno. psicologia cognitiva
    obiettivo: comprendere intelligenza umana
    metodo: costruzione di modelli computazionali, veririficati sperimentalmente
    criterio successo: risolvere i problemi con gli stessi processi dell'uomo
- **Intelligenza artificiale debole**: non tutta l'intelligenza può essere meccanizzata
  - costruttivo, riprodurre artefatti
    obiettivo: 
    metodo: costruire entità aventi razionalità
    criterio successo: risolvere il problema anche se diversamente dall'uomo

**Definizione di IA**
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210216162723512.png" alt="image-20210216162723512" style="zoom: 33%;" />

IA: indagine tecnologica ed intellettuale a lungo termine sia scientifica che pratica:

- costruzione di macchine intelligenti
- comprensione mediante modelli computazionali dei comportamenti e della psicologia di uomini, animali e agenti artificiali
- rendere il lavoro con il calcolatore altrettanto utile e facile che con persone collaborative ed esperte

Fondamenti dell'IA: *filosofia, matematica, economia, neuroscienze, psicologia, informatica, linguistica, cibernetica*

AI: *general purpose technology*, tipo elettricita, stampa, pc...

Prendiamo per buona la definizione di kurzweil, 1990:
*arte di creare macchine che svolgono funzioni che richiedono intelligenza quando svolte da esseri umani*

?*Cosa vuol dire intelligente?*
«qualità mentale che consiste nell'abilità di apprendere dall'esperienza e di adattarsi a nuove situazioni, comprendere e gesitre concetti astratti.»

Definizione di intelligenza, che piace a me:

> The role of intelligence is to determine the positive and negative potential of an event or factor which could have both positive and negative results. It is the role of intelligence, with the full awareness that is provided by education, to judge accordingly utilize the potential for one's own benefit or well-being.
>
> -Dalai Lama (*The heart of the Buddha's path*)

?È una qualità intrinseca o un comportamento? Che tipi di capacità?

*Test di Turing, 1950*

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210216163854696.png" alt="image-20210216163854696" style="zoom:33%;" />

Dopo 5 minuti di dialogo il test è concluso e l'interrogato dovrà dire se sta comunicando con un computer o con una persona.
Nel 2014 il 30% dei giudici è stato ingannato in un esperimento.

Le capacità auspicabili sono:

- simulare il comportamento umano 
- ragionamento logico/matematico
- buon senso
- expertise
- skills sociali, comunicazione
- emozioni, creatività...
- immaginazione, esperienza

## Breve storia

1943: primo lavoro sulle reti neurali

1956: logic theorist
Capacità di ragionamento simbolico. Algebra simbolica e trasposizione in logica
Newell, Simon

1956-1969 grandi aspettative
Advice Taker, programma basato su conoscenza ed estensibile
Vari successi nei problemi giocattolo

1966-1974: dose di realismo
La manipolazione simbolica e sintattica non è adeguata per tutti gli usi.
Complessità di problemi troppo alta, intrattabili; tutti di complessità esponenziale.
Limiti di rappresentazione delle reti neurali di tipo semplice
Rapporto Lighthill in UK: non vale più la pena investirvi

1969-1979: knowledge, specializzazione
Dominiamo complessità con conoscenza specifica del domini ed euristiche
Il collo di bottiglia è l'acquisizione di conoscenza.
Il problema è la mancanza di *buon senso*. Difficoltà di codificare il senso comune.

*? Cos'è il senso comune?*
Abilitá mentale che la maggior parte delle persone condividono. Coinvolge molte tipologie di rappresentazione e richiede un insieme più ampio di abilità.
Varie tipologie di rappresentazione	

progetto CYC(Lenat), codificare tutto lo scibile umano.
OpenMind: progetto più recente e meno ambizioso che accetta contribti via web. Fatti di senso comune via web.
Grafi di conoscenza: estrarre conoscenza da big data (google graph..)

1995-ora: *agenti*, visione moderna (AIMA: AI a Modern Approach)
Punto di svolta, agenti intelligenti che uniscono vari settori dell'IA.
La visione moderna dell'IA è il fronte del progresso dei metodi/sistemi informatici (algoritmica, logica, ottimizzazione) per dotare le macchine di comportamente *razionali* (intelligenti) in problemi generali *difficili*.
L'accento è quindi posto sulla costruzione di agenti intelligenti.

1997: DeepBlue, Kasparov
supercomputer IBM vince a scacchi contro il campione mondiale, ma la realtà è che non serve vera *intelligenza* per giocare a scacchi.

## Agenti


Gli agenti sono situati, immersi in un ambiente. Ricevono percezioni da un ambiente. Agiscono sull'ambiente mediante *attuatori*. Possono avere *abilità sociali* (sanno comunicare). Hanno un corpo. Hanno opionioni, credenze, obiettivi, forse ...mhmhmhm.. "hanno emozioni..."

Robocup: problema attuale fino al 2050 come banco di prova
calcio simulato: agenti individuali, senza una mente centralizzata

Capacità di emozioni: sono importanti nella capacità di prendere decisioni, quantomeno nell'uomo (io parlerei più di omeostasi).

*Narrow AI vs General AI*
magazzini intelligenti, aspirapolveri intelligenti, guida automatica, sistemi di raccomandazione

*AI revolution?* 
IBM Watson, Project Debater.
L'IBM la chiama una grande sfida. 
BlueGene: genoma

*?L'intelligenza può essere estratta o inferita dai dati?*
Più dati maggiore l'accuratezza.. unreasonable effectiveness of big data

Reti neurali: solo dal 2011 si sono avuti successi evidenti. 
Cos'è successo? applicabile dal punto di vista computazionale, GPU efficienti...

DeepMind (società di Google), è in grado di imparare GO, anche da zero nel 2017 giocando da solo con tecniche di *reinforcement learning*.

AI: sorgenti di incertezza, sensori imperfetti. é la disciplina che si usa quando non sai cosa fare, quando l'approccio algoritmico tradizionale non è sufficiente.
*Gervasi: se non ci sorprende non è A.I.*

Machine Learning: come dotare sistemi di apprendimento automatico.
Learning is the core of intelligence, sia in biologia che in informatica

Si dovrebbe dire un sistema di AI, non una AI.
É difficile programmare l'intelligenza. 
DL e reti neurali sono sottocategorie di ML, che a sua volta è una sottocategoria dell'AI.

## Agenti intelligenti

> Cap. 2 AIMA

L'approccio moderno all'IA riguarda la costruzione di *agenti intelligenti*.
La visione a sistemi è comoda per trattare *sitemi razionali*. La visione ad agenti è diversa dalla visione offerta dai sistemi software.

**Primo obiettivo: agenti per risoluzione di problemi vista come ricerca in uno spazio di stati** 

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210219141638740.png" alt="image-20210219141638740" style="zoom: 50%;" />

Il nostro focus è nel punto interrogativo. Ci interessa costruire il programma dell'agente, cosa fargli fare. Vogliamo che interagisca nel modo giusto con l'ambiente.

**Caratteristiche degli agenti**
Vanno oltre uno standard modulo software poichè gli agenti: 

- sono *situati*: ricevono percezioni da un ambiente e agiscono su esso mediante azioni attuate dagli attuatori
- hanno *abilità sociale*: sono in grado di comunicare e collaborare
- hanno *credenze, obiettivi, intezioni*
- sono *embodied*: hanno un corpo

**Percezioni e azioni**
Le *percezioni* sono input da sensori.
Una *sequenza percettiva* è la storia completa delle percezioni.
La *scelta* dell'azione è funzione unicamente della sequenza percettiva.
La *funzione agente* definisce l'azione da compiere per ogni sequenza percettiva, in altre parole descrive completamente l'agente. Essa è implementata da un programma agente.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210219141858644.png" alt="image-20210219141858644" style="zoom:33%;" />

Si possono avere varie forme della funzione, implementate dal programma agente. Il nostro compito è progettare la sequenza dell'agente, date le percezioni in input.

**Agenti razionali**
Un *agente razionale* fa la cosa giusta secondo una certa misura. Interagisce con il suo ambiente in maniera efficace. É necessario quindi un *criterio di valutazione* oggettivo dell'effetto delle azioni dell'agente, una misura della prestazione (ad es: il costo di un cammino minimo trovato). 

La razionalità è relativa e dipende dalla misura delle prestazioni, dalle conoscenze pregresse dell'ambiente, dalle percezioni presenti e passate e dalle azioni possibili per l'agente.
Una definizione più dettagliata di un *agente razionale* è pertanto la seguente:

> Per ogni sequenza di percezioni un *agente razionale* compie l'azione che massimizza il valore atteso della misura delle prestazioni considerando le sue percezioni presenti, passate e la conoscenza pregressa

La razionalità non è né *onniscenza* né onnipotenza. Raramente tutta la conoscenza dell'ambiente può essere fornita a priori. Un agente razionale deve essere in grado di modificare il proprio comportamento con l'esperienza, migliorando tramite esplorazione e *apprendimento*.

**Agente autonomo**: un agente lo è nella misura in cui il suo comportamento dipende dalla sua esperienza. 
Un agente il cui comportamento è determinato solo dalla sua conoscenza iniziale (*built-in*) non è autonomo, in quanto molto poco flessibile.

(https://www.repubblica.it/scienze/2013/01/28/news/mangia_letame_ma_in_realt_un_astronomo_lo_stercorario_si_muove_seguendo_le_stelle-51341644/).

## **Ambiente**
Descrizione *PEAS* dell'ambiente: Performance, Environment, Actuators, Sensors
Esempio: un agente *guidatore di taxi*:

| Prestazione   | Arrivare alla destinazione in modo sicuro e veloce rispettando ala legge e ottimizzando i consumi |
| ------------- | ------------------------------------------------------------ |
| **Ambiente**  | Clienti e strada con altri veicoli e pedoni                  |
| **Attuatori** | Sterzo, acceleratore, freni, sintesi vocale o interfaccia non vocale |
| **Sensori**   | Telecamere, sensori, tachimetro, GPS, contachilometri, tastiera/microfono/touchscreen |

## Proprietà dell'ambiente

**Osservabilità**
Un ambiente può essere *completamente osservabile* quando siamo in grado di percepire tutto ciò che serve o di avere una conoscenza completa dell'ambiente, senza mantenere lo stato del mondo. Un esempio di ambiente completamente osservabile è una scacchiera.
Un ambiente è *parzialmente osservabile* quando nell'apparato sensoriale dell'agente vi sono limiti o inaccuratezze che non permettono la totale conoscenza dell'ambiente esterno.


**Ambiente singolo/multiagente**
Il mondo può cambiare anche per eventi (es. pandemia), non necessariamente per azioni di agenti.
Un ambiente *multi-agente* può essere competitivo (es. scacchi) o cooperativo dove gli agenti condividono un obiettivo e comunicano fra loro.

**Predicibilità**
Un ambiente è *deterministico* se lo stato successivo è <u>completamente</u> determinato dallo stato corrente e dall'azione.
Un ambiente si dice invece *stocastico* quando esistono elementi di incertezza cui è associata una certa probabilità (es. guida, tiro in porta).
Un ambiente è *non deterministico* quando come risultato di un azione vi sono più stati possibili in cui ci si può trovare (senza avere probabilità associate).

**Episodicità**
Un ambiente è *episodico* se l'esperienza dell'agente è divisa in episodi atomici indipendenti fra loro. In questi ambienti non vi è bisogno di pianificare.
Un ambiente è *sequenziale* se ogni azione influenza le successive.

**Staticità**
Un ambiente è *statico* se il mondo non cambia mentre l'agente decide l'azione.
Un ambiente si dice *dinamico* se cambia nel tempo, pertanto in ogni momento va riosservato per decidere; tardare equivale a non agire.
Un ambiente è *semi-dinamico* se non cambia nel tempo ma con lo scorrere dello stesso cambia la valutazione dello stesso (es. scacchi con un timer, Alan Turing style; allo scadere del timer l'agente sa che cambia qualcosa semanticamente ma l'ambiente rimane lo stesso).

**Dati**
Lo stato, il tempo, le percezioni e le azioni possono assumere valori *discreti* o *continui*.
Il discreto porta a problemi combinatoriali mentre il continuo porta a esplorare un ambiente infinito.
Non sempre il discreto è più semplice da risolvere (es. problema dello zaino).

**Noto/ignoto**
Lo stato di conoscenza dell'ambiente intorno all'agente; questo conosce ciò che deve sapere o deve compiere azioni esplorative?
Le regole sono note, ma l'ambiente può non esserlo (es. carte coperte, non so cosa si celi in esse). Noto è diverso da osservabile. 

*Gli ambienti reali sono:* 
stocastici, ignoti, parzialmente osservabili, multi-agente, dinamici, continui e sequenziali.
Inizieremo con le assunzioni più semplici (cioè ambienti deterministici, statico, discreto, mono-agente).

**Simulatori di ambienti**
Sono strumenti software che generano stimoli per gli agenti, raccogliendo risposte e aggiornando lo stato dell'ambiente. Inoltre valutano le prestazioni dell'agente.
Risulta fondamentale valutare le prestazioni su classi di ambienti differenti, per valutare poi la prestazione generale.

## Struttura di un agente

Un agente ha un'architettura più un programma.
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210219144247432.png" alt="image-20210219144247432" style="zoom: 33%;" />

**Agenti basati su tabella**
L'agente potrebbe essere anche una tabella, dove a uno stimolo associa un'azione a ogni possibile sequenza di percezioni.
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210219144440330.png" alt="image-20210219144440330" style="zoom:50%;" />

In IA vogliamo realizzare agenti razionali dotati di un programma *compatto*.

**Agenti reattivi**
Non c'è una storia da memorizzare. Semplicemente volta per volta procedo ad agire.
L'algoritmo restituisce un'azione poichè è il programma dell'agente, che ritorna agli attuatori.

|                                                              |                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| <img src="/home/ludo/.config/Typora/typora-user-images/image-20210320191336878.png" alt="image-20210320191336878" style="zoom: 33%;" /> | <img src="/home/ludo/.config/Typora/typora-user-images/image-20210320191319949.png" alt="image-20210320191319949" style="zoom:33%;" /> |

**Agenti basati su un modello**
La regola viene estratta in base allo stato, che si aggiorna col tempo

|                                                              |                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| <img src="/home/ludo/.config/Typora/typora-user-images/image-20210320191455211.png" alt="image-20210320191455211" style="zoom:33%;" /> | <img src="/home/ludo/.config/Typora/typora-user-images/image-20210320191503255.png" alt="image-20210320191503255" style="zoom:33%;" /> |

**Agenti con obiettivo**
Aumenta la complessità, vogliamo aggiungere flessibilità. 
Mentre prima l'obiettivo era fissato dal programmatore (ovvero in modo abbastanza rigido) sarebbe comodo specificarlo a seconda del caso. Si vuole pianificare una sequenza di azioni per raggiungere il goal
es. un cammino per raggiungere una certa destinazione

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320191641117.png" alt="image-20210320191641117" style="zoom:33%;" />

**Agenti con valutazione di attività**
Oltre all'obiettivo hanno anche una funzione di utilità. Permette di scegliere il miglior obiettivo da raggiungere, non tutti lo hanno lo stesso livello, potrebbero essere anche in conflitto.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320191812529.png" alt="image-20210320191812529" style="zoom:33%;" />

**Agenti che apprendono**
L'architettura si semplifica grazie all'apprendimento, ha la capacità di adattarsi in manierza semi-automatica a quello che succede.
La permanenza dell'agente nell'ambiente gli fornisce nuovi feedback.
Il programma non è fissato ma può mutare in base all'esperienza che viene accumulata.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320191849956.png" alt="image-20210320191849956" style="zoom:33%;" />

**Tipi di rappresentazione dello stato**
Rappresentazione

- atomico: indivisibile, navigare in una mappa da una città all'altra

- *fattorizzata* : distanza fra stati, dare delle metriche, anche nel ML, dove le informazioni sono codificate in vettori di feature
- *strutturata*: la più sofisticata, rappresentiamo oggetti e relazioni fra questi oggetti, basati sulla logica (stiamo aggiungendo esplicitamente le relazioni)

*Conclusioni*

- IA come progettazione di agenti e programmi agente

- Massima misura di prestazioni
- classificazione dei problemi PEAS
- dipendenza dalla lettura dell'ambiente 
- tutti gli aspetti possono migliorarsi con l'apprendimento.

# Agenti risolutori di problemi

Adottano il paradigma della risoluzione dei problemi come ricerca in uno spazio di stati. 
Sono agenti 

- con modello
- con obiettivo
- rappresentazione atomica dello stato

In questo capitolo si considera un particolare tipo di agente *con obiettivo*, l'agente *problem-solving*. Essi pianificano in anticipo una sequenza di azioni che portano ad uno stato obiettivo. Il processo computazionale sottostante è chiamato *ricerca*.
Usa rappresentazioni **atomiche**, stati del mondo considerati come un'unità.

- formula il problema (parte non automatica)
- ricerca la soluzione nello spazio degli stati (automatico)

Immaginiamo che verrà eseguito l'intero piano: 

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320203334771.png" alt="image-20210320203334771" style="zoom: 50%;" />

*Assunzioni sull'ambiente*:

- statico, 
- osservabile, so dove sono,
- discreto, 
- determinisitico, l'agente può eseguire il piano ad occhi chiusi.

Formulazione in 5 componenti:

- stato iniziale
- azioni possibili in esso
- modello di transizione (coppia <stato, azione> -> stato')

1,2,3 definiscono implicitamente lo *spazio degli stati*.

- test obiettivo
- costo del cammino,
  - non è mai negativo il costo di un azione

**Ricerca**: il processo che cerca una sequenza di azioni che raggiunge l'obiettivo

**misura prestazioni**: quanto costa trovare la soluzione, somma di 2 costi: 

- costo della ricerca stessa (valutazione dell'algoritmo)  
- costo del cammino soluzione

## Formulazione di problemi
Conoscenza implicita dell'ambiente: conosco solamente le azioni possibili nell'ambiente.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320203704689.png" alt="image-20210320203704689" style="zoom:33%;" />

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210219153132017.png" alt="image-20210219153132017" style="zoom:33%;" />

Le formulazioni possono avere costi diversi

- formulazione incrementale(una regina in una qualsiasi casella): 178.000 miliardi di stati
- formulazione incrementale 2(una regina per colonna): 2057 sequenze da considerare
  es. 3.6 dell'AIMA, radice cubica di n!
  ogni volta che aggiungete una regina 
- formulazione a stato completo: metto tutte le regine sulla scacchiera, una per colonna. Azione: sposta la regina se minacciata

**Dimostrazione di teoremi**
È una ricerca nello spazio degli stati; albero di ricerca fra gli stati

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320204303880.png" alt="image-20210320204303880" style="zoom: 33%;" />

## Risoluzione di problemi come ricerca

**Informed algorithms, uninformed algorithms**
Distinguiamo fra gli algoritmi con informazioni, dove l'agente può stimare la distanza dell'obiettivo, da quelli senza informazioni, dove questa stima non è disponibile.

La *ricerca* per un agente avviene prima di ogni azione da effettuare nel mondo reale. Esso deve simulare le sequenze di azione nel modello, cercando finché non trova una sequenza di azioni che raggiunge l'obettivo, ovvero la *soluzione*.
L'esecuzione è il processo per cui l'agente esegue le azioni della soluzione trovata, una alla volta.

**Open loop, closed loop**
*Open loop: ignora percezioni durante esecuzione*
*Closed loop: continua a monitorare percezioni* 

Quando un agente si trova in un ambiente completamente osservabile, deterministico e conosciuto la soluzione è un sequenza fissata di azioni. 
Durante l'esecuzione della soluzione l'agente *ignora* le percezioni rompendo il ciclo fra agente ed ambiente. Questo perchè la soluzione è garantita condurre all'obiettivo e niente può cambiare, l'agente *chiude gli occhi*.

Se vi è anche qualche possibilità che il modello sia incorretto o l'ambiente è non deterministico allora è più sicuro usare una modalità *closed-loop* dove le percezioni continuano ad essere monitorate.

La nostra formulazione dei problemi è un *modello*, una descrizione matematica astratta della realtà. Il processo di rimuovere dettagli da una rappresentazioni è chiamato *astrazione*.
L'astrazione è valida se possiamo elaborare ogni soluzione astratta in una soluzione nel mondo reale. L'astrazione è utile se rimuovendo i dettagli il problema risulta più semplice.

**Problems**
*problemi standardizzati*: hanno lo scopo di illustrare vari metodi di problem-solving e di essere un benchmark. 

*real-world problems*: le cui soluzioni sono effettivamente usate dall'uomo, la cui formulazione non è idiosincratica (*che influenza una particolare variabile e nessun’altra*), non standardizzata, poichè ogni robot e ogni ambiente differisce.

| standardized problems              | real-world problems           |
| ---------------------------------- | ----------------------------- |
| grid world(vacuum, sokoban puzzle) | route-finding                 |
| sliding-tile puzzle                | touring                       |
| 8-puzzle, 15-puzzle                | VLSI layout                   |
| Knuth 4                            | Robot navigation              |
|                                    | automatic assembly sequencing |
|                                    | protein design                |

*Knuth 4*: Knuth congettura che partendo dal numero 4, con una sequenza di radici quadrate, floor e fattoriali si può raggiungere ogni intero positivo desiderato, es: raggiungere 5 partendo da 4: 

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226130509906.png" alt="image-20210226130509906" style="zoom: 50%;" />

## Algoritmi di ricerca

Un algortimo di ricerca prende in input un problema di ricerca e restituisce una soluzione o un fallimento. Consideriamo algoritmi che sovrappongono un albero di ricerca su un grafo dello spazio degli stati. Ogni nodo dell'albero di ricerca corrisponde a uno stato nello spazio degli stati.

**Dati e definizioni**

*spazio degli stati*: insieme dei possibili stati in cui l'ambiente può trovarsi

*stato iniziale*: stato dove si trova inizialmente l'agente

*stati obiettivo*: a volte è unico, a volte un piccol set di alternative, a volte è definito da una proprietà che si applica a molti stati (anche un numero infinito). Per un aspirapolvere l'obiettivo è non avere sporco in ogni locazione.

```pseudocode
struct node {
	stato
	padre
	azione 	% che lo ha generato
	costo 	% del cammino dal nodo iniziale al nodo, == padre.costo + costo_ultimo_passo
}
frontiera = coda %lista dei nodi in attesa di essere espansi
```

*Oss: differenza fra nodi e stati*
Esistono nodi dell'albero di ricerca con lo stesso stato.
Lo spazio degli stati descrive i possibilmente infiniti insiemi di stati del mondo e le azioni che permettono transizioni da uno stato all'altro.
Nell'albero di ricerca un determinato stato (es. città di Oradea) può avere percorsi multipli per arrivarvi (e di conseguenza mutipli nodi che descrivono lo stesso stato), ma ogni nodo nell'albero ha un unico percorso che lo collega alla radice.

*espandere un nodo:* considerare tutte le azioni disponibili per quello stato (ad ogni nodo corrispone uno stato), ottenendo i risultati che queste azioni forniscono e generando nodi per ogni risultato

*generare un nodo figlio*: assegnare i valori di stato, padre, costo e azione generatrice.

*frontiera:* lista dei nodi in attesa di essere espansi (foglie dell'albero di ricerca); raggiunti ma non espansi. Essa è implementata come una coda con operazioni.

*reached table:* ogni stato che ha un nodo generato per esso se è stato raggiunto, e quindi viene aggiunto alla tabella

*soluzione:* una sequenza di azioni forma un percorso, e una solzuione è un percorso dallo stato iniziale allo stato obiettivo. Una soluzione ottimale ha il più basso costo tra tutte le soluzioni.

Un nodo rimane foglia (rimane nella *frontiera*) fintanto che non si decide di espanderlo. 

**Ridondanza**
*repeated state*: anche se lo spazio degli stati è finito è possibile che stati si ripetano

*percorso ridondante*: un ciclo è solo un caso particolare di percorso ridondante. Ogni modo peggiore di raggiungere uno stato rispetto ad uno ottimo. 

> Gli algoritmi che non ricordano il passato sono destinati a ripeterlo

*vari approcci*, in ordine crescente di efficacia e costo:

- In problemi in cui è impossibile o molto raro che due percorsi raggiungano lo stesso stato possiamo ignorare il problema (es. problemi di assemblaggio)

- *Non tornare nello stato da cui si proviene*: si elimina il genitore dai nodi successori (non evita però tutti i cammini ridondanti)

- *Non creare cammini con cicli*: si possono controllare i cicli evitando di controllare i percorsi ridondanti. Si possono controllare risalendo nella catena dei *parent* di ogni nodo; per efficienza si può scegliere di controllare solo i cicli brevi (3 generazioni sopra) e affidarsi ad altri meccanismi (come dei vincoli) per i cicli maggiori.
- Non *generare nodi con stati già visitati/esplorati*: O(s) dove s è il numero degli stati possibili: quando la tabella degli stati raggiunti entra in memoria e ci sono molti percorsi ridondanti la scelta preferita è ricordare tutti gli stati precedentemente raggiunti 

Diversi tipi di code corrispondono a diversi tipi di strategie di ricerca

- FIFO -> BF (Breadth First)
- LIFO -> DF (Depth First)
- Coda con priorità -> UC e altri successivi, dopo l'inserimento c'è un riordinamento; viene estratto il nodo a priorità più alta

**Cammini ciclici**
*I cammini ciclici rendono gli alberi di ricerca infiniti.*

Il problema della ridondanza si presenta anche in assenza di cicli. 
Su spazi di stati a grafo (abbastanza strani) si generano più volte gli stessi nodi nella ricerca.

*Visitare stati già visitati fa sprecare tempo e/o occupa spazio*. Ricordare gli stati già visitati occupa spazio ma ci consente di evitare di visitarli di nuovo.

Ricerca su grafo: mantiene una lista degli stati  visitati/esplorati (*lista chiusa*)

*<u>graph search</u>:* se l'algoritmo di ricerca controlla per percorsi ridondanti, mantiene una lista degli stati esplorati. Prima di visitare un nodo controlla se lo stato corrispondente era già stato incontrato o è in frontiera.

*<u>tree-like search</u>:* se l'algoritmo di ricerca non fa questo controllo, scegliamo di vedere i nodi come in un albero accettando le ripetizioni degli stati (non escludendo il padre dai successori, negli algoritmi qui presentati).

Oss: nella ricerca ad albero i successori (padre) vengono rigenerati!

La *frontiera* separa i nodi *esplorati* da quelli *non esplorati*. Ogni cammino dallo stato iniziale a inesplorati deve attraversare uno stato di frontiera.

### Best First Search

È un approccio molto generale, dove si sceglie dalla frontiera un nodo *n* con un valore minimo della funzione di valutazione f.

```pseudocode
function BEST_FIRST_SEARCH_graph(problem, f) return solution || failure
	node = Node(state = problem.initial)
	frontier = a priority queue ordered by f
	frontier.add(node)
	
	explored = a lookup table <stato, nodo>
	explored.put(problem.initial, node)
	
	while(!frontier.isEmpty)
	  node = frontier.pop()
      // controllo del goal posticipato
      if(problem.isGoal(node.state))
        return node
      		
       explored.add(node.state)
        foreach child in EXPAND(problem, node):
            if (child.state NOT IN explored and child NOT IN frontier:
                frontier.append(child)
            else if (child IN frontier)
                if f(child) < frontier[child]:
                    del frontier[child]
                    frontier.append(child)
    
    return failure
```

```pseudocode
function EXPAND(problem, node) return a list of nodes
    s = node.state
    node_list = empty list

    foreach action in problem.ACTIONS(s)
        s1 = problem.RESULT(s, action)
        cost = node.PATH_COST + problem.ACTION_COST(s, action, s1)
        node_list.add(NODE(state = s1, parent = node, action = action, path_cost = cost))

    return node_list
```

## Ricerca non informata

Non si hanno inforazioni sulla distanza stimata dall'obiettivo.

- Ricerca in ampiezza (BF)
- Ricerca in profondità (DF)
- Ricerca in profondità limitata (DL)
- Ricerca con approfondimento iterativo (ID)
- Ricerca di costo uniforme (UC)

Per valutarle terremo conto di:

- *completezza*: se esiste una soluzione, la trova sempre;
  per soluzione si può intendere anche *fallimento* (anche se il goal è precluso, magari da muri)
- *ottimalità*: trova la soluzione migliore, con costo minore
- complessità in *tempo*
- complessità in *spazio*

**Variabili per analisi**
**b** = fattore di ramificazione, *branching* (numero max di successori)
**d** = profondità del nodo obiettivo più superficiale (la prima che troviamo va bene)
**m** = lunghezza massima dei cammini in ogni percorso (nel caso dovessimo andare lunghi)

### Ricerca in ampiezza (BF)

Quando tutte le azioni hanno lo stesso costo è sensato usare la Breadth First Search. 
È una ricerca completa anche in uno spazio degli stati infinito.
Esplora il grafo dello spazio degli stati a livelli progressivi di stessa profondità, partendo dalla radice, poi tutti i successori della radice ecc...

*Oss:* una volta che incontriamo uno stato sappiamo che non potremo trovare un percorso migliore, quindi possiamo usare un *set* per salvare gli stati raggiunti (ricerca su grafo).
Di conseguenza possiamo anche effettuare un *early-test* dell'obiettivo.

```pseudocode
function BREADTH_FIRST_SEARCH_graph(problem) return solution || failure
	
	node = NODE(problema.initial) // costo = 0
	// controlla se il nodo è obiettivo
	if(problema.isGoal(node.state)) 
		return node
	
	frontier = FIFOQueue()
	frontier.push(nodo)
	explored = a set
	explored.add(problem.initial)
	
	while(!frontier.isEmpty())
		node = frontier.pop()
		explored.add(node.state)
		
		foreach child in EXPAND(problem, node)
			// per ogni azione disponibile a partire dal nodo esplora i figli
			s = child.state
			
			if(s NOT IN explored && child NOT IN frontier)
				if(problem.isGoal(s))
					return child
					
				frontier.push(child)
    
    return failure
```

Una volta generati i nodi sono *goal-tested*, per ragioni di efficienza. Più avanti vedremo algoritmi che per necessità non lo fanno.
Non partiamo conoscendo gli stati, quindi non ci segniamo lo stato *esplorato* nelle informazioni dei nodi.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226185250923.png" alt="image-20210226185250923" style="zoom: 50%;" />

**Analisi**

| completezza | tempo    | spazio   | ottimalità                                   |
| ----------- | -------- | -------- | -------------------------------------------- |
| sì          | $O(b^d)$ | $O(b^d)$ | sì, se le azioni hanno tutte lo stesso costo |

Trova una soluzione col minimo numero di azioni, perchè quando scende al livello di profondità *d* ha già controllato tutti i nodi al livello *d-1*. Se le azioni hanno tutte lo stesso costo allora è ottimo.

Il numero dei nodi cresce esponenzialmente.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210223163857970.png" alt="image-20210223163857970" style="zoom: 25%;" />

La memoria è il fatto più incisivo, ingestibile.

### Ricerca in profondità (DF)

Esplora sempre i nodi più profondi in frontiera. La ricerca poi torna sui suoi passi al nodo successivo più profondo che ha ancora successori non espansi.
È spesso implementata come una ricera ad albero dove non si tiene conto degli stati esplorati. Non è ottima, ritorna la prima soluzione che trova.

Viene utilizzata una coda LIFO, mettendo i successori in testa alla lista.
*Oss*: possiamo dimenticare rami completamente esplorati. 

**visita a grafo**
Si perdono i vantaggi della memoria, si torna a salvare in memoria tutti i possibili stati al caso pessimo. Diventa però una ricerca completa su uno spazio degli stati finito.

**versione ricorsiva**
Realizzato da un algortimo ricorsivo con *backtracking*. È ancora più efficiente in occupazione di memoria, mantiene solo il cammino corrente. Salva lo stato su uno stack a cui torna in caso di fallimento per fare altri tentativi.

```pseudocode
function depth_first_sarch_tree(problem) return solution || failure
	node = problem.initial
	
	frontier = LIFOQueue([node])
	
	while(!frontier.isEmpty())
		node = frontier.pop()
		
		if(problem.isGoal(node))
			return node
			
        foreach child in EXPAND(problem, node)
        	frontier.push(child)
        	
----------------------------------------------------------------------------

function depth_first_search_recursive(problem) return solution || failure
	return solution = rec_depth_first_search(problem, problem.initial)

function rec_depth_first_search_tree(problem, node) return solution || failure
	if(problem.isGoal(node))
			return node
            
	foreach child in EXPAND(problem, node)
        sol = rec_depth_first_search(problem, node)
        if(sol != failure) return sol
        
    return failure
```

*Oss:* l'algoritmo ha un ordinamento di esplorazione dei nodi a pari profondità differente tra ricorsivo e non ricorsivo.

**Analisi**

| versione                | completo                             | ottimo | tempo    | spazio        |
| ----------------------- | ------------------------------------ | ------ | -------- | ------------- |
| <u>albero</u>           | no, solo per spazi finiti e aciclici | no     | $O(b^m)$ | $O(b\cdot m)$ |
| <u>albero ricorsiva</u> | no, ""                               | no     | ""       | $O(m)$        |
| <u>grafo</u>            | no, solo per spazi finiti            | no     | ""       | $O(b^m)$      |

(*m = lunghezza massima del cammino nello spazio degli stati*)
L'algoritmo è completo solo per spazi degli stati finiti. 
In spazi finiti aciclici la ricerca termina, mentre per spazi con cicli nella versione ad albero si può rimanere bloccati in un loop. Per questa ragione alcune implementazioni controllano la presenza di cicli per ogni nuovo nodo.
In spazi infiniti invece si può rimanere incarcerati nel seguire un percorso in profondità infinito. 

La complessità in tempo $O(b^m)$ può essere maggiore di $O(b^d)$.

Il guadagno lo si ha in memoria, nella versione ad albero, non teniamo la lista esplorati e la frontiera è tendenzialmente molto piccola.
	<img src="/home/ludo/.config/Typora/typora-user-images/image-20210227162446823.png" alt="image-20210227162446823" style="zoom:33%;" />

Per questa ragione il DF è adottato in problemi come la soddisfacibilità di vincoli, proposizioni e prorgammazione logica.

### Ricerca in profondità limitata (DL)

Per evitare che la *depth first search* si ingabbi in un percorso di infinità profondità usiamo una versione in cui si va in profondità fino ad un certo livello predefinito *l*. 
È una ricerca *completa* per problemi in cui si conosce un limite superiore per la profondità della soluzione, ovvero se *d<l*; non è ottimale ma completo (in quei casi). 
Si considerano tutti i nodi a profondità *l* come foglie, non si considerano i loro eventuali successori.

```pseudocode
function depth_limited_search_tree(problem, l) return solution || failure || cutoff
	node = problem.initial
	frontier = LIFOQueue([node])
	result = failure
	
	while(!frontier.isEmpty())
		node = frontier.pop()
		
		if(problem.isGoal(node.state))
			return node
			
        if(node.depth > l)
        	result = cutoff
        else if(!isCycle(node))
        	foreach child in EXPAND(problem, node)
        		frontier.push(node)
   	
   	return result // failure se i nodi vengono esauriti (quindi non per colpa del limite l)
	
```

È sempre una ricerca ad albero che controlla gli stati esplorati, per cui consuma poca memoria. Porta con sé il rischio di visitare lo stesso stato più volte su differenti percorsi. Se la funzione *isCycle(node)* non controlla la presenza di *tutti* i cicli l'algoritmo potrebbe bloccarsi in un loop.

I cicli corti sono bloccati dalla funzione *isCycle*, verosimilmente risalendo di qualche livello la catena di parentela del nodo, i cicli più lunghi dovrebbero essere gestiti dal limite *l*.

**Analisi**

| completezza       | ottimalità | tempo    | spazio         |
| ----------------- | ---------- | -------- | -------------- |
| no, solo se *d<l* | no         | $O(b^l)$ | $O(b \cdot l)$ |



### Approfondimento iterativo (ID)

È il miglior compromesso fra BF e DF. *Iterative deepening* è il metodo di ricerca non informata preferito quando lo spazio degli stati è più grande della memoria e la profondità della soluzione non è nota.

Risolve il problema di scegliere un buon valore per *l* provando successivamente tutti i valori.

```pseudocode
function iterative_deepening_search(problem) return solution || failure
	for depth = 0 to +inf
		result = depth_limited_search(problem, depth)
		if(result != cutoff)
			return result
```

**Analisi**

| completezza | ottimalità                                   | tempo    | spazio         |
| ----------- | -------------------------------------------- | -------- | -------------- |
| sì*         | si, se le azioni hanno tutte lo stesso costo | $O(b^d)$ | $O(b \cdot d)$ |

*a patto che venga controllata la presenza di cicli fino alla radice. 

È ottimo se le azioni hanno tutte lo stesso costo. 

Come *breadth first* genera un livello per volta, la differenza è che *breadth first* salva in memoria i livelli, ID ripete i precedenti livelli in esecuzioni successive della *depth limited*. Al costo di più tempo salva memoria.

Potrebbe sembrare uno spreco di computazione che i primi livelli (specialmente) vengano rigenerati più volte, nella pratica la maggior parte dei nodi si trovano nei livelli più bassi.
I nodi al livello *d* sono generati 1 volta, quelli a (*d-1*) 2 volte, ...
Il numero dei nodi è pertanto dato da: $d(b) + (d-1)\cdot b^{2} + (d-2)\cdot b^3 ...  + b^d$ che asintoticamente è sempre $O(b^d)$, infatti: 

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210227170731593.png" alt="image-20210227170731593" style="zoom: 50%;" />

Sono abbastanza sicuro che sia completo anche su spazi degli stati infiniti (a patto che ci sia una soluzione chiaramente).

### Ricerca bidirezionale

Finora abbiamo assunto una ricerca in avanti, si può provare anche all'indietro.

Si procede nelle due direzione fino ad incontrarsi (si spera): in avanti dallo stato iniziale e all'indietro dallo stato obiettivo.
Si deve tener traccia di 2 frontiere  e 2 tabelle degli esplorati. Quando le 2 frontiere collidono si ha una soluzione.

Si preferisce una *ricerca all'indietro* quando 

- l'obiettivo è chiaramente definito (*theorem proving*) o si possono formulare una serie limitata di ipotesi
- i dati del problema non sono noti e la loro acquisizione può essere guidata dall'obiettivo

Si può partire dal goal perchè lo si conosce, ciò che non si conosce è il cammino.

Si preferisce una *ricerca in avanti* quando:

- gli obiettivi possibili sono molti
- abbiamo una serie di dati da cui partire

La ricerca bidirezionale non è sempre applicabile (es. quando i predecessori non sono definiti, quando ci sono troppi stati obiettivo).

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210301115429521.png" alt="image-20210301115429521" style="zoom:33%;" />

**Analisi**

| completo | ottimo | tempo              | spazio             |
| -------- | ------ | ------------------ | ------------------ |
| si*      | *      | $O(b^\frac{d}{2})$ | $O(b^\frac{d}{2})$ |

Posso utilizzare varie tecniche di ricerca. Assumiamo qui che si utilizza una *breadth first* o una *uniform cost*.

### Ricerca di costo uniforme (UC)

*È l'algortitmo di Dijkstra.* 
Quando le azioni hanno costi differenti una soluzione semplice è usare la *best first search* prendendo come funzione di valutazione il costo del percorso dalla radice al nodo corrente. 
L'idea è che l'algoritmo si espande in onde di *costo-percorso uniforme*, invece che onde di profondità uniforme (come per il *breadth first search*).

È una generalizzazione della ricerca in ampiezza: si sceglie il nodo di costo minore sulla frontiera.
Abbiamo 2 ingredienti principali: 

- coda con *priorità* (in cima i nodi di costo minore)
- *goal-test posticipato* (tipico per coda con priorità), costa di più ma serve per l'algoritmo con priorità in modo da trovare ottimalità

Se incontro un nodo il cui stato è in frontiera ma con costo più alto il nuovo nodo è migliore, pertanto lo si sostituisce nella *frontiera*.

```pseudocode
function UC_graph(problem) return solution || failure
	node = problem.initial
	frontier = PriorityQueue([node])
	explored = {}
	
	while(!frontier.isEmpty())
		node = frontier.pop()
		
		if(problem.isGoal(node.state))
			return node
            
        explored.add(node.state)
		
		foreach child in EXPAND(problem, node)
			s = child.state
			
			if(s NOT in explored)
				if(child NOT IN frontier)
					frontier.push(child, child.cost)
                else
                	if(frontier.get(s).cost > child.cost)
            		frontier.delete(s)
            		frontier.push(child, child.cost)
	
```

Una volta che uno stato passa nello stato *esplorato* altri eventuali percorsi che conducono ad un nodo con lo stesso stato saranno peggiori (altrimenti essi stessi sarebbero stati esplorati prima).

**Analisi**

| completezza | ottimalità | tempo                                              | spazio                                             |
| ----------- | ---------- | -------------------------------------------------- | -------------------------------------------------- |
| completo    | ottimo     | $O(b^{1 + \lfloor \frac{C^*}{\epsilon} \rfloor })$ | $O(b^{1 + \lfloor \frac{C^*}{\epsilon} \rfloor })$ |

Assumendo che tutte le azioni abbiano un costo minimo > 0 l'agoritmo è completo e ottimo.

Assunto $C^*$ come il costo della soluzione ottima, $\lfloor \frac{C^*}{\epsilon} \rfloor$ è il numero di mosse al caso peggiore arrotondando per difetto.
Quando tutte le azioni hanno lo stesso costo UC somiglia a BF ma ha un costo di $O(b^{1+d})$, dovuta al goal-test posticipato. 

$O(b^{1 + \lfloor \frac{C^*}{\epsilon} \rfloor })$ può essere molto più grand di $O(b^d)$! Questo poichè l'algoritmo tende a esplorare larghe porzioni di albero che apparantemente sono ghiotte, ovvero con azione di basso costo, prima di esplorare percorsi con un alto costo ma più utili per raggiugere il goal.

### Panoramica

Versioni ad albero che non controllano stati ripetuti

![image-20210226115040724](/home/ludo/.config/Typora/typora-user-images/image-20210226115040724.png)

## Ricerca euristica 

In problemi di complessità esponenziale la ricerca esasutiva non è praticabile.
Usiamo una conoscenza a priori sul problema, una stima del costo futuro. 
Questa stima del costo futuro permette di evitare di generare  i cammini che non sono i più promettenti: *pruning*.

*eruistica (dal greco eureca):* riduce lo sforzo di fare una ricerca.
Sotto certe condizioni garantisce ottimalità e completezza.

Funzione di valutazione euritistica $h$; h(n) è una stima del costo per raggiungere da n un nodo goal.
Si applica al nodo ma dipende soltanto dallo stato, prima invece dipendeva dal nodo! (più nodi per lo stesso stato).

$f(n) = g(n) + h(n)$ // costo cammino + nuova funzione euristica

esempio di euristica: segue una problem-specific-information
Sulla mappa della Romania, possiamo tenerci la distanza in linea d'aria da Bucharest, numero delle caselle fuoriposto nel gioco dell'8.

### Algortimi Best First

Best-first heuristic, stessa di UC ma al posto di g(n) solamente per la valutazione dei nodi nella frontiera (coda con priorità) abbiamo f (g+h).
Ad ogni passo si sceglie il valore del nodo sulla frontiera con valore di f *migliore*.

### Greedy best-first

$f = h$. Si usa solo la funzione euristica per valutare i nodi.
In maniera ingorda seguo sempre il più promettente. Non trova sempre l'ottimo.

### Algoritmo A 

Un algoritmo A è un algortimo *Best First* con una funzione di valutazione *f* del tipo:

$f(n) = g(n) + h(n) \quad con \quad h(n) >= 0 \quad e \quad h(goal) = 0$

Casi particolare dell'algoritmo A:

- Se *h(n) = 0* -> UC
- Se *g(n) = 0* -> Greedy best-first

Il costo minimo di ogni azione deve essere > 0.

*Teorema: <u>completezza A</u>*

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226142923234.png" alt="image-20210226142923234" style="zoom: 33%;" />

*Idea*
Vogliamo evitare situazioni particolari in cui il costo delle azioni diminuisca infinetesimalmente.

*Dimostrazione*
Assumiamo che il percorso suluzione esista, e che comprenda n'. 
Se n' sta sulla frontiera prima o poi sarà espanso. 
Questo è vero perché esistono solo un numero finito di nodi x che possono essere aggiunti alla frontiera con $f(x) \leq f(n')$ per la condizione sulla crescita di g sul costo minimo degli archi.
Quindi se la soluzione non viene trovata prima n' verrà espanso e i suoi successori aggiunti alla frontiera; tra essi c'è il successore che conduce al goal.
Il ragionamento si ripete fino ad arrivare al goal che sarà espanso per l'espansione.

### Algoritmo A*

È un algoritmo A in cui h è una funzione euristica ammissibile.

Definiamo la funzione $f^*$ come un oracolo, nessuno ce l'ha veramente, serve come valutazione ideale, $f^*(n) = g^*(n) + h^*(n)$, con

- $g^*(n)$: costo del cammino minimo dalla radice a n (il migliore)
- $h^*(n)$: costo del cammino minimo dalla n a goal (il migliore)
- $f^*(n)$: costo del cammino minimo dalla radice al goal (il migliore)

Si può andare in sottostima (es. distanza in linea d'aria) o in soprastima della soluzione. Definiamo a rigaurdo una funzione euristica ammissibile.

*Definizione:* *euristica ammissibile*
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226143518146.png" alt="image-20210226143518146" style="zoom:33%;" />

È una condizione lower-bound.

*Teorema*: Gli algoritmi A* sono ottimali
Corollario: anche BF con passi a costo costante e UC sono ottimali (*h(n) = 0*).

Vantaggio: non ci perdiamo il percorso ottimo, e facciamo un po' di pruning.
La cosa migliore è ciò che non facciamo!

**Osservazioni su A***

- Abbandoniamo cammini che vanno troppo in profondità. 
- Una sottostima di h può farci compiere del lavoro inutile, ma non ci fa perdere il cammino migliore. 
- Una soluzione che va in sovrastima può farci perdere la soluzione ottimale (taglio causa sovrastima ma poteva esser buono e non posso recuperarlo)

**Ottimalità di A***
In caso di ricerca su albero l'uso di un'euristica ammissibile è sufficiente a garantire l'ottimalità di A*.
In caso su grafo si ha bisogno della proprietà di *monotonicità*.
Il rischio è di scartare candidati ottimi per averli già incontrati (la visita a grafo tiene conto del passato).

Abbiamo bisogno della *consistenza (monotonicità)*. Dobbiamo avere la garanzia che il primo espanso sia il migliore.

Def. *euristica consistente*

- h(goal) = 0
- $\forall n.  h(n) \leq c(n, a, n') + h(n')$ dove n' è il successore di n
  - ne segue che $f(n)\leq f(n')$, poiché
    - $g(n) + h(n) \leq g(n) + c(n, a, n') + h(n')$
    - {dato che $g(n) + c(n, a,n') = g(n')$}
    - $g(n) + h(n) \leq g(n') + h(n')$
    - {$f(n) = g(n) + h(n)$}
    - $f(n) \leq f(n')$

*Idea*: se h è consistente la f non decresce mai lungo i cammini, da cui *monotona*. Si fa prima passare da n a goal che passare per un nodo intermedio. 

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210321173143155.png" alt="image-20210321173143155" style="zoom:50%;" />

Attraverso una strada che costa c non devo avvicinarmi più di quanto sia in linea d'aria.

**Proprietà**
*Teorema*: *Un'euristica monotona è ammissibile.*
Esistono euristiche ammissibile che non sono monotone (ma rare):

*Esempio di euristica ammissibile ma non consistente* (si può notare che porta a prendere una strada non ottima in quanto D viene esplorato prima di C e pertanto rimane nella lista esplorati):
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210321173635429.png" alt="image-20210321173635429" style="zoom: 80%;" />

Le euristiche monotone garantiscono che la *soluzione meno costosa venga trovata per prima* e quindi sono ottimali anche nel caso di ricerca su grafo.

**Dimostrazione ottimalità**

- se h(n) è consistente i valori di f(n) lungo un cammino sono non decrescenti, ovver f è monotona
- ogni volta che A* selezione un nodo *n* per l'espansione il cammino ottimo a *n* è stato trovato
  - altrimenti ci sarebbe un altro nodo *n'* in frontiera sul cammino ottimo per *n* con $f(n') <$ (per la monotonia)
    - ciò non è possibile perché altrimenti sarebbe già stato espanso (espande in ordine di f crescente)
- quando seleziona un nodo goal è cammino ottimo, con $f=C^*, h=0$.  

**Commenti**
A* espande tutti i nodi con $f(n)<C^*$, ne espande alcuni con $f(n)=C^*$ e nessuno con $f(n) > C^*$.
Allunghiamo ellissoidi sul cammino ottimo. 

Cerchiamo una h il più alta possibile fra le ammissibili, altrimenti se fosse molto bassa finisco nel caso di UC, che non è informata.

Il punto fondamentale è il pruning dei sottoalberi.

**Panoramica su A**

A* è un caso particolare di A, con euristica ammissibile.
A è un algortimo di tipo Best First con f. di valutazione dei nodi in frontiera g+h.
A* è completo, discende dalla completezza di A.
A* è ottimo su ricerca ad albero; è ottimo su grafi se l'euristica è consistente.
A* è ottimamente efficiente: a parità di euristica nessun altro algoritmo espande meno nodi senza rinunciare all'ottimalità.

**Limiti**
In memoria il footprint resta $O(b^{d+1})$.
Quale eusitica scegliere? Come trovarla?

**Ricavare altri algoritmi da A* **

- UC: f=g, h=0
- Greedy Best First: f=h, g=0
- BF: f=d, h=0
- DF: f=1/d, h=0

*?Greedy Best First ad albero è completo?*
Secondo me no, tende ad andare in loop se ad esempio i successori di un nodo n hanno euristiche > del valore di h del padre di n.

### Euristiche per A*

L'efficienza nel trovare un cammino soluzione dipende da quanto è *informata* l'euristica (grado di informazione posseduta).

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210321182634363.png" alt="image-20210321182634363" style="zoom:33%;" />

*Teorema*: Se $h_1 \leq h_2$ ($h_2$ è più informata di $h_1$) i nodi espansi da A* con $h_2$ sono un sottoinsieme di quelli espansi da A* con $h_1$. 

*Idea*: A* espande tutti i nodi con $f(n)<C^*$ e sono in quantità minore per h maggiore, in altre parole h fa andare più nodi oltre C*.

Un'euristica più informata riduce lo spazio di ricerca ma tipicamente è più difficile da calcolare.

Def. Se $\forall n.h_1(n)\leq h_2(n)$ allora $h_2$ <u>domina</u> $h_1$.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226152611047.png" alt="image-20210226152611047" style="zoom:33%;" />

**Valutazione algoritmi di ricerca euristici** 
Si prende in considerazione il fattore di *diramazione effettiva* b* .

Dati N = numero di nodi generati, d = profondità della soluzione,
b* è il fattore di diramazione di un albero uniforme con N+1 nodi, soluzione dell'equazione:
$N+1=b^*+b^{*^2} + ...+b^{*^d}$

es. con $d=5, N=52 \implies b^*=1.92$

Sperimentalmente una buona euristica ha un b* vicino ad 1, < 1.5.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226153114092.png" alt="image-20210226153114092" style="zoom:33%;" />

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210321184027625.png" alt="image-20210321184027625" style="zoom:33%;" />

Capacità di esplorazione, migliorando di poco l'euristica si riesce a parità di nodi espansi raggiungere profondità maggiore (= vincere).

**Riassunto**

- l'euristica può migliorare di molto la capacità di esplorazione
- migliorando anche di poco l'euristica si riesce a esplorare uno spazio molto più grande

Ammissibile => Ottimale. Ma un’euristica potrebbe essere dimostrata ottimale per altra via.

#### Inventiamo un'euristica
Alcune strategie: 

- *rilassamento del problema*
  - viaggiare in linea diretta (es. rilasciare il vincolo delle strade), supergrafo rispetto al grafo dello spazio degli stati originale, dove si aggiungono archi in più
  - distanza Manhattan
- *massimizzazione di euristiche*
  - se si hanno una serie di euristiche ammissibile e nessuna domina un'altra conviene prendere il massimo dei loro valori. L'euristica risultante rimane ammissibile e dominerà tutte le altre (ovvero sarà più informata)
  - <img src="/home/ludo/.config/Typora/typora-user-images/image-20210321184722225.png" alt="image-20210321184722225" style="zoom:33%;" />
- euristiche da *sottoproblemi*
  - es. gioco dell'8 considero solamente di sistemare 1,2,3,4
  - *database di pattern*: memorizzare ogni istanza del sottoproblema con relativo costo soluzione; successivamente userò questo database per estrarre l'euristica corrispondende a questo stato
  - sottoproblemi multipli: anche qui si può poi prendere il massimo e ottenere un'euristica ammissibile.
    *?Ma la loro somma sarebbe ammissibile?*
    - In genere no, le soluzioni ai sottoproblemi interferiscono (condividono alcune mosse), per cui la somma delle euristiche non è ammissibile! Potremmo sovrastimare avendo aiuti mutui.
    - *pattern disgiunti*: eliminando il costo delle mosse che contribuiscono all'altro sottoproblema si possono ottenere euristiche additive ammissibili
- *apprendere dall'esperienza*: 
  - far girare il programma raccogliendo dati <stato, h*>. Algoritmi di apprendimento induttivo per predire la h, ci facciamo guidare alla soluzione dalle caratteristiche salienti dello stato.
- *combinazione lineare* di euristiche
  - combinazione lineare, il peso dei coefficienti può essere aggiustato con l'esperienza, apprendendo automaticamente
  - ammissibilità e consistenza non automatiche
  - <img src="/home/ludo/.config/Typora/typora-user-images/image-20210321185353594.png" alt="image-20210321185353594" style="zoom:33%;" />

### Algoritmi evoluti basati su A*

- Beam search
- IDA*
- RBFS
- MA*, SMA*

#### Beam search

Nel Best First viene tenuta in memoria tutta la frontiera, e noi qui la vogliamo tagliare. 
Nella *Beam search* si tengono ad ogni passo solo i *k* nodi più promettenti, dove *k* è l'ampiezza del raggio (beam). 
Non è completa. 

#### IDA*

Combina A* con ID. È un po' geniale, ad ogni iterazione si ricerca in profondità con un limite *cut-off* dato dal valore di f (e non dalla profondità).

Il limite *f-limit* viene aumentato ad ogni iterazione, fino a trovare la soluzione.
Per garantire l'ottimalità è cruciale la scelta dell'incremento, il punto critico.
Si hanno 3 strade:

| caso                                | incrementi di *f-limit*                                      |
| ----------------------------------- | ------------------------------------------------------------ |
| se le azioni hanno costo costante k | k                                                            |
| se le azioni hanno costo variabile  | $\leq \epsilon$ (minimo costo degli archi)                   |
| [generico]                          | f-limit = minimo valore f dei nodi generati ed esclusi all'iterazione precedente |

In questi casi IDA* è completo e ottimo.
In memoria abbiamo O(bd). 

## Oltre la ricerca classica

*Ricerca locale, cenni di ricerca online*
Critica al passato: gli agenti risolutori di problemi *classici* assumono ambienti completamente osservabili, deterministici. Possono produrre offline un piano da seguire.
Le percezioni non servono se non nello stato iniziale.

In ambienti più realistici la ricerca sistematica o euristica risulta troppo costosa, da qui nasce l'idea di Metodi di ricerca locale.
Vanno riconsiderate molte assunzioni sull'ambiente: 

- azioni non deterministiche
- ambiente parzialmente osservabile
- ambienti sconosciuti e problemi di esplorazione -> ricerca online (non lo faremo)

### Ricerca locale

Assunzioni: non ci serve il cammino soluzione, l'importante è lo stato goal.
Gli algoritmi di ricerca locale sono adatti per problemi in cui la sequenza delle azioni non è importante, quello che conta è unicamente lo stato goal. 
Tutti gli elementi (da configurare) della soluzione sono nello stato ma alcuni vincoli sono violati, ad *es. le 8 regine* (non è importante il cammino per arrivare alle 8 regine senza interferenze ma solo arrivare a quell'obiettivo -> non dobbiamo salvarci il cammino).

Gli algortimi in questa categoria sono

- non sistematici, non esplorano completamente
- tengono traccia solo del nodo corrente e si spostano su nodi adiacenti 
- non tengono traccia dei cammini (non serve darli in output)

Per queste ragioni sono efficienti per l'uso della memoria, possono trovare soluzioni ragionevoli anche in spazi molto grandi e infiniti, come nel caso di spazi continui

Sono utili per risolvere problemi di *ottimizzazione*: 

- A seconda di una funzione obiettivo viene identificato lo stato migliore (minimizzando l'errore)
- identificare lo stato di costo minore

es. training di un modello di Machine Learning

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210301125741074.png" alt="image-20210301125741074" style="zoom: 50%;" />

Funzione euristica <u>di costo della funzione obiettivo</u> (non del cammino!).
L'obiettivo è trovare avvallamenti più bassi o il picco più alto.

### Hill climbing (Ricerca in salita)

Ricerca locale greedy.
L'albero di ricerca non viene salvato in memoria. 
Ci sono 3 tipi, a seconda della scelta del nodo che migliora la valutazione dello stato attuale:

- hill climbing *a salita rapida*: il migliore
- hill climbing *stocastico*: a caso tra quelli che salgono
- hill climbing *con prima scelta*: il primo

Lo scheletro è il seguente (assumeno di scegliere il vicino con valore più alto).

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210302162148391.png" alt="image-20210302162148391" style="zoom:50%;" />

Se non ci sono successori migliori l'algoritmo termina con fallimento.
Non c'è frontiera, si tiene 1 solo stato. Si prosegue solo se il vicino è migliore dello stato corrente (se tutti i vicini sono peggiori si ferma). 
Miglioriamo finchè posssiamo, finché tutti i successori non sono peggiori continuiamo.
Tempo: variabile, numero cicli in base al punto di partenza. 
Finché salgo vado (non è troppo smart).

*Nell'esempio delle 8 regine:* 
Si cerca *una* configurazione che ci dia la soluzione. 
Si blocca l'86% delle volte. In media servono solo 4 passi per la soluzione e 3 quando si blocca.
La trova rapidamente ma spesso si blocca, e nel caso lo fa rapidamente.

h = euristica di costo della funzione obiettivo da minimizzare

*Problemi di Hill-climbing*, in cui fallisce: i picchi possono essere massimi locali o soluzioni ottimali

- massimi locali, 
- spalle (pianori), 
- crinali

es. romania greedy -> non si presta alle assunzioni dell'hill-clioming: non salviamo albero di ricerca

**Miglioramenti**

- consentire un numero limitato di *mosse laterali* (per scavallare pianure ecc..) (< invece che $\leq$ nell'algoritmo)

  - l'alg delle 8 regine ha successo al 94% ma ci impeiga 21 passi in media

- hill-climbing *stocastico*: si sceglie a caso tra le masse in salita (tenendo conto della pendenza)

  - converge più lentamente

- hill-climbing con *prima scelta*

  - prende il primo migliore, anche generando mosse a caso
  - utile quando i successori sono molti

- hill-climbing con *riavvio casuale (random restart)*: riparte da un punto scelto a caso, non mi dispero e riprovo da una configurazione casuale tanto in poche mosse mi accorgo eventualmente di aver fallito

  - 1/p ripartenze se la probabilità di successo è p

  - es. regine: 6 fallimenti e 1 di successo, 0.14; in un caso di 3mln di regine ci impiega meno di 1 minuto

  - tendenzialmente è completo (quasi un brute-force, insistendo).

  - dipende molto dalla configurazione dei problemi se funziona o meno (NP-Hard, molti minimi locali; il problema è spinoso.. porcospino)

    <img src="/home/ludo/.config/Typora/typora-user-images/image-20210302164341899.png" alt="image-20210302164341899" style="zoom:33%;" />

### Simulated Annealing (tempra simulata)

Analogia: processo di tempra dei metalli in metallurgia (*cross-fertilization* fra settori scientifici apparentemente sconnessi).
Combina *hill-climbing* con una scelta stocastica (non del tutto casuale) che consente alcune scelte peggiorative.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210302164615605.png" alt="image-20210302164615605" style="zoom: 50%;" />

La temperatura decresce col progredire dell'algoritmo, rendendo improbabili le mosse peggiorative.

- Ad ogni passo scelgo sempre un successore n' a caso
  - se migliora lo stato corrente viene espanso
  - else *seconda chance*
    - quel nodo viene scelto con probabilità $e^{\frac{\Delta E}{T}}$, con $\Delta E=f(n')-f(n), \Delta E <0$
    - si genera un numero casuale x tra 0 e 1, se $x<p$ viene scelto come successore

*Idea*: 

T temperatura, $\Delta E$ variazione di energia.

- p è inversamente proporzionale al peggioramento, se la mossa peggiora molto $\Delta E$ diventa $<<0$ e la p si abbassa (l'esponente è negativo, $e^{\Delta E}$ cresce ma sta al denominatore). 
- T decresce col progredire dell'algoritmo (e di conseguenza anche p, poiché  ricordando che l'esponente $\Delta E$ è negativo si ha: $p = \frac{1}{\sqrt[T]{e^{-\Delta E}}}$, pertanto il denominatore cresce e la frazione assume un valore più piccolo).

È bene tornare indietro! 

La probabilità di una mossa in discesa diminuisce col tempo e l'algortimo si comporta sempre più come l'hill climbing.

Soluzione ottimale: se T viene decrementato abbastanza lentamente con prob. tendente ad 1,

>If the schedule lowers T to 0 slowly enough, then a property of the Boltzmann distribution is that all the probability is concentrated on the global maxima, which the algorithm will find with probability approaching 1.

*pensando a valori estremi di T, ?che tipi di Hill-climbing si ottengono?*
Variando i parametri otteniamo i tipi di HC di prima?? mi viene in mente solo T=1 e semplicemente dovrebbe comportarsi come un Hill-climbing a prima scelta poiché vengono scelti solo successori migliorativi.

Sperimentalmente il valore di T è tale che per valori medi di $\Delta E$, la p sia circa 0.5.

### Local beam search

È spartano: tiene solo i k migliori, dove k è l'ampiezza del raggio (beam). È la versione locale della *beam search*. 
Si tengono in memoria *k* stati, anzichè uno, e ad ogni passo si generano i successori di tutti i k stati. 

- Inizialmente parte con k stati casuali
- Se uno degli stati generati è goal ci fermiamo altrimenti seleziona i k successori migliori dalla lista completa e continua

Note:

- è diverso da *random-restart*
  - sembra quasi un'esecuzione parallela di k random-restart; non è così poiché le esecuzioni sarebbero indipendenti, qua si ha in comune la lista dei k migliori e non si riparte da 0
- è diverso da *beam search*
  - questo è un algoritmo locale, non è un A*. Inizialmente sceglie k stati casualmente e ne genera i successori; nella beam search si parte da un unico stato e si tiene una fronitera composta da k nodi

Se K = 1 => hill-climbing a salita rapida (sceglie il migliore)

Se K = illimitato => BF (anche se secondo me inizialmente non si può partire con K=inf altrimenti prenderei tutti gli stati e boom)

**Beam search stocastica**
Vorremmo diversificare un po', potremmo trovarci in una regione ristretta dello spazio degli stati altrimenti. Si introduce un elemento di casualità! Ci avviciniamo al concetto di selezione naturale.. non si scelgono direttamente i k successori migliori ma si scelgono i successori con una probabilità proporzionale al valore dei successori, incrementando la variabilità.

### Algoritmi genetici

Sono varianti della *beam search stocastica* in cui gli stati successori sono ottenuti combinando due stati genitore (anziché per evoluzione).

*organismo*: al posto dello stato
*progenie*: successori
*fintess*: il valore della f, per cui la nostra progenie avrà probabilità di sopravvivere.*popolazione di individui*: stati 
*accoppiamenti + mutazione genetica*
*generazioni*

Inizialmente si ha una *popolazione* con k stati/individui generati casualmente. Ogni individuo è rappresentato come una stringa.(es. regine con 24bit perché ho 8 colonne e mi serve salvare valori da 0 a 7 per ogni colonna per identificare la riga sulla quale posizione l'i-esima regina, $log_2 8 = 3$ per cui 24bit).

Gli individui sono valutati da una *funzione di fitness*. (es. n° coppie di regine che non si attaccano), ci dicono quanto quell'individuo è migliore.

Si selezionano gli individui per gli accoppiamenti con una *probabilità* proporzionale alla fitness.
Le coppie danno vita alla generazione successiva combinando materiale genetico (*crossover*) e con un meccanismo aggiuntivo di mutazione genetica casuale.
La cosa si ripete fino ad ottenere stati abbastanza buoni.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210302171254699.png" alt="image-20210302171254699" style="zoom:33%;" />

Estratte in modo stocastico, in base al fitness.
La variabilità è data da :

- Crossing-over del DNA (elemento di stocasticità) più 
- mutazione casuale

Tende al miglioramento della specie, all'accrescimento della fitness.
La nuova fitness non è correlata, va ricalcolata.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210321213554887.png" alt="image-20210321213554887" style="zoom:33%;" />

[*natural computing:* swarm computing]
[Come le formiche ottimizzano il percorso? tutte partono alla ricerca di cibo, se più formiche scoprono uno stesso percorso interessante verrà seguito da altre. Ogni formica nel percorso rilascia una sostanza chimica, seguono quello col maggior intensità di sostanza. Percorso ottimo! ]
[[Etologia!]

Combinano la tendenza a salire della *beam search stocastica* con l'interscambio di informazioni tra thread *paralleli* di ricerca (blocchi utili che si combinano).
Funziona meglio se il problema ha componenti significative rappresentabili in sottostringhe.

Il punto critico di questi algoritmi è la rappresentazione del problema in stringhe. 

### Spazi continui

Sono problemi difficili in principio ma gli algortimi di ricerca locale funzionano molto bene.
Molti casi reali hanno spazi di ricerca continui. (es. Machine Learning)

Stato descritto da var. continue, vettore x, $x_1, ..., x_n$.
Per ogni posizione abbiamo infiniti punti in cui muoverci. Abbiamo strumenti matematici interessanti.

Lo strumento principale è il *gradiente*. Se la f è continua e differenziabile, il minimo o massimo lo si può cercare utilizzando il gradiente, che restituisce la direzione di massima pendenza nel punto.

Gradiente: derivata parziale di f su ogni componente del vettore, si ottiene un vettore di derivate.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210321213803243.png" alt="image-20210321213803243" style="zoom:50%;" />*Hill-climbing iterativo*: $x_{new} = x \pm  \eta  \nabla f(x)$, + per salire (massimizzazione) - per scendere, (minimizzazione), $\eta$ è lo step size, il passo.

Quantifica lo spostamento senza cercarlo tra gli infiniti possibili successori.
Abbiamo una *bussola* fondamentale, ci dice dove andare e di quanto. Quantifica la pendenza della cruva.

Arriviamo quando.. il gradiente è nullo e altro boh

Non sempre è necessario il min/max assoluto: vedremo nel ML.

Idea dell'algortimo che controlla le reti neurali oggigiorno (SGD, stocastic gradient descent).

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210321214343697.png" alt="image-20210321214343697" style="zoom: 33%;" />

### Ambienti più realistici

Si considerano azioni non deterministiche, le percezioni sono importanti. L'agente può elaborare una strategia più che un piano, un piano con *contingenza*. 

**Aspirapolvere: azioni non deterministiche**
Sono necessarie variazioni al modello. L'agente non sa in che stato si troverà alla fine dell'azione.
Agiamo di conseguenza alle percezioni.

### Aberi di ricerca AND/OR

Si creano dei nodi OR, le scelte dell'agente (fare 1 sola azione)
Nodi AND, le diverse contingenze (le scelte dell'ambiente, più stati possibili), da considerare tutte

Una soluzione è un albero! che

- ha un nodo obiettivo in ogni foglia
- un'azione nei nodi OR
- include tutti gli archi uscenti da nodi AND (tutte le contingenze)

Se non avesse AND sarebbe un percorso normale come prima.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210321214731670.png" alt="image-20210321214731670" style="zoom:50%;" />

## Giochi con avversario

Assumiamo che l'ambiente in questo caso sia

- osservabile
- deterministico
- multi-agente

Adottiamo una rappresentazione degli stati non più atomica, ma complessa.

1. Giochi con avversario, dove i piani devono tenere conto delle mosse dell'avversario
2. I problemi di soddisfacimento di vincoli, dove lo stato ha una struttura *fattorizzata*
3. I sistemi basati su conoscenza: lo stato è una base di conoscenza a cui rivolgere domande sul mondo, rappresentato in un *linguaggio espressivo*
   Si utilizzano calcolo proposizionale (PROP) e logica del prim'ordine (FOL)

**Giochi con avversario**

- Le regole risultano essere semplici e formalizzabili
- l'ambiente è *accessibile*, deterministico, multi-agente competitivo
  - ciò rende tutto più strategico e si hanno vincoli in tempo reale obbligando a trovare la mossa migliore nel tempo disponibile
- Ci sono 2 giocatori che giocano a *turni alterni*, a *somma zero*, cioè se uno vince l'altro perde, detti anche giochi dove l'informazione è perfetta

Ci sono solo 2 agenti, di tipo competitivo, in tempo reale, in questi termini i giochi sembrano più simili a quelli reali. 

**Ciclo: *pianifica-agisci-percepisci***
Si decide la mossa, la si esegue, si vede cosa si fa l'avverssario, si percepisce cosa l'avversario ha fatto.

**Giochi come problemi di ricerca**
*Stati:* configurazione del gioco (stati di una scacchiera) 
	la funzione *player(s)*: a chi tocca muovere nello stato s, è una parte importante dello stato
*Stato iniziale*
*Actions*(s): mosse legali in s
*Result*(s, a): funzione di transizione, lo stato risultante dall'eseguire la mossa *a* nello stato *s*, non c'è incertezza
*Terminal-test*(s): determina la fine del gioco, se s è uno stato finale, al posto di IsGoal()
*Utility*(s, p): funzione di utilità o payoff, ci dice con un valore numerico quanto valgono gli stati terminali del gioco per *p* (es. conteggio punti, 1 per vittoria, 0 per pareggio, -1 per perdita).
	per questo si chiamano giochi a somma zero: se uno vince l'altro perdio, la somma dei punteggi *deve essere costante, se non zero*.

Che cosa vedremo?

-  La decisione ottima teorica: come si sceglie la mossa migliore in un gioco con uno spazio di ricerca completamente esplorabile -> MIN-MAX
- Estensione a giochi in cui a causa della complessità non si può esplorare tutto -> ALFA-BETA
- cenni a giochi più complessi

Ora immagianiamo:

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210309163100811.png" alt="image-20210309163100811" style="zoom:33%;" />
So valutare le situazioni terminali del gioco, devo sempre valutare dal punto di vista di chi deve muovere: 

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210309163311255.png" alt="image-20210309163311255" style="zoom:50%;" />

Posso pianificare e trasportare indietro la funzione di utilità, che si può applicare solo agli stati terminali.

Assumo di prendere il caso peggiore delle possibili scelte, immagino che l'avversario faccia la mossa più intelligente per lui.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210309163943831.png" alt="image-20210309163943831" style="zoom: 33%;" />

Conviene ricercare in profondità in maniera ricorsiva, per la memoria.

Secondo Claude Shannon ci sono $10^{120}$ foglie in un albero degli scacchi. Facendo un rapido e approssimativa calcolo scopriamo che:

- Ci sono circa $10^{80}$ atomi nell'universo
- Ci sono $\pi \cdot 10^7$ secondi in un anno
- in nanosecondi moltiplico per $10^9$
- si stima che l'universo abbia $10^{10}$ anni (10 miliardi)

In totale abbiamo un ordine di $10^{106}$ il che vuol dire che anche se ogni atomo svolgesse computazione per risolvere questo problema sin dall'inizio dell'universo non si sarebbero valutate ancora tutte le possibili scelte.

### MIN-MAX

**Ricorsivo**

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210305180704404.png" alt="image-20210305180704404" style="zoom:50%;" />

**Analisi**

| tempo    | spazio |      |
| -------- | ------ | ---- |
| $O(b^m)$ | $O(m)$ |      |

È lineare nella memoria grazie ad una ricerca in profondità ricorsiva.
É improponibile un'esplorazione sistematica del grafo degli stati se non per giochi semplici, ad es. gli scacchi richiedono $35^{100}$ mosse, con un grafo che arriva a $10^{40}$ nodi.

Sono necessarie delle euristiche per stimare la bontà dello stato del gioco.

![/home/ludo/Videos/minmax2.gif](/home/ludo/Videos/minmax2.gif)

**Min-Max euristico (con orizzonte)**
In casi più complessi occorre una funzione di valutazione euristica dello stato, *Eval(s)*.
Si guardanio in avanti *d* livelli.

La *funzione di valutazione Eval* è una stima dell'utilità attesa a partire da una certa posizione. La sua qualità è fondamentale, deve:

- essere consistente con l'utilità se applicata a stati terminali del gioco, non vuol dire che deve dare lo stesso risultato ma deve indurre lo stesso ordinamento
- essere efficiente
- riflettere le probabilità effettive di vittoria

**Esempi di Eval**

- Per gli scacchi una funzione Eval che funziona può focalizzarsi su alcune caratteristiche, es. i pezzi che ancora posseggo con pesi diversi a seconda dei valori del pezzo (pedone 1, regina 9..), la posizione del re ecc.. 
  Devo costruire sorte di classi di equivalenza. 

- Funziona lineare pesata: $Eval(s) = w_1f_1(s) + w_2f_2(s) + ... + W_nf_n(s)$
  Combinazioni non lineari di caratteristiche: l'alfiere vale di più nei finali di partita.

Giocando si dovrebbe apprendere a stimare meglio la funzione di valutazione.

Un problema di guardare avanti fino ad un certo livello è:
*Stato non quiescente*: l'esplorazione fino a un certo livello può mostrare una situazione molto vantaggiosa.  La soluzione è di cercare di applicare la valutazione a stati quiescenti, ovvero quelli per cui la funzione di valutazione non è soggetta a mutamenti repentini.

*Effettivo orizzonte*: può accadere che vengano privilegiate mosse diversive aventi il fine di spingere il problema oltre l'orizzonte

**Per ottimizzare..**
*?Abbiamo bisogno necessariamente di esplorare ogni cammino?*
No, esiste un modo per dimezzare la ricerca pur mantenendo la decisione min-max ottima.
Potatura alfa-beta (McCarthy 1956, per scacchi)

### ALFA-BETA

Tecnica di *potatura*: per ridurre l'esplorazione dello spazio di ricerca in algoritmi min-max.
Si va avanti fino al livello di esplorazione *d* desiderato e propagando indietro i valori si decide se si può abbandonare l'esplorazione nel sotto-albero (facendo *tagli*).

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210309171635685.png" alt="image-20210309171635685" style="zoom: 50%;" />

Metto x,y poiché in quel livello devo minimizzare ma al livello precedente devo massimizzare.
Le funzioni Max e Min hanno in più due valori di riferimento ($\beta = +\infin$ per Max, $a=-\infin$ per Min). 
Tagli alfa e tagli beta.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210305181051193.png" alt="image-20210305181051193" style="zoom: 33%;" />

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210305181103451.png" alt="image-20210305181103451" style="zoom: 33%;" />

![](/home/ludo/Videos/alfabeta.gif)

**Ordinamento delle mosse**
La potatura ottimale si ottiene quando ad ogni livello sono generate prima le mosse *migliori* per  chi gioca. 
Per i nodi MAX sono generate prima le mosse con valore più alto.
Per i nodi MIN sono generate prima le mosse con valore più basso.

**Analisi**
Complessità $O(b^{\frac{m}{2}})$.

**Come ordinare dinamicamente**

- *Approfondimento iterativo*
  - si scoprono in una iterazione informazioni utili per l'ordinamento delle mosse da usare in una successiva iterazione; 
- *Tabella delle trasposizioni*
  - per ogni stato incontrato si memorizza la sua valutazione, se ho già incontrato una mossa tagliata allora la taglio

**Miglioramenti**
Al di là di alfa-beta, per ridurre l'esplorazione si può optare per:

- *Potatura in avanti*: esplorare solo le mosse ritenute promettenti, una specie di beam search, oppure tagli probabilistici basati su esperienza
- Database di mosse di apertura e chiusura; nelle mosse finali ci sono poche mosse sensate e ben studiate mentre per le aperture avendo tante possibilità e tanta libertà ha poco senso fare ricerca; per le fasi finali si può esplorare esaustivamente e ricordarsi le migliori chiusure

L'estensione ai giochi multiplayer si utilizzano invece di min e max un *vettore* di più elementi (A,B,C).

**Cenni a giochi più complessi**
Giochi con ambiente stocastico (lancio di dadi, carte ), parzialmente osservabile e deterministici

## CSP: Soddisfacimento di vincoli

Lo stato ha una rappresetazione *fattorizzata*, insieme di caratteristiche che descrivono lo stato (la più usata negli algoritmi di apprendimento); non è più una blackbox ma una struttura dati  sfruttata per un ricerca più efficiente. 
Dei problemi reali sono il layout dei circuiti, lo scheduling, ...

**Formulazione di un problema CSP**
Il problema è descritto da 3 componenti

- X, insieme di variabili
- D, insieme di domini, dove $D_i$ è l'insieme dei valore possibili per $X_i$
- C un insieme di vincoli

Lo stato è completamente definito da un assegnamento;
*stato*: un assegnamento [parziale/completo] di valori a variabili

*Stato iniziale*: stato vuoto

*Azioni*: assegnamento di un valore a una variabile
*Soluzione*: assegnamento completo e consistente (tutte le var assegnate e tutti i vincoli soddisfatti)

**Esempi di formulazione**

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210309174413858.png" alt="image-20210309174413858" style="zoom: 50%;" />

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210309174526525.png" alt="image-20210309174526525" style="zoom:33%;" />

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210309174641569.png" alt="image-20210309174641569" style="zoom:33%;" />

Nella formulazione incrementale: nessuna regina sulla scacchiera e ne metto una per volta, mentre nella formulazione a stato completo le sistemo tutte una per colonna e cerco di gestire le cose dopo.

**Strategie per CSP**

- euristiche specifiche
- propagazione di vincoli: fare inferenze che portano a restringere domini e quindi limitare la ricerca 
- backtracking intelligente

Tipicamente si fa una combinazione di queste 3 strategie.

**Idea di ricerca in problemi CSP**
Ad ogni passo si assegna una variabile, siccome il numero di var. è finitio => la massima profondità di ricerca è fissata dal numero di variabili. 
*Quindi sarà un algoritmo a profondità limitata*. 
Uno potrebbe essere tentato da dire, *ingenuamente*, che:

-  l'ampiezza dello spazio di ricerca è  $|D_1| \cdot|D_2|\cdot ... \cdot |D_n|$ 
  quindi  il fattore di diramazione è $n\cdot d$ e le foglie sono $n!\cdot d^n$.

 L'ordine con cui assegno le variabili non è importante, infine avrò $d^n$ foglie.

**Ricerca a profondità limitata con backtracking**

- è lo scheletro principale per gli algoritmi CSP

- controllo anticipato: controllare dopo ogni assegnamento se qualche vincolo è stato violato e fare subito backtracking provando una nuova possiblità non appena scopro che un vincolo è stato violato.
  
  <img src="/home/ludo/.config/Typora/typora-user-images/image-20210319093543657.png" alt="image-20210319093543657" style="zoom: 33%;" />
  
  - se un vincolo è stato violato è inutile procedere, faccio subito *backtracking* e provo un altro valore

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210305182848605.png" alt="image-20210305182848605" style="zoom: 67%;" />

Dentro *csp* c'è la descrizione del problema, con la formulazione vista sopra.

```pseudocode
var = SELECT-UNASSIGNED-VARIABLE(csp)
```

- Seleziona una variabile non assegnata *secondo un criterio definito* nella funzione.
- Successivamente effettua un *controllo anticipato* della consistenza dell'assegnamento con in vincoli
- Poi fa l'inferenza per diminuire i domini delle altre variabili ancora non assegnate
  - se ci sono domini vuoti fallisco
- richiamo la funzione con il nuovo assegnamento e i domini ristretti
- Se vi sono fallimenti allora *torna indietro* rimuovendo le inferenze e l'assegnamento
  - è un backtracking *cronologico*

Il primo assegnamento è vuoto, il che ci ricorda che siamo in una formulazione *incrementale*.

*Inferenza*: si vuole ridurre il problema, ridurre i domini dopo ogni assegnamento. L'effetto è che ho un problema più piccolo: dovuto al fatto che ho preso una scelta. 
Per fare backtracking, siccome mantengo un unico stato lo riporto a condizioni precedenti! cancellando stato e inferenze fatte.

Fallisco se esaurisco i valori da considerare o per il controllo anticipato dei vincoli, o perchè ho chiamato ricorsivamente bacaktrack e ho restituito un fallimento.

Le funzioni sottolineate sono dove si può *iniettare* intelligenza: nella scelta delle variabili, nella scelta dei valori e nel tipo di inferenza che si fa.

### **Euristiche e strategie per CSP**

- *SelectUnassignedVariable*
  - quale variabile scegliere?
- *OrderDomainValues*
  - quali valori scegliere?
- *Inference*
  - qual è l'influenza di un assegnamento sulle altre variabili?
- *BackTrack*
  - come evitare di ripetere i fallimenti?

**Scelta delle variabili**

- *MRV*(Minimum Remaining Values): si sceglie la variabile più vincolata, che ha meno valori legali residui, strategia *fail first*.
- Euristica del grado: a parità di MRV, sceglie la var. coinvolta in più vincoli, la più vincolante (i vicini nel grafo dei vincoli)

**Scelta dei valori**

- *Valore meno vincolante*: quello che esclude meno valori per le altre variaibili direttamente collegate con la var. scelta; meglio valutare prima un assegnamento che ha più probabilità di successo

**Propagazione di vincoli** (Inference)

- Verifica in avanti, *Forward Checking*

  - assegnato un valore ad una var si possono eliminare i valori in incompatibili per le altre var. *direttamente collegate* da vincoli (non itera)

    <img src="/home/ludo/Videos/fowrardchecking.gif" style="zoom: 33%;" />

- Consistenza di nodo e d'arco

  - più costoso, su tutto il grafo (non sui vicini come sopra), itera finché tutti i nodi ed archi sono consistenti

**Backtracking cronologico vs intelligente**

- *Backtracking cronologico* 
  - può portare a situazioni poco efficienti, in quanto si torna indietro all'ultimo assegnamento ma la variabile in questione potrebbe non essere la causa del fallimento e quindi ritenta altri assegnamenti per l'ultima variabile senza riuscire ad avanzare
- *Backtracking intelligente*
  - si considerano le alternative solo per le variabili nell'*insieme dei conflitti* ovvero quelle che causano il fallimento. È un backtracking guidato dalle dipendenze

**Metodi CSP locali**
Si parte con tutte le variabili assegnate (formulazione a stato completo) e ad ogni passo si modifica l'assegnamento ad una variabile per cui un vincolo è violato (casualmente).
È un algoritmo di *riparazione euristica*.
Una strategia euristica nello scegliere un nuovo valore può essere quella dei *conflitti minimi* scegliendo il valore che crea meno conflitti.

È molto efficace, ad es. 1 milione di regine in 50 mosse

# Rappresentazione della conoscenza e ragionamento

Lo stato è rappresentato in maniera ancora più espressiva 

## Agenti basati su conoscenza

Vogliamo migliorare le capacità di ragionamento dei nostri agenti:

- rappresentazioni di mondi più complessi e astratti
- basati su *conoscenza*: dotati di una *knowledge base* espressa in maniera esplicita e dichiarativa

Tipi particolari di agenti basati su modello:

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210319112221534.png" alt="image-20210319112221534" style="zoom:50%;" />Usa le percezioni per aggiornare subito il suo stato del mondo.
Ci servono linguaggi più espressivi e capacità inferenziali.
La conoscenza può essere codificata a mano o estratta da testi o appresa dall'esperienza, deve comunque essere rappresentata dall'agente.

La KB è in forma *dichiarativa*, è più flessibile, permette di acquisire più semplicemente nuove informazioni incrementalmente piuttosto che in un approccio *procedurale* dove si dovrebbe cambiare  il programma.

Mantiene una base di conosceza, interagisce tramite un'interfaccia funzionale *Tell-Ask*:

- tell: 
- ask: 
- retract:

Gli enunciati nella KB rappresentano le opinioni/credenze dell'agente, formalmente la KB è un insieme di enunciati espressi in un linguaggio di rappresentazione.

Il *problema* da risolvere è: data una base di conoscenza KB, contenente una rappresentazione dei fatti che si ritengono veri, vorrei sapere se un certo fatto $\alpha$ è vero di conseguenza (*conseguenza logica*).

 **KB vs BD** 
La KB:

- contiene fatti specifici sul mondo ma anche fatti generali
- rappresentazione esplicita in un linguaggio simbolico
- è caratterizzata dalla *capacità inferenziale*

Nelle BD

-  abbiamo solo fatti specifici

**Trade-off fondamentale della rappresentazione della conoscenza**
Più il linguaggio è espressivo meno efficiente è il meccanismo funzionale.

Il problema sta nel trovare il giusto compromesso fra 

- *espressività* del linguaggio di rappresentazione
- *complessità* del meccanismo inferenziale

**Formalismi per la rappresentazione della conoscenza**
3 componenti per un formalismo:

- sintassi
- semantica
- meccanismo inferenzialie

**Logica come linguaggio**
*?Qual è la complessità computazionale del problema KB è conseguenza logica di $\alpha$ nei vari linguaggi logici?*
I linguaggi logici del calcolo proposizionale (PROP) e logica di predicati (FOL) sono adatti per la rappresentazione della conoscenza?

Scopriremo che sono troppo complessi e ci limiteremo a *linguaggi a regole* e *programmazione logica*.

## Ripasso, calcolo proposizionale

La *sintassi* definisce quali sono le frasi legittime del linguaggio:

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210319154930215.png" alt="image-20210319154930215" style="zoom:33%;" />
Assumiamo la precedenza degli operatori per omettere le parentesi:
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210319155040229.png" alt="image-20210319155040229" style="zoom: 33%;" />

La *semantica* ha a che fare col significato delle frasi: definisce se un enunciato è vero o falso rispetto ad una *interpretazione* (un mondo possibile).

Un'*interpretazione* definisce un valore di verità per tutti i simboli proposizionali.
Un *modello* è un'interpretazione che rende vera una formula o un insieme di formule.

Una formula è *conseguenza logica* di un insieme di formule KB se e solo se in ogni modello di KB anche $\alpha$ è vera:

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210319155654239.png" alt="image-20210319155654239" style="zoom:33%;" />

Ovvero se l'insieme dei modelli di KB è contenuto nell'insieme dei modelli di alpha.
In altre parole non è possibile interpretare i simboli coinvolti in modo da rendere falso $\alpha$ e veri tutti gli asserti in KB. Corrisponde al concetto di *ragionamento legittimo*. È un'estensione del concetto di *tautologia* visto nel calcolo proposizionale.

Esempio del Wumpus (o in altri termini, del cazzo):

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210319160651859.png" alt="image-20210319160651859" style="zoom:50%;" />

Le equivalenze logiche ci permettono di scambiare termini. 
A è *valida* (== *tautologia*) sse è vera in tutte le interpretazioni.
A è *soddisfacibile* sse esiste una interpretazione in cui A è vera. Da questo si deduce che A è valida sse notA è insoddisfacibile.

## Inferenza per PROP

Si basa sulla semantica.

??2 approcci:

- Model checking
  - una forma di inferenza che fa riferimento alla definizione di conseguenza logica enumerando i possibili modelli.
    È la trasposizione algoritimica della tecnica di scrivere le tabelle di verità.
- Algoritmi per la soddisfacibilità (SAT)
  - <img src="/home/ludo/.config/Typora/typora-user-images/image-20210319164807129.png" alt="image-20210319164807129" style="zoom:50%;" />
  - il problema della conseguenza logica può essere ricondotto a quello della soddisfacibilità di una frase logica composta da clausole
  - gli algoritmi sono molto più efficienti

### TT-entails

Enumera tutte le possibili interpretazioni di KB. 
Se soddisfa KB si controlla che soddisfa anche $\alpha$. Se si trova anche solo un'interpretazione che soddifa KB ma non $\alpha$ la risposta sarà no.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210319165147725.png" alt="image-20210319165147725" style="zoom:50%;" />

- La prima cosa è crearsi una *lista di simboli* che compaiono in KB e $\alpha$
- L'insieme vuoto che passo alla funzione TT-check-all conterrà il modello se va a buon fine.
- Se ho assegnato valori a tutti i simboli
  - se la KB è soddisfatta va a vedere se anche $\alpha$ è soddisfatta (nel modello)
  - else: vado avanti
- else: prendo il primo dei simboli e memorizzo i restanti simboli in un'altra lista
- ritorna l'AND della funzione in cui nel modello assegno da una parte P = true e nell'altro P=false

Solo dopo aver provato tutti i possibili assegnamenti possiamo rispondere se $\alpha$ è o meno conseguenza logica di KB.

### SAT, Algoritmi per la soddisfacibilità

Usano KB in *forma a clausole* (insieme di letterali). La forma a clausole è la *forma normale congiuntiva*, ovvero una congiunzione di disgiunzioni di letterali.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210319170413176.png" alt="image-20210319170413176" style="zoom:33%;" />

**Trasformazioni in clausole**
È sempre possibile ottenere la forma a clausole tramite *trasformazioni* che preservano l'equivalenza logica.  

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210319171740766.png" alt="image-20210319171740766" style="zoom: 33%;" />

Esempio:

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320104914753.png" alt="image-20210320104914753" style="zoom:50%;" />

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210319171910423.png" alt="image-20210319171910423" style="zoom: 33%;" />
L'ultimo passaggio è la forma a clausole, solo sintassi.

#### DPLL

Parte da una KB in forma a clausole. È un'enumerazione in profondità di tutte le possibili interpretazioni alla ricerca di un modello.

Ci sono 3 miglioramenti rispetto a TTentails:

- *terminazione anticipata*
  - interpretazioni parziali degli OR, se uno è vero basta quello
  - se una clausola è falsa => l'interpretazione non può essere un modello dell'insieme di clausole
- euristica dei *simboli puri*
  - simbolo puro: appare con lo stesso segno in tutte le clausole (rispetto al not)
  - i simboli puri possono essere assegnati a True se il letterale è positivo, False se negativo
  - in clausole già rese vere si può ignorare l'occorrenza del simbolo nel determinare se esso è puro o meno
  - l'assegnamento è obbligato; non perdo modelli utili
- euristica delle *clausole unitarie*
  - lo è se vi è un solo letterale non assegnato
  - conviene assegnare prima queste: True se positivo, False se negativo

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210319172700396.png" alt="image-20210319172700396" style="zoom:50%;" />

- si salva la lista delle *clausole* (in rappresentazione CNF, forma normale congiuntiva) e dei *simboli*
- Se  ogni clausola è vera nel modello ritorna True; se c'è qualche clausola falsa ritorna False
- troviamo un simbolo puro con relativo valore (True se positivo..)
  - richiama DPLL con questo assegnamento P=value
- trova una clausola unitaria con relativo valore
  - richiama DPLL con P=value
- si salva il primo simbolo fra quelli non assegnati e i restanti in 2 variabili
- ritorna l'OR delle due chiamate a DPLL con gli assegnamenti P=True e P=False

<img src="/home/ludo/Videos/DPLL.gif" style="zoom: 33%;" />

DPLL è completo e termina sempre.

**Metodi locali per SAT**
È un algortimo decidibile ma complesso. Si possono usare delle varianti più semplici.
Si usa una formulazione a stato completo (e non incrementale), si ha già un assegnamento completo.

Si parte da un assegnamento casuale; ad ogni passo si cambia il valore di un simbolo   proposizionale (*flip*).
Gli stati sono valutati contando il numero di clausole non soddisfatte.

Ci sono molti minimi locali e per sfuggire a questi serve introdurre perturbazioni casuali.
Walk-SAT è uno dei migliori (si possono usare Hill-climbing a riavvio casuale, Simulated Annealing..)

#### WalkSAT

Ad ogni passo: 

- sceglie a *caso* una clausola non ancora soddisfatto
- sceglie quale simbolo flippare con probabilità p (solitamente 0.5) tra e 2 seguenti strade:
  - passo *casuale*: sceglie un simbolo a caso
  - passo di ottimizzazione: sceglie quello che rende più clausole soddisfatte

Si arrende dopo un certo numero di flip.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210319182139882.png" alt="image-20210319182139882" style="zoom: 50%;" />

- inizialmente assegnamento casuale True/False
- facciamo al massimo *max_flips* iterazioni
  - se il modello soddisfa tutte le clausole allora ritorna il modello con gli assegnamenti
  - else: seleziona una clausola a caso
    - con probabilità p:
      - flip il valore di un simbolo a caso nella clausola
      - flip il il simbolo che massimizza il numero di clausole soddisfatte

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320092810772.png" alt="image-20210320092810772" style="zoom: 33%;" />

**Analisi di WalkSAT**
Ha senso solo per *l'efficienza*, ma posso applicarlo solo a proposizioni che so essere soddisfacibili.
Se max_flips=$\infin$ e l'insieme delle clausole è soddisfacibile prima o poi termina; ma se sono insoddisfacibili non termina. In più l'ipotesi di fare infinite iterazioni non è realistica.

Il problema è decidibile ma l'algoritmo non è completo. Non può essere usato per verificare l'insoddsifacibilità. 

**Problemi SAT difficile**
Se un problema è sottovincolato ha molte soluzioni. 
*?Come posso misurare quanto è vincolato un problema SAT?*
Conta il rapporto $\frac{m}{n}, m= \#clausole, n=\#simboli$. Più grande è il rapporto più vincolato è il problema.
Es. le regine sono facili perchè il problema è sottovincoalto.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320095041088.png" alt="image-20210320095041088" style="zoom: 67%;" />

La fascia 3-5.5 è la parte più interessante da studiare, oltre non è soddisfacibile.
In questa categoria il WalkSAT è molto più efficiente del DPLL.

## Inferenza come deduzione

Si usa un sistema di deduzione, basato su *sintassi* (mentre prima sfruttavo la semantica) sempre per decidere se A è conseguenza logica di KB.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320101003985.png" alt="image-20210320101003985" style="zoom:33%;" />

La deduzione avviene specificando delle regole di inferenza. Le regole dovrebbero derivare *tutte  e sole* le formule che sono conseguenza logica.

Una regola di inferenza è una legge che permette di derivare da uno o più asserti un altro asserto. L'applicazione di una regola di inferenza ad uno o più asserti dati è un passo di dimostrazione; e una dimostrazione è una sequenza di passi.

La dimostrazione è un concetto puramente *sintattico*, è indipendente da qualsiasi interpretazione, è una pura sequenza di trasformazioni simboliche.

È possibile ricondurre il concetto *semantico* di conseguenza logica al concetto puramente *sintattico* di dimostrazione.

**Proprietà delle regole di inferenza (desiderabili)** 

- *correttezza*
  - <img src="/home/ludo/.config/Typora/typora-user-images/image-20210320101347968.png" alt="image-20210320101347968" style="zoom:33%;" />
  - tutto ciò che è derivabile è conseguenza logica; le regole preservano la verità
  - l'applicazione di una regola ad un insieme di premesse deve garantire che la conclusione che se ne trae è effettivamente conseguenza logica di tali premesse
- completezza
  - <img src="/home/ludo/.config/Typora/typora-user-images/image-20210320101427714.png" alt="image-20210320101427714" style="zoom:33%;" />
  - tutto ciò che è conseguenza logica è deducibile; è una proprietà globale
  - se una formula è effettivamente conseguenza logica di un insieme di premesse l'insieme di regole deve garantire l'esistenza di una dimostrazione di tale fatto

Le regole di inferenza sono schemi deduttivi del tipo:  

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320101640446.png" alt="image-20210320101640446" style="zoom:33%;" />

Applicando regole di inferenze dimostro la formula. Esempio:

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320102207077.png" alt="image-20210320102207077" style="zoom: 50%;" /><img src="/home/ludo/.config/Typora/typora-user-images/image-20210320102232951.png" alt="image-20210320102232951" style="zoom: 33%;" />

*?Come decido ad ogni passo quale regola applicare? come evitare l'esplosione combinatoria?*
 È una problema di esplorazione in uno spazio di stati; una dimostrazione definisce la *direzione* della ricerca e la *strategia* della ricerca.

**Direzione della ricerca**
Conviene procedere all'indietro:

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320102635851.png" alt="image-20210320102635851" style="zoom:33%;" />

**Strategia di ricerca**
Ci interessa la *completezza e l'efficienza*.

- *completezza*
  - mi chiedo se le regole che sto usando sono un insieme di regole completo...;
  - nel calcolo proposizionale ne abbiamo 2 per ogni connettivo logico (1 per l'introduzione e 1 per l'eliminazione)
  - le regole della deduzione naturale sono un insieme di regole di inferenza completo
- *efficienza*
  - è un problema decidibile ma NP-completo

Cerchiamo un insieme di regole di inferenza *minimale*.

**Regola di risoluzione per PROP**
Un'unica regola: la regola di *risoluzione* (forma a clausole)

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320103140192.png" alt="image-20210320103140192" style="zoom: 50%;" />

È una regola corretta; meglio la notazione insiemistica così da eliminare duplicati.

**Regole di risoluzione in generale**
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320103435959.png" alt="image-20210320103435959" style="zoom: 33%;" />

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320112719033.png" alt="image-20210320112719033" style="zoom: 33%;" />

*?Siamo sicuri che basti solo la regola di risoluzione?*
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320133659808.png" alt="image-20210320133659808" style="zoom:50%;" />

**Teorema di risoluzione**
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320113406696.png" alt="image-20210320113406696" style="zoom: 50%;" />
Se la KB è insoddisfacibile posso ricavare da KB la clausola vuota e viceversa. È una garanzia di completezza. Ci viene in aiuto: 

**Teorema di refutazione**
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320113432121.png" alt="image-20210320113432121" style="zoom:50%;" />

unisco il $\lnot \alpha$ a KB e vedo se riesco a ricavare la clausola vuota per il teorema di risoluzione.

In sintesi: il metodo è completo se lo uso per *refutazione*.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320134358024.png" alt="image-20210320134358024" style="zoom:33%;" />

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320134439042.png" alt="image-20210320134439042" style="zoom: 33%;" />

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320113712375.png" alt="image-20210320113712375" style="zoom: 33%;" />

## FOL, Agenti logici

Si usa la *logica del prim'ordine*, logica dei predicati più ricca: oggetti, proprità e relazioni. 
Si deve decidere il livello di astrazione, contettualizzando:

- oggetti
  - identificati da simboli o funzioni
  - dominio del discorso: insieme oggetti rilveanti
- proprietà
- relazioni

Le concettualizzazioni sono infinite, è importante introdurre il giusto livello di astrazione:

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320152911288.png" alt="image-20210320152911288" style="zoom:50%;" />

Le relazioni restituiscono un valore di verità; le funzioni sono termini. 

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320153025130.png" alt="image-20210320153025130" style="zoom:33%;" />

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320153058493.png" alt="image-20210320153058493" style="zoom:33%;" />

Le funzioni sono *termini* e i predicati sono *formule*.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320153356019.png" alt="image-20210320153356019" style="zoom: 33%;" />

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320153457733.png" alt="image-20210320153457733" style="zoom:33%;" />

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320153550000.png" alt="image-20210320153550000" style="zoom:33%;" />

La *semantica* (dichiarativa) nella logica del prim'ordine consiste nello stabilire una corrispondenza fra 

- i termini del linguaggio e gli oggetti del mondo
- le formule chiuse e i valori di verità

Un'interpretazione stabilisce una corrispondenza precisa fra elementi atomici del linugaggio ed elementi della concettualizzazione

- simboli di costanti -> elementi del dominio
- simboli di funzione -> funzione da n-uple di D in D (D=?dominio del discorso)
- simboli di predicato -> insiemi di n-uple (relazioni)

**Semantica composizionale**
Una volta fissata un'interpretazione tutto il resto discende di conseguenza.
Il significato di un termine o di una formula composta è determinato in funzione del significato dei suoi componenti.

**Quantificatori**
Solitamente un $\forall$ si usa in accoppiata ad un $\implies$ per restringerne la portata (poche proprietà sono del tutto universali).

Un $\exists$ si usa insieme all'AND in genere (un implicazione sarebbe troppo debole).

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320155141728.png" alt="image-20210320155141728" style="zoom: 33%;" />

**Semantica database**
Nella logica standard dovrei..
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210320155421536.png" alt="image-20210320155421536" style="zoom:33%;" />

Nella semantica dei database (e di alcuni linguaggi per la rappresentazione della conoscenza):

- ipotesi dei *nomi unici*: simboli distinti $\implies$ oggetti distinti
- ipotesi del mondo chiuso: tutto ciò che non si sa che è vero è falso (soooo sad)
- chiusura del dominio: esistono solo gli oggetti di cui si parla

**Interazione con la KB in FOL**
 <img src="/home/ludo/.config/Typora/typora-user-images/image-20210320155750219.png" alt="image-20210320155750219" style="zoom: 33%;" />

La risposta dà un'esistenziale tipicamente è una serie di risposte (sì/no).

## Inferenza nel FOL

### Riduzione a inferenza proposizionale

### Il metodo di risoluzione per FOL

#### Trasformazione in forma a clausole

#### Unificazione

### Casi particolari: sistemi a regole

#### Backward chaining e programmazione logica

#### Forward chaining e basi di dati deduttive

#  Introduzione all’apprendimento automatico

## Paradigma,  “forme” e metodi dell’ apprendimento automatico

## Apprendimento induttivo di regole proposizionali

## Apprendimento supervisionato: classificazione e regressione (modelli lineari e instance based)

## **Apprendimento non supervisionato (clustering)**

## Validazione: tecniche e aspetti teorici

## Cenni a modelli dei paradigmi Bayesiano, simbolico, sub-simbolico

## Esempi di applicazioni.

# Esercitazioni

## Esercitazione 1

## Esercitazione 2

Per dire che un'euristica è ammissibile lo si deve dire per ogni stato iniziale, non per uno specifico. 
La h è una stima di distanza, perciò deve essere sempre >= 0 in tutti gli stati, e 0 sul goal.

La monotonicità è sulla f, non sulla h. È difficile trovare una funzione eurisitica ammissibile con una f non monotona. 

Un'euristica domina un'altra quando.. vince h2 perchè per ogni *stato iniziale s* h2(s)>= h1(s). 

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210322091237298.png" alt="image-20210322091237298" style="zoom: 50%;" />

# Bibliografia consigliata

- S. Russell, P. Norvig, “Intelligenza Artificiale: un approccio moderno", Prentice
  Hall, Terza edizione, 2010 (AIMA), http://aima.cs.berkeley.edu/
- T. Mitchell, Machine Learning, McGraw-Hill 1997

# Domande al prof

- sulla DF ad albero possiamo dire che una ricerca è completa solo se lo spazio degli stati è finito *e aciclico*. Se l'aciclità, dato un certo spazio degli stati, dipende dall'ordine di esplorazione, possiamo dire che l'algortimo è completo (in quello spazio) o l'ordine di esplorazione non influisce sulla definizione di completezza?
  - 



 