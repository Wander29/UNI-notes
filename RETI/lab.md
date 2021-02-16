RETI LAB: Teoria
a.a. 2020/21
*Ludovico Venturi, UniPi*

---

<u>INDICE</u>

[toc]

# REST

**web service**: è un programma che utilizza una connessione web e richiede ad un server di fornire dati o eseguire un algoritmo
*TIPOLOGIE di web services*:

- RESTful
- RCP style
- ibirido REST, RPC

**REST** (REpresentational State Transfer)
É uno stile architetturale per lo sviluppo di web services *debolemente accoppiati*, in altre parole un insieme di vincoli, introdotto nel 2001 da Roy Fielding. É stato sviluppato a posteriori dall'HTTP.

Il web non viene più usato come strumento di trasporto, viene usato *correttamente* seguendone i principi originari.

Non  è qualsiasi cosa utilizzi HTTP e XML/JSON, ad esempio XML-RPC che fu il primo approccio di questo genere non ha un'interfaccia uniforme e non è pertanto definibile come arhcitettura di tipo REST

## Principi del REST

**ROA** (Resource Oriented Application) 
è un insieme di linee guida per implementare un web service RESTful

### Resource Identification

*Risorsa*: qualsiasi oggetto rappresentabile sufficientemente importante da poter essere considerata come entità a sé stante

Si deve dare un nome a tutto ciò di cui si vuole parlare, per tale ragione si utilizzano gli URI (gli HTTP URI appartengono ad uno spazio di indirizzamento *globale*). 

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210120133314575.png" alt="image-20210120133314575" style="zoom:50%;" />

*es: `https://github.com/google/gson/archive/gson-parent-2.8.6.zip`* 

*URI Templates*: sono una tecnica per definire URI che includono *parametri*, specificano come costruire ed eseguire il parsing di URI parametrici, ad es: `http://example.com/prodotti/{id}`. 

Dettagli sulla URI, template compresi, non sono richiesti dal REST in quanto a specifiche ma nella pratica si rivelano una *best practice*.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210120133844749.png" alt="image-20210120133844749" style="zoom: 80%;" />

### Uniform Interface

Lo stesso piccolo insieme di operazioni si applica a ogni caso d'uso. *Un piccolo insieme di verbi applicato ad un largo insieme di sostantivi*.

I verbi sono universali, non inventati in base all'applicazione; l'interfaccia dei verbi può comunque essere *estesa*.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210120131843230.png" alt="image-20210120131843230" style="zoom:67%;" />

1. POST consente di creare risorse come subordinate ad una esistente, è una *append*. É il *server a decidere l'URI*.
   Il server, in caso positivio, risponde con *201 Created*. 
   Nel response header viene indicata l'URI della risorsa creata.
   É un'operazione di lettura e scrittura, potrebbe modificare lo stato della risorsa e provocare effetti collaterali sul server.
   <img src="/home/ludo/.config/Typora/typora-user-images/image-20210120160334497.png" alt="image-20210120160334497" style="zoom:50%;" />
2. PUT inizializza o aggiorna lo stato di una risorsa, utilizzato quando *il client decide l'URI*. 
   <img src="/home/ludo/.config/Typora/typora-user-images/image-20210120160306867.png" alt="image-20210120160306867" style="zoom:50%;" />
3. GET è un'operazione di sola scrittura, idempotente e soggetta a cache

#### Idempotenza e Safety

Un metodo *idempotente* genera sul server lo stesso effetto quando applicato 1 o n volte. Lo stato della risorsa dalla seconda richiesta in poi è lo stesso di quello  lasciato dopo la prima applicazione del metodo. 

Un metodo *safe* non genera effetti collaterali sul server, possono essere ripetuti n volte senza effetti collaterali. Lo sono : *GET, HEAD*. Un eventuali contatore di accessi incrementato nel server non è da intendersi come "effetto collaterale".

Al contrario i metodi *unsafe* modificano lo stato del server e non possono essere ripetute senza effetti collaterali. 

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210120160730657.png" alt="image-20210120160730657" style="zoom:67%;" />



### Self-descriptive messages

Ogni messaggio contiene le informazioni necessarie per la propria gestione. 
Le risorse sono entità *astratte*, non utilizzaibli di per sé ma accedibili attraverso una *rappresentazione*, il cui formato è negoziabile tra pari (es. XML/JSON, o qualunque altro formato che supporta i link).

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210120132239091.png" alt="image-20210120132239091" style="zoom:50%;" />

