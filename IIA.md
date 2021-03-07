IIA: **Introduzione all'intelligenza artificiale**
CdL Informatica, a.a. 2020/21
*Prof. Alessio Micheli & Maria Simi*

---

[toc]

---

# Introduzione

*Lo scopo del corso è di far apprendere i concetti principali e i metodi che stanno alla base della progettazione e sviluppo di sistemi intelligenti.*
*Il corso introduce le tecniche di base per la realizzazione di agenti intelligenti e in particolare il paradigma di risoluzione dei problemi  come ricerca in uno spazio di stati, la rappresentazione della  conoscenza e il ragionamento automatico, i metodi e modelli di base  dell’apprendimento automatico.*

risolvere un puzzle: difficile o semplice? tool per il problem solving
face recognition: machine learning

intelligenza: strumento umano
AI: nuovo strumento umano, affiancare la nostra intelligenza a quella dell'IA

goal dell'ia: fornire strumenti potenti all'uomo

L'ia si occupa di costruire entità intelligenti, si occupa di una doppia sfida: comprensione e riproduzione del comportamento intelligente

Due tipi di approcci:

- analisi e comprensione di un fenomeno. psicologia cognitiva
  obiettivo: comprendere intelligenza umana
  metodo: costruzione di modelli computazionali, veririfica sperimentale
  criterio successo: risolvere i problemi con gli stessi processi dell'uomo

  **Intelligenza artificiale forte.** assunzione che tutta l'intelligenza può essere meccanizzata

- costruttivo, riprodurre artefatti
  obiettivo:
  criterio successo: risolvere il problema anche se diversamente dall'uomo

  **Intelligenza artificiale debole**, non tutta l'intelligenza può essere meccanizzata

**Definizione di IA**
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210216162723512.png" alt="image-20210216162723512" style="zoom: 33%;" />

IA: indagine tecnologica ed intellettuale a lungo termine che sono sia scientifici che pratici:

- costruzione di macchine intelligenti
- comprensione mediante modelli computazionali dei comportamenti viventi
- rendere il lavoro con il calcolatore altrettanto utile e facile che con persone collaborative ed esperte

fondamenti dell'IA: *filosofia, matematica, economia, neuroscienze, psicologia, informatica, linguistica, cibernetica*

AI: *general purpose technology*, tipo elettricita, stampa, pc...

prendiamo per buona la definizione di kurzweil, 1990:
*arte di creare macchine che svolgono funzioni che richiedono intelligenza quando svolte da esseri umani*

?*cosa vuol dire intelligente?*
Definizione di intelligenza, che piace a me:

