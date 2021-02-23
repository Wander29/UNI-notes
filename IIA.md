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

# Agenti intelligenti

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

# Risoluzione dei problemi come ricerca

**Problem solving agent, search, **
In questo capitolo si considera un particolare tipo di agente *con obiettivo*, l'agente *problem-solving*. Essi pianificano in anticipo una sequenza di azioni che portano ad uno stato obiettivo. Il processo computazionale sottostante è chiamato *ricerca*.
Usa rappresentazioni **atomiche**, stati del mondo considerati come un'unità.

**Informed algorithms, uninformed algorithms**
Distinguiamo fra gli algoritmi con informazioni, dove l'agente può stimare la distanza dell'obiettivo, da quelli senza informazioni, dove questa stima non è disponibile.

**Goal formulation, Problem formulation**

**Search, solution, execution**

**Open loop, closed loop**

Uno nodo n è una struttura dati:

```pseudocode
struct node {
	padre
}
frontiera = coda %lista dei nodi in attesa di essere espansi
```

Diversi tipi di strategie di ricerca: 

- FIFO -> BF (Breadth First)
- LIFO -> DF (Depth First)
- Coda con priorità -> UC e altri successivi, dopo l'inserimento c'è un riordinamento

## Strategie non informate

Per valutarle terremo conto di:

- completezza: se esiste una soluzione, trova sempre la soluzione
- ottimalità: trova la soluzione migliore, con consto minore
- complessità in tempo
- complessità in spazio

### Ricerca in ampiezza (BF)

Esplora il grafo dello spazio degli stati a livelli progressivi di stessa profondità.

```python
def breadth_first_search(problem): """Ricerca-grafo in ampiezza"""
	explored = [] # insieme degli stati gia' visitati (implementato come una lista)
    node = Node(problem.initial_state) 
    
    	# il costo del cammino e' inizializzato nel costruttore del nodo
    if problem.goal_test(node.state):
    	return node.solution(explored_set = explored)
    
    frontier = FIFOQueue() # la frontiera e' una coda FIFO
    frontier.insert(node)
    
    while not frontier.isempty(): # seleziona il nodo per l'espansione
        node = frontier.pop()
        explored.append(node.state) # inserisce il nodo nell'insieme dei nodi esplorati
        
        for action in problem.actions(node.state):
        	child_node = node.child_node(problem,action)
        if (child_node.state not in explored) 
        	and (not frontier.contains_state(child_node.state)):
                if problem.goal_test(child_node.state):
                	return child_node.solution(explored_set = explored)
       	 	# se lo stato non e' uno stato obiettivo allora inserisci il nodo nella frontiera
       		frontier.insert(child_node)
    return None # in questo caso ritorna con fallimento

```

Una volta generati i nodi sono *goal-tested*.
Non partiamo conoscendo gli stati, quindi non ci segniamo lo stato *esplorato* nelle informazioni dei nodi.

**Analisi di complessità**
**b** = fattore di ramificazione, *branching* (numero max di successori)
**d** = profondità del nodo obiettivo più superficiale (la prima che troviamo va bene)
**m** = lunghezza massima dei cammini nello spazio degli stati (nel caso dovessimo andare lunghi)

| completezza | tempo    | spazio   | ottimalità                                          |
| ----------- | -------- | -------- | --------------------------------------------------- |
| completa    | $O(b^d)$ | $O(b^d)$ | ottima se gli operatori hanno tutti lo stesso costo |

Complessita nel tempo: nodi generati, ogni livello 
Il numero dei nodi cresce esponenzialmente.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210223163857970.png" alt="image-20210223163857970" style="zoom: 25%;" />

La memoria è il fatto più incisivo, ingestibile.

### Ricerca in profondità (DF)

LIFO, mette i successori in testa alla lista.
Esplora il grafo dello spazio degli stati scavando in profondità. Quando sto ad un certo nodo, so che ho scoperto
Notare che possiamo dimenticare rami completamente esplorati. 

**versione su albero, Analisi complessità**

| completo                                       | ottimo | tempo                                  | spazio   |
| ---------------------------------------------- | ------ | -------------------------------------- | -------- |
| no, ci si può infilare <br />in possibili loop |        | $O(b^m)$ che può essre<br />> $O(b^d)$ | $O(b*m)$ |

