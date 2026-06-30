# IL PONTE — Sito web (LEGGIMI)

Sito statico (un solo `index.html`). Niente build, niente npm. Vercel lo serve così com'è.

## Struttura
```
ilponte/
├── index.html          ← tutto il sito (HTML + CSS + JS in un file)
├── menu-del-dia.pdf     ← il PDF del menù del giorno (DA AGGIORNARE)
├── favicon.webp
├── vercel.json
├── .gitignore
└── img/                 ← tutte le foto (.webp)
    ├── hero.webp
    ├── logo.webp
    └── ... (le altre)
```

## Come metterlo online la prima volta

1. Sposta questa cartella in `~/Desktop/PROGETTI/ilponte`
2. Aprila in VS Code
3. Per vederla in locale: tasto destro su `index.html` → "Open with Live Server"
   (oppure dal terminale del Mac, dentro la cartella: `python3 -m http.server 8000` e apri http://localhost:8000)
4. Crea il repo su GitHub e collegalo a Vercel come fai di solito
5. Dal **terminale del Mac**:
   ```
   cd ~/Desktop/PROGETTI/ilponte && git init && git add . && git commit -m "Sito IL PONTE - prima versione" && git branch -M main && git remote add origin URL_DEL_TUO_REPO && git push -u origin main
   ```
6. Su Vercel: New Project → importa il repo → Deploy
   (Framework Preset: **Other**. Nessun build command. Output: la root.)

## Aggiornamenti successivi (modifiche col tuo flusso)
Dopo aver modificato i file (anche con Claude Code):
```
cd ~/Desktop/PROGETTI/ilponte && git add . && git commit -m "descrizione modifica" && git push
```
Vercel deploya da solo in ~1 minuto.

## ⭐ Il MENÙ DEL GIORNO (la parte importante)
Per cambiare il menù del giorno che si vede nel sito:
1. Sostituisci il file `menu-del-dia.pdf` nella cartella (stesso nome esatto!)
2. ```
   cd ~/Desktop/PROGETTI/ilponte && git add . && git commit -m "menu del dia" && git push
   ```
3. Dopo ~1 minuto il nuovo PDF è online.

Più avanti, se vuoi, si può fare in modo che lo carichino loro senza toccare il codice.

## Note
- **3 lingue** (ES/IT/EN): le bandiere in alto cambiano tutto il sito. Testo in `index.html` dentro l'oggetto `I18N`.
- **Telefono**: +34 689 34 41 63 (cercalo nel file per cambiarlo, è scritto come `+34689344163` nei link e `+34 689 34 41 63` a video).
- **Foto**: per cambiarne una, metti il nuovo `.webp` in `img/` con lo stesso nome, oppure cambia il percorso nell'oggetto `IMG` dentro `index.html`.
- **Dominio**: quando lo collegate, ricordati di NON dover toccare niente nel codice (è già relativo).

## DA FARE DOPO IL SITO (promemoria)
Sistemare la scheda Google del locale: più recensioni, foto, link al sito.
Vale quanto il sito stesso per farli trovare.
