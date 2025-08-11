# Ultimo Iscritto YouTube - Widget

Questo progetto è un **widget personalizzabile** che mostra in tempo reale l'ultimo iscritto del proprio canale YouTube, utilizzando le API ufficiali di Google.

## Demo
Demo disponibile al link [https://bisumto.github.io/lastsubscriber](https://bisumto.github.io/lastsubscriber
)

> **Nota:** Per essere aggiunto alla whitelist dell'OAuth di Google e poter utilizzare questo widget, è sufficiente inviare una mail a **bisumto[at]gmail[dot]it** con il proprio indirizzo Gmail associato al canale youtube


## Funzionalità

- Autenticazione tramite **OAuth 2.0** di Google.
- Aggiornamento automatico dell'ultimo iscritto ogni *n* secondi (configurabile).
- Supporto per **CSS personalizzato** salvato in `localStorage` per modificare l'aspetto del widget senza dover toccare i file originali.
- Pagina di configurazione (`config.html`) per modificare:
  - Intervallo di aggiornamento.
  - Stili CSS personalizzati.
- Ricaricamento dinamico del CSS ad ogni aggiornamento, così le modifiche sono visibili subito.

## Struttura del progetto

- **index.html** – Widget principale che mostra l'ultimo iscritto.
- **style.css** – Stile base del widget.
- **config.html** – Pagina di configurazione delle preferenze e del CSS personalizzato.
- **config.js** – File di configurazione delle costanti OAuth (CLIENT_ID, REDIRECT_URI, SCOPE).

## Requisiti

- Un progetto Google Cloud con API YouTube Data v3 attivata.
- Credenziali OAuth 2.0 con `CLIENT_ID` e `REDIRECT_URI` correttamente impostati.

## Installazione (self-host)

1. Clona il repository:
```bash
   git clone https://github.com/tuo-utente/ultimo-iscritto-youtube-widget.git
   cd ultimo-iscritto-youtube-widget
```

2. Configura config.js con i tuoi dati OAuth:
```
  const CLIENT_ID = 'IL_TUO_CLIENT_ID';
  const REDIRECT_URI = 'IL_TUO_REDIRECT_URI';
  const SCOPE = 'https://www.googleapis.com/auth/youtube.readonly';
```

3. Apri config.html in un browser per impostare:
- Intervallo di aggiornamento (in secondi).
- CSS personalizzato.

4.	Apri index.html per vedere il widget in funzione.
