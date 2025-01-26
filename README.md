
# ProgettoWEB2025

**Nome:** Well.io

## Gestione dei Sottomoduli

Quello che vedete dopo il nome `backend` o `frontend` corrisponde al commit al quale è collegato il sottomodulo. Purtroppo, non c'è la possibilità di collegarsi direttamente a un sottomodulo specifico (come il `main`). L'unica cosa che possiamo fare è, man mano che aggiorniamo il `main` di ogni sottomodulo, eseguire i seguenti comandi per allineare la repository principale con gli ultimi commit.

### Clonazione della Repository Principale con Sottomoduli

Si dà per scontato che sia già stato eseguito il clone della repository principale con entrambi i sottomoduli tramite il comando:

```bash
git clone --recurse-submodules https://github.com/GhadPRG/ProgettoWEB2025.git
```

### Aggiornamento dei Sottomoduli

Dopo aver eseguito il clone, andare nella directory della repository principale e,
dopo aver effettuato i commit sul  `main`  di uno dei due sottomoduli,
eseguire i seguenti comandi:

```bash
git submodule update --remote --merge
git add .
git commit -m "Commento"
git push
```

### Spiegazione dei Comandi

1.**`git submodule update --remote --merge`**: Aggiorna i sottomoduli ai loro ultimi commit remoti e li unisce con il branch corrente.
2.**`git add .`**: Aggiunge tutte le modifiche allo staging area.
3.**`git commit -m "Commento"`**: Crea un nuovo commit con un messaggio descrittivo.  
4.**`git push`**: Carica i commit locali sulla repository remota.