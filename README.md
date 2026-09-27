# Angolo di Benni — sito demo (multi-pagina)

Sito vetrina per un negozio di abbigliamento fittizio ("Angolo di Benni"), ristrutturato in versione **multi-pagina** con foglio di stile condiviso, sullo stesso modello usato per il sito "Da Tommy".

## Struttura

```
index.html        → Home (hero, fascia info rapida, link alle sezioni)
collezione.html    → Catalogo ad accordion per categoria + guida taglie
outfit.html         → Outfit pronti
chi-siamo.html     → Storia del negozio + recensioni
contatti.html      → Contatti, orari, mappa
style.css           → Tutto lo stile del sito, condiviso da ogni pagina
script.js            → Tutta la logica (catalogo, carrello, filtri, modal), condivisa da ogni pagina
images/             → Tutte le foto prodotto e del negozio
```

Ogni pagina HTML è ora molto più leggera: contiene solo il contenuto di quella sezione, non più uno stile e uno script ripetuti — esattamente come nel sito "Da Tommy".

## Come usarlo su GitHub Pages

1. Carica **tutti** i file (le 5 pagine .html, style.css, script.js) e la cartella images/ nella root del repository, mantenendo questa struttura piatta (nessuna sottocartella per le pagine).
2. Su GitHub Pages, la home resta `index.html` come prima: `https://tuonome.github.io/repo/`.
3. Le altre pagine sono raggiungibili come `.../collezione.html`, `.../outfit.html`, ecc.

## Novità di questa versione

- **Sito multi-pagina** invece di scroll unico: ogni sezione ha la sua pagina, con una vera navigazione (non più ancore su un'unica pagina lunghissima).
- **Meno HTML, più CSS**: stile e logica sono in due file esterni condivisi (`style.css`, `script.js`) invece di essere ripetuti identici in ogni pagina.
- **Sezioni raggruppate**: la guida taglie è ora dentro la pagina Collezione (era troppo corta per stare da sola), le recensioni sono dentro Chi Siamo.
- **Home più leggera**: hero, fascia rapida con indirizzo/orari/contatti, e tre link visivi alle altre sezioni.
- **Il carrello (richiesta) ora è persistente tra le pagine**: se aggiungi un pezzo su Collezione e vai su Contatti, la richiesta resta salvata (usa il localStorage del browser, non il server).
- Navigazione: la voce di menu della pagina in cui ti trovi è evidenziata in oro.

## Nota

`Fashionista.jpg` (foto dell'interno del negozio) non è inclusa in questo pacchetto perché l'avevi già caricata tu direttamente su GitHub — assicurati solo di non cancellarla quando carichi la cartella images/.

## Aggiornamento: animazioni e rifiniture (allineato a Da Tommy / BR1)

- **Foto sbiadite come sfondo** nelle intestazioni di Collezione, Outfit, Chi Siamo e Contatti (immagine reale attenuata con un velo di colore sopra, sempre leggibile).
- **Animazioni allo scorrimento**: i blocchi di contenuto compaiono con una dissolvenza leggera man mano che scorri, invece di apparire tutti insieme. Questa volta il sistema ha una **rete di sicurezza**: se per qualsiasi motivo l'animazione non si attivasse, il contenuto torna comunque visibile dopo 1,2 secondi — non può più restare "bloccato" nero come il vecchio bug.
- **Pulsante "torna su"** in basso a destra, compare dopo un po' di scroll su tutte le pagine.
- **Numeri animati** nella pagina Chi Siamo (anno di fondazione, generazioni, pezzi in collezione, % selezione a mano) che si contano da soli quando li scorri.

## Aggiornamento: email, note legali e "Crea il tuo look"

- **Email aggiornata** a studiomenny.web@gmail.com in tutto il sito (topbar, footer, contatti, script).
- **3 nuove pagine legali**: `privacy.html`, `cookie.html`, `note-legali.html`, collegate dal footer di ogni pagina.
- **Banner cookie**: compare una volta sola al primo accesso, ricorda la scelta (accetta/rifiuta) nel browser del visitatore.
- **Nuova funzione "Crea il tuo look"** (pagina Outfit): al posto di un manichino fotorealistico — che con foto di prodotti fotografati in modo diverso tra loro avrebbe rischiato di risultare posticcio — ho costruito una composizione "flat-lay" interattiva, la stessa tecnica che usano le boutique vere sui social. Il cliente sceglie un pezzo per zona (sopra, sotto, scarpe, accessorio: quest'ultima si disattiva da sola se si sceglie un vestito) e vede la composizione formarsi in tempo reale con le foto vere del catalogo, con tanto di totale prezzo (sconto incluso) e un pulsante per aggiungere l'intero look alla richiesta in un click.
