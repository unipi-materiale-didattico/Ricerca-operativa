# Lezione 27/09/2022

## Problema dello zaino

* n oggetti;
* $p_i > 0$ peso dell'oggetto;
* $c_i > 0$ benefico dell'oggetto;
* 1 zaino;
* $b (> 0) =$ capacità dello zaino;
* $p_i < b$.

Per ciascun oggetto devo decidere se prenderlo o no$\implies x_i \in \{{0,1\}}$ 

$x_i(variabile\space logica) =$

* 0 se non prendo l'oggetto;
* 1 se prendo l'oggetto;

$X = \{0,1\}^n$

### Vincoli

$\sum_{i = 1}^{n} p_ix_i \leq b$

### Funzione obiettivo

$max\{\sum_{c = 1}^{n} c_ix_i\}$

## Problema: Bin packing/Impacchettamento

* n oggetti;
* m contenitori;
* $p_i > 0$ peso dell'oggetto i;
* $c_j > 0$ capacità del contenitore j;
* $p_i < c_j$;
* $\sum_{i = 1}^{n}p_i \leq\sum_{j = 1}^{m}c_j$;

Inserire tutti gli oggetti nei contenitori in modo da minimizzare il numero di contenitori usati.

$x_{ij} =$

* 1 se l'oggetto i viene inserito nel contenitore j
* 0 se l'oggetto i viene inserito in un altro contenitore.

$y_j =$

* 1 se si usa il contenitore j;
* 0 se non si usa il contenitore j.

### Funzione obiettivo

$min\{\sum_{j=1}^{m}y_j\}$

### Vincoli

* $\sum_{j=1}^{m} x_{ij} = 1;\space\space i fissato = 1...n\longrightarrow vincoli\space di\space semiassegnamento$;
* $\sum_{i=1}^{n} p_ix_{ij} \leq c_jy_j;\space\space j fissato = 1...m\longrightarrow Vincoli\space di\space capacità$;
* $x_{ij} \in \{0,1\}\longrightarrow Vincolo\space di\space interezza$
* $y_j \in \{0,1\}$. 

### Variante

Se prendo 4 oggetti da mettere in 3 contenitori:

* i:
  * 1
  * 2
  * 3
  * 4
* $p_i$:
  * 5
  * 2
  * 5
  * 6
* j:
  * 1
  * 2
  * 3
* $c_j$:
  * 9
  * 6
  * 9     

Sena vincolo di interezza, potrei usare 2 contenitori frazionando gli oggetti.

### Variante 2

$\{1...n\} = I\space U\space A;$

$I \cap A = \varnothing$

$i \in I,l \in A$

$x_{ij} + x_{lj} \leq 1,\space j = 1...n\longrightarrow Vincolo\space di\space incompatibilità$

$x_{ij}x_{lj} = 0 \longrightarrow Corretta\space ma\space non\space lineare.$