#### Content negotiation

? Se i consumer cambiano requisiti per il formato dei messaggi in modo non retrocompatibile ?

Si utilizza la *content negotiation*, in particolare i *media types*.
Un servizio (su un server) dovrebbe supportare sia i vecchi che i nuovi consumer senza dover introdurre un'interfaccia specifica per ogni tipo di consumer.
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210120163427170.png" alt="image-20210120163427170" style="zoom:50%;" />
I formati dei dati da accettare/restituire sono negoziati a runtime come parte dell'invocazione. 
La negoziazione del formato non richiede l'aggiunta di ulteriori messaggi. Il client invia i formati comprensibili (MIME types) con il relativo *formato di qualità* ad indicare la prefernza e il server sceglie il formato più appropriato fra questi per la risposta.

> GET /resource
> Accept: text/html; q=0.5, text/plain; q=0.1
>
> 200 OK
> Content-type: text/html

![image-20210120164307908](/home/ludo/.config/Typora/typora-user-images/image-20210120164307908.png)

Per servizi su larga scala ha senso fornire le risorse sia in formato JSON che XML.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210120164425113.png" alt="image-20210120164425113" style="zoom:50%;" />

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210120164444460.png" alt="image-20210120164444460" style="zoom:50%;" />

### Hypermedia as the engine of app state (HATEAOS)

Le applicazione RESTful *navigano invece di chiamare*, il client può scegliere un link contenuto nelle rappresentazioni delle risorse.
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210120164636370.png" alt="image-20210120164636370" style="zoom:50%;" />

### Stateless interactions

 Ogni richiesta dal client al server deve contenere le informazioni necessarie per capire completamente la richiesta indipendentemente dalle precedenti.
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210120164727620.png" alt="image-20210120164727620" style="zoom: 50%;" />

Ciò non equivale a dire che le applicazioni siano *stateless*. L'idea del REST è di evitare transazioni di lunga durata. Nell'esempio sopra il carrello diventa una *risorsa* utilizzabile anche da altri servizi, non viene nascosto nella sessione ma  appunto esposto come risorsa.

Lo stato delle risorse è gestito sul server, identico per ogni client che lavora con il servizio. Se un client cambia lo stato di una risorsa gli altri cliente devono vedere questa modifica.
Lo stato del client è gestito sul client.

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210120133150813.png" alt="image-20210120133150813" style="zoom:50%;" />

## Metodologia di progettazione

1. Identificare le risorse da esporre come servizi (*es. catalogo di libri, urne e voti* )
2. Modellare le relazione fra le risorse con link che possono essere seguiti per ottenere più dettagli o eseguire *transizioni di stato*. 
3. Progettare URI *carini* per indirizzare le risorse
4. Specificare la semantica di GET, POST, PUT e DELETE per ogni risorsa e stabilire se sono ammissibili o meno
5. Progettare e documentare le rappresentazioni delle risorse
6. Implentare e deployare su server web
7. Testare (web browser)

<u>ESEMPIO: API di un semplice Doodle</u>

1. Risorse: urne e voti
2. Relazioni di contenimento
   <img src="/home/ludo/.config/Typora/typora-user-images/image-20210120170435270.png" alt="image-20210120170435270" style="zoom:50%;" />
3. Gli URI contengono gli ID delle risorse figlio
   <img src="/home/ludo/.config/Typora/typora-user-images/image-20210120170514983.png" alt="image-20210120170514983" style="zoom:50%;" />

4. POST sui contenitori -> creare risorse figlie
   PUT e DELETE -> aggiornano/rimuovono le risorse figlie
   <img src="/home/ludo/.config/Typora/typora-user-images/image-20210120170614007.png" alt="image-20210120170614007" style="zoom: 67%;" />

   

| <img src="/home/ludo/.config/Typora/typora-user-images/image-20210120170729671.png" alt="image-20210120170729671" style="zoom:50%;" /> | <img src="/home/ludo/.config/Typora/typora-user-images/image-20210120170750534.png" alt="image-20210120170750534" style="zoom:50%;" /> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| <img src="/home/ludo/.config/Typora/typora-user-images/image-20210120170813806.png" alt="image-20210120170813806" style="zoom:50%;" /> | <img src="/home/ludo/.config/Typora/typora-user-images/image-20210120170824760.png" alt="image-20210120170824760" style="zoom:50%;" /> |

