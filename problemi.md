# Problem 1

## [**La Lettera Palindroma di James**](https://www.hackerrank.com/challenges/the-love-letter-mystery/problem)

### Descrizione del Problema

James ha trovato una lettera d'amore che il suo amico Harry ha scritto alla sua fidanzata. James è un burlone, quindi decide di interferire con la lettera. Cambia tutte le parole nella lettera in palindromi.

Per fare questo, segue due regole:

1. Può solo ridurre il valore di una lettera, ovvero può cambiare 'd' in 'c', ma non può cambiare 'c' in 'd' o 'd' in 'b'.
2. La lettera 'a' non può essere ridotta ulteriormente.

Ogni riduzione nel valore di qualsiasi lettera viene contata come una singola operazione. Trova il numero minimo di operazioni necessarie per convertire una data stringa in un palindromo.

### Esempio

Le seguenti due operazioni sono eseguite: `cde → cdd → cdc`. Restituire `2`.

### Definizione

- Parametri:  `String s` - il testo della lettera
- Restituisce: `int` - il numero minimo di operazioni

### Formato di Input

- La prima riga contiene un intero `q`, il numero di richieste.
- Le prossime `q` righe conterranno ciascuna una stringa `s`.

### Vincoli

- `1 ≤ $|s|$ ≤ $10^4$`
- Tutte le stringhe sono composte da lettere minuscole dell'alfabeto inglese, ascii[a-z], senza spazi.

### Esempi:

**Input:**

```
STDIN   Function
-----   --------
4       q = 4
abc     query 1 = 'abc'
abcba
abcd
cba
```

**Output:**

```
2
0
4
2
```

**Spiegazione**

•	Per la prima richiesta, `abc → abb → aba`.

•	Per la seconda richiesta, `abcba` è già una stringa palindroma.

•	Per la terza richiesta, `abcd → abcc → abcb → abca → abba`.

•	Per la quarta richiesta, `cba → bba → aba`.

# **Input: `letter.txt` Output**: `“**300883**"`

Note: il risultato deve essere la somma di tutti gli output. Quindi la somma delle operazioni minime per ogni riga.
E**sempio**: 2 + 0 + 4 + 2 = 8

---

# Problem 2

## [**AlternateParity**](https://archive.topcoder.com/ProblemStatement/pm/18085)

### Descrizione del Problema

Ti vengono dati due numeri interi positivi `N` e `L`. Conta tutte le sequenze di numeri interi positivi che soddisfano le seguenti proprietà:

1. La sequenza è strettamente crescente.
2. La lunghezza della sequenza è `L`.
3. Nessun due elementi consecutivi condividono la stessa parità.

Ritorna il numero di queste sequenze, modulo $10^9 + 7$.

### Definizione

- **Parametri**: `int N`, `int L`
- **Restituisce**: `int`

### Vincoli

- `1 ≤ N ≤ 100.000`
- `1 ≤ L ≤ N`

### Esempi

1. **Input**:
    - `N = 6`, `L = 6` **Output**: `“1"`
    
    **Spiegazione**:
    
    L'unica sequenza valida è `{1, 2, 3, 4, 5, 6}`.
    
2. **Input**:
    - `N = 5`, `L = 2` **Output**: `“6"`
    
    **Spiegazione**:
    
    Le sei sequenze valide sono: `{1, 2}`, `{1, 4}`, `{2, 3}`, `{2, 5}`, `{3, 4}`, e `{4, 5}`.
    
3. **Input**:
    - `N = 12`, `L = 4` **Output**: `“105"`
    
    **Spiegazione**:
    
    Alcune di queste 105 sequenze sono: `{1, 2, 5, 10}`, `{2, 5, 8, 11}`, `{3, 6, 7, 8}`, e `{5, 8, 9, 12}`.
    

# `N = 99998`, `L = 51234` **Output**: `“658225097"`

# Problem 3

## [PezzoDiPuzzleMancante](https://archive.topcoder.com/ProblemStatement/pm/18084)

Hai un puzzle rettangolare. Il puzzle è composto da R righe e C colonne di pezzi di puzzle, approssimativamente quadrati.

Quando il puzzle è completato, ogni pezzo ha un posto specifico nella griglia. Possiamo etichettare le righe del puzzle usando le prime R lettere maiuscole dell'alfabeto inglese (dall'alto verso il basso) e le colonne del puzzle con numeri interi positivi (da sinistra a destra). L'etichetta di ciascun pezzo del puzzle viene quindi prodotta concatenando l'etichetta della riga e della colonna.

