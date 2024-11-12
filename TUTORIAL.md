# Benvenuto in questo tutorial!

In questo tutorial ti insegneremo ad usare **GIT** e **GitHub** per un progetto in solitario o in team.

Ti consigliamo di vedere la storia di [GIT](./GIT.md) e di [GitHub](./GITHUB.md), clicca sui rispettivi nomi per la corrispettiva storia

## Capitolo 1- Come utilizzare GIT

### 0. Configurazione di Git
Una volta installato, Git ha bisogno di alcune informazioni di base per identificarti quando fai modifiche al codice.

Nel terminale, inserisci questi comandi (sostituisci tuo_nome e tua_email con il tuo nome e la tua email):

bash
Copia codice
git config --global user.name "tuo_nome"
git config --global user.email "tua_email"

### 1. **Inizializzazione di un Progetto Git**

Per iniziare a utilizzare Git, il primo passo è creare un repository locale sul tuo computer. Un repository è il luogo dove verranno conservate tutte le versioni del tuo progetto e le sue modifiche.

1. Crea una cartella per il tuo progetto sul computer, apri il terminale e spostati in quella directory.
2. Esegui il comando:

   ```bash
   git init
   ```

   Questo comando crea un repository Git locale nella cartella corrente. Ora, ogni file o sottocartella che aggiungerai sarà tracciato da Git. L'inizializzazione del repository aggiunge anche una cartella nascosta chiamata `.git`, che contiene tutte le informazioni necessarie per il controllo delle versioni del progetto.

### 2. **Aggiunta di File al Repository**

Una volta creato il repository, puoi iniziare ad aggiungere file al progetto e dirgli di tracciarli.

1. Crea o aggiungi dei file nella cartella del progetto.
2. Per iniziare a tracciare questi file, usa il comando:

   ```bash
   git add nomefile
   ```

   Se vuoi aggiungere tutti i file nuovi o modificati, usa:

   ```bash
   git add .
   ```

   Questo comando prepara i file per il commit. L'operazione di `add` non salva le modifiche in modo permanente ma indica a Git quali file includere nel prossimo commit.

### 3. **Creazione del Primo Commit**

Dopo aver aggiunto i file, il passo successivo è fare un commit. Un commit è un’istantanea del tuo progetto in un determinato stato.

1. Esegui il comando:

   ```bash
   git commit -m "Primo commit del progetto"
   ```

   Il messaggio tra virgolette dovrebbe descrivere le modifiche apportate in modo chiaro. Ogni commit crea una "versione" del progetto e memorizza tutte le modifiche apportate fino a quel momento.

### 4. **Le Quattro Interazioni Fondamentali con Git**

Per gestire e mantenere il tuo progetto nel tempo, ci sono quattro operazioni principali che devi conoscere:

   **a) Commit**

   Quando lavori su un progetto e apporti modifiche al codice, devi salvare tali modifiche in una nuova "versione" tramite il commit.

   1. Per aggiungere i file che hai modificato, usa:

      ```bash
      git add .
      ```

   2. Poi, per registrare il commit, usa:

      ```bash
      git commit -m "Descrizione delle modifiche"
      ```

   **b) Log**

   Per vedere una cronologia dei commit effettuati, puoi usare il comando:

      ```bash
      git log
      ```

   Questo comando elenca tutti i commit precedenti, con dettagli come il nome dell'autore, la data, e il messaggio di commit. È utile per tenere traccia di chi ha fatto quali modifiche e quando.

   **c) Checkout**

   Se hai bisogno di tornare a una versione precedente del progetto, puoi usare il comando `checkout` per spostarti su un commit specifico. Per fare ciò, prendi nota dell'ID del commit (mostrato con `git log`) e usa:

      ```bash
      git checkout id-del-commit
      ```

   Attenzione: questa operazione rende il progetto in modalità “detached HEAD,” il che significa che non sei su un branch attivo.

   **d) Branching**

   Il branching ti permette di lavorare su nuove funzionalità o correggere bug senza interferire con il codice principale. I branch sono essenziali per lo sviluppo parallelo e facilitano l’integrazione delle modifiche solo quando sono pronte.

   1. Per creare un nuovo branch, usa:

      ```bash
      git checkout -b nome-del-branch
      ```

   2. Dopo aver finito il lavoro su un branch, puoi unire le modifiche con il branch principale (tipicamente chiamato `main`) usando:

      ```bash
      git checkout main
      git merge nome-del-branch
      ```

   Questo comando integra le modifiche fatte sul branch secondario nel branch principale.