## Anti-Patterns

Pratiche da evitare in un'architettura RESTful.

**Tunneling su GET/POST**: é sconsigliato effettuare un tunnellng sul metodo GET e POST, ovvero un'operazione del tipo:
`GET /api?method=addCustomer&name=Mario+Rossi`
I problemi possono sorgere ad esempio se si salva il link nei preferiti, o se si utilizza un crawler. 

**Ignorare gli Status Code**: Spesso è utilizzato uno status code ridotto: `200 OK, 404 NOT FOUND, 500 Internal Server Error` mentre è consigliabile arricchire semanticamente la comunicazione con più status code, ad es:
`201 Created, 409 Conflict, 412 Precondition Failed`, dove la prima indica che è stata creata con successo una nuova risorsa, la seconda che un conflitto, come una PUT basata su dati di una vecchia versione della risorsa, impedisce l'operazione mentre la terza indica che a causa di una precondizione non soddisfatta non è possibile completare l'operazione.

**Dimenticare gli Hypermedia**: non si collegano le risorse fra loro. Scenari:

- Ci si può dimenticare di inserire link nelle rappresentazioni, è il client che costruisce gli URI.
- Costruzione degli URI a metà fra client e link nelle rappresentazioni
- Idealmente gli URI e le modalità per costruirli come le *query* devono essere comunicati via *hypermedia* come link nelle rappresentazioni delle risorse

**Rompere la self-descriptiveness**: ogni HTTP request e response deve contenere tutta l'informazione necessaria per poter essere processata dal client/server. Tale assioma viene a mancare quando si utilizzadono headers/formati/protocolli non standard

## Codici di stato HTTP

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210120172058280.png" alt="image-20210120172058280" style="zoom:50%;" /> 

| <img src="/home/ludo/.config/Typora/typora-user-images/image-20210120172113813.png" alt="image-20210120172113813" style="zoom:50%;" />![image-20210120172122241](/home/ludo/.config/Typora/typora-user-images/image-20210120172122241.png) | ![image-20210120172122241](/home/ludo/.config/Typora/typora-user-images/image-20210120172122241.png) |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| <img src="/home/ludo/.config/Typora/typora-user-images/image-20210120172131474.png" alt="image-20210120172131474" style="zoom:50%;" /> | <img src="/home/ludo/.config/Typora/typora-user-images/image-20210120172142951.png" alt="image-20210120172142951" style="zoom:67%;" /> |
| <img src="/home/ludo/.config/Typora/typora-user-images/image-20210120172202864.png" alt="image-20210120172202864" style="zoom:50%;" /> |                                                              |



## Esempio REST server: JAX-RS

*JAX-RS* sono delle API Java aventi l'obiettivo di semplificare lo sviluppo di applicazioni che utilizzano l'architettura REST.
Utilizza *annotazioni* Java per semplificare lo sviluppo di servizi Web RESTful . 
Tali annotazioni definiscono le risorse e le azioni permesse. Sono annotazioni di runtime che attraverso meccanismi di *reflection* genereranno classi di supporto per la risorsa.

> Una risorsa JAX-RS è un **POJO (Plain Old Java Object)** annotato che fornisce metodi per gestire le richieste HTTP alle URI a cui la risorsa è associata

**Jersey** è l'implementazione di riferimento della specifica di API *JAX-RS*.
Permette di creare risorse utilizzando annotazioni per metodi e classi. Il programmatore si occupa della soluzione del problema richiesto dal client, il framework gestisce le richieste HTTP e la negoziazione della rappresentazione.

```java
/**
* semplice esempio di risorsa utilizzabile tramite Jersey
* è una class Java più un insieme di annotazioni
*/

import javax.ws.rs.GET;
import javax.ws.rs.Produces;
import javax.ws.rs.Path;

// class will be at addressable at the URI "/helloworld"
@Path("/helloworld")
public class HelloWorldResource 
{
    // The java method will process HTTP GET requests
    @GET

    /* The Java method will produce content identified by the
    * MIME Media type "text/plain"
    */
    @Produces("text/plain")
	public String getMessage() {
		return "Hello World";
	} 
}
```

