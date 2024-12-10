La **rilocazione della memoria** è un processo essenziale per la gestione della memoria nei sistemi operativi, che consente di tradurre indirizzi virtuali in indirizzi fisici. Esistono due modalità principali di rilocazione: 

				Statica e Dinamica.

### Rilocazione Statica

-La rilocazione statica si verifica durante il caricamento del programma. Gli indirizzi virtuali vengono convertiti in indirizzi fisici dal loader, che aggiunge un valore fisso (indirizzo di base) a ciascun indirizzo logico.
- **Vantaggi**:
  - Semplicità nell’implementazione.
  - Non richiede hardware complesso per la traduzione degli indirizzi.
- **Svantaggi**:
  - Limitata flessibilità: un programma non può essere spostato in un’altra area di memoria una volta caricato.
  - Inefficienza in caso di swapping, poiché richiede una nuova rilocazione se il programma deve essere ricaricato.

### Rilocazione Dinamica

-Nella rilocazione dinamica, gli indirizzi virtuali vengono tradotti in indirizzi fisici durante l’esecuzione del programma, utilizzando una Memory Management Unit (MMU) che gestisce la traduzione in tempo reale.
- **Vantaggi**:
  - Maggiore flessibilità: i programmi possono essere spostati liberamente in memoria, facilitando operazioni di swapping e compattamento.
  - Riduzione della frammentazione esterna grazie alla possibilità di compattare aree di memoria libere.
- **Svantaggi**:
  - Maggiore complessità e overhead dovuti alla necessità di hardware per la gestione degli indirizzi.

# Frammentazione

La frammentazione è una condizione che si verifica quando la memoria allocata non viene utilizzata in modo efficiente, portando a spazi vuoti inutilizzati. Essa può essere suddivisa in due categorie principali:

#### Frammentazione Interna

La **frammentazione interna** si verifica quando a un processo viene allocata più memoria di quanto necessario, lasciando spazio inutilizzato all'interno di un blocco. Ad esempio, se un processo richiede 10 KB ma gli viene assegnato un blocco di 12 KB, i 2 KB rimanenti rimangono inutilizzati. Questo tipo di frammentazione è comune nelle tecniche di allocazione a partizioni fisse

#### Frammentazione Esterna

La **frammentazione esterna** si verifica quando ci sono piccole aree di memoria libera sparse che non possono essere utilizzate efficacemente per allocare nuovi processi. Anche se c'è sufficiente memoria totale disponibile, potrebbe non esserci uno spazio contiguo sufficiente per soddisfare una richiesta. Questo problema è tipico delle tecniche di allocazione dinamica della memoria

## Tecniche di Allocazione della Memoria

Nella gestione della memoria, le tecniche di allocazione possono essere classificate come segue:

- **Partizioni Fisse**: La memoria è suddivisa in partizioni di dimensioni fisse, il che può portare a frammentazione interna.
- **Partizioni Variabili**: Le partizioni sono allocate in base alle esigenze dei processi, riducendo la frammentazione interna ma aumentando il rischio di frammentazione esterna.
- **Paginazione**: La memoria è suddivisa in pagine di dimensioni fisse, consentendo una gestione più efficiente e flessibile della memoria virtuale. Le pagine possono essere allocate in qualsiasi area libera della memoria fisica, migliorando l’utilizzo complessivo.

### Prevenzione della Frammentazione

Per mitigare la frammentazione:

- La frammentazione interna può essere ridotta utilizzando partizioni di dimensioni variabili o tecniche come il paging.
- La frammentazione esterna può essere affrontata attraverso metodi come la compattazione, che sposta i processi nella memoria per creare blocchi contigui.