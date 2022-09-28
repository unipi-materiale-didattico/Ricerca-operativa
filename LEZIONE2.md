# Classificazione dei problemi di ottimizzazione

Si fanno 3 distinzioni: per spazio delle soluzioni, per funzione obiettivo e per vincoli.

## 1

* $X = ℝ^n$ ottimizzazione continua;
* $X$ finito/numerabile => ottimizzazione discreta
  * $X = {0,1} \implies$ ottimizzazione combinatoria;
  * $X = Z^n  \implies$ ottimizzazione intera
* $X = ℝ^n \space x \space Z^n \implies$ ottimizzazione mista.

## 2

* $f: X => ℝ$ 
  * lineare $(f(x) = c_1x_1 + ... c_nx_n);$
  * non lineare.    

## 3

* $A = \{{x \subset X : g_1(x)\leq 0 ... g_n(x) \leq 0}$
  * $g_i$ = funzioni vincolari $X \rightarrow ℝ$ possono essere:
    * Affini (lineare + costante)
    * Non lineari.

Programmazione lineare: f lineare, gi affini (spazio $ℝ^n$).

* Lineare intera: $X = Z^n, X = \{{0,1\}}.$

Programmazione non lineare: almeno una delle funzioni non e' lineare.

### Problema:

Si devono produrre 1000 pezzi ferrosi da 1kg ciascuno che contengano:

* Una quantita' di Manganese >= 0,45%;
* Una quantita' di Silicio compresa tra il 3,25% e il 5,5%.

Supponiamo di avere 4 materiali:

* A con 0,45% di M, 4% di S e di prezzo al chilo 25;
* B con 0,5% di M, 1% di S e di prezzo al chilo 30;
* C con 0,4% di M, 0,6% di S e di prezzo al chilo 18.
* Manganesio che costa 10.000 al chilo.

#### Spazio:

$X = ℝ^4$ perche' ho 4 variabili/componenti.
$x = (x_a,x_b,x_c,x_M).$

#### Vincoli:

* $x_a + x_b + x_c + x_M = 1.000;$
* $x_a, x_b, x_c, x_M \geq 0;$
* $0,0045 x_a + 0,005 x_b + 0,004 x_c + x_M >= 4,5;$
* $32,5 \leq 0,04 x_a + 0,01 x_b + 0,006 x_c;$
* Quantita' totale di Silicio $\leq 55;$

#### Funzione obiettivo:

$min \space f(x) = 25x_a + 30 x_b + 18 x_c + 10.000 x_M$

E' un problema di programmazione lineare.

Le variabili introdotte sono variabili quantitative.

### Problema

3.000 wafer di silicio

* Con i wafer produco:
  * 500 C;
  * 300 P;
* resa: 
  * C = 60%;
  * P = 50%;
* prezzo:
  * 200 C;
  * 500 P;
* Produzione massima:
  * 400.000 P;
  * 700.000 C;

#### Spazio

$X = Z^2.$

#### Funzione obiettivo

$max\space f(x) = 200 x_c + 500 x_p$

#### Vincoli

* $x_c \leq 700.000$
* $x_p \leq 400.000$
* $x_p/150 + x_c/300 (numero\space di\space  wafer\space necessari\space a \space produrre\space x_\space c \space processori \space C\space e\space x_p\space processori \space P) \leq 3000. \space Semplificando: 2 x_p + x_c \leq 900.000.$
* $x ∈ \Z_+$(vincolo di interezza).

#### Osservazione

Il fatto che una variabile sia quantitativa non indica se e' continua o discreta.

#### Osservazione

Avremmo potuto fare in maniera diversa:

* $w_c =$ # wafer dedicati ai processori C;
* $w_p$ = # wafer dedicati ai processori P;
* $x_p = 150 w_p \implies$ sostituzione nel ragionamento $\implies$ formulazione in termini di wafer.
* In questo modo siamo sicuri di ottenere degli interi
* Le due soluzioni ottimali potrebbero essere leggermente diverse.
