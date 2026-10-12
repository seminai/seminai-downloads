# Guida a Seminai Cloud

Il servizio è in preparazione. Le istruzioni seguenti si applicano dopo l’apertura.

## Account e installazione

1. Usa il browser su `cloud.seminai.tech`, oppure scarica un installer Cloud dalla pagina ufficiale.
2. Crea un account gratuito e conferma l’indirizzo tramite l’email ricevuta.
3. Accedi e crea la tua azienda. Gli account hanno privilegi ordinari.

Puoi richiedere un nuovo messaggio di verifica dalla pagina di accesso. Se dimentichi la password,
usa “Password dimenticata”; il collegamento ricevuto scade e può essere utilizzato una sola volta.

Gli installer si chiamano **Seminai-Cloud-…**. Le vecchie edizioni locali sono separate.
Controlla SHA256SUMS.txt e le note della versione; la disponibilità di una firma viene dichiarata
solo quando verificata. Non è necessario disattivare le protezioni del sistema operativo.

## Dati e disponibilità

Quaderno e allegati sono conservati sul server Seminai. Serve Internet anche per lavorare manualmente.
Il client desktop non contiene il database del server o i dataset riservati e non fornisce uso offline.
Se il servizio non risponde, usa “Riconnetti”. Non presumere che modifiche non confermate siano state salvate.
Le installazioni locali esistenti restano indipendenti: questa fase non include importazione o migrazione.

## Quota AI

L'AI è attualmente disabilitata. Le funzioni manuali restano disponibili quando
il servizio è aperto. Una futura attivazione richiede limiti di spesa verificati
e controlli sulla riservatezza dei risultati.

Quando abilitata, ogni utente dispone di un limite di 1 USD per mese UTC,
subordinato al limite condiviso di 20 USD.
Il servizio prenota il costo massimo prima della chiamata e conguaglia quando il provider comunica il costo.
Le richieste dall’esito incerto mantengono la prenotazione finché non vengono riconciliate.
Non ci sono ricariche o addebiti automatici agli utenti. Consumo, disponibilità e rinnovo sono visibili
nelle impostazioni. Esaurire la quota AI non blocca le funzioni manuali online.

Le richieste AI eventualmente abilitate inviano a OpenRouter i dati necessari
all’elaborazione. Audio, visione, OCR a pagamento e indicizzazione con embedding
restano esclusi finché non hanno controlli di costo e riservatezza verificati.

## Dataset riservati

Il servizio non consente di scaricare archivi o dataset completi, neppure tramite
chat o API. Per le selezioni nell'interfaccia sono mostrati solo nomi e codici
necessari; i parametri agronomici riservati non fanno parte delle risposte del catalogo.
I dati inseriti dall'utente e le esportazioni autorizzate della sua azienda restano
distinti dai dataset del gestore. Si applicano i [termini dell'edizione](TERMS.md).