**visita a grafo**
Si perdono i vantaggi della memoria, si torna da b*m a tutti i possibili stati, DF diventa così completa (se lo spazio degli stato è finito). Resta *non completa* in spazi infiniti.

**versione ricorsiva**
Realizzato da un algortimo ricorsivo con backtracking. É ancora più efficiente in occupazione di memoria, mantiente solo il cammino corrente.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210223165319883.png" alt="image-20210223165319883" style="zoom:33%;" />

``` python
def recursive _depth_first_search(problem, node):
"""Ricerca in profondita' ricorsiva """
# controlla se lo stato del nodo e' uno stato obiettivo
if problem.goal_test(node.state):
return node.solution()
# in caso contrario continua
for action in problem.actions(node.state):
child_node = node.child_node(problem, action)
result = recursive_depth_first_search(problem, child_node)
if result is not None:
return result
return None #con fallimento

```

### Ricerca in profondità limitata (DL)

Si va in profondità fino ad un certo livello predefinito *l*. É una ricerca *completa* per problemi in cui si conosce un limite superiore per la profondità della soluzione, completo se d<l. Non ottimale ma completo. 

**analisi**

|                 |            |          | spazio         |
| --------------- | ---------- | -------- | -------------- |
| completo se d<l | non ottimo | $O(b^l)$ | $O(b \cdot l)$ |

É il miglior compromesso fra BF e DF.
mi sono perso ID!


Finora abbiamo assunto una ricerca in avanti, si può provare all'indietro. Si preferisce qunado l'obiettivo è chiaramente definito (theorem proving) o si possono formulare una serie limitata di ipotesi. 
Si parte dal goal perchè lo si conosce, non si conosce il cammino.

### Ricerca bidirezionale

Si procede nelle due direzione fino ad incontrarsi.
**analisi**

|      |      |                    |                    |
| ---- | ---- | ------------------ | ------------------ |
|      |      | $O(b^\frac{d}{2})$ | $O(b^\frac{d}{2})$ |



### Cammini ciclici

I cammini ciclici rendono gli alberi di ricerca infiniti.
**Ridondanze**
Il problema si presenta anche in assenza di cicli. Su spazi di stati a grafo si generano più volte gli stessi nodi nella ricerca.
*Visitare stati già visitati fa sprecare tempo o occupa spazio*. Ricordare gli stati già visitati occupa spazio ma ci consente di evitare di visitarli di nuovo.
*Gli algoritmi che dimenticano la loro storia sono destinati a ripeterla*.

In ordine crescente di costo e di efficacia:

- *Non tornare nello stato da cui si proviene*: si elimina il genitore
- *Non creare cammini con cicli*: si controlla che i successori non siano antenati del nodo corrente
- Non *generare nodi con stati già visitati/esplorati*: O(s) dove s è il numero degli stati possibili

Ricerca su grafo: mantiene una lista dei nodi (stati) visitati/esplorati (*lista chiusa*)
Vorremmo un algoritmo che fa una ricerca smart, un *pruning*, non generare neanche i nodi che non portano alla soluzione. Ottimale solo se abbiamo la garanzia che il costo del nuovo cammino sia maggiore o uguale.

La *frontiera* separa i nodi *esplorati* da quelli *non esplorati*.

### Ricerca di costo uniforme (UC)

Generalizzazione della ricerca in ampiezza (costi diversi tra passi): si sceglie il nodo di costo minore sulla frontiera
Abbiamo 2 ingredienti principali: coda con priorita (in cima i nodi di costo minore), goal-test posticipato (tipico per coda con priorità), costa di più ma serve per l'algoritmo con priorità i nmodo da trovare ottimalità.

Se incontro un nodo il cui stato è gia in frontierà con costo più alto allora il nuovo figlio è migliore.
**Analisi costo uniforme**

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210223174327737.png" alt="image-20210223174327737" style="zoom:33%;" />



## Formulazione di problemi come ricerca in uno spazio di stati 

## Strategie di ricerca non informata ed euristica 

## Giochi con avversario

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