> The role of intelligence is to determine the positive and negative potential of an event or factor which could have both positive and negative results. It is the role of intelligence, with the full awareness that is provided by education, to judge accordingly utilize the potential for one's own benefit or well-being.
>
> -Dalai Lama (*The heart of the Buddha's path*)

è una qualità intrinseca o un comportamento?

che tipi di capacità?

Test di Turing. 



<img src="/home/ludo/.config/Typora/typora-user-images/image-20210216163854696.png" alt="image-20210216163854696" style="zoom:33%;" />

Dopo 5 minuti di dialogo il test è concluso e l'interrogato dovrà dire se sta comunicando con un computer o con una persona.

## Breve storia

1943: primo lavoro sulle reti neurali

1956: logic theorist
capacità di ragionamento simbolico. Algebra simbolica e trasposizione in logica

Newell, Simon

1956-1969 grandi aspettative
Advice Taker, programma basato su conoscenza ed estensibile
Vari successi nei problemi giocattolo

1966-1974: dose di realismo
la manipolazione simbolica e sintattica non è adeguata per tutti gli usi.
Complessità di problemi troppo alta, intrattabili
Tutti di complessità esponenziale.
Limiti di rappresentazione delle reti neurali di tipo semplice
Rapporto Lighthill in UK: non vale più la pena investirvi

1969-1979: knowledge
Dominiamo complessità con conoscenza specifica del domini ed euristiche
Il collo di bottiglia è l'acquisizione di conoscenza
Il problema è la mancanza di *buon senso*. Difficoltà di codificare il senso comune.

*? Cos'è il senso comune?*
abilitá mentale che la maggior parte delle persone condividono. Coinvolge molte tipologie di rappresentazione e richiede un insieme più ampio di abilità.
Tipologie di rappresentazione: 	

progetto CYC(Lenat), codificare tutto lo scibile umano.
OpenMind: progetto più recente e meno ambizioso che accetta contribti via web. Fatti di senso comune via web

Grafi di conoscenza: estrarre conoscenza da big data (google graph..)

1995-ora: visione moderna (AIMA: AI a Modern Approach)
punto di svolta, agenti intelligenti che unisce vari settori dell'IA.
La visione moderna dell'IA è il fronte del progresso dei metodi/sistemi informatici (algoritmica, logica, ottimizzazione) per dotare le macchine di comportamente *razionali* (intelligenti) in problemi generali *difficili*.
L'accento è quindi posto sulla costruzione di agenti intelligenti.

## Agenti


Gli agenti sono situati, immersi in un ambiente. Ricevono percezioni da un ambiente. Agiscono sull'ambiente mediante *azioni*

Hanno *abilità sociali* (comunicare)

Hanno un corpo. Hanno opionioni, obiettivi, forse "hanno emozioni..."

Robocup: problema attuale fino al 2050 come banco di prova
calcio simulato: agenti individuali, no una 

Capacità di emozioni: importanti nella capacità di prendere decisioni

Narrow AI vs General AI
magazzini intelligenti, aspirapolveri intelligenti, guida automatica, sistemi di raccomandazione

AI revolution? 
IBM Watson, Project Debater.
L'IBM la chiama una grande sfida. 
BlueGene: genoma

*?L'intelligenza può essere estratta o inferita dai dati?*
Più dati maggiore l'accuratezza.. unreasonable effectiveness of big data

Reti neurali: solo dal 2011 si sono avuti successi evidenti. 
Cos'è successo? applicabile dal punto di vista computazionale, GPU efficienti...

DeepMind (società di Google), è in grado di imparare GO , anche da zero nel 2017 giocando da solo con tecniche di *reinforcement learning*.

AI: sorgenti di incertezza, sensori imperfetti. é la disciplina che si usa quando non sai cosa fare, quando l'approccio algoritmico tradizionale non è sufficiente.
*Gervasi: se non ci sorprende non è A.I.*

Machine Learning: come dotare sistemi di apprendimento automatico.
Learning is the core of intelligence, sia in biologia che in informatica

si dovrebbe dire un sistema di AI.
É difficile programmare l'intelligenza. 
DL e reti neurali sono sottocategorie di ML, che a sua volta è una sottocategoria dell'AI

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
Un *agente razionale* fa la cosa giusta secondo una certa misura. Interagisce con il suo ambiente in maniera efficace. É necessario quindi un *criterio di vautazione* oggettivo dell'effetto delle azioni dell'agente, una una misura della prestazione (ad es: il costo di un cammino minimo trovato). 

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

L'agente potrebbe essere anche una tabella, dove a uno stimolo associa un'azione a ogni possibile sequenza di percezioni.
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210219144440330.png" alt="image-20210219144440330" style="zoom:50%;" />

In IA vogliamo realizzare agenti razionali dotati di un programma *compatto*.

**Agenti reattivi**
Non c'è una storia da memorizzare. Semplicemente volta per volta procedo ad agire.
L'algoritmo restituisce un'azione poichè è il programma dell'agente, che ritorna agli attuatori.

**Agenti basati su un modello**
La regola viene estratta in base allo stato, che si aggiorna col tempo

**Agenti con obiettivo**
Aumenta la complessità, vogliamo aggiungere flessibilità. Mentre prima l'obiettivo era fissato dal programmatore (ovvero in modo abbastanza rigido) sarebbe comodo specificarlo a seconda del caso.
es. un cammino per raggiungere una certa destinazione

**Agenti con valutazione di attività**
Oltre all'obiettivo hanno anche una funzione di utilità. Permette di scegliere il miglior obiettivo da raggiungere, non tutti lo hanno lo stesso livello, potrebbero essere anche in conflitto.

**Agenti che apprendono**
L'architettura si semplifica grazie all'apprendimento, di adattarsi in manierza semi- automatica a quello che succede.
La permanenza dell'agente nell'ambiente
Il programma non è fissato ma può mutare in base all'esperienza che viene accumulata

**Tipi di rappresentazione dello stato**
Rappresentazione

- atomico: indivisibile, navigare in una mappa da una città all'altra

- *fattorizzata* : distanza fra stati, dare delle metriche, anche nel ML, dove le informazioni sono codificate in vettori di feature
- *strutturata*: la più sofisticata, rappresentiamo oggetti e relazioni fra questi oggetti, basati sulla logica (stiamo aggiungendo esplicitamente le relazioni)

IA come progettazione di agenti e programmi agente

Massima misura di prestazioni, classificazione dei problemi PEAS,
Dipendenza dalla lettura dell'ambiente. Tutti gli aspetti possono migliorarsi con l'apprendimento.

## Agenti risolutori di problemi

Agenti con modello, con obiettivo
Rappresentazione atomica dello stato
Immaginiamo che verrà eseguito l'intero piano

Tutto è nel dseign. É solo un'introduzione

Assunzioni:
Ambiente statico, osservabile, discreto, determinisitico
L'agente può eseguire il piano ad occhi chiusi 

Formulazione in 5 componenti:

- stato iniziale
- azioni possibili in esso
- modello di transizione (coppia <stato, azione> -> stato')

1,2,3 definiscono implicitamente lo *spazio degli stati*.

- test obiettivo
- costo del cammino: non è mai negativo

**Ricerca**: il processo che cerca una sequenza di azioni che raggiunge l'obiettivo
misura prestazioni: quanto costa trovare la soluzione, quanto
somma di 2 costi: costo della ricerca stessa e il costo (valutazione dell'algoritmo) del cammino soluzione. C'è un costo della ricerca e un costo della soluzione

## Esempi di formulazioni

Conoscenza implicita dell'ambiente: conosco solamente le azioni possibili nell'ambiente

Il grafo è bipartito 

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210219153132017.png" alt="image-20210219153132017" style="zoom:33%;" />

Le formulazioni possono avere costi diversi

- formulazione incrementale: 178.000 miliardi di stati
- formulazione incrementale 2: 2057 sequenze da considerare
  es. 3.6 dell'AIMA, radice cubica di n!
  ogni volta che aggiungete una regina 
- formulazione a stato completo: metto tutte le regine sulla scacchiera, una per colonna. Azione: sposta la regina se minacciata

**Dimostrazione di teoremi**
É una ricerca nello spazio degli stati. 
Albero di ricerca fra gli stati

Anche nei problemi reali

Si tengono 
Un nodo rimane foglia (rimane nella *frontiera*) fintanto che non si decide di espanderlo. 

# Risoluzione di problemi come ricerca

**Problem solving agent, search, **
In questo capitolo si considera un particolare tipo di agente *con obiettivo*, l'agente *problem-solving*. Essi pianificano in anticipo una sequenza di azioni che portano ad uno stato obiettivo. Il processo computazionale sottostante è chiamato *ricerca*.
Usa rappresentazioni **atomiche**, stati del mondo considerati come un'unità.

- formula il problema (parte non automatica)
- ricerca la soluzione nello spazio degli stati (automatico)

**Informed algorithms, uninformed algorithms**
Distinguiamo fra gli algoritmi con informazioni, dove l'agente può stimare la distanza dell'obiettivo, da quelli senza informazioni, dove questa stima non è disponibile.

La *ricerca* per un agente avviene prima di ogni azione da effettuare nel mondo reale. Esso deve simulare le sequenze di azione nel modello, cercando finchè non trova una sequenza di azioni che raggiunge l'obettivo, ovvero la *soluzione*.
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
*problemi standardizzati*: ha lo scopo di illustrara vari metodi di problem-solving e di essere un benchmark. 

*real-world problems*: le cui soluzioni sono effettivamente usate dall'uomo, la cui formulazione non è idiosincratica (*che influenza una particolare variabile e nessun’altra*), non standardizzata, poichè ogni robot e ogni ambiente differisce.

| standardized problems              | real-world problems           |
| ---------------------------------- | ----------------------------- |
| grid world(vaccum, sokoban puzzle) | route-finding                 |
| sliding-tile puzzle                | touring                       |
| 8-puzzle, 15-puzzle                | VLSI layout                   |
| Knuth 4                            | Robot navigation              |
|                                    | automatic assembly sequencing |
|                                    | protein design                |

*Knuth 4*: Knuth congettura che partendo dal numero 4, con una sequenza di radici quadrate, floor e fattoriali si può raggiungere ogni intero positivo desiderato, es: raggiungere 5 partendo da 4: 

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226130509906.png" alt="image-20210226130509906" style="zoom: 50%;" />

## Formulazione di problemi

## Algoritmi di ricerca

Un algortimo di ricerca prende in input un problema di ricerca e restituisce una soluzione o un fallimento. Consideriamo algoritmo che sovrappongono un albero di ricerca su un grafo dello spazio degli stati. Ogni nodo dell'albero di ricerca corrisponde a uno stato nello spazio degli stati.

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
Lo spazio degli stati descrivi i possibilmente infiniti insiemi di stati del mondo e le azioni che permettono transizioni da uno stato all'altro.
Nell'albero di ricerca un determinato stato (es. città di Oradea) può avere percorsi multipli per arrivarvi (e di conseguenza mutipli nodi che descrivono lo stesso stato), ma ogni nodo nell'albero ha un unico percorso che lo collega alla radice.

*espandere un nodo:* considerare tutte le azioni disponibili per quello stato (ad ogni nodo corrispone uno stato), ottenendo i risultati che queste azioni forniscono e generando nodi per ogni risultato

*generare un nodo figlio*: assegnare i valori di stato, padre, costo e azione generatrice.

*frontiera:* lista dei nodi in attesa di essere espansi (foglie dell'albero di ricerca); raggiunti ma non espansi. Essa è implementata come una coda con operazioni.

*reached table:* ogni stato che ha un nodo generato per esso è stato raggiunto, e quindi aggiunto alla tabella

*soluzione:* una sequenza di azioni forma un percorso, e una solzuione è un percorso dallo stato iniziale allo stato obiettivo. Una soluzione ottimale ha il più basso costo tra tutte le soluzioni.

**Ridondanza**
*repeated state*: anche se lo spazio degli stati è finito è possibile che stati si ripetano

*percorso ridondante*: un ciclo è solo un caso particolare di percorso ridondante. Ogni modo peggiore di raggiungere uno stato rispetto ad uno ottimo. 

> Gli algoritmi che non ricordano il passato sono destinati a ripeterlo

*3 approcci*

- Quando la tabella degli stati raggiunti entra in memoria e ci sono molti percorsi ridondanti la scelta preferita è ricordare tutti gli stati precedentemente raggiunti 
- In problemi in cui è impossibile o molto raro che due percorsi raggiungano lo stesso stato possiamo ignorare il problema (es. problemi di assemblaggio)
- si possono controllare i cicli evitando di controllare i percorsi ridondanti. Si possono controllare risalendo nella catena dei *parent* di ogni nodo; per efficienza si può scegliere di controllare solo i cicli brevi (3 generazioni sopra) e affidarsi ad altri meccanismi (come dei vincoli) per i cicli maggiori.

Diversi tipi di code corrispondono a diversi tipi di strategie di ricerca

- FIFO -> BF (Breadth First)
- LIFO -> DF (Depth First)
- Coda con priorità -> UC e altri successivi, dopo l'inserimento c'è un riordinamento; viene estratto il nodo a priorità più alta

**Cammini ciclici**
*I cammini ciclici rendono gli alberi di ricerca infiniti.*

Il problema della ridondanza si presenta anche in assenza di cicli. 
Su spazi di stati a grafo (abbastanza strani) si generano più volte gli stessi nodi nella ricerca.

*Visitare stati già visitati fa sprecare tempo o occupa spazio*. Ricordare gli stati già visitati occupa spazio ma ci consente di evitare di visitarli di nuovo.
*Gli algoritmi che dimenticano la loro storia sono destinati a ripeterla*.

In ordine crescente di costo e di efficacia abbiamo varie soluzioni (in ordine crescente di efficacia e costo):

- *Non tornare nello stato da cui si proviene*: si elimina il genitore dai nodi successori (non evita però tutti i cammini ridondanti)
- *Non creare cammini con cicli*: si controlla che i successori non siano antenati del nodo corrente
- Non *generare nodi con stati già visitati/esplorati*: O(s) dove s è il numero degli stati possibili

Ricerca su grafo: mantiene una lista dei nodi (stati) visitati/esplorati (*lista chiusa*)

*<u>graph search</u>:* se l'algoritmo di ricerca controlla per percorsi ridondanti, mantiene una lista degli stati esplorati. Prima di visitare un nodo controlla se lo stato corrispondente era già stato incontrato o è in frontiera.

*<u>tree-like search</u>:* se l'algoritmo di ricerca non fa questo controllo, scegliamo di vedere i nodi come in un albero accettando le ripetizioni degli stati (escludendo il padre dai successori).

Nella ricerca ad albero i successori (padre) vengono rigenerati!

La *frontiera* separa i nodi *esplorati* da quelli *non esplorati*. Ogni cammino dallo stato iniziale a inesplorati deve attraversare uno stato di frontiera.

### Best First Search

É un approccio molto generale, dove si sceglie dalla frontiera un nodo n con un valore minimo della funzione di valutazione f.

```pseudocode
function BEST_FIRST_SEARCH(problem, f) return solution || failure
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
É una ricerca completa anche in uno spazio degli stati infinito.
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
		
		foreach child in EXPAND(problem, node)
			// per ogni azione disponibile a partire dal nodo esplora i figli
			s = child.state
			
			if(problem.isGoal(s))
				return child
				
            if(s NOT IN explored && child NOT IN frontier)
            	explored.add(s)
				frontier.push(child)
			
			frontier.push(figlio)
    
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

Esplora sempte i nodi più profondi in frontiera. La ricerca poi torna sui suoi passi al nodo successivo più profondo che ha ancora successori non espansi.
É spesso implementata come una ricera ad albero dove non si tiene conto degli stati esplorati. Non è ottima, ritorna la prima soluzione che trova.

Viene utilizzata una coda LIFO, mettendo i successori in testa alla lista.
*Oss*: possiamo dimenticare rami completamente esplorati. 

**visita a grafo**
Si perdono i vantaggi della memoria, si torna a salvare in memoria tutti i possibili stati al caso pessimo. Diventa però una ricerca completa su uno spazio degli stati finito.

**versione ricorsiva**
Realizzato da un algortimo ricorsivo con *backtracking*. É ancora più efficiente in occupazione di memoria, mantiente solo il cammino corrente. Salva lo stato su uno stack a cui torna in caso di fallimento per fare altri tentativi.

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
É una ricerca *completa* per problemi in cui si conosce un limite superiore per la profondità della soluzione, ovvero se *d<l*. Non è ottimale ma completo. 
Si considerano tutti i nodi a profondità *l* come foglie, non si considerano i loro eventuali successori.

```pseudocode
function depth_limited_search_tree(problem, l) return solution || failure || cutoff
	node = problem.initial
	frontier = LIFOQueue([node])
	result = failure
	
	while(!frontier.isEmpty())
		node = pop(frontier)
		
		if(problem.isGoal(node.state))
			return node
			
        if(node.depth > l)
        	result = cutoff
        else if(!isCycle(node))
        	foreach child in EXPAND(problem, node)
        		frontier.push(frontier)
   	
   	return result // failure se i nodi vengono esauriti (quindi non per colpa del limite l)
	
```

É sempre una ricerca ad albero che controlla gli stati esplorati, per cui consuma poca memoria. Porta con sè il rischio di visitare lo stesso stato più volte su differenti percorsi. Se la funzione *isCycle(node)* non controlla la presenza di *tutti* i cicli l'algoritmo potrebbe bloccarsi in un loop.

I cicli corti sono bloccati dalla funzione *isCycle*, verosimilmente risalendo di qualche livello la catena di parentela del nodo, i cicli più lunghi dovrebbero essere gestiti dal limite *l*.

**Analisi**

| completezza       | ottimalità | tempo    | spazio         |
| ----------------- | ---------- | -------- | -------------- |
| no, solo se *d<l* | no         | $O(b^l)$ | $O(b \cdot l)$ |



### Approfondimento iterativo (ID)

É il miglior compromesso fra BF e DF. *Iterative deepening* è il metodo di ricerca non informata preferito quando lo spazio degli stati è più grande della memoria e la profondità della soluzione non è nota.

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

É ottimo se le azioni hanno tutte lo stesso costo. 

Come *breadth first* genera un livello per volta, la differenza è che *breadth first* salva in memoria i livelli, ID ripete i precedenti livelli in esecuzioni successive della *depth limited*. Al costo di più tempo salva memoria.

Potrebbe sembrare uno spreco di computazione che i primi livelli (specialmente) vengano rigenerati più volte, nella pratica la maggior parte dei nodi si trovano nei livelli più bassi.
I nodi al livello *d* sono generati 1 volta, quelli a (*d-1*) 2 volte, ...
Il numero dei nodi è pertanto dato da: $d(b) + (d-1)\cdot b^{2} + (d-2)\cdot b^3 ...  + b^d$ che asintoticamente è sempre $O(b^d)$, infatti: 

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210227170731593.png" alt="image-20210227170731593" style="zoom: 50%;" />

Sono abbastanza sicuro che sia completo anche su spazi degli stati infiniti (a patto che ci sia una soluzione chiaramente).

### Ricerca bidirezionale

Finora abbiamo assunto una ricerca in avanti, si può provare anche all'indietro.

Si procede nelle due direzione fino ad incontrarsi (si spera): in avanti dallo stato iniziale e all'indietro dallo stato obiettivo.
Si deve tener traccia di 2 frontiere  e 2 tabelle degli splorati. Quando le 2 frontiere collidono si ha una soluzione

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

Posso utilizare varie tecniche di ricerca. Assumiamo qui che si utilizza una *breadth first* o una *uniform cost*.

### Ricerca di costo uniforme (UC)

*É l'algortitmo di Dijkstra.* 
Quando le azioni hanno costi differenti una soluzione semplice è usare la *best first search* con funzione di valutazione il costo del percorso dalla radice al nodo corrente. 
L'idea è che l'algoritmo si espande in onde di *costo-percorso uniforme*, invece che onde di profondità uniforme (come per il *breadth first search*).

É una generalizzazione della ricerca in ampiezza: si sceglie il nodo di costo minore sulla frontiera.
Abbiamo 2 ingredienti principali: 

- coda con *priorita* (in cima i nodi di costo minore)
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
                	if(frontier.get(child).cost > child.cost)
            		frontier.delete(child)
            		frontier.push(child, child.cost)
	
```

Una volta che uno stato passa nello stato *esplorato* altri eventuali percorsi allo stesso stato saranno peggiori. 

**Analisi**

| completezza | ottimalità | tempo                                              | spazio                                             |
| ----------- | ---------- | -------------------------------------------------- | -------------------------------------------------- |
| completo    | ottimo     | $O(b^{1 + \lfloor \frac{C^*}{\epsilon} \rfloor })$ | $O(b^{1 + \lfloor \frac{C^*}{\epsilon} \rfloor })$ |

Assumendo che tutte le azioni abbiano un costo minimo > 0 l'agoritmo è completo e ottimo.

Assunto $C^*$ come il costo della soluzione ottima, $\lfloor \frac{C^*}{\epsilon} \rfloor$ è il numero di mosse al caso peggiore arrotondando per difetto.
Quando tutte le azioni hanno lo stesso costo UC somiglia a BF ma ha un costo di $O(b^{1+d})$, dovuta al goal-test posticipato. 

$O(b^{1 + \lfloor \frac{C^*}{\epsilon} \rfloor })$ può essere molto più grand di $O(b^d)$! Questo poichè l'algoritmo tende a esplorare larghe porzioni di albero che apparantemente sono ghiotte, ovvero con azione corrispondente di basso costo, prima di esplorare percorsi con un alto costo ma più utili.

### Panoramica

Versioni ad albero che non controllano stati ripetuti

![image-20210226115040724](/home/ludo/.config/Typora/typora-user-images/image-20210226115040724.png)



## Ricerca euristica 

In problemi di complessità esponenziale la ricerca esasutiva non è praticabile.
Usare una conoscenza a priori sul problema, una stima del costo futuro. Questa stima del costo futuro permette di evitare di generare  i cammini che non sono i più promettenti: *pruning*.

*eruistica (dal greco eureca):* riduce lo sforzo di fare una ricerca.
Sotto certe condizioni garantisce ottimalità e completezza

Funzione di valutazione euritisticaL h : n -> R
Si applica al nodo ma dipende soltando dallo stato

Prima invece dipendeva dal nodo! (più nodi per lo stesos stato)

f(n) = g(n) + h(n) // costo cammino + nuova funzione

esempio di euristica: segue una problem-specific-information
Sulla mappa della Romania, possiamo tenerci la distanza in linea d'aria da Bucharest, numero delle caselle fuoriposto nel gioco dell'8.

### Algortimi Best First

Best-first heuristic, stessa di UC ma al posto di g abbiamo f
Ad ogni passo si sceglie il valore del nodo sulla frontiera con valore *migliore*

### Greedy best-first

```pseudocode

```



In maniera ingorda seguo sempre il più promettente. Non trova l'ottimo sempre.

### Algoritmo A 

f(n) = g(n) + h(n) con h(n) >= 0 e h(goal) = 0

h(n) una stima del costo per raggiungere da n un nodo goal

Casi particolare dell'algoritmo A:

- Se h(n) =0 -> UC
- Se f(n) = 0 -> Greedy best-first

Il costo minimo deve essere > 0, di ogni azione, l'importante 

Teorema: l'algoritmo A con la condizione $g(n) \more$

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226142923234.png" alt="image-20210226142923234" style="zoom: 33%;" />

DIMO
Assumiamo che il percorso suluzione esista, che comprenda n'. Se n' sta sulla frontiera prima o poi sarà espanso. Questo è vero solo perchè esistono solo un numero finito di nodi x che possono essere aggiunti alla frontiera con $f(x) \leq f(n')$ per la condizione sulla crescita di g sul costo minimo degli archi.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226143121988.png" alt="image-20210226143121988" style="zoom:33%;" />

Ragioniamo meglio su h

### Algoritmo A*

L'oracolo che consideriamo è <img src="/home/ludo/.config/Typora/typora-user-images/image-20210226144230411.png" alt="image-20210226144230411" style="zoom:33%;" /><img src="/home/ludo/.config/Typora/typora-user-images/image-20210226143321846.png" alt="image-20210226143321846" style="zoom:33%;" />

É un oracolo, nessuno ce l'ha veramete, serve come valutazione ideale.
Si può andare in sottostima o in soprastima della soluzione (dist in linea d'aria). 

Definizione: *euristica ammissibile*
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226143518146.png" alt="image-20210226143518146" style="zoom:33%;" />

É una condizione lower-bound.
Anche BF con passi a costo costante e UC sono ottimali (h(n) = 0)

Th. gli algoritmi A* sono ottimali.
Vantaggio: non ci perdiamo il percorso ottimo, e per il pruning

La cosa migliore è ciò che non facciamo!

**Osservazioni su A***

- Abbandoniamo cammini che vanno troppo in profondità. 
- Una sottostima di h può farci compiere del lavoro inutile, ma non ci fa perdere il cammino migliore. 
- Una soluzione che va in sovrastima può farci perdere la soluzione ottimale (taglio causa sovrastima ma poteva esser buono, non posso recuperarlo)

**Ottimalità di A***
In caso di ricerca su albero ok
In caso su grafo si ah bisogno
Il rischio è di scartare candidati ottimi per averli già incontrati (visita a grafo tiene conto del passato), potrebbe essere uno nuovo buono ma potrebbe sparire.

Abbiamo bisogno della *consistenza (monotonicità)*
Dobbiamo avere la garanzia che il primo espanso sia il migliore.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226144935193.png" alt="image-20210226144935193" style="zoom:33%;" />

disuguaglianza triangolare (vari alg. di routing)
Se h è consistente la f non decresce mai lungo i cammini. Si fa prima passare da n a goal che passare per un nodo intermedio. 

Attraverso una strada che costa c non devo avvicinarmi più di quanto sia in linea d'aria.

**Proprietà**
Un'euristica monotona è ammissibile.
Esistono euristiche ammissibile che non sono monotone (ma rare)
Le eur. monotone garantiscono che la soluzione meno costoso venga trovata per prima e quindi sono ottimali anche nel caso di ricerca su grafo.

Potevo anche reinserire i nodi in frontiera. Serve lo stesso perchè dobbiamo gestire la frontiera per tenerla pulita.

**Dimostrazione ottimalità**
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226145711503.png" alt="image-20210226145711503" style="zoom: 33%;" />

a tale nodo = 
dimo per assurdo
Lo si ripete per tutti i nodi fino al goal. C* = costo cammino ottimo

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226150756701.png" alt="image-20210226150756701" style="zoom:33%;" />

Allunghiamo ellissoidi sul cammino ottimo. 

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226151056205.png" alt="image-20210226151056205" style="zoom:33%;" />

esempio è UC.
**Riassunto**
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226151220115.png" alt="image-20210226151220115" style="zoom:33%;" />

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226151234040.png" alt="image-20210226151234040" style="zoom:33%;" />

In memoria il footprint resta $O(b^{d+1})$ per 
A* è una generalizzazione di Dijkstra 

### Costruire le euristiche di A*

Come faccio? Efficienza dipende da quanto è informata l'euristica (grado di informazione posseduta).


caso estremo di un'euristica: UC, costa tantissimo.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226152611047.png" alt="image-20210226152611047" style="zoom:33%;" />

fattore di diramazione effettiva b*
Più gli 
Sperimentalmente una buona euristica ha un b* vicino ad 1, < 1.5

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210226153114092.png" alt="image-20210226153114092" style="zoom:33%;" />

Capacità di esplorazione, migliorando di poco l'euristica si riesce a parità di nodi espandi raggiungere profondità maggiore (= vincere).

![image-20210228120714089](/home/ludo/.config/Typora/typora-user-images/image-20210228120714089.png)

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210305155748851.png" alt="image-20210305155748851" style="zoom:50%;" />



### Inventiamo un'euristica
Alcune strategie: 

- rilassamento del problema: viaggiare in linea diretta (es. rilasciare il vincolo delle strade), supergrafo rispetto al grafo dello spazio degli stati originale, dove si aggiungono archi in più
- Masimizzazione euristiche
- euristiche da sottoproblemi, database di pattern, memorizzare sottoproblemi..
  - pattern disgiunti: le soluzioni ai sottoproblemi interferiscono (condividono alcune mosse), la somma delle euristiche non è ammissibile! (potremmo sovrastimare avendo aiuti mutui). euristiche additive.
- apprendere dall'esperienza: fa girare il programma raccogliendo dati. algoritmi di apprendimento induttivo, ci facciamo guidare alla soluzione dalle caratteristiche salienti dello stato
- combinazione di euristiche: combinazione lineare, il peso dei coefficienti può essere aggiustato con l'esperienza, apprendendo automaticamente

### Algoritmi evoluti basati su A*

- Beam search
- IDA*
- RBFS
- MA*, SMA*

#### Beam search

Nel Best First viene tenuta tutta la frontiera, si può tagliare. Si tiene ad ogni passo solo i *k* nodi più promettenti, dove *k* è l'ampiezza del raggio (beam). 
Non è completa. 

#### IDA*

Combina A* con ID. È un po' geniale, ad ogni iterazione si ricerca in profondità con un limite *cut-off*. Tiene conto di f (e non dalla profondità).

Il limite *f-limit* viene aumentato ad ogni iterazione, fino a trovare la soluzione.

In memoria abbiamo O(bd). Se il nuovo f-limit = min. valore f dei nodi generati ed esclusi all'iterazione precedente. 

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
???? Tutti gli elementi (da configurare) della soluzione sono nello ???stato?? ma alcuni vincoli sono violati????
*es. le 8 regine* (non è importante il cammino per arrivare alle 8 regine senza interferenze ma solo arrivare a quell'obiettivo -> non dobbiamo salvarci il cammino).

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

### Ricerca in salita (Hill climbing)

Ricerca locale greedy.
L'albero di ricerca non viene salvato in memoria. 
Ci sono 3 tipi, a seconda della scelta del nodo che migliora la valutazione dello stato attuale:

- hill climbing *a salita rapida*: il migliore
- hill climbing *stocastico*: a caso tra quelli che salgono
- hill climbing *con prima scelta*: il primo

Se non ci sono successori migliori l'algoritmo termina con fallimento.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210302162148391.png" alt="image-20210302162148391" style="zoom:50%;" />

Non c'è frontiera, si tiene 1 solo stato. Si prosegue solo se il vicino è migliore dello stato corrente (se tutti i vicini sono peggiori si ferma). Miglioriamo finchè posssiamo, finchè tutti i successori non sono migliori ci fermiamo.
Tempo: variabile, numero cicli in base al punto di partenza. Finchè salgo vado (non è troppo smart).

Nell'esempio delle 8 regine: 
Si cerca *una* configurazione che ci dia la soluzione. 
Si blocca l'86% delle volte. In media servono solo 4 passi per la soluzione e 3 quando si blocca.
La trova rapidamente ma spesso si blocca, e nel caso lo fa rapidamente.

h = euristica di costo della funzione obiettivo da minimizzare

Problemi di Hill-climbing, in cui fallisce.

- massimi locali, spalle (pianori), crinali

es. romania greedy -> non si presta alle assunzioni dell'hill-clioming: non salviamo albero di ricerca

**Miglioramenti**

- consentire un numero limitato di mosse laterali (per scavallare pianure ecc..) 

  - l'alg delle 8 regine ha successo al 94% ma ci impeiga 21 passi in media

- hill-climbing stocastico: si sceglie a caso tra le masse in salita (tenendo conto della pendenza)

  - converge più lentamente

- hill-climbing con prima scelta

  - <img src="/home/ludo/.config/Typora/typora-user-images/image-20210302163825680.png" alt="image-20210302163825680" style="zoom:33%;" />

- hill-climbing con *riavvio casuale (random restart)*: riparte da un punto scelto a caso, non mi dispero e riprovo da una configurazione casuale tanto in poche mosse mi accorgo eventualmente di aver fallito

  - 1/p ripartenze se la probabilità di successo è p

  - es. regine: 6 fallimenti e 1 di successo, 0.14; in un caso di 3mln di regine ci impiega meno di 1 minuto

  - tendenzialmente è completo (quasi un brute-force, insistendo).

  - dipende molto dalla configurazione dei problemi se funziona o meno (NP-Hard, molti minimi locali; il problema è spinoso.. porcospino)

    <img src="/home/ludo/.config/Typora/typora-user-images/image-20210302164341899.png" alt="image-20210302164341899" style="zoom:33%;" />

### Simulated Annealing (tempra simulata)

Analogia: processo di tempra dei metalli in metallurgia (*cross-fertilization* fra settori scientifici apparentemente sconnessi).
Combina *hill-climbing* con una scelta stocastica (non del tutto casuale).

![image-20210302164615605](/home/ludo/.config/Typora/typora-user-images/image-20210302164615605.png)

La temperatura decresce col progredire dell'algoritmo, rendendo improbabili le mosse peggiorative.

Ad ogni passo scelgo sempre un successore n' a caso

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210302164659516.png" alt="image-20210302164659516" style="zoom: 33%;" />

Se non migliora, invece di scartarlo, gli diamo una chance. Guardiamo il DELTA dell'energia, se è <0 stiamo nella salita, stiamo peggiorando. La probabilità è inversamente proporzionale al peggioramento $p=e^{\frac {\Delta E} {T}}$

Abbiamo un altro fattore: probabilità guidata da questo come funziona l'alg. 

Altro parametro: temperatura, decresce col progredire dell'algoritmo.
È bene tornare indietro! 

La probabilità di una mossa in discesa col tempo e l'algortimo si comporta empre più come l'hill climbing

Soluzione ottimale: se T viene decrementato abbastanza lentamente con prob. tendente ad 1

*pensa a valori estremi di T, che tipi di Hill-climbing si ottengono?*
Variando i parametri otteniamo i tipi di HC di prima.

Sperimentalmente il valore di T è tale che per valori medi di $\Delta E$, la p sia circa 0.5

### Local beam

spartano: tiene solo i k migliori, dove k è l'ampiezza del raggio (beam). 
É la versione locale della *beam search*. (sopra)
Si tengono in memoria *k* stati, anzichè uno, e ad ogni passo si generano i successori di tutti i k stati. 
Ci portiamo avanti k successorri insieme. Non ripartiamo da zero ogni volta. Non è né il beam-search di prima (no frontiera) né il k-restart.

Parliamo dei prossimi k appena generati, appena visitati!
 <img src="/home/ludo/.config/Typora/typora-user-images/image-20210302165945170.png" alt="image-20210302165945170" style="zoom:33%;" />

K=1 => hill-climbing 

K = illimitato => secondo me UC, secondo lui BF

**Beam search stocastica**
Vorremmo diversificare un po'. Si introduce un elemento di casualità! Selezione naturale..
Si scelgono k successori, ma con probabilità maggioreper i migliore

organismo: al posto dello stato

progenie: successori
fintess: il valore della f, per cui la nostra progenie avrà probabilità di sopravvivere.



### Algoritmi genetici

Sono varianti della *beam search stocastica* in cui gli stati successori sono ottenuti combinando due stati genitore (anzichè per evoluzione).

*stati*: popolazione di individui
*fitness*: 
*accoppiamenti + mutazione genetica*:
*generazioni*

Inizialmente si hanno k stati/individui generati casualmente. Ogni individuo è rappresentato come una stringa.
Gli individui sono valutati da una *funzione di fitness*. (es. n° coppie di regine che non si attaccano), ci dicono quanto quell'individuo è migliore.

Si selezionano gli individui per gli accoppiamenti con una probabilità proporzionale alla fitness.
Le coppie danno vita alla generazione successiva combinando materiale genetico (*crossover*) e con un meccanismo aggiuntivo di mutazione genetica casuale.
La cosa si ripete fino ad ottenere stati abbastanza buoni.

Il punto critico di questi algoritmi è la rappresentazione del problema in stringhe. 

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210302171254699.png" alt="image-20210302171254699" style="zoom:33%;" />

Estratte in modo stocastico, in base al fitness.
Crossing-over del DNA (elemento di stocasticità) più mutazione casuale.

Tende al miglioramento della specie, all'accrescimento della fitness.
La nuova fitness non è correlata, va ricalcolata.

*natural computing:* swarm computing
Come le formiche ottimizzano il percorso? tutte partono alla ricerca di cibo, se più formiche scoprono 
Ogni formica nel percorso rilascia una sostanza chimica, seguono quello col maggior intensità di sostanza. Percorso ottimo! (1:28:00)

Etologia!

Tendenza a salire della beam stocastica, interscambio info tra thread paralleli di ricerca (blocchi utili che si combinano).
Funziona meglio se il problema ha componenti significative rappresentabili in sottostringhe.

punto critico: rappresentazione delle info in stringhe.

### Spazi continui

Sono problemi difficili in principio ma gli algortimi di ricerca locale ci funzionano molto bene.
Molti casi reali hanno spazi di ricerca continui. (es. Machine Learning)

Stato descritto da var. continue, vettore x, $x_1, ..., x_n$.
Per ogni posizione abbiamo infiniti punti in cui muoverci. Abbiamo strumenti matematici interessanti
Lo strumento principale è il *gradiente*. Se la f è continua e differenziabile, il minimo o massimo si può cercare utilizzando il gradiente, che restituisce la direzione di massima pendenza nel punto.

Gradiente: derivata parziale di f su ogni componente del vettore, si ha un vettore di derivate.
Hill-climbing iterativo: $x_{new} = x \pm  \eta  $

Quantifica lo spostamento senza cercarlo tra gli infiniti possibili successori.
Abbiamo una *bussola* fondamentale, ci dice dove andare e di quanto. Quantifica la pendenza della cruva.
Arriviamo quando.. il gradiente è nullo e altro boh

Non sempre è necessario il min/max assoluto: vedremo nel ML.

Se voglio il minimo (minimizzazione) uso meno. 

$\eta$ è il passo.

Idea dell'algortimo che controlla le reti neurali oggigiorno (sgd, stocastic gradient descent).

### Ambienti più realistici

Si considerano azioni non deterministiche, le percezioni sono importanti. L'agente può elaborare una strategia più che un piano, un piano con *contingenza*. 

**Aspirapolvere: azioni non deterministiche**
Sono necessarie variazioni al modello. L'agente non sa in che stato si troverà alla fine dell'azione.
Agiamo di conseguenza alle percezioni

### Aberi di ricerca AND/OR

Si creano dei nodi OR, le scelte dell'agente (fare 1 sola azione)
Nodi AND, le diverse contingenze (le scelte dell'ambiente, più stati possibili), da considerare tutte

Una soluzione è un albero! che

- ha un nodo obiettivo in ogni foglia
- OR
- AND

Se non avesse AND sarebbe un percorso normale come prima.

## Giochi con avversario

Assumiamo che l'ambiente in questo caso sia

- osservabile
- deterministico
- multi-agente

Adottiamo una rappresentazione degli stati non più atomica, ma più complessa.

1. Giochi con avversario, dove i piani devono tenere conto delle mosse dell'avversario
2. I problemi di soddisfacimento di vincoli, dove lo stato ha una struttura *fattorizzata*
3. I sistemi basati su conoscenza: lo stato è una base di conoscenza a cui rivolgere domande sul mondo, rappresentato in un *linguaggio espressivo*
   Si utilizzano calcolo proposizionale (PROP) e logica del prim'ordine (FOL)

**Giochi con avversario**

- Le regole risultano essere semplici e formalizzabili
- l'ambiente è *accessibile*, deterministico, multi-agente competitivo
  - ciò rende tutto più strategico e si hanno vincoli in tempo reale obbligando a trovare la mossa migliore nel tempo disponibile
- Ci sono 2 giocatori che giocano a *turni alterni*, a *somma zero: *
- l'informazione è perfetta

**Ciclo: *pianifica-agisci-percepisci***

**Giochi come problemi di ricerca**
*Stati:* configurazione del gioco (es. player(s): a chi tocca muovere nello stato s)
*Stato iniziale**
**Actions*(s): mosse legali in s
*Result*(s, a): lo stato risultante dalla mossa *a* nello stato *s*
*Terminal-test*(s): determina la fine del gioco
*Utility*(s, p): funzione di utilità, valore numerico che valuta gli stati terminali del gioco per *p* (es. conteggio punti)

### MIN-MAX

**Ricorsivo**

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210305180704404.png" alt="image-20210305180704404" style="zoom:50%;" />

**Analisi**

| tempo    | spazio |      |
| -------- | ------ | ---- |
| $O(b^m)$ | $O(m)$ |      |

É improponibile un'esplorazione sistematica del grafo degli stati se non per giochi semplici, ad es. gli scacchi richiedono $35^{100}$ mosse, con un grafo che arriva a $10^{40}$ nodi.

Sono necessarie delle euristiche per stimare la bontà dello stato del gioco.

**Min-Max euristico (con orizzonte)**
In casi più complessi occorre una funzione di valutazione euristica dello stato, *Eval(s)*.
Si guardani in avanti *d* livelli.

La *funzione di valutazione Eval* è una stima dell'utilità attesa a partire da una certa posizione. La sua qualità è fondamentale, deve:

- essere consistente con l'utilità se applicata a stati terminali del gioco
- essere efficiente
- riflettere le probabilità effettive di vittoria

*Stato non quiescente*: l'esplorazione fino a un certo livello può mostrare una situazione molto vantaggiosa.

*Effettivo orizzonte*: può accadere che vengano privilegiate mosse diversive aventi il fine di spingere il problema oltre l'orizzonte

**Per ottimizzare..**
*?Abbiamo bisogno necessariamente di esplorare ogni cammino?*
No, esiste un modo per dimezzare la ricerca pur mantenendo la decisione min-max ottima.

### Giochi senza esplorazione esaustiva

### ALFA-BETA

Tecnica di *potatura*: per ridurre l'esplorazione dello spazio di ricerca in algoritmi min-max.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210305181051193.png" alt="image-20210305181051193" style="zoom: 33%;" />![image-20210305181103451](/home/ludo/.config/Typora/typora-user-images/image-20210305181103451.png)

![image-20210305181103451](/home/ludo/.config/Typora/typora-user-images/image-20210305181103451.png)

**Ordinamento delle mosse**
La potatura ottimale si ottiene quando ad ogni livello sono generate prima le mosse migliori per  chi gioca.

**Analisi**
Complessità $Ob^{m/2}$.

**Come ordinare**

- *Approfondimento iterativo*
  - si scoprono in una iterazioni informazioni utili per l'ordinamento delle mosse da usare in una successiva iterazione
- Tabella delle trasposizioni
  - per ogni stato incontrato si memorizza la sua valutazione

**Miglioramenti**

- *Potatura in avanti*: beam search
- Database di mose di apertura e chiusura

### Cenni a giochi più complessi

Giochi con ambiente stocastico, parzialmente osservabile e deterministici.

## CSP: Soddisfacimento di vincoli

Esempio di rappresetazione *fattorizzata*. Dei problemi reali sono il layout dei circuiti, lo scheduling ...

Strategie per CSP:

- euristiche specifiche
- restringere domini, propagazione di vincoli
- backtracking intelligente

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210305182848605.png" alt="image-20210305182848605" style="zoom:50%;" />

**Scelta delle variabili**

- MRV(Minimum Remaining Values): si sceglie la variabile più vincolata, che ha meno valori legali residui, strategia *fail first*.
- Euristica del grado: a parità di MRV, sceglie la var. coinvolta in più vincoli, la più vincolante

**Scelta dei valori**

- Valore meno vincolante: quello che esclude meno valori per le altre variaibili direttamente collegate con la var. scelta

**Propagazione di vincoli**

- Verifica in avanti, *Forward Checking*
- Consistenza di nodo e d'arco

Backtracking cronologico vs intelligente

Metodi CSP locali

**Min-conflicts**

# Rappresentazione della conoscenza e ragionamento

## Il problema fondamentale della rappresentazione della conoscenza: espressività e complessità computazionale

## Algoritmi efficienti per la soddisfacibilità

## Deduzioni automatica: il metodo di risoluzione

## Sistemi a regole: basi di dati deduttive e programmazione  logica

## Rappresentazioni strutturate (frames, semantic networks)

#  Introduzione all’apprendimento automatico

## Paradigma,  “forme” e metodi dell’ apprendimento automatico

## Apprendimento induttivo di regole proposizionali

## Apprendimento supervisionato: classificazione e regressione (modelli lineari e instance based)

## **Apprendimento non supervisionato (clustering)**

## Validazione: tecniche e aspetti teorici

## Cenni a modelli dei paradigmi Bayesiano, simbolico, sub-simbolico

## Esempi di applicazioni.

# Bibliografia consigliata

- S. Russell, P. Norvig, “Intelligenza Artificiale: un approccio moderno", Prentice
  Hall, Terza edizione, 2010 (AIMA), http://aima.cs.berkeley.edu/
- T. Mitchell, Machine Learning, McGraw-Hill 1997

# Domande al prof

- sulla DF ad albero possiamo dire che una ricerca è completa solo se lo spazio degli stati è finito *e aciclico*. Se l'aciclità, dato un certo spazio degli stati, dipende dall'ordine di esplorazione, possiamo dire che l'algortimo è completo (in quello spazio) o l'ordine di esplorazione non influisce sulla definizione di completezza?
  - 



 