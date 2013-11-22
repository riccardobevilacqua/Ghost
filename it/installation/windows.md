---
lang: it
layout: installation
meta_title: Come installare Ghost sul tuo server - Ghost Docs
meta_description: Tutto quello che ti serve per avviare la piattaforma di blog Ghost in locale o sul tuo ambiente remoto.
heading: Installazione di Ghost &amp; Primi Passi
subheading: I primi passi per installare il tuo nuovo blog per la prima volta.
permalink: /it/installation/windows/
chapter: installation
section: windows
prev_section: mac
next_section: linux
---

# Installare su Windows <a id="install-windows"></a>

### Installare Node

*   Visita [http://nodejs.org](http://nodejs.org) e premi 'install', ti verrà chiesto di scaricare un file con estensione '.msi'
*   Clicca sul download per aprire l'installer, in questo modo installerai sia node sia npm.
*   Procedi attraverso i passi proposti dall'installer.

In caso di problemi puoi guardare l'intera [procedura in azione qui](https://s3-eu-west-1.amazonaws.com/ghost-website-cdn/install-node-win.gif "Installare node su Windows").

### Scarica & Estrai Ghost

*   Esegui il login su [http://ghost.org](http://ghost.org), quindi clicca il pulsante blu 'Download Ghost Source Code'.
*   Nella pagina di download, premi il pulsante per scaricare il file zip più recente.
*   Clicca sulla freccia accanto al file più recentemente scaricato, poi scegli 'mostra nella cartella'.
*   Nella cartella aperta, fai tasto destro sul file zip scaricato e scegli 'Estrai tutto'.

In caso di problemi puoi guardare l'intera [procedura in azione qui](https://s3-eu-west-1.amazonaws.com/ghost-website-cdn/install-ghost-win.gif "Installare Ghost su Windows Parte 1").

### Installare e Avviare Ghost

*   Dal menu Start, trova 'Node.js' e scegli 'Node.js Command Prompt'
*   Nel terminale di Node, posizionati sulla cartella dove hai estratto Ghost. Digita: `cd Downloads/ghost-#.#.#` (sostituisci i cancelletti con la versione di Ghost scaricata).
*   Nel terminale digita `npm install --production` <span class="note">attenzione al doppio trattino</span>
*   Una volta finita l'installazione attraverso npm, digita `npm start` per avviare Ghost in modalità sviluppo
*   Da un browser, naviga all'indirizzo <code class="path">127.0.0.1:2368</code> per verificare la corretta installazione del blog Ghost
*   Visita <code class="path">127.0.0.1:2368/ghost</code> e crea un utente admin con cui eseguire il login alla gestione di Ghost.
*   Leggi la [guida all'utilizzo](/usage) per le istruzioni sui passi successivi

![](https://s3-eu-west-1.amazonaws.com/ghost-website-cdn/install-ghost-win-2.gif "Installare Ghost su Windows Parte 2")

