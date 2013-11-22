---
lang: it
layout: installation
meta_title: Come installare Ghost sul tuo server - Ghost Docs
meta_description: Tutto quello che ti serve per avviare la piattaforma di blog Ghost in locale o sul tuo ambiente remoto.
heading: Installazione di Ghost &amp; Primi Passi
subheading: I primi passi per installare il tuo nuovo blog per la prima volta.
chapter: installation
next_section: mac
---

## Introduzione <a id="overview"></a>

La documentazione di Ghost è prevalentemente in lavorazione, viene aggiornata e migliorata regolarmente. Non esitare a contattarci nel caso avessi problemi o suggerimenti.

Ghost è basato su [Node.js](http://nodejs.org), versione `0.10.*` (ultima versione stabile).

Eseguire Ghost in locale è possibile, ma occorre prima installare Node.js.

### Cos'è Node.js?

[Node.js](http://nodejs.org) è una moderna piattaforma per programmare applicazioni web veloci, scalabili ed efficienti.
    Negli ultimi 20 anni, il web si è evoluto da un insieme di pagine statiche in una piattaforma capace di supportare complesse applicazioni web come Gmail e facebook.
    JavaScript è il linguaggio di programmazione che ha consentito questo progresso.

[Node.js](http://nodejs.org) ci permette di programmare in JavaScript lato server. In passato JavaScript esisteva unicamente nel browser ed era richiesto per programmare lato server un secondo linguaggio, ad esempio PHP. Avere un'applicazione web programmata in un singolo linguaggio è un grande beneficio, inoltre rende Node.js accessibile a sviluppatori tradizionalmente legati alla programmazione lato client.

Grazie a [Node.js](http://nodejs.org) è possibile installare ovunque il motore JavaScript creato per il browser Google Chrome. Ciò significa che puoi installare Ghost sul tuo computer per provarlo, in maniera facile e veloce.
    Le sezioni seguenti approfondiscono l'installazione locale di Ghost su [Mac]({% if page.lang %}/{{ page.lang }}{% endif %}/installation/mac/),  [Windows]({% if page.lang %}/{{ page.lang }}{% endif %}/installation/windows/) o [Linux]({% if page.lang %}/{{ page.lang }}{% endif %}/installation/linux/) oppure ti aiuteranno ad installare Ghost su [un server o un servizio di hosting]({% if page.lang %}/{{ page.lang }}{% endif %}/installation/deploy).

### Primi passi

Se non sei incline a seguire le istruzioni di installazione manuale di Node.js e Ghost, la brava gente di [BitNami](http://bitnami.com/) ha creato [Ghost installers](http://bitnami.com/stack/ghost) per la maggior parte delle piattaforme.

Voglio installare Ghost su:

<div class="text-center install-ghost">
    <a href="{% if page.lang %}/{{ page.lang }}{% endif %}/installation/mac/" class="btn btn-success btn-large">Mac</a>
    <a href="{% if page.lang %}/{{ page.lang }}{% endif %}/installation/windows/" class="btn btn-success btn-large">Windows</a>
    <a href="{% if page.lang %}/{{ page.lang }}{% endif %}/installation/linux/" class="btn btn-success btn-large">Linux</a>
</div>

Se hai già deciso di installare Ghost sul tuo server o sul tuo servizio di hosting, ottimo! La seguente documentazione ti guiderà attraverso la varie opzioni di installazione di Ghost, dal setup manuale agli installers automatici.

<div class="text-center install-ghost">
    <a href="{% if page.lang %}/{{ page.lang }}{% endif %}/installation/deploy/" class="btn btn-success btn-large">Scarica Ghost</a>
</div>

Ricorda che Ghost è un nuovo prodotto e lo staff sta lavorando alacremente per implementare nuove funzionalità. Se hai bisogno di un upgrade di Ghost all'ultima versione, segui la nostra [documentazione di upgrade](/installation/upgrading/).
    In caso di problemi leggi la [guida al troubleshooting]({% if page.lang %}/{{ page.lang }}{% endif %}/installation/troubleshooting/), se non fosse sufficiente visita il [forum di Ghost](http://ghost.org/forum) dove lo staff e la community sono sempre pronti ad aiutare.

