![Static Badge](https://img.shields.io/badge/status-active-green?style=flat)  ![Static Badge](https://img.shields.io/badge/python-v.3-brightgreen?style=flat&logo=python&logoColor=f5f5f5)

&nbsp;

# 🎒 Classe 5CLS | anno scolastico 2025-2026

Questo repo è un fork di [marimo WebAssembly + GitHub Pages Template](https://github.com/marimo-team/marimo-gh-pages-template), personalizzato per ospitare su GitHub i notebook e le app create con [marimo](https://marimo.io).
Fai riferimento a questo repo se vuoi maggiori informazioni.

&nbsp;

## 📒 Notebooks e apps contenuti

Notebooks:
1. **Gaussiana Pt1** &nbsp; [![Open in molab](https://marimo.io/molab-shield.svg)](https://molab.marimo.io/github/stefanocaglio/AS2526_5CLS/blob/270d558277d4378f06f27fee84911d192163bffb/notebooks/gaussiana_pt1.py)
<br>Obiettivi: 
   1. ripasso della creazione di un grafico a partire dalle liste di ascisse e ordinate (senza usare altre librerie come `numpy` per esempio)
   2. creazione del grafico interattivo della funzione $y= A e^{-B{(x-C)}^2}$ per ragionare su come i parametri $A$, $B$ e $C$ influenzano il grafico 

N.B.: link per la creazione del [badge marimo](https://molab.marimo.io/github)
&nbsp;

## 🚀 Utilizzo

1. Aggiungi i file marimo alle cartelle `notebooks/` o `apps/`
   1. I notebook in `notebooks/` vengono esportati con `--mode edit`
   2. I notebook in `apps/` vengono esportati con `--mode run`
2. Esegui il push al branch main
3. Vai a **Settings > Pages** del repo e dal menu a tendina "Source" scegli "GitHub Actions"
4. GitHub Actions eseguirà automaticamente il build e il deploy su GitHub Pages

&nbsp;

## 📥 Includere dati o altri assets

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

&nbsp;

## 🎨 Template

La versione originale del repo include diversi template. L'unico che è stato personalizzato è  `tailwind.html.j2`.

In questo template sono utilizzati:
- **il framework CSS [Tailwind](https://tailwindcss.com/)**
- **il motore di templating [Jinja2](https://jinja.palletsprojects.com/en/stable/)**: è stata personalizzata la capacità di elencare notebooks e apps in ordine alfabetico tramite `sort`. 

Puoi creare altri template. Per maggiori informazioni consulta [templates/README.md](templates/README.md).
