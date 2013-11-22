---
lang: it
layout: installation
meta_title: Come installare Ghost sul tuo server - Ghost Docs
meta_description: Tutto quello che ti serve per avviare la piattaforma di blog Ghost in locale o sul tuo ambiente remoto.
heading: Installazione di Ghost &amp; Primi Passi
subheading: I primi passi per installare il tuo nuovo blog per la prima volta.
permalink: /it/installation/mac/
chapter: installation
section: mac
prev_section: installation
next_section: windows
---


# Installare su Mac <a id="install-mac"></a>

Per installare Node.js e Ghost sul tuo mac dovrai aprire la finestra del terminale. Puoi aprirne una digitando "Terminal" su spotlight.

### Installare Node

*   Visita [http://nodejs.org](http://nodejs.org) e premi 'install', ti verrà chiesto di scaricare un file con estensione '.pkg'
*   Clicca sul download per aprire l'installer, in questo modo installerai sia node sia npm.
*   Procedi attraverso i passi proposti dall'installer, infine inserisci la tua password e clicca 'install software'.
*   Una volta completata l'installazione, vai al Terminal e digita `echo $PATH` per controllare che '/usr/local/bin/' sia nel tuo percorso.

<p class="note"><strong>Nota:</strong> Se '/usr/local/bin' non dovesse apparire nel tuo $PATH, consulta i <a href="#export-path">suggerimenti di troubleshooting</a> per scoprire come aggiungerlo</p>

In caso di problemi puoi guardare l'intera [procedura in azione qui](https://s3-eu-west-1.amazonaws.com/ghost-website-cdn/install-node-mac.gif "Install Node on Mac").

### Installare e Avviare Ghost

*   Esegui il login su [http://ghost.org](http://ghost.org), quindi clicca il pulsante blu 'Download Ghost Source Code'.
*   Nella pagina di download, premi il pulsante per scaricare il file zip più recente.
*   Clicca sulla freccia accanto al file più recentemente scaricato, poi scegli 'show in finder'.
*   Nel finder, fai doppio click sul file zip scaricato e decomprimilo.
*   Individua la cartella 'ghost-#.#.#' appena estratta e trascinala sulla barra della scheda del tuo terminale, in questo modo si aprirà una nuova scheda di terminale con il percorso corretto.
*   Nella nuova scheda di terminale digita `npm install --production` <span class="note">attenzione al doppio trattino</span>
*   Una volta finita l'installazione attraverso npm, digita `npm start` per avviare Ghost in modalità sviluppo
*   Da un browser, naviga all'indirizzo <code class="path">127.0.0.1:2368</code> per verificare la corretta installazione del blog Ghost
*   Visita <code class="path">127.0.0.1:2368/ghost</code> e crea un utente admin con cui eseguire il login alla gestione di Ghost.
*   Leggi la [guida all'utilizzo](/usage) per le istruzioni sui passi successivi

![](https://s3-eu-west-1.amazonaws.com/ghost-website-cdn/install-ghost-mac.gif)

