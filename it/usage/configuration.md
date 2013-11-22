---
lang: it
layout: usage
meta_title: Come Usare Ghost - Ghost Docs
meta_description: Una guida approfondita all'utilizzo della piattaforma di blog Ghost. Hai Ghost ma non sei sicuro su come proseguire? Inizia qui!
heading: Usare Ghost
subheading: Trova la tua strada e segui la tua ispirazione
chapter: usage
section: configuration
permalink: /it/usage/configuration/
prev_section: usage
next_section: settings
---


## Configurare Ghost <a id="configuration"></a>

Dopo il primo avvio di Ghost troverai un file `config.js` nella root di Ghost, assieme ad un `index.js`. Questo file consente di impostare configurazioni a livello d'ambiente per elementi come URL, database e mail.

Se non hai ancora avviato Ghost per la prima volta, il file non sarà presente. Puoi crearne uno copiando `config.example.js` - essenzialmente ciò che fa Ghost all'avvio. 

Per configurare la tua URL di Ghost, la mail o il database, apri `config.js` col tuo editor preferito e modifica le impostazioni per l'ambiente desiderato. Se non ti sei ancora imbattutto negli ambienti leggi i prossimi paragrafi.

## Cosa sono gli Ambienti? <a id="environments"></a>

Node.js, di conseguenza Ghost, ha un concetto integrato di ambienti. Gli ambienti permettono di creare configurazioni differenti a seconda di come si desidera avviare Ghost. Le modalità predefinite sono due: **sviluppo** e **produzione**.

Esiste qualche sottile differenza tra le due modalità. Essenzialmente **sviluppo** è attrezzato per svolgere sviluppo e debug con Ghost, mentre "produzione" si riferisce all'uso pubblico di Ghost. Le differenze comprendono i log e i messaggi d'errore, così come quanti asset statici è possibile concatenare e minificare. In **produzione** avrai un solo file JavaScript contenente tutto il codice per l'amministrazione, in **sviluppo** invece sono più numerosi.

Col progredire di Ghost queste differenze cresceranno e saranno più evidenti, pertanto diverrà sempre più importante che ogni blog pubblico sia avviato in ambiente di **produzione**. Questo potrebbe far sorgere la domanda: perchè l'ambiente predefinito è **sviluppo** se principalmente si utilizza la modalità **produzione**? Ghost ha **sviluppo** come ambiente predefinito perchè è il più adatto per la risoluzione di problemi, dunque risulta spesso il più utile al primo avvio.

##  Uso degli Ambienti <a id="using-env"></a>

Per avviare Ghost in una determinata modalità è necessario impostare una variabile d'ambiente. Per esempio se normalmente per avviare Ghost usassi `node index.js` allora ti servirebbe:

`NODE_ENV=production node index.js`

Oppure se di solito utilizzi forever:

`NODE_ENV=production forever start index.js`

Altrimenti se sei abituato a `npm start` potresti usare semplicemente:

`npm start --production`

### Perchè Usare `npm install --production`?

Spesso ci domandano perchè, essendo sviluppo la modalità d'avvio predefinita di Ghost, la documentazione di installazione dice di utilizzare `npm install --production`? Ottima domanda! Se non includessi `--production` nella procedura di installazione di Ghost non ci sarebbero problemi, tuttavia sarebbero installati molti pacchetti aggiuntivi utili solo per chi intende sviluppare il core stesso di Ghost. In questo caso inoltre sarebbe richiesto un ulteriore pacchetto, `grunt-cli`, installato globalmente tramite il comando `npm install -g grunt-cli`. É un passo in più che risulta superfluo per chi intende semplicemente utilizzare Ghost come blog.

