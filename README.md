# Tabelline Quest 🦊✖️

Un piccolo gioco web per imparare le tabelline, pensato per bambini di 7-9 anni. Funziona sul telefono, anche offline, e non ha bisogno di server: è una pagina HTML con pochi file.

## Come è pensato

Invece di far ripetere a memoria la filastrocca (3×1=3, 3×2=6…), il gioco insegna **scorciatoie di ragionamento**, con disegni e strumenti sempre a portata di mano. Nessun cronometro, errori senza penalità.

- **Tabelline "ancora" prima, le altre ricavate**: si parte da 2 (il doppio), 10 (uno zero), 5 (metà del 10) e 4 (doppio del doppio). Poi 3 (2 volte + 1), 9 (10 volte − 1), 6 (5 volte + 1), 8 (doppio del 4) e 7 (5 volte + 2). Ogni moltiplicazione mostra il suo ragionamento passo passo.
- **Proprietà commutativa**: 7 × 3 = 3 × 7, con i pallini girati per vederlo. Il gioco dice quali moltiplicazioni "si sanno già" da una tabellina precedente: nel 7 resta da imparare davvero solo 7×7.
- **Tavola Pitagorica 🔢 sempre disponibile** (pulsante in alto in quasi ogni schermata e nella home). È colorata: ogni colore è una tabellina e i numeri "specchio" hanno lo stesso colore. Toccando un numero si vedono riga, colonna, disegno e ragionamento. Usarla non toglie stelle né monete.
- **Trucco delle dita 🖐️**: per il 9 (si abbassa un dito) e per le tabelline dal 6 al 10 (dita alzate = decine, dita abbassate si moltiplicano per le unità).
- **Aiutino con il ragionamento**, non con il risultato.
- **Calcolo veloce** 🧠: Amici del 10, Amici del 100, Passo dalla decina (8 + 5 → 10, poi 3), Trucco del +9 (+10 e −1).
- **Giochi** 🎲: Memory (operazione ↔ risultato), Tombola (cerca il risultato sulla cartella), Battaglia navale numerica (trova il numero sulla griglia della tavola: riga × colonna).
- **Si adatta**: la Missione del giorno pesca di più le moltiplicazioni sbagliate o poco ripassate; se ci sono troppi errori passa da sola alle risposte a scelta, poi torna alla tastiera quando va meglio.

## Per ogni tabellina

- 📖 **Impara**: il trucco, cosa si sa già, ogni moltiplicazione con disegno e passaggi.
- 🎯 **Allenati**: risposta a scelta tra 4 opzioni, con aiutino e dita.
- 🏆 **Sfida**: 10 domande a risposta scritta. 10/10 = 3 ⭐, 8-9 = 2 ⭐, 6-7 = 1 ⭐.

Le tabelline si sbloccano una alla volta (ordine: 1, 2, 10, 5, 4, 3, 9, 6, 8, 7) prendendo almeno 1 ⭐ nella Sfida della precedente. Dall'area genitori si possono sbloccare tutte.

## Ricompense

Monete 🪙, giorni di fila 🔥, forzieri 🎁 con 26 figurine (comuni, rare, epiche) e medaglie 🏅.

## Area genitori (⚙️ nella home)

Mappa a colori di tutti i prodotti da 1×1 a 10×10 (rosso = da ripassare, verde = saputo), suoni, voce che legge le tabelline, sblocco di tutte le tabelline e azzeramento dei progressi.

I progressi sono salvati nel browser del telefono (`localStorage`): non viene inviato nulla in rete.

> Questo gioco è un aiuto per esercitarsi in modo diverso, non sostituisce un percorso con insegnanti o specialisti.

## Pubblicare su GitHub Pages

1. Crea un nuovo repository su GitHub (ad esempio `tabelline-quest`), pubblico.
2. Carica questi file nella radice: `index.html`, `manifest.json`, `sw.js`, `icon.svg`, `README.md`.
3. Vai in **Settings → Pages**, scegli **Deploy from a branch**, branch `main`, cartella `/ (root)`, e salva.
4. Dopo circa un minuto il gioco è online su `https://TUO-UTENTE.github.io/tabelline-quest/`.

## Installarlo sul telefono

- **Android (Chrome)**: apri il link → menu ⋮ → *Aggiungi a schermata Home*.
- **iPhone (Safari)**: apri il link → tasto Condividi → *Aggiungi alla schermata Home*.

Dopo la prima apertura funziona anche senza connessione. I progressi sono legati al telefono e al browser usati.

## Personalizzare

Tutto è in `index.html`, in cima allo script:

- `ORDER`: ordine di sblocco; `ROLE` e `TRICK`: i trucchi mostrati per ogni tabellina.
- `STICKERS`: figurine (emoji) e rarità; `BADGES`: medaglie; `starsFor()`: soglie per le stelle.
- `HUE`: i colori della tavola pitagorica.
