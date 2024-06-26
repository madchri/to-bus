# TO Bus
Questa applicazione per Android, creata utilizzando Python e la libreria Flet, consente di recuperare gli orari di transito dei veicoli della GTT (Gruppo Torinese Trasporti) ad una fermata specifica.

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

## Funzionalità
**Avvisi**:

Appena avviata, l'app accoglie l'utente con una pagina contenente tutti gli avvisi sulla mobilità recentemente pubblicati da GTT.

**Ricerca**:

Nella parte superiore della pagina è ben evidenziata ed accessibile la barra di ricerca che consente di immettere il numero della fermata che si desidera per ottenere gli orari di transito.
Una volta eseguita, la ricerca mostra tutti i mezzi in arrivo alla fermata specificata, ognuno con la relativa direzione ed orario: quest'ultimo è reso di immediata comprensione grazie alla visualizzazione dei minuti restanti all'arrivo del mezzo rispetto all'orario in cui è stata effettuata la ricerca.

In particolare, le diciture sono articolate come segue:
-  Indicazione del tipo di mezzo (tramite icona)
-  Indicazione del nome della linea
-  Indicazione dei minuti rimanenti all'arrivo
-  Indicazione del tipo di orario: programmato o in tempo reale
-  Indicazione dell'orario di arrivo stimato
-  Indicazione della direzione del mezzo
-  Indicazione dell'accessibilità del mezzo per utenti disabili (tramite icona)

**Impostazioni**:

Permette di consultare i crediti dell'applicazione, verificarne gli aggiornamenti e gestire alcune impostazioni.
- Tema: consente di scegliere tra tema chiaro o scuro
- Cerca all'avvio: consente di selezionare il campo di ricerca in modo automatico all'avvio dell'app

## Funzionamento
Una volta inserito il numero della fermata, l'applicazione si connette al server grazie al modulo `requests` e recupera le informazioni sugli orari di transito dei veicoli in formato json.
La query utilizzata per le richieste restituisce le informazioni organizzate in diversi dizionari, i quali includono il nome della linea, la direzione del veicolo e l'orario di arrivo alla fermata in secondi a partire dalla mezzanotte. Questi dati vengono gestiti in modo da renderne possibile la visualizzazione a schermo.

## Crediti
L'icona dell'app è stata ottenuta da icon-icons.com sotto licenza Creative Commons CC BY 4.0 Deed.

I dati sugli orari dei mezzi pubblici e gli avvisi di servizio presenti nell'app sono forniti da GTT e sono utilizzati solo a fine informativo.

La funzione per contattare l'api GraphQL di "Muoversi a Torino" (MATO) è stata da me sviluppata partendo dal lavoro svolto da @madbob con la sua "GTT Pirate API", disponibile su GitHub sotto licenza GPL-3.0.

L'applicazione è open source e non ha scopo di lucro.