### 5. **Risoluzione dei Conflitti**

Quando lavori con più branch o torni a versioni precedenti, può capitare di incontrare dei conflitti, cioè modifiche incompatibili tra file che devono essere risolte manualmente.

1. Per gestire i conflitti, Git evidenzierà le sezioni in conflitto nei file interessati.
2. Apri i file e cerca i segnaposto `<<<<<<<`, `=======`, e `>>>>>>>` per capire le differenze.
3. Modifica il file per risolvere il conflitto, quindi usa `git add` per aggiungere il file risolto e `git commit` per salvare le modifiche.

### 6. **Stash: Salvare le Modifiche Temporanee**

Se hai modifiche non committate ma hai bisogno di passare rapidamente a un altro branch, puoi usare `git stash` per salvarle temporaneamente.

1. Per salvare le modifiche temporanee, usa:

   ```bash
   git stash
   ```

2. Quando sei pronto per riprendere il lavoro, puoi recuperare le modifiche salvate con:

   ```bash
   git stash pop
   ```

Il comando `stash` è utile per evitare di fare commit incompleti quando devi interrompere il lavoro.

### 7. **Ripristino di Modifiche con `git reset` e `git revert`**

Ci sono vari modi per annullare le modifiche in Git, a seconda di come e dove sono state apportate:

- **git reset**: Cancella le modifiche nella cronologia del commit locale. Ad esempio, per annullare l’ultimo commit:

   ```bash
   git reset --soft HEAD~1
   ```

- **git revert**: Se desideri annullare un commit già condiviso senza alterare la cronologia, usa `git revert`. Creerà un nuovo commit che annulla le modifiche di un commit precedente.

   ```bash
   git revert id-del-commit
   ```

Queste operazioni ti permettono di gestire il progetto in modo efficace e mantenere una cronologia pulita.

### 8. **Conclusioni**

Git è uno strumento potente per la gestione del codice, e usarlo a livello locale ti permette di creare versioni, tracciare modifiche, risolvere conflitti e lavorare in parallelo tramite branch.

## Capitolo 2 - Come utilizzare GitHub

#### **Creazione del Profilo GitHub**

Il primo passo per cominciare a usare **GitHub** è creare un account. **GitHub** è una piattaforma online che consente di ospitare i tuoi progetti software, gestire il codice e collaborare con altri sviluppatori. Per creare un account, vai su **_https://github.com_** e registrati. Ti verrà chiesto di scegliere un nome utente, inserire la tua email e impostare una password sicura.

Una volta creato l'account, ti verrà inviata un'email di conferma. Dopo averla verificata, avrai accesso completo alla piattaforma e potrai iniziare a creare i tuoi _repository_. Il profilo **GitHub** è essenzialmente il tuo spazio di lavoro e visibilità nel mondo della programmazione open source. Potrai condividerlo con i tuoi colleghi, potenziali datori di lavoro, o contribuire a progetti open source.


#### 2. **Creazione di un Nuovo Repository**

Il passo successivo consiste nella creazione di un _repository_. Un _repository_ è il contenitore principale dove viene conservato il codice di un progetto. Quando inizi a lavorare su un nuovo progetto, dovrai creare un _repository_ per organizzare il codice, le risorse, e tutte le versioni del progetto.

Per farlo, accedi al tuo account **GitHub** e vai alla tua homepage. Clicca sul pulsante verde “_New_” per creare un nuovo repository. **GitHub** ti chiederà di assegnargli un nome e di scegliere altre opzioni come la visibilità (pubblico o privato). Puoi anche inizializzare il _repository_ con un file **README**, che è utile per documentare il progetto.

Una volta creato, avrai accesso al _repository_ dove potrai caricare il tuo codice, aggiungere altre risorse o documentazione e gestire le versioni del progetto.


