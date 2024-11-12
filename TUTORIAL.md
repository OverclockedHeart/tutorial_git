Benvenuto in questo tutorial!

In questo tutorial ti isegneremo ad usare GIT e GitHub per un progetto in solitario o in team

cap1. Come usare GIT




cap2. Come usare GitHub

### 1. **Creazione del Profilo GitHub**

Il primo passo per cominciare a usare GitHub è creare un account. GitHub è una piattaforma online che consente di ospitare i tuoi progetti software, gestire il codice e collaborare con altri sviluppatori. Per creare un account, vai su https://github.com e registrati. Ti verrà chiesto di scegliere un nome utente, inserire la tua email e impostare una password sicura.

Una volta creato l'account, ti verrà inviata un'email di conferma. Dopo averla verificata, avrai accesso completo alla piattaforma e potrai iniziare a creare i tuoi repository. Il profilo GitHub è essenzialmente il tuo spazio di lavoro e visibilità nel mondo della programmazione open source. Potrai condividerlo con i tuoi colleghi, potenziali datori di lavoro, o contribuire a progetti open source.


### 2. **Creazione di un Nuovo Repository**

Il passo successivo consiste nella creazione di un repository. Un repository è il contenitore principale dove viene conservato il codice di un progetto. Quando inizi a lavorare su un nuovo progetto, dovrai creare un repository per organizzare il codice, le risorse, e tutte le versioni del progetto.

Per farlo, accedi al tuo account GitHub e vai alla tua homepage. Clicca sul pulsante verde “New” per creare un nuovo repository. GitHub ti chiederà di assegnargli un nome e di scegliere altre opzioni come la visibilità (pubblico o privato). Puoi anche inizializzare il repository con un file README, che è utile per documentare il progetto.

Una volta creato, avrai accesso al repository dove potrai caricare il tuo codice, aggiungere altre risorse o documentazione e gestire le versioni del progetto.


### 3. **Clonazione del Repository sul Tuo Computer**

Una volta che hai creato il tuo repository, il passo successivo è “clonarlo” sul tuo computer. La clonazione ti permette di avere una copia locale del repository in modo da poter lavorare su di esso offline e poi sincronizzare le modifiche con il repository su GitHub.

Per clonare un repository, vai sulla pagina del repository GitHub e copia l'URL HTTPS o SSH. Apri il terminale sul tuo computer e usa il comando `git clone` seguito dall'URL del repository:

    git clone https://github.com/tuo-username/tuo-repository.git

Questo comando crea una copia locale del repository. A questo punto, puoi iniziare a lavorare sul codice direttamente sul tuo computer.


### 4. **Le Quattro Interazioni Fondamentali con Git**

Una delle funzionalità principali di GitHub è l’integrazione con Git, il sistema di controllo versione che gestisce le modifiche al codice. Per usare GitHub in modo efficace, devi conoscere le principali operazioni di interazione con Git. Ecco le quattro operazioni principali che ogni sviluppatore dovrebbe sapere:

    a) Commit

    Quando lavori su un progetto, ogni volta che apporti modifiche al codice, queste modifiche devono essere salvate in una "versione" per tenere traccia del lavoro. Questo processo è chiamato **commit**. Un commit registra un'istantanea del tuo codice, includendo tutte le modifiche fatte.

    Per fare un commit, prima esegui il comando:

        git add .

    Questo comando prepara tutte le modifiche fatte per essere aggiunte al commit. Dopodiché, per registrare il commit, usa:

        git commit -m "Messaggio del commit"

    Il messaggio del commit deve essere chiaro e descrivere brevemente cosa è stato cambiato.

    b) Push

    Dopo aver effettuato un commit, il passo successivo è quello di inviare le modifiche al repository remoto su GitHub. Questo si fa tramite il comando push:

        git push origin main

    Questo comando invia le modifiche locali al repository su GitHub, aggiornando la versione remota con il tuo lavoro. La parola “main” si riferisce al ramo principale del progetto. Se stai lavorando su un ramo diverso, sostituirai "main" con il nome del ramo su cui stai lavorando.

    c) Pull

    Nel lavoro collaborativo, è essenziale aggiornare il proprio repository locale con le modifiche fatte da altri. Per fare ciò, usi il comando pull:

        git pull origin main

    Il comando pull scarica le modifiche più recenti dal repository remoto e le integra nel tuo progetto locale. Questo ti assicura di avere sempre l'ultima versione del codice prima di iniziare a lavorare.

    d) Branching

    Un altro concetto fondamentale di Git è la gestione dei **branch**, ovvero i rami del progetto. I branch ti permettono di lavorare su nuove funzionalità o correzioni di bug senza compromettere il codice principale. Creando un nuovo branch, puoi sviluppare la tua parte del codice in isolamento.

    Per creare un nuovo branch, usa:

        git checkout -b nome-del-branch

    Una volta completato il lavoro sul branch, puoi fare un commit e successivamente una **pull request** su GitHub per proporre l'integrazione delle modifiche nel ramo principale (main)



cap3. Come usarli insieme



by Andrea Militano, Alessandra Lo Coco, Daniele Ruoppolo