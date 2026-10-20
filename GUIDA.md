# Guida a Seminai

La versione preliminare 1.1.1 è scaricabile da [download.seminai.tech](https://download.seminai.tech).
La registrazione gratuita è aperta con verifica email obbligatoria.
Nuovi utenti e utenti Core esistenti accedono allo stesso servizio su
[app.seminai.tech](https://app.seminai.tech).

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

Pacchetti pubblicati:

| Sistema | Architettura | Formato |
| --- | --- | --- |
| macOS | Apple Silicon e Intel | DMG e ZIP |
| Windows | x64 | Installer EXE |
| Linux | x64 e ARM64 | AppImage e DEB |

I DMG Mac sono firmati, notarizzati e corredati dal ticket Apple. L'installer Windows,
l'app e il disinstallatore sono firmati; la verifica crittografica è stata eseguita
senza un ambiente Windows. Il collaudo nativo Windows è stato rinviato dal gestore.
L'emulazione su Windows ARM non è verificata e non viene distribuito un pacchetto ARM nativo.
Tutti i pacchetti Linux contengono il client controllato; il DEB ARM64 ha superato
installazione, avvio e rimozione in un contenitore isolato. Questo non certifica
ogni distribuzione o tutte le interazioni desktop. Per questo la release è preliminare.

Verifica dei file scaricati:

```sh
shasum -a 256 "<file scaricato>"                   # Linux: sha256sum "<file scaricato>"
gpg --import seminai-release-signing-key.asc        # confronta l'impronta con quella pubblicata qui sotto
gpg --verify SHA256SUMS.txt.asc SHA256SUMS.txt
```

Su Windows: `Get-FileHash .\<file> -Algorithm SHA256`. L'impronta della chiave GPG di
release è `C03C7844C7FD8F6B6C9B8DE48C567C22DBDECFBC`.
Confronta il risultato SHA-256 con la riga dello stesso file in `SHA256SUMS.txt`.

## Dati e disponibilità

Quaderno e allegati sono conservati sul server Seminai. Serve Internet anche per lavorare manualmente.
Il client desktop non contiene il database del server o i dataset riservati e non fornisce uso offline.
Se il servizio non risponde, usa “Riconnetti”. Non presumere che modifiche non confermate siano state salvate.
Le installazioni locali esistenti restano indipendenti: questa fase non include importazione o migrazione.

## Quota AI

L'AI dei nuovi account gratuiti è attualmente disabilitata. Le condizioni e le
integrazioni degli account Core esistenti restano invariate. Le funzioni manuali
sono disponibili ai nuovi utenti dopo la verifica dell'email.
L'attivazione dell'AI gratuita richiede limiti di spesa verificati e controlli
sulla riservatezza dei risultati; le integrazioni con costi richiedono l'abilitazione del gestore.

Il piano previsto include un limite di 1 USD per utente al mese UTC, subordinato
a 20 USD condivisi. Il registro dei costi, le prenotazioni e il rinnovo delle quote
devono essere completati e verificati prima dell'attivazione. Non ci sono ricariche
o addebiti automatici agli utenti. Le funzioni manuali online restano indipendenti dall'AI.

Le richieste AI eventualmente abilitate inviano a OpenRouter i dati necessari
all’elaborazione. Audio, visione, OCR a pagamento e indicizzazione con embedding
restano esclusi finché non hanno controlli di costo e riservatezza verificati.

## Dataset riservati

Il servizio non consente di scaricare archivi o dataset completi, neppure tramite
chat o API. Per le selezioni nell'interfaccia sono mostrati solo nomi e codici
necessari; i parametri agronomici riservati non fanno parte delle risposte del catalogo.
I dati inseriti dall'utente e le esportazioni autorizzate della sua azienda restano
distinti dai dataset del gestore. Si applicano i [termini dell'edizione](TERMS.md).
