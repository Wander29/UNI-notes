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
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210216162723512.png" alt="image-20210216162723512" style="zoom:67%;" />

IA: indagine tecnologica ed intellettuale a lungo termine che sono sia scientifici che pratici:

- costruzione di macchine intelligenti
- comprensione mediante modelli computazionali dei comportamenti viventi
- rendere il lavoro con il calcolatore altrettanto utile e facile che con persone collaborative ed esperte

fondamenti dell'IA: *filosofia, matematica, economia, neuroscienze, psicologia, informatica, linguistica, cibernetica*

AI: *general purpose technology*, tipo elettricita, stampa, pc...

prendiamo per buona la definizione di kurzweil, 1990:
*arte di creare macchine che svolgono funzioni che richiedono intelligenza quando svolte da esseri umani*

?*cosa vuol dire intelligente?*
è una qualità intrinseca o un comportamento?

che tipi di capacità?

Test di Turing. 



![image-20210216163854696](/home/ludo/.config/Typora/typora-user-images/image-20210216163854696.png)

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
punto di svolta, agenti intelligenti che unisce vari settori dell'IA

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





# Risoluzione dei problemi come ricerca

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



