---
lang: it
layout: installation
meta_title: Come installare Ghost sul tuo server - Ghost Docs
meta_description: Tutto quello che ti serve per avviare la piattaforma di blog Ghost in locale o sul tuo ambiente remoto.
heading: Installazione di Ghost &amp; Primi Passi
subheading: I primi passi per installare il tuo nuovo blog per la prima volta.
permalink: /it/installation/upgrading/
chapter: installation
section: upgrading
prev_section: deploy
next_section: troubleshooting
---

# Aggiornare Ghost <a id="upgrade"></a>

Aggiornare Ghost è molto semplice.

Ci sono un paio di strade che si possono intraprendere. Quanto segue descrive cosa deve accadere, successivamente viene illustrato passo dopo passo come procedere tramite [interfaccia grafica](#how-to) e tramite [linea di comando](#cli), lasciandoti libero di scegliere il metodo che preferisci.

<p class="note"><strong>Fai un backup!</strong> Prima di aggiornare esegui sempre un backup. Leggi le <a href="#backing-up">istruzioni per il backup</a> innanzi tutto!</p>

## Panoramica

<img src="https://s3-eu-west-1.amazonaws.com/ghost-website-cdn/folder-structure.png" style="float:left" />

Ghost, una volta installato, ha un'alberatura di cartelle simile a quella mostrata a sinistra. Ci sono due cartelle principali, <code class="path">content</code> e <code class="path">core</code>, più alcuni files nella root.

Aggiornare Ghost consiste nel sostituire i vecchi files coi nuovi, eseguire nuovamente `npm install` per aggiornare la cartella <code class="path">node_modules</code> e riavviare Ghost per applicare le modifiche.

Ricorda, Ghost archivia in maniera predefinita i tuoi dati, i temi, le immagini, etc nella cartella <code class="path">content</code>, quindi fai attenzione! Sostituisci solo i files in <code class="path">core</code> e nella root, in questo modo tutto andrà per il meglio.

## Fare un Backup <a id="backing-up"></a>

<img src="https://s3-eu-west-1.amazonaws.com/ghost-website-cdn/export.png" style="float:right" />

*   Per eseguire un backup del tuo database, accedi alla tua installazione di Ghost e vai su <code class="path">/ghost/debug/</code>. Premi il pulsante di esportazione per scaricare un file JSON contenente tutti i tuoi dati. Ecco fatto!
*   Per eseguire un backup di temi personalizzati e immagini, dovrai copiare i files in <code class="path">content/themes</code> e <code class="path">content/images</code>

<p class="note"><strong>Nota:</strong> Se vuoi puoi copiare il tuo database da <code class="path">content/data</code> ma <strong>attenzione</strong> a non farlo mentre Ghost è in esecuzione. Prima di procedere ferma l'esecuzione di Ghost.</p>


## Come Aggiornare <a id="how-to"></a>

Come aggiornare in locale

<p class="warn"><strong>ATTENZIONE:</strong> non devi <strong>MAI</strong> copiare e incollare l'intera cartella di Ghost sopra un'installazione su mac. Non devi <strong>MAI</strong> scegliere <kbd>REPLACE</kbd> se esegui un upload con Transmit o altri programmi di FTP, scegli invece <strong>MERGE</strong>.</p>

*   Scarica la versione più recente di Ghost da [Ghost.org](http://ghost.org/download/)
*   Estrai il file zip in una cartella temporanea
*   Copia tutti i files presenti nella root dell'ultima versione. Inclusi quindi: index.js, package.json, Gruntfile.js, config.example.js, la licenza e il readme.
*   Sostituisci la vecchia cartella <code class="path">core</code> con la nuova cartella `core`
*   Se il rilascio include aggiornamenti di Casper (il tema predefinito), sostituisci la vecchia cartella <code class="path">content/themes/casper</code> con la nuova
*   Esegui `npm install --production`
*   Infine riavvia Ghost affinchè le modifiche abbiano effetto

## Solo Riga di Comando <a id="cli"></a>

<p class="note"><strong>Fai un backup!</strong> Prima di aggiornare esegui sempre un backup. Leggi le <a href="#backing-up">istruzioni per il backup</a> innanzi tutto!</p>

### Solo Riga di Comando su Mac <a id="cli-mac"></a>

Lo screencast sotto mostra i passi per aggiornare Ghost supponendo che il file zip sia stato scaricato in <code class="path">~/Downloads</code> e che Ghost sia installato in <code class="path">~/ghost</code> <span class="note">**Nota:** `~` si riferisce alla home dell'utente su mac e linux</span>

![](https://s3-eu-west-1.amazonaws.com/ghost-website-cdn/upgrade-ghost.gif)

I passi nello screencast sono:

*   <code class="path">cd ~/Downloads</code> - si posiziona sulla cartella in cui è stata scaricata l'ultima versione di Ghost
*   `unzip ghost-0.3.1.zip -d ghost-0.3.3` - estrae ghost nella cartella <code class="path">ghost-0.3.3</code>
*   <code class="path">cd ghost-0.3.3</code> - si posiziona nella cartella <code class="path">ghost-0.3.3</code>
*   `ls` - mostra tutti i files e le sottocartelle in questa cartella
*   `cp *.md *.js *.txt *.json ~/ghost` - copia tutti i files .md .js .txt e .json da questa cartella a <code class="path">~/ghost</code>
*   `cp -R core ~/ghost` - copia la cartella <code class="path">core</code> e tutto il suo contenuto in <code class="path">~/ghost</code>
*   `cp -R content/themes/casper ~/ghost/content/themes` - copia la cartella <code class="path">casper</code> e tutto il suo contenuto in <code class="path">~/ghost/content/themes</code>
*   `cd ~/ghost` - si posiziona sulla cartella <code class="path">~/ghost</code>
*   `npm install --production` - installa Ghost
*   `npm start` - avvia Ghost

### Solo Riga di Comando su Server Linux <a id="cli-server"></a>

*   Innanzi tutto dovrai trovare la URL della versione più recente di Ghost. Dovrebbe essere simile a `http://ghost.org/zip/ghost-latest.zip`.
*   Scarica il file zip con `wget http://ghost.org/zip/ghost-latest.zip` (o qualunque sia la URL della più recente versione di Ghost).
*   Estrai l'archivio con `unzip -uo ghost-0.3.*.zip -d path-to-your-ghost-install`
*   Esegui `npm install --production` per applicare le nuove dipendenze
*   Infine riavvia Ghost affinchè le modifiche abbiano effetto

**Approfondimento**, [howtoinstallghost.com](http://www.howtoinstallghost.com/how-to-update-ghost/) contiene istruzioni per l'aggiornamento di Ghost su server linux.

### Come Aggiornare una DigitalOcean Droplet <a id="digitalocean"></a>

<p class="note"><strong>Fai un backup!</strong> Prima di aggiornare esegui sempre un backup. Leggi le <a href="#backing-up">istruzioni per il backup</a> innanzi tutto!</p>

*   Innanzi tutto dovrai trovare la URL della versione più recente di Ghost. Dovrebbe essere simile a `http://ghost.org/zip/ghost-latest.zip`.
*   Una volta nota la URL dell'ultima versione, nella console della tua Droplet digita `cd /var/www/` per posizionarti nella cartella usata da Ghost.
*   Scarica il file zip con `wget http://ghost.org/zip/ghost-latest.zip` (o qualunque sia la URL della più recente versione di Ghost).
*   Estrai l'archivio con `unzip -uo ghost-0.3.*.zip -d ghost`
*   Assicurati che tutti i files abbiano i permessi corretti con `chown -R ghost:ghost ghost/*`
*   Esegui `npm install` per applicare le nuove dipendenze
*   Infine riavvia Ghost affinchè le modifiche abbiano effetto usando `service ghost restart`

##  Come Aggiornare Node.js all'Ultima Versione <a id="upgrading-node"></a>

Se hai installato Node.js dal sito [Node.js](nodejs.org) puoi aggiornare Node.js all'ultima versione semplicemente scaricando ed eseguendo l'installer più recente. Questo sostituirà la versione corrente con la nuova versione.

Se usi Ubuntu o un'altra distro linux che dispone di `apt-get`, il comando per aggiornare node è lo stesso usato per installarlo: `sudo apt-get install nodejs`.

**Non** occorre nè riavviare il server nè riavviare Ghost.