#### 3. **Clonazione del Repository sul Tuo Computer**

Una volta che hai creato il tuo _repository_, il passo successivo è “clonarlo” sul tuo computer. La **clonazione** ti permette di avere una copia locale del repository in modo da poter lavorare su di esso offline e poi sincronizzare le modifiche con il repository su **GitHub**.

Per clonare un _repository_, vai sulla pagina del repository **GitHub** e copia l'URL HTTPS o SSH. Apri il terminale sul tuo computer e usa il comando **_`git clone`_** seguito dall'URL del _repository_:

    git clone https://github.com/tuo-username/tuo-repository.git

**Questo comando crea una copia locale del _repository_**. A questo punto, puoi iniziare a lavorare sul codice direttamente sul tuo computer.


#### 4. **Le Quattro Interazioni Fondamentali con Git**

Una delle funzionalità principali di **GitHub** è l’integrazione con **Git**, il sistema di controllo versione che gestisce le modifiche al codice. Per usare **GitHub** in modo efficace, devi conoscere le principali operazioni di interazione con **Git**. Ecco le quattro operazioni principali che ogni sviluppatore dovrebbe sapere:

a) **Commit**

Quando lavori su un progetto, ogni volta che apporti modifiche al codice, queste modifiche devono essere salvate in una "versione" per tenere traccia del lavoro. Questo processo è chiamato **_commit_**. Un _commit_ registra un'istantanea del tuo codice, includendo tutte le modifiche fatte.

Per fare un _commit_, prima esegui il comando:

    git add .

Questo comando prepara tutte le modifiche fatte per essere aggiunte al commit. Dopodiché, per registrare il commit, usa:

    git commit -m "Messaggio del commit"

Il messaggio del commit deve essere chiaro e descrivere brevemente cosa è stato cambiato.

b) **Push**

Dopo aver effettuato un commit, il passo successivo è quello di inviare le modifiche al _repository_ remoto su **GitHub**. Questo si fa tramite il comando **_push_**:

    git push origin main

Questo comando invia le modifiche locali al repository su **GitHub**, aggiornando la versione remota con il tuo lavoro. La parola “main” si riferisce al ramo principale del progetto. Se stai lavorando su un ramo diverso, sostituirai "main" con il nome del ramo su cui stai lavorando.

c) **Pull**

Nel lavoro collaborativo, è essenziale aggiornare il proprio repository locale con le modifiche fatte da altri. Per fare ciò, usi il comando pull:

    git pull origin main

Il comando **_pull_** scarica le modifiche più recenti dal _repository_ remoto e le integra nel tuo progetto locale. Questo ti assicura di avere sempre l'ultima versione del codice prima di iniziare a lavorare.

d) **Branching**

Un altro concetto fondamentale di Git è la gestione dei **_branch_**, ovvero i rami del progetto. I _branch_ ti permettono di lavorare su nuove funzionalità o correzioni di bug senza compromettere il codice principale. Creando un nuovo _branch_, puoi sviluppare la tua parte del codice in isolamento.

Per creare un nuovo _branch_, usa:

    git checkout -b nome-del-branch

Una volta completato il lavoro sul _branch_, puoi fare un _commit_ e successivamente una **_pull request_** su **GitHub** per proporre l'integrazione delle modifiche nel ramo principale (main).



## Capitolo 3 - Come utilizzare Git e GitHub insieme

### 1. **Creazione di un Nuovo Repository su GitHub**

Ora che hai configurato Git, è il momento di creare un repository (o "repo") su GitHub per ospitare il tuo progetto.

1. Accedi a GitHub e vai alla tua homepage.
2. Clicca sul pulsante verde “New” per creare un nuovo repository.
3. Dai un nome al repository (ad esempio, “progetto-prova”) e scegli se renderlo pubblico o privato.
4. Seleziona l'opzione per aggiungere un file README (questo è un file di descrizione del progetto).
5. Clicca su “Create repository” per finalizzare.

A questo punto, GitHub crea il repository e ti mostra la sua pagina. Tieni aperta questa pagina perché contiene l'URL del repository, che useremo nel prossimo passaggio.

### 2. **Clonazione del Repository su GitHub al Computer**