**`@Path`** indica l'URI a cui la risorsa risulta raggiungibile, in questo caso: `http://www.ecample.com/hellowrold`. 
È possibile utilizzare gli URI template (URI parametrici):
`@Path("/helloworld/{username}")`

**`@GET`** indica il metodo HTTP da gestire

**`@Produces`** specifica uno o più MIME type con cui la rappresentazione della risorsa può essere trasferita al client che ne fa richiesta

**`@Consumes`** specifica uno o più MIME type che possono essere accettati in ingresso


**Jersey ResourceConfig**: utile per configurare le risorse usate da un'applicazione

```java
//packages() method lists the package(s) you want Jersey to scan for @Path and @Provider classes and register them for you
ResourceConfig config = 
    new ResourceConfig().packages("it.cnit.rest.server.controller");

//Set up the logging feature to print out requests/responses
// The register() method lets you manually register classes and instances of resources manually
config.register(new LoggingFeature(Logger.getLogger("Server"), Level.INFO,
null, null));

config.register(new JacksonFeature()); // a way to tell Jersey "please use the Jackson libraries for JSON parsing and serialization",
```

**Deployment**

```java
/**
* @param uri URI on which the Jersey web application will be deployed. Only first *		path segment will be used as context path, the rest will be ignored.
* @param config  web application configuration.
* @returns newly created HttpServer.
*/
HttpServer httpServer =
GrizzlyHttpServerFactory.createHttpServer(URI.create("http://localhost:9999"),
config);
```

Crea un'istanza di un server HTTP *embedded* (è possibile anche utilizare una web app serviata da un application server quale Tomcat o GlassFish).

## URL

URL (Uniform Resource Locator) specifica la locazione di una risorsa su Internet e il protocollo per reperirla (HTTP, FTP).

La risorsa può essere un file su un host, una query per un database o l'output di un comando.

```java
// rappresenta una URL assoluta
URL cli = new URL("http://www.di.unipi.it/");

// rappresenta una URL relativa [URL (URL baseURL, String relativeURL)]
URL faq = new URL(cli, "faq");

// URL costruita a partire dalle sue componenti
try {
    URL url = new URL("http", "didattica.di.unipi.it", "laurea-in-informatica/");
}
catch (MalformedURLException e) {
    // se la URL non è corretta sintatticamente o il protocollo non è supportato
} 
```

### Recuperare dati da una URL

La definizione di un client che accede ad un server web REST può essere effettuata in Java sfruttando varie classi:

- URL
- URLConnection
- HttpURLConnection

#### URL

```java
URL url = new URL("https://docs.oracle.com/javase/tutorial/networking/urls/creatingUrls.html");

// restituisce un InputStream, è un'implementazione di una richiesta GET
// la cui è risposta è disponibile nello stream
InputStream stream= url.openStream();
```

#### URLConnection

```Java
try {
    URL u = new URL("http://www.bogus.com");
    URLConnection uc = u.openConnection();
    InputStream raw = uc.getInputStream(); // implicitamente chiama connect()
    // read from URL ...
} 
catch (MalformedURLException ex) 	{ System.err.println(ex); } 
catch (IOException ex) 				{ System.err.println(ex); }


// restituiscono, rispettivamente, chiave e valore dell'i-esimo header
public String getHeaderFieldKey (int n);
public String getHeaderField (int n);

//  restituisce il MIME media type dei dati contenuti nel corpo del messaggio, null, se il content type non è disponibile
public String getContentType();
```

Permette di scegliere diverse parametri della connessione, analizzare gli header inviati dal server e settare i campi header del client, **leggere e scrivere** sulla connessione. 
Permette di inviare dati ad un web server con metodi POST e PUT.

#### HttpURLConnection

```java
URL u = new URL("http://www.di.unipi.it");
URLConnection uc = u.openConnection();
HttpURLConnection http = (HttpURLConnection) uc;
```

É una sottoclasse astratta di URLConnection, fornisce metodi aggiuntivi per lavorare con URL HTTP, ad esempio 

- metodi *get/set* : `setRequestMethod (GET, POST, HEAD, ecc.)`, 
- decidere se eseguire *redirect*
- reperire i *response code*
  `public int getResponseCode() throws IOException
  public String getResponseMessage() throws IOException`
- determinare se la connessione è intermediata da un *proxy*
  `public abstract boolean usingProxy();`