Ad esempio, il pezzo in alto a sinistra è "A1", e in un puzzle con R=4 righe e C=14 colonne il pezzo in basso a destra è "D14".

La tua amica sta lavorando su un'app che può aiutare a montare il puzzle. Finora, ha implementato la parte che può analizzare un pezzo di puzzle e determinarne l'etichetta.

Purtroppo, dopo aver testato il suo codice sul tuo puzzle, hai capito che manca un pezzo del puzzle.

Ti vengono dati R, C e una stringa `pieces[]` che contiene le etichette di tutti i pezzi del puzzle che possiedi. Devi restituire l'etichetta del pezzo mancante.

### Definizione

- Parametri: `int R`, `int C`, `String[] pieces`
- Restituisce: `String`

### Vincoli

- `1 ≤ R ≤ 20`
- `1 ≤ C ≤ 20`
- `pieces[R*C - 1]`
- Tutti gli elementi di `pieces` saranno distinti.
- Ogni elemento di `pieces` sarà un'etichetta valida di un pezzo del puzzle in un puzzle di dimensioni `R x C`.

### Esempi

1. **Input:**
    - `R = 1`, `C = 1`, `pieces = {}`**Output:** `"A1"`
    
    Un caso molto triste: l'unico pezzo del tuo puzzle 1x1 è mancante. Ovviamente, il pezzo mancante è "A1".
    
2. **Input:**
    - `R = 3`, `C = 3`, `pieces = {"A1", "B1", "C1", "C2", "C3", "B3", "A3", "A2"}`**Output:** `"B2"`
    
    Il pezzo centrale di un puzzle 3x3 è mancante in questo caso di test.
    
3. **Input:**
    - `R = 3`, `C = 3`, `pieces = {"A1", "A2", "A3", "B1", "B3", "C1", "C2", "C3"}`**Output:** `"B2"`
    
    Lo stesso puzzle dell'esempio precedente. L'unica differenza è che i pezzi non mancanti sono presentati in un ordine diverso.
    

# `R = 19`, `C = 10`, `pieces = {"P6","H9","D10","R9","E6","M8","G7","J1","R8","N7","P1","A9","C6","E4","L6","F10","A4","B1","C2","J4","D7","P10","F4","S1","L8","A8","G9","I7","M7","K8","O4","H4","B3","J10","K7","S9","C8","M4","B4","L10","I1","J3","P7","K9","P2","Q7","S6","I9","N6","I6","C10","K1","N2","N4","Q9","D3","B10","F1","L5","E1","E10","B6","G4","A3","C7","A6","Q3","E8","S10","C1","S2","L4","S7","I8","H5","J5","H8","R1","M6","L2","B8","O1","N1","Q6","R3","M5","A5","F8","L1","G5","H3","C5","Q8","G3","K4","E3","K5","R5","E2","H6","L3","Q1","P9","J9","D4","N3","F9","N10","A2","P4","G10","R10","O2","F3","J6","L7","K6","F7","R7","S4","J2","F5","E7","O5","N5","D2","I4","L9","S3","G1","B5","R2","O8","H10","H2","C3","A1","R6","O7","A7","B9","M9","E5","M1","Q4","I3","J7","D9","K3","G6","K10","P8","D8","Q2","N8","C9","F6","I2","D6","P3","F2","I10","J8","G2","I5","H1","G8","N9","O6","B7","M2","O3","A10","O10","Q10","Q5","C4","H7","D5","D1","S5","S8","M10","O9","E9","R4","B2","M3","K2"}` **Output:** `"P5"`

# Problem 4

---

## [**MonitoraggioSpeseFrodolente**](https://www.hackerrank.com/challenges/fraudulent-activity-notifications/problem)

### Descrizione del Problema

La Banca Nazionale di Jemoria ha una semplice politica per avvisare i clienti riguardo a possibili attività fraudolente sul conto. Se l'importo speso da un cliente in un determinato giorno è maggiore o uguale al doppio mediana delle spese del cliente per un numero precedente di giorni, la banca invia una notifica al cliente riguardo a un potenziale rischio di frode. La banca non invia notifiche al cliente finché non ha almeno quel numero di giorni di dati sulle transazioni precedenti.

