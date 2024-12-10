Un **processo** è un'istanza in esecuzione di un programma e include sia il codice che i dati necessari per il suo funzionamento. In altre parole, quando avvii un programma sul tuo computer, il sistema operativo crea un processo per gestire quell'operazione. Ogni processo è composto da diverse parti:

## Componenti di un Processo

1. **Codice**: Queste sono le istruzioni del programma che il computer deve eseguire.
2. **Dati**: Questi possono essere suddivisi in diverse categorie:
    
    - **Variabili globali**: Dati accessibili da qualsiasi parte del programma.
    - **Variabili locali**: Dati utilizzati solo all'interno di una specifica funzione o blocco di codice.
    - **Variabili temporanee**: Dati utilizzati per operazioni temporanee durante l'esecuzione.
    - **Dati allocati dinamicamente**: Memoria richiesta durante l'esecuzione del programma, come ad esempio quando si usano strutture dati come liste o array.
    

## Tipi di Processi

I processi possono essere classificati in base al loro comportamento e interazione:

1. **Processi Indipendenti**: Questi processi operano autonomamente e non scambiano dati con altri processi. Possono funzionare senza dipendere da altri.
2. **Processi Cooperanti**: Questi processi lavorano insieme e necessitano di scambiarsi informazioni per completare il loro compito. Ad esempio, un processo potrebbe inviare dati a un altro per elaborazione.
3. **Processi Competitori**: Questi processi competono per le stesse risorse del sistema, come la memoria o la CPU. Questa competizione può portare a conflitti se non gestita correttamente.

## Creazione di Processi

Ogni programma può generare più processi, ma ogni processo è legato a un solo programma. Ci sono due principali tipi di processi:

1. **Processo Utente**: Questo tipo di processo è creato da un programma scritto dall'utente, come un'applicazione o un gioco.
2. **Processo Supervisore**: Questo processo è generato dal sistema operativo stesso, come ad esempio il gestore delle attività, che controlla e gestisce altri processi in esecuzione.

Quando avvii un programma, il sistema operativo crea un processo e lo memorizza nella memoria centrale del computer. Ogni processo è rappresentato da una struttura chiamata **PCB (Process Control Block)**, che contiene informazioni fondamentali per il suo funzionamento, come lo stato del processo, le risorse allocate e i registri della CPU.