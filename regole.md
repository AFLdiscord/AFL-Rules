# Introduzione

Benvenuto/a su AFL (AFL Finisce per L), un server dedicato a discussioni e dibattiti di ogni genere, al commento di news e ad attività di gruppo (quali giornate di condivisione, cineforum, sessioni di gioco ecc.).

Il server è di sua natura poco gerarchico: viene riconosciuta la partecipazione attiva (vedi [Ruolo 🟩**Oratore**](https://github.com/AFLdiscord/AFL-Rules/blob/main/regole.md#ruolo-oratore) e [Ruolo 🟪**Cazzaro**](https://github.com/AFLdiscord/AFL-Rules/blob/main/regole.md#ruolo-cazzaro)) ed è presente uno staff di moderazione per mantenere tutto in ordine, ma non vi sono ruoli che facciano la differenza in una discussione, quindi non preoccuparti di esprimere la tua opinione [liberamente](https://github.com/AFLdiscord/AFL-Rules/blob/main/regole.md#come-affrontare-un-dibattito).

Inoltre, per evitare di fare troppa confusione, abbiamo limitato la possibilità di cambiare nickname nel server: attualmente, è possibile modificarlo una volta sola ogni 30 giorni, a partire dall'ultima modifica (o dall'ammissione ad AFL), dalle impostazioni di Discord o usando il comando `<setnick`.  
NOTA: il nickname non può contenere:
- nickname e/o username di altri AFL;
- termini che indichino l'appartenza allo staff (mod o simili).

Buona permanenza👍

## Regole di base
Le regole principali del server sono le seguenti:
1. Rimani nel topic del canale in cui stai mandando il messaggio;
2. Non mandare nulla che non rispetti la privacy di un altro AFL;
3. Non adottare comportamenti atti a creare disordine nel server;
4. Non commettere violenza verbale;
5. L'ultima parola spetta **sempre** ai moderatori, in qualunque situazione.

La lettura delle [linee guida di Discord](https://discordapp.com/guidelines) è invece obbligatoria per chiunque usi Discord. Sono 18 punti molto brevi, non vi prenderà troppo tempo e ne trarranno beneficio tutti i membri del server👍

Sul canale #anarchia valgono solamente le regole 2, 4, 5 e le linee guida di Discord sopraccitate.
***
## Ruoli
Qui verranno dettagliati i ruoli presenti nel server.

### 🟦 AFL
Ruolo conferito a chiunque venga ammesso nel server.
### 🟨 [dev](https://github.com/AFLdiscord/AFL-Rules/blob/main/regole.md#progetti-del-forum)
Ruolo conferito a chi lavora sul bot del server.
### 🟩 [Oratore](https://github.com/AFLdiscord/AFL-Rules/blob/main/regole.md#ruolo-oratore)
Ruolo conferito automaticamente a chi partecipa attivamente nei canali di discussione del server.
### 🟪 [Cazzaro](https://github.com/AFLdiscord/AFL-Rules/blob/main/regole.md#ruolo-cazzaro)
Ruolo conferito automaticamente a chi partecipa attivamente nei canali extra.
### 🟩 [AFL Moderatore](https://github.com/AFLdiscord/AFL-Rules/blob/main/regole.md#ruolo-afl-moderatore)
Ruolo conferito a chi si occupa della moderazione del server.
### 🟩 AFL M
Ruolo di amministrazione del server.
### 🟧 [Sotto sorveglianza](https://github.com/AFLdiscord/AFL-Rules/blob/main/regole.md#gestione-infrazioni)
Ruolo conferito automaticamente a chi viene warnato 3 volte nell'arco di una settimana.
### 🟥 Bot
Ruolo riservato ai bot.
***
## Ruolo 🟩**Oratore**
Il ruolo 🟩**Oratore** permette di partecipare alle discussioni su **#politica-interna** e votare le proposte nel canale **#proposte**.<br>L'assegnamento di tale ruolo è affidato al bot del server ed è attualmente impostato come segue:
- I canali considerati sono i canali di discussione;
- Si tiene conto di quanti messaggi sono stati mandati, giorno per giorno.
- Il bot, una volta al giorno, controlla il conteggio dei messaggi mandati da ogni AFL: se tale conteggio è maggiore o uguale a 100, il bot:
  - resetta il conteggio dei messaggi dell'AFL;
  - gli assegna il ruolo 🟩**Oratore**;
  - imposta la data di scadenza del ruolo alla settimana successiva.
- Se il conteggio è inferiore a 100, vengono resettati i messaggi dello stesso giorno della settimana precedente (se oggi è lunedì, i messaggi annullati saranno quelli del lunedì precedente, e così via).

Il ruolo viene prolungato se vengono scritti altri 100 (o più) messaggi entro una settimana dal ricevimento del ruolo.
Il resto è a discrezione dell'utente.
***
## Ruolo 🟪**Cazzaro**
Il ruolo 🟪**Cazzaro** indica una continuata attività nei canali extra.<br>L'assegnamento di tale ruolo è affidato al bot del server ed è attualmente impostato come segue:
- Ogni messaggio incrementa un contatore buffer;
- Si tiene conto della data e ora (timestamp) del primo messaggio inviato in uno dei canali della categoria extra;
- Ad ogni messaggio successivo, il bot effettua la seguente procedura:
  - se dal timestamp al momento del messaggio è passato almeno il tempo indicato nel campo `dank_time_window` del file di configurazione, il buffer ed il timestamp vengono resettati;
  - altrimenti, incrementa il contatore.
- Dopo aver incrementato il contatore, il bot legge il valore del contatore buffer e, se la soglia è stata raggiunta:
  - assegna il ruolo Cazzaro all'afler;
  - azzera il contatore;
  - ripristina il timestamp.

Il ruolo viene prolungato e rimosso allo stesso modo del ruolo 🟩**Oratore**, e le soglie sono indipendenti. La configurazione attuale prevede:
- Messaggi da inviare: 100
- Finestra di tempo: 7 giorni
- Durata del ruolo: 7 giorni

Il ruolo attualmente ha solo scopo estetico e - al contrario del ruolo 🟩**Oratore** - non consente di ottenere alcun privilegio aggiuntivo.

A parte il colore viola.
***
## Ruolo 🟩**AFL Moderatore**
Il ruolo 🟩**AFL Moderatore** viene assegnato da un 🟩**AFL M** esclusivamente su base fiduciaria: non può essere richiesto attraverso una votazione.

Chi riceve tale ruolo, è autorizzato a:
- cancellare eventuali messaggi non adeguati;
- accettare nuovi AFL che abbiano presentato correttamente (e solo in tale caso) la richiesta di iscrizione;
- controllare che le proposte siano valide e attuare quelle che ottengono un numero sufficiente di voti positivi, mettendone l'annuncio.

Un 🟩**AFL Moderatore** non può, invece:
- modificare la struttura del server di propria iniziativa;
- aggiungere bot di propria iniziativa;
- violare il regolamento;
- abusare del suo potere, nelle discussioni e/o nei provvedimenti da prendere.

La violazione di queste regole comporta un provvedimento stabilito da un 🟩**AFL M**, oltre alla perdita del ruolo.
***
## Gestione infrazioni
L'infrazione delle regole viene così gestita:
- 1a infrazione: warn;
- 2a infrazione: warn;
- 3a infrazione: warn + assegnamento del ruolo 🟧**Sotto sorveglianza**;
- 4a infrazione: ban.

È previsto il ban **immediato** per le seguenti infrazioni:
- tentativo di raid;
- utilizzo di account multipli sul server;
- violenza verbale.

I warn vengono **azzerati** dopo 7 giorni dall'ultimo warn ricevuto, mentre la revoca dei ban è gestita da 🟩**AFL M**.

***NB***: si precisa che 🟩**AFL Moderatore** e 🟩**AFL M** si riservano il diritto di eliminare ogni messaggio ritenuto inadeguato, ed eventualmente assegnare warn.
***
## #proposte
Il canale **#proposte** è pensato per poter dar voce alle proprie idee e contribuire attivamente al miglioramento del forum.

Regole del canale:

- Le proposte sono visibili a tutti, ma possono essere fatte e votate solo da membri con il ruolo [🟩**Oratore**](https://github.com/AFLdiscord/AFL-Rules/blob/main/regole.md#ruolo-oratore);
- Il sistema di voto è basato su due reaction: 🟢 e 🔴. Altre reaction, salvo approvazione dei moderatori, non sono ammesse;
- L'esito di una proposta è valido quando essa consegue la maggioranza assoluta (più della metà degli oratori ha votato un'opzione);
- Ogni proposta che ottiene la maggioranza favorevole verrà realizzata non appena possibile;
- Una proposta che non ottenga un esito valido (oppure che ottenga un pareggio) entro 2 giorni viene annullata;
- Gli 🟩**AFL M** hanno diritto di veto su proposte che puntino a modificare la struttura del server.
***
## #politica-interna
Queto canale è pensato per discutere in merito alla struttura del server stesso.

I messaggi mandati sono pubblici e chiunque può vedere le discussioni in tempo reale, ma l'invio di messaggi al suo interno è consentito solo a:
- moderatori;
- oratori.
***
## Come affrontare un dibattito
Un **dibattito** consiste nel mettere a confronto le proprie idee con quelle di un'altra persona, mettendo in mostra **fatti** e **conoscenze**, con l'ulteriore tentativo di abbattere eventuali bias cognitivi.

Le basi di un dibattito sensato sono poche:
- Sii informato su ciò che affermi, disponendo di **prove** qualora necessario, e argomentale adeguatamente.
- Se vuoi partecipare in ogni caso, devi dichiarare **in anticipo** che le tue sono semplici opinioni.
- Un dibattito **non è** un litigio: non arrabbiarti se una persona non la pensa come te, specie se è su internet.
- Se l'altra persona non riesce a controbattere, probabilmente hai vinto. Se dopo la umili, hai perso tu.
- Se invece hai perso, verifica la correttezza delle affermazioni dell'altra persona ed eventualmente accetta che possa avere ragione lei.

Se avete del tempo libero, vi consigliamo di leggere [questa pagina](https://it.wikipedia.org/wiki/Fallacia): riporta molte delle argomentazioni da evitare in un dibattito di qualità.
***
## Progetti del forum
Tutti i progetti pubblici del forum sono reperibili dalla [pagina dell'organizzazione su GitHub](https://github.com/AFLdiscord), amministrata da:
- [Skylake](https://github.com/Skylake-dev)
- [cathartyc](https://github.com/cathartyc)

Ogni membro del server può contribuire allo sviluppo *previa approvazione degli admin*: gli sviluppatori sono contrassegnati dal ruolo 🟨**dev**.

Per quanto riguarda le modalità di contribuzione, si rimanda al README dei singoli progetti.
