# Scenario
Il nostro negozio sta crescendo e quindi è arrivato il momento di vendere i nostri prodotti all'estero. Pertanto, consentiamo ai clienti di pagare in diverse valute. A seconda della valuta, il cliente deve pagare un sovrapprezzo oltre al prezzo effettivo, che è definito dalla somma dei prezzi totali dei prodotti. In questo scenario non ci preoccupiamo di sommare il premio, ma di implementare il calcolo del sovrapprezzo e di convertire il prezzo nella valuta scelta.
 
## Task 1 - Calcolo del prezzo della tariffa extra
Poiché vendiamo i nostri prodotti dalla Germania, nessun cliente dell'area Euro deve pagare una tassa. **Per tutti gli altri paesi applichiamo una tariffa del 7%, ma almeno di 10,00€**. Ci sono alcuni casi eccezionali che dobbiamo considerare:

| States  |  Percentage  |
|---|---|
| GBP: 5%  | nessuna commissione minima (sterline britanniche)  |
| CHF: 3%  | nessuna commissione minima (Franchi svizzeri) |
| DKK: 4% | nessuna commissione minima (corone danesi)  |
| USD: 6% | commissione minima di 8,00 EUR (dollari USA)  |
| CAD: 6% | commissione minima di 9,00 EUR (dollari canadesi) |

Fate attenzione ai casi di errore come, ad esempio, i prezzi negativi.
Il vostro compito è quello di implementare la logica aziendale per il calcolo della tariffa. A questo punto, non ci si deve preoccupare di convertire il prezzo da €  alla valuta del cliente.

Utilizzare il ciclo di sviluppo guidato dai test:

Scrivere un test che fallisce

Far passare il test

Riformulare il codice

## Task 2 - Conversione di valuta Calcolo del prezzo
È giunto il momento di calcolare il prezzo che il cliente dovrà pagare. Se il cliente vuole pagare nella sua valuta, dobbiamo convertire il prezzo calcolato con le spese nella valuta corretta.
Poiché non abbiamo alcun controllo sui risultati e sulla disponibilità dei servizi, i test non dovrebbero dipendere direttamente da essi, ma usare i mock per simulare il loro comportamento.
Ci si deve preoccupare dei casi di errore, come l'assenza di un tasso di conversione per una determinata valuta o per un momento specifico, come qualcosa nel futuro.
Il vostro compito è quello di implementare la logica di business estesa per la conversione di valuta. Continuare a fare TDD e utilizzare anche la libreria Moq per simulare il comportamento. Ricordare che i convertitori forniti sono delle scatole nere per voi. Non si può prevedere il loro comportamento.
