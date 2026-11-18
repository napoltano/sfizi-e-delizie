# Sfizi e Delizie – Gestionale

Gestionale web per il negozio di alimentari **Sfizi e Delizie**: funziona dal browser su telefono, tablet e computer, senza installare niente.

## Funzioni
- **Cassa**: lettura del codice a barre con la fotocamera, con un lettore USB/Bluetooth o scrivendolo a mano; ricerca per nome; articoli rapidi; importo libero.
  Chiusura con **Pagato** (contanti con resto, oppure carta/POS), **Aggiungi a debito di…** oppure **Crea nuovo debito**.
- **Magazzino**: articoli divisi per categoria, prezzi di vendita e di acquisto con margine, vendita a pezzo o a peso, scorta minima con avviso quando sta finendo.
- **Carico merce**: quantità per ogni prodotto, con tasti rapidi per le confezioni (+6, +12, +24…) e prezzo di acquisto.
- **Debiti**: conto per ogni cliente con fido facoltativo, prodotti o importi a mano messi a debito, acconti e saldi, storico dei movimenti.
- **Statistiche**: incasso, articoli più venduti (in generale e per categoria), incasso per categoria, articoli fermi.
- Modalità **chiara / scura**.

## Pubblicazione
Il sito è un'unica pagina (`index.html`) pubblicata con GitHub Pages.

## Database online (Firebase)
La versione pubblicata su GitHub salva i dati su **Firebase Firestore**, così sono gli stessi su ogni dispositivo. Funziona anche senza internet per un po': le vendite si sincronizzano appena torna la connessione.

- `firebase-config.json`: i dati di collegamento al progetto Firebase (non sono segreti: la protezione è data dal login e dalle regole).
- `firestore.rules`: le regole di accesso da incollare nella console di Firebase (Firestore → Regole). Solo le email elencate possono entrare.

Finché `firebase-config.json` non è compilato, il gestionale funziona lo stesso ma salva i dati solo sul dispositivo in uso.
