# Lezione 28/09/2022

## Problema: fornitura di gas

### Testo

Per mitigare gli effetti della crisi energetica in corso il Ministro dell'Energia deve acquistare da produttori esteri L milioni di $m^3$ si gas da stoccare nei depositi nazionali. A tale scopo il Governo ha messo a disposizione uno stanziamento di E milioni di euro. Gli n produttori disponibili hanno dichiarato le loro tempistiche di fornitura e avanzato le loro richieste economiche: il produttore i può fornire $d_i$ milioni di $m^3$ al giorno al prezzo unitario $c_i$(espresso in milioni di euro).

Aiuta il ministro a decidere quanto gas acquistare da ciascun produttore in maniera da minimizzare il tempo complessivo di fornitura nel rispetto dello stanziamento disponibile (per tempo complessivo di fornitura si intenda il numero di giorni necessari a ricevere tutti gli L $m^3$ di gas).

### Dati

* L milioni di $m^3$ di gas da comprare;
* E milioni di euro a disposizione;
* n produttori
* $d_i$ milioni di gas al giorno che ogni produttore ci può mandare;
* $c_i$ prezzo unitario

### Variabili

$x_i$ = milioni di $m^3$ di gas da acquistare dal produttore i.

$X\in \Reals^n$.

### Vincoli

* $\sum_{i=1}^{n} c_i x_i \leq E \longrightarrow Vincolo\space di\space costo.$
* $\sum_{i=1}^n x_i = L \longrightarrow Vincolo\space di\space domanda.$

### Funzione obiettivo

$min\{max\space x_i/d_i\}$ non è lineare a causa del massimo (massimo di funzioni lineari $\implies$ non lineare).

$min \{t\} \longrightarrow t = Variabile\space ausiliaria$ 

$t \geq max\{x_i/d_i\}\space i= 1...n \longrightarrow Vincolo\space non\space lineare.$

$t \geq x_i/d_i\space\space\space\forall i \longrightarrow lineare.$

Approssimazione superiore del valore massimo cercato che va accompagnata con i $vincoli\space di\space soglia\space(t\geq x_i/d_i,\space i=1...n)$.

### Aggiunta

Aggiungo il costo del contratto con ogni produttore. Questo mi modifica il vincolo di costo. E' utile la variabile $y_i:$

$y_i$ =

* 1 se compro da i;
* 0 se non compro da i.

$\sum_{i=1}^{n} c_ix_i + cy_i\leq E \longrightarrow Vincolo\space di\space costo\space modificato.$

$x_i\leq y_iL$

