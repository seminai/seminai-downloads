# Guida a Seminai

La distribuzione pubblica e la registrazione dei nuovi account sono in preparazione.
Gli utenti Core esistenti continuano ad accedere a [app.seminai.tech](https://app.seminai.tech).
Le istruzioni di download e registrazione seguenti si applicano dopo l’apertura.

## Account e installazione

1. Usa il browser su [app.seminai.tech](https://app.seminai.tech), oppure scarica un installer dalla pagina ufficiale.
2. Crea un account gratuito e conferma l’indirizzo tramite l’email ricevuta.
3. Accedi e crea la tua azienda. Gli account hanno privilegi ordinari.

Puoi richiedere un nuovo messaggio di verifica dalla pagina di accesso. Se dimentichi la password,
usa “Password dimenticata”; il collegamento ricevuto scade e può essere utilizzato una sola volta.

Gli installer si chiamano **Seminai-Cloud-…**. Le vecchie edizioni locali sono separate.
Controlla `SHA256SUMS.txt` e le note della versione; la disponibilità di una firma viene dichiarata
solo quando verificata e le ricevute (notarizzazione Apple, Authenticode Windows, firma GPG)
sono allegate alla release. Non è necessario disattivare le protezioni del sistema operativo.

Pacchetti previsti, ancora in verifica:

| Sistema | Architettura | Formato |
| --- | --- | --- |
| macOS | Apple Silicon e Intel | DMG |
| Windows | x64 | Installer EXE |
| Linux | x64 e ARM64 | AppImage e DEB |

Su Windows ARM la prova prevista riguarda l'emulazione x64: non è un pacchetto ARM nativo.
Le note della versione pubblicata confermeranno sistemi operativi e prove effettivamente completate.

Verifica dei file scaricati:

```sh
shasum -a 256 -c SHA256SUMS.txt --ignore-missing   # Linux: sha256sum -c SHA256SUMS.txt --ignore-missing
gpg --import seminai-release-signing-key.asc        # confronta l'impronta con quella pubblicata qui sotto
gpg --verify SHA256SUMS.txt.asc SHA256SUMS.txt
```

Su Windows: `Get-FileHash .\<file> -Algorithm SHA256`. L'impronta della chiave GPG di
release è `C03C7844C7FD8F6B6C9B8DE48C567C22DBDECFBC`.

## Dati e disponibilità

Quaderno e allegati sono conservati sul server Seminai. Serve Internet anche per lavorare manualmente.
Il client desktop non contiene il database del server o i dataset riservati e non fornisce uso offline.
Se il servizio non risponde, usa “Riconnetti”. Non presumere che modifiche non confermate siano state salvate.
Le installazioni locali esistenti restano indipendenti: questa fase non include importazione o migrazione.

## Quota AI

L'AI dei nuovi account gratuiti è attualmente disabilitata. Le condizioni e le
integrazioni degli account Core esistenti restano invariate. Le funzioni manuali
saranno disponibili ai nuovi utenti dopo l'apertura delle registrazioni.
L'attivazione dell'AI gratuita richiede limiti di spesa verificati e controlli
sulla riservatezza dei risultati; le integrazioni con costi richiedono l'abilitazione del gestore.

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