Ora è il momento di copiare il repository di GitHub sul tuo computer, così puoi lavorare sui file in locale.

1. Sulla pagina del repository GitHub, copia l’URL HTTPS del repository (lo trovi cliccando su “Code” e selezionando “HTTPS”).
2. Apri il terminale sul tuo computer e vai nella cartella dove vuoi salvare il progetto.
3. Usa il comando `git clone` seguito dall'URL che hai copiato:

   ```bash
   git clone https://github.com/tuo-username/progetto-prova.git
   ```

Questo comando crea una copia completa del repository GitHub sul tuo computer.

### 3. **Aggiungere Modifiche e Fare il Commit**

Ora puoi lavorare sul tuo progetto. Aggiungi o modifica file all’interno della cartella del progetto sul tuo computer.

Quando hai fatto modifiche che vuoi salvare, segui questi passaggi per preparare e registrare le modifiche:

1. **Aggiungere le modifiche**: Dì a Git di preparare le modifiche per il commit usando `git add`. Per aggiungere tutti i file modificati:

   ```bash
   git add .
   ```

2. **Fare il commit**: Dopo aver aggiunto i file, salva le modifiche nel repository con un commit. Un commit è una versione salvata del tuo lavoro:

   ```bash
   git commit -m "Descrizione delle modifiche"
   ```

Il messaggio tra virgolette deve descrivere le modifiche che hai fatto, come “Aggiunto file di benvenuto.”

### 4. **Inviare le Modifiche a GitHub (Push)**

Ora che hai salvato le modifiche in locale, è il momento di inviarle al repository su GitHub.

1. Usa il comando `git push` per inviare le modifiche al repository remoto:

   ```bash
   git push origin main
   ```

   Se il branch principale si chiama “main,” usa “main” nel comando. Altrimenti, sostituiscilo con il nome del branch su cui stai lavorando.

Ora le tue modifiche sono visibili anche su GitHub!

### 5. **Scaricare le Modifiche da GitHub (Pull)**

Se lavori su un progetto collaborativo, potrebbe esserci bisogno di scaricare le modifiche fatte da altri. Usa il comando `git pull` per aggiornare il tuo repository locale:

```bash
git pull origin main
```

Questo comando scarica tutte le modifiche recenti dal repository GitHub e le integra con il tuo progetto locale.

### 6. **Branching e Pull Request**

GitHub ti permette di lavorare su nuove funzionalità senza interferire con il codice principale utilizzando i branch. Per esempio, se vuoi aggiungere una funzionalità senza modificare direttamente il branch principale, puoi:

1. Creare un nuovo branch:

   ```bash
   git checkout -b nome-del-branch
   ```

2. Lavorare sul branch creato, aggiungere modifiche e fare commit.

3. Dopo aver completato il lavoro, puoi inviare le modifiche a GitHub con `git push`:

   ```bash
   git push origin nome-del-branch
   ```

4. Vai su GitHub e crea una pull request per unire le modifiche del branch secondario nel branch principale (`main`). La pull request richiede l’approvazione dei collaboratori o può essere un’autovalutazione prima di fondere i cambiamenti.

### 7. **Ricapitolazione dei Comandi**

Ecco un riepilogo dei comandi principali che userai con Git e GitHub:

- **git clone [URL]**: Clona un repository GitHub sul tuo computer.
- **git add .**: Aggiunge tutti i file modificati per il prossimo commit.
- **git commit -m "Messaggio"**: Salva le modifiche locali con un messaggio descrittivo.
- **git push origin main**: Invia le modifiche al repository GitHub.
- **git pull origin main**: Scarica e integra le modifiche dal repository GitHub.
- **git checkout -b nome-del-branch**: Crea un nuovo branch e si sposta su di esso.
- **git merge nome-del-branch**: Unisce un branch al branch corrente.

Ora hai tutto il necessario per iniziare a utilizzare Git e GitHub insieme!

Ricorda facendo un progetto di gruppo alcune interazioni potrebbero essere limitate e dovrai far approvare eventuali pull request da altri membri del gruppo con il ruolo adatto.

by **_Andrea Militano_**, **_Alessandra Lo Coco_**, **_Daniele Ruoppolo_**