# Tabelline Quest 🦊✖️

Un piccolo gioco web per imparare le tabelline, pensato per bambini di 7-9 anni. Funziona sul telefono, anche offline, e non ha bisogno di server: è un'unica pagina HTML.

## Come funziona il gioco

- **Mappa delle tabelline**: si parte da 1 e 2, le altre si sbloccano una alla volta (ordine: 1, 2, 10, 5, 3, 4, 6, 9, 7, 8) prendendo almeno 1 ⭐ nella Sfida della precedente.
- **Per ogni tabellina, tre modi di giocare**
  - 📖 **Impara**: ogni moltiplicazione con i pallini a righe, la sequenza dei multipli e un trucco per ricordarla.
  - 🎯 **Allenati**: risposta a scelta tra 4 opzioni, con aiutino. Gli errori non penalizzano, ma tornano a fine partita.
  - 🏆 **Sfida**: 10 domande a risposta scritta col tastierino. 10/10 = 3 ⭐, 8-9 = 2 ⭐, 6-7 = 1 ⭐.
- **Missione del giorno**: 10 domande scelte dalle tabelline sbloccate, con più peso a quelle sbagliate o poco ripassate (ripetizione dilazionata).
- **Ricompense**: monete 🪙, serie di giorni consecutivi 🔥, forzieri 🎁 con figurine comuni/rare/epiche, medaglie 🏅.
- **Area genitori** (⚙️ nella home): mappa a colori di tutti i prodotti da 1×1 a 10×10 (rosso = da ripassare, verde = saputo), suoni, voce che legge le tabelline, sblocco di tutte le tabelline, azzeramento.

I progressi sono salvati nel browser del telefono (`localStorage`): non viene inviato nulla in rete.

## Pubblicare su GitHub Pages

1. Crea un nuovo repository su GitHub (ad esempio `tabelline-quest`).
2. Carica questi file nella radice: `index.html`, `manifest.json`, `sw.js`, `icon.svg`, `README.md`.
3. Vai in **Settings → Pages**, scegli **Deploy from a branch**, branch `main`, cartella `/ (root)`, e salva.
4. Dopo circa un minuto il gioco è online su `https://TUO-UTENTE.github.io/tabelline-quest/`.

## Installarlo sul telefono

- **Android (Chrome)**: apri il link → menu ⋮ → *Aggiungi a schermata Home*.
- **iPhone (Safari)**: apri il link → tasto Condividi → *Aggiungi alla schermata Home*.

Dopo la prima apertura funziona anche senza connessione. Attenzione: i progressi sono legati al telefono e al browser usati; se si cambiano o si cancellano i dati del sito, si ripartirà da zero.

## Personalizzare

Tutto è in `index.html`, in cima allo script:

- `ORDER`: ordine di sblocco delle tabelline.
- `TIPS`: i trucchetti mostrati per ogni tabellina.
- `STICKERS`: figurine disponibili (emoji) e rarità (`c` comune, `r` rara, `e` epica).
- `BADGES`: medaglie e condizioni per ottenerle.
- `starsFor()`: soglie per le stelle.