Dato il numero di giorni precedenti e le spese giornaliere totali di un cliente per un periodo di giorni, determina il numero di volte in cui il cliente riceverà una notifica su tutti i giorni.

### Esempio

Per i primi tre giorni, la banca raccoglie solo dati sulle spese. Al giorno 4, le spese precedenti sono [2, 3, 4, 2, 3]. La mediana è 3 e la spesa del giorno è 6. Poiché 6 ≥ 6 (dove 6 è il doppio della mediana), verrà inviata una notifica. Il giorno successivo, le spese precedenti sono [3, 4, 2, 3, 6] e le spese sono 8. Anche questo è maggiore della mediana, quindi verrà inviata un'altra notifica. In totale, durante questo periodo, sono state inviate due notifiche.

Nota: La mediana di una lista di numeri può essere trovata ordinando i numeri in ordine crescente. Se c'è un numero dispari di valori, viene scelto quello centrale. Se c'è un numero pari di valori, la mediana è definita come la media dei due valori centrali.

### **Function Description**

- `int d`: il numero di notifiche inviate
- `int expenditure[n]`*:* daily expenditures

### Vincoli

- `1 ≤ n ≤ 2 × $10^5$`
- `1 ≤ d ≤ n`
- `0 ≤ expenditure[i] ≤ 200`

### Esempi

1. **Input:**
    - `n = 9`, `d = 5`, `pieces = {2 3 4 2 3 6 8 4 5}`**Output:** `"2"`
    
    **Spiegazione**:
    
    Calcola il numero totale di notifiche che il cliente riceve durante un periodo di 9 giorni. Per i primi cinque giorni, il cliente non riceve notifiche perché la banca non ha dati sufficienti sulle transazioni. Il sesto giorno, la banca ha 5 giorni di dati precedenti sulle transazioni [2, 3, 4, 2, 3] e il cliente spende 6 dollari. Poiché 6 ≥ 6 (dove 6 è il doppio della mediana), viene inviata una notifica. Il giorno successivo, la banca ha 5 giorni di dati precedenti [3, 4, 2, 3, 6] e il cliente spende 8 dollari, che è maggiore della mediana, quindi viene inviata un'altra notifica. In totale, sono state inviate due notifiche.
    
2. Input:
    - `n = 5`, `d = 4`, `pieces = {1 2 3 4 4}`**Output:** `"0"`
    
    **Spiegazione**:
    
    Sono necessari 4 giorni di dati, quindi il primo giorno in cui potrebbe essere inviata una notifica è il giorno 5. Le spese precedenti sono [1, 2, 3, 4] con una mediana di 2.5. Il cliente spende 4, che è inferiore a 2 × 2.5, quindi non viene inviata alcuna notifica.
    

# n = `200000` d = **`10122`** output: `1026`

input.txt

1.	**Giorni 1-3**: La banca raccoglie solo dati e non invia notifiche.

2.	**Giorno 4**:

•	Spese precedenti: [2, 3, 4]

•	Mediana delle spese precedenti: 3

•	Spesa del giorno: 6

•	Poiché 6 ≥ 3, **viene inviata una notifica**.

3.	**Giorno 5**:

•	Spese precedenti: [3, 4, 2]

•	Mediana delle spese precedenti: 3

•	Spesa del giorno: 8

•	Poiché 8 ≥ 3, **viene inviata un’altra notifica**.

# Problem 5

---

## [CiotoleDiCaramelle](https://archive.topcoder.com/ProblemStatement/pm/18239)

### Descrizione del Problema

Il gioco delle caramelle si gioca con `N` ciotole di caramelle. Le ciotole sono disposte in fila e numerate da 0 a `N-1` in sequenza.

Il gioco viene giocato da due giocatori che si alternano nei turni. Il giocatore che non può effettuare una mossa valida perde la partita. Ad ogni turno, il giocatore attuale ha due opzioni:

1. Selezionare una ciotola che attualmente contiene almeno due caramelle. Mangiare esattamente due di quelle caramelle.
2. Selezionare un numero dispari `k`. Selezionare una ciotola `x >= k` che attualmente contiene almeno `k` caramelle. Prendere esattamente `k` caramelle dalla ciotola `x` e metterle nella ciotola `(x-k)`.
(Ad esempio, supponiamo che tu scelga il numero dispari `k = 3`. Se la ciotola `10` contiene 100 caramelle, puoi selezionare `x = 10`. Prenderai quindi le `k = 3` caramelle dalla ciotola `x = 10`, lasciando 97 caramelle lì, e aggiungerai quelle tre caramelle a quelle presenti nella ciotola `(x-k) = 7`.)

