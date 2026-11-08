# Café BLOOM · Torino

Sito vetrina responsive per Café BLOOM, Via Catania 21/A, Torino. Tutto il codice della pagina — HTML, CSS, menu e interazioni — è contenuto in **[`dist/index.html`](dist/index.html)**. Le fotografie sono nella cartella `dist/assets/`.

## Aprire il sito

Apri `dist/index.html` nel browser, oppure servi la cartella `dist` con un qualsiasi server statico. Non sono necessari installazione, compilazione, chiavi API o database. Font, Tailwind CSS, GSAP, ScrollTrigger e Lucide vengono caricati tramite CDN; è quindi consigliata una connessione internet. Lo stile principale è definito nel file HTML e rimane disponibile anche se Tailwind non si carica. Il contenuto resta leggibile anche se le animazioni non sono disponibili.

## Contenuti e funzionalità

- Palette ispirata alle foto: crema `#f5f2e9`, verde botanico `#2f4336`, salvia `#dfe5d6`, terracotta `#aa4e35`, rosa `#e5c8b8`, espresso `#302d26`. Il logo fornito è monocromatico: i colori del sito sono una direzione creativa, non una palette ufficiale attestata.
- Fraunces per i titoli e DM Sans per i testi.
- Apertura botanica, navbar flottante, piccoli effetti di parallax, tilt e pulsanti magnetici, fascia scorrevole e cursore contestuale su desktop.
- Quattro schede menu accessibili da tastiera: brunch; colazione e bakery; coffee e tea bar; vegan e veggie.
- **49 voci con prezzi reali trascritti dalla foto del listino fornita dall’utente**, consultabili anche senza JavaScript. La foto del listino non è inclusa nel sito o nella repository.
- Nessun prezzo inventato per le bevande. Le proposte con latticini o uova non sono presentate come vegane; i piatti vegetali richiedono conferma degli ingredienti allo staff.
- Galleria con ingrandimento, dialoghi chiudibili con Escape e pulsanti di prenotazione telefonica.
- Rispetto di `prefers-reduced-motion`, navigazione mobile, focus visibile, etichette e link per saltare al contenuto.
- Nessun modulo di prenotazione fittizio, tracker, feed social simulato o cookie di profilazione introdotto dalla pagina.

## Foto già collegate

| File nel sito | Foto fornita | Utilizzo |
| --- | --- | --- |
| `dist/assets/logo.jpg` | `logo.jpg` | Marchio nella barra di navigazione |
| `dist/assets/interior.jpg` | `interni locale.jpg` | Anteprima hero, atmosfera, salotto |
| `dist/assets/breakfast.jpg` | `colazione.jpg` | Colazione, tea bar, galleria |
| `dist/assets/toast.jpg` | `toast.jpg` | Proposte veggie e galleria |
| `dist/assets/pancakes.jpg` | `pancake.jpg` | Hero, brunch e galleria |
| `dist/assets/lunch.jpg` | `pranzo.jpg` | Galleria pranzo |

Non ci sono immagini placeholder da sostituire. Per cambiare una foto basta sostituire il corrispondente file, mantenendo il nome.

## Aggiornare menu e contatti

I prezzi e gli ingredienti sono raccolti nell’oggetto `menuData`, nello script di `dist/index.html`. Il blocco `<noscript>` contiene una copia testuale per chi disattiva JavaScript: aggiornala insieme ai dati. Per modificare le voci in evidenza usa gli array nelle chiamate a `renderGroup` subito dopo i dati.

Numero, indirizzo, orari e social sono quelli indicati nel brief dell’utente. Non è stata verificata la loro attualità con il locale. Prima dell’utilizzo commerciale, il gestore dovrà confermare listino, orari, informazioni di accessibilità e gli eventuali dati legali da aggiungere al footer. I nomi e i prezzi riproducono la fonte fornita, non un listino aggiornato acquisito online.

## Caricare su Vercel

La repository è pronta da importare in Vercel. `vercel.json` configura un sito statico senza installazione e senza compilazione:

1. Importa la repository `siti-web-torino/cafe-bloom`.
2. Mantieni la cartella principale del progetto sulla radice della repository (`./`).
3. Il preset è **Other**, la cartella di pubblicazione è **dist**. Lascia vuoti i comandi di installazione e compilazione.
4. Avvia il deploy dal tuo account Vercel. Non sono necessarie variabili d’ambiente.

La configurazione viene letta direttamente da `vercel.json`. Non viene fornito alcun collegamento automatico a un account o progetto Vercel. Dopo aver scelto il dominio, puoi aggiungere il suo URL canonico ai metadati della pagina. Qualsiasi altro hosting statico può pubblicare la stessa cartella `dist`.

Le fotografie e il marchio sono materiali forniti dall’utente. Non viene attribuita una licenza di riutilizzo a questi asset.
