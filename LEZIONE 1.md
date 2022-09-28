# $Ricerca\space Operativa - Operations\space Research$

Si occupa di problemi di natura decisionale.

## Procedimento

* Problema reale
* Raccolta e analisi di informazioni e dati
* Costruzione di un modello logico-matematico (modellazione)
* Studio delle proprieta' matematiche del modello
* Determinazione di una o piu' soluzioni (algoritmi)
* Analisi ed interpretazione dei risultati

## Problemi di ottimizzazione

$X =$  spazio delle soluzioni (delle variabili)

$A ⊆ X =$ insieme delle soluzioni ammissibili (Regione ammissibile)

$f: X => ℝ =$ misura della "qualita'" delle soluzioni (Funzione obiettivo)

I problemi di ottimizzazione si dividono principalmente in:

* problemi di minimizzazione
* problemi di massimizzazione 

Un problema di massimizzazione puo' essere convertito in uno di minimizzazione. Massimizzare una funzione vuol dire minimizzare la sua opposta.

## Nomenclatura

### Valore ottimo

estremo inferiore di $\{f(x): x ∈ A\}$

$z* ∈ ℝ$ e' il valore ottimo di (P) se:

* $z^* \leftarrow f(x) ∀ x ∈ A$
* $z \leftarrow f(x) ∀ x ∈ A \rightarrow z \leq z^*$

$x^* ∈ X$ e' soluzione ottima di (P) se:

* $x^* ∈ A;$
* $f(x^*) \leq f(x) ∀ x ∈ A.$

$x^*\space è\space soluzione\space ottima\space \leftrightarrow f(x^*)\space e'\space il\space valore\space ottimo\space del\space problema.$

### Caso 1

$A = ∅$ 
Se il problema e' di minimo si dice che il valore ottimo e' +$\infty$

### Caso 2

Esiste il valore ottimo ed esiste la soluzione ottima

#### Esempio

$min \{{x^2 : x ∈ ℝ\}}$ 

$v^* = 0$

$x^* = 0$

### Caso 3

Esiste il valore ottimo ma non esiste la soluzione ottima

#### Esempio

$min\{{e^-x : x ∈ ℝ\}}$ 

$v^* = 0$ ma non esiste un punto in cui $e^-x$ vale 0.

### Caso 4

Non esiste il valore ottimo

#### Esempio

$min\{{logx : x > 0\}}$   

$∀ k ∈ ℕ \space ∃ x^k ∈ A \space t.c.\space f(x^k) < -k$

Problema infieriormente illimitato, $v^* = -\infty$