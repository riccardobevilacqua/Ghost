---
lang: it
layout: installation
meta_title: Come installare Ghost sul tuo server - Ghost Docs
meta_description: Tutto quello che ti serve per avviare la piattaforma di blog Ghost in locale o sul tuo ambiente remoto.
heading: Installazione di Ghost &amp; Primi Passi
subheading: I primi passi per installare il tuo nuovo blog per la prima volta.
permalink: /it/installation/linux/
chapter: installation
section: linux
prev_section: windows
next_section: deploy
---


# Installare su Linux <a id="install-linux"></a>

### Installare Node

*   Puoi scaricare l'archivio `.tar.gz` da [http://nodejs.org](http://nodejs.org) oppure seguire le istruzioni su come [installare dal package manager](https://github.com/joyent/node/wiki/Installing-Node.js-via-package-manager).
*   Da terminale, verifica che sia installato Node digitando `node -v` e che sia installato npm digitando `npm -v`

### Installare e Avviare Ghost

*   Esegui il login su [http://ghost.org](http://ghost.org), quindi clicca il pulsante blu 'Download Ghost Source Code'
*   Nella pagina di download, premi il pulsante per scaricare il file zip più recente ed estrai il file nel percorso da cui vuoi avviare Ghost
*   Da terminale, posizionati nella cartella in cui hai estratto Ghost
*   Digita `npm install --production` <span class="note">attenzione al doppio trattino</span>
*   Una volta finita l'installazione attraverso npm, digita `npm start` per avviare Ghost in modalità sviluppo
*   Da un browser, naviga all'indirizzo <code class="path">127.0.0.1:2368</code> per verificare la corretta installazione del blog Ghost
*   Visita <code class="path">127.0.0.1:2368/ghost</code> e crea un utente admin con cui eseguire il login alla gestione di Ghost

Se stai usando linux come guest OS o attraverso SSH e disponi solo del terminale, procedi come segue:

*   Usa il tuo normale sistema operativo per trovare la URL del file zip di Ghost (varia a seconda della versione), salva la url ma sostituisci '/zip/' con '/archives/'
*   Da terminale, digita `wget url-of-ghost.zip` per scaricare Ghost
*   Estrai l'archivio digitando `unzip -uo Ghost-#.#.#.zip -d ghost`, poi `cd ghost`
*   Digita `npm install --production` per installare Ghost <span class="note">attenzione al doppio trattino</span>
*   Una volta finita l'installazione attraverso npm, digita `npm start` per avviare Ghost in modalità sviluppo
*   Ghost sarà quindi eseguito su localhost