Ti viene data la distribuzione iniziale di alcune caramelle: l'array `int[] C` con `N` elementi tale che per ogni `i`, la ciotola `i` contiene `C[i]` caramelle.

Ti vengono anche date `E` caramelle extra che devono essere aggiunte alle ciotole. (Devi aggiungere ciascuna delle `E` caramelle a una delle ciotole.)

Una distribuzione di caramelle è vincente se il giocatore che inizia il gioco ha una strategia vincente, cioè una strategia tale che il giocatore iniziale, seguendola, è garantito di vincere il gioco, indipendentemente da ciò che fa l'avversario.

Considera tutte le diverse distribuzioni di caramelle che possono essere ottenute iniziando con la distribuzione `C` e poi aggiungendo le `E` caramelle extra. Tra di esse, conta tutte quelle vincenti. Restituisci il loro conteggio modulo \(10^9 + 7\).

### Definizione

- **Parametri**: `int[] C`, `int E`
- **Restituisce**: `int`

### Note

Le caramelle sono indistinguibili. Pertanto, diverse distribuzioni di caramelle nelle ciotole sono semplicemente diverse `N`-tuple di numeri interi non negativi.

### Vincoli

- `1 ≤ C ≤ 100`
- `0 ≤ C[i] ≤ $10^9$`
- `0 ≤ E ≤ $10^6$`

### Esempi

1. **Input**:
    - `C = {4}`, `E = 3` **Output:** `"1"`
    
    **Spiegazione**:
    
    La posizione in cui l'unica ciotola (ciotola 0) contiene 7 caramelle è vincente. Questo perché l'unica mossa valida è mangiare due caramelle. Dopo che il primo, il secondo, e di nuovo il primo giocatore lo fanno, la ciotola avrà solo una caramella rimasta, e a quel punto il secondo giocatore perderà la partita poiché non ci sono mosse valide rimaste.
    
2. **Input**:
    - `C = {0, 0, 0, 0, 0, 0, 1}`, `E = 0` **Output:** `"0"`
    
    **Spiegazione**:
    
    La posizione descritta da questo `C` è perdente. L'unica mossa valida è prendere l'unica caramella e spostarla una ciotola a sinistra. Alla fine, il secondo giocatore sposterà la caramella nella ciotola 0 e poi il primo giocatore perderà.
    
3. **Input**:
    - `C = {0, 0, 0, 0, 0, 5, 0}`, `E = 0` **Output:** `"1"`
    
    **Spiegazione**:
    
    Il primo giocatore ha una mossa vincente: può iniziare spostando tutte e cinque le caramelle nella ciotola 0. Poi il secondo giocatore è costretto a mangiarne due, il primo giocatore ne mangia altre due, e poi il secondo giocatore perde la partita (con una caramella rimasta nella ciotola 0).
    

---

# `C = {13801157, 396785468, 682951182, 265601509, 431034015, 544656689, 192270657, 844502691, 189381670, 192209615, 647481449, 53886781, 231001523, 338394543, 654959070, 432279362, 703765701, 322000707, 786839155, 287368544, 671933863, 99681987, 325095825, 247043053, 46682255, 601999444, 506017811, 997758613, 965973116, 875313313, 328610375, 253339595, 317597696, 894692255, 490139238, 192337769, 189849489, 595094751, 325087308, 850177816, 494085229, 310477149, 312925620, 657037925, 795951971, 55600562, 896589650, 329287801, 975807843, 40733571, 707908843, 929726138, 73633916, 655557036, 643533008, 429162252, 609167346, 543472064, 456325863, 157158293, 406337811, 412934040, 706612068, 582866171, 240725785, 569160043, 601548321, 444055918, 742740156, 477778426, 579570713, 873508151, 951141124, 195851681, 271125097, 430168720, 343942783, 982086238, 359893798, 965526417, 133832752, 405968573, 467516742, 150919523, 96397850, 788783620, 465623791, 268026355, 253058919, 3795734, 275981015, 581999942, 878244190, 27255389, 860733383, 361917826, 425869258, 923440938}` ,`E = 470305` Output: `“111217051"`
