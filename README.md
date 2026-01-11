![Static Badge](https://img.shields.io/badge/status-active-brightgreen?style=flat)  ![Static Badge](https://img.shields.io/badge/python-v.3-brightgreen?style=flat&logo=python&logoColor=f5f5f5)

# 🎒 Classe 5CLS, anno scolastico 2025-2026

Questo repo è un fork di [marimo WebAssembly + GitHub Pages Template](https://github.com/marimo-team/marimo-gh-pages-template), personalizzato per ospitare su GitHub i notebook e le app create con [marimo](https://marimo.io).
Fai riferimento a questo repo se vuoi maggiori informazioni.

## 🚀 Utilizzo

1. Aggiungi i file marimo alle cartelle `notebooks/` o `apps/`
   1. I notebook in `notebooks/` vengono esportati con `--mode edit`
   2. I notebook in `apps/` vengono esportati con `--mode run`
2. Esegui il push al branch main
3. Vai a **Settings > Pages** del repo e dal menu a tendina "Source" scegli "GitHub Actions"
4. GitHub Actions eseguirà automaticamente il build e il deploy su GitHub Pages


## Includere dati o altri assets

Per includere dati nei tuoi notebooks, aggiungili alla cartella `public/`.

Per esempio, se il notebook `apps/charts.py` carica un'immagine dalla cartella  `public/` nel notebook uso:

```markdown
<img src="public/logo.png" width="200" />
```

Se il notebook `notebooks/penguins.py` carica una dataset in formato CSV dalla cartela `public/` nel notebook uso:

```python
import polars as pl
df = pl.read_csv(mo.notebook_location() / "public" / "penguins.csv")
```



## 🎨 Template

La versione originale del repo include diversi template. L'unico che è stato personalizzato è  `tailwind.html.j2`.

Puoi creare altri template. Per maggiori informazioni consulta [templates/README.md](templates/README.md).
