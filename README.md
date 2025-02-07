
# PULLATE SEMPRE COSì RIDUCIAMO AL MINIMO LA POSSIBILITà DI CONFLITTI  

# ProgettoWEB2025

  

**Nome:** Well.io

  

## Gestione dei Sottomoduli

  

Quello che vedete dopo il nome `backend` o `frontend` corrisponde al commit al quale è collegato il sottomodulo. Purtroppo, non c'è la possibilità di collegarsi direttamente a un sottomodulo specifico (come il `main`). L'unica cosa che possiamo fare è, man mano che aggiorniamo il `main` di ogni sottomodulo, eseguire i seguenti comandi per allineare la repository principale con gli ultimi commit.

  

### Clonazione della Repository Principale con Sottomoduli

  

Si dà per scontato che sia già stato eseguito il clone della repository principale con entrambi i sottomoduli tramite il comando:

```bash

git  clone  --recurse-submodules  https://github.com/GhadPRG/ProgettoWEB2025.git

```

### E' IMPORTANTE AVERE I BRANCH MAIN DEI SOTTOMODULI AGGIORNATI ALL'ULTIMO COMMIT PER EVITARE DI AVERE PROBLEMI DI CONFLITTI

### Quando fate il clone della repo principale con i sottomoduli, bisogna spostarsi nella directory del sottomodulo in cui lavorare e fare il checkout sul branch su cui si vuole lavorare. 
### Vi capiterà di trovarvi su intellij nella sezione di git un simbolo giallo di avviso con il codice di un commit, vi sta avvertendo che non siete su un branch principale come il main, i branch dev o i nostri personali, bensì siamo in un branch di uno specifico commit. E questo non va bene, quindi occorre fare il checkout su uno dei branch interessati.
![image](https://github.com/user-attachments/assets/2afed61b-9eb2-4f0b-9538-38ad9548ad6c)


#### (Questa operazione capiterà di farla sicuramente la prima volta in cui si apre il progetto su intellij dopo aver fatto il clone della repo principale e dopo esservi spostati su uno dei due sottomoduli)
### Se usate la riga di comando per eseguire i commit push e cazzi vari, quando farete un `git status` vi ritroverete sicuramente un avviso di questo tipo:
```bash
HEAD detached from 6f25e09
```
### Indica che il puntatore `HEAD` (che normalmente punta a un branch, come `main` o `develop`) non è collegato a un branch specifico, ma punta direttamente a un commit specifico. In questo caso occorre semplicemente usare il comando `git checkout nomebranch` e lavorare normalmente

Una volta fatti i commit su uno dei sottomoduli, se dovete seguire la guida per aggiornarli e allinearli agli ultimi commit sulla repo principale, ricordatevi di spostarvi nella directory della repo principale.

### Aggiornamento dei Sottomoduli

Dopo aver eseguito il clone, andare nella directory della repository principale e,

dopo aver effettuato i commit sul `main` di uno dei due sottomoduli,

eseguire i seguenti comandi:



```bash

git  submodule  update  --remote  --merge

git  add  .

git  commit  -m  "Commento"

git  push

```

  

### Spiegazione dei Comandi

1.**`git submodule update --remote --merge`**: Aggiorna i sottomoduli ai loro ultimi commit remoti e li unisce con il branch corrente.

2.**`git add .`**: Aggiunge tutte le modifiche allo staging area.

3.**`git commit -m "Commento"`**: Crea un nuovo commit con un messaggio descrittivo.

4.**`git push`**: Carica i commit locali sulla repository remota.
