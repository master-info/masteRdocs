
## masteRstradario

### Dati

- `...` 


### Funzionalità

- `aggiorna_indirizzo` Dato l'identificativo di un indirizzo, aggiorna le corrispondenti coordinate nella tabella del database MySQL o Postgres

- `estrai_indirizzi_id` Dato un insieme di identificativi di indirizzi, ritorna le informazioni associate in una delle forme: vettoriale, tabellare, geografica o visuale.

- `estrai_indirizzi`  Dato uno fra: 
    - un codice di Zona (vedi campo `codice` della tabella `zone` del pacchetto `masteRgeo`)
    - la coppia di coordinate geografiche di un punto ed un raggio per poter calcolare un *buffer* circolare; 
    - le due coppie di coordinate geografiche tipiche di un riquadro di delimitazione (angoli inferiore sinistro e superiore destro); 
    - un oggetto `sf` poligoni, oppure punti /linee sui quali poter calcolare un riquadro che li racchiude;
    ritorna le informazioni associate agli indirizzi trovati, in una delle forme: vettoriale, tabellare, geografica o visuale.

- `estrai_strada` Dato l'identificativo di una sola strada, ritorna l'elenco di tutti gli indirizzi associati, ed eventualmente le informazioni corrispondenti, in una delle forme: vettoriale, tabellare, geografica o visuale.

- `estrai_strade` Dati l'identificativo di un insieme di strade, ritorna l'elenco di tutti gli indirizzi associati, ed eventualmente le informazioni corrispondenti, in una delle forme: vettoriale, tabellare, geografica o visuale.

- `indirizzo_da_coords` Date le coordinate geografiche di un punto, se questo risulta incluso in un Comune di cui sono noti tutti gli indirizzi ritorna l'indirizzo più vicino.

- `normalizza_indirizzo` Dato il testo di un possibile indirizzo, cerca di scomporlo nelle parti di cui è composto.

- `mappa_indirizzi` Dato un opportuno oggetto geografico `sf` di punti concernenti un insieme di identificativi di indirizzi (tipicamente il risultato dell'esecuzione di una delle funzione `estrai_*` di cui sopra), ritorna una mappa leaflet dei medesimi.
  Sebbene sia possibile mappare gli indirizzi direttamente con le altre funzioni usando l'opzione `out = 'M'`, con `mappa_indirizzi` è possibile aggiungere livelli addizionali di dati, quali edifici, popolazione da griglia 30mt, operatori, poi.

