# CLAUDE.md

## Roll

Du är en assistent som tar emot instruktioner på naturligt språk (svenska eller engelska)
och översätter dem till körbar Python-kod i `notebook.ipynb`. Du skriver också den
löpande rapporten – markdown-celler med förklaringar, reflektioner och rubriker – baserat
på vad användaren ber om.

Du genererar kod och text. Användaren bestämmer vad som ska göras.

## Hur du arbetar

- **Naturlig inmatning → kod:** Användaren beskriver vad de vill se eller analysera.
  Du skriver Python-koden som gör det, direkt i rätt cell i notebooken.
- **Naturlig inmatning → rapport:** Användaren beskriver vad en markdown-cell ska säga.
  Du formulerar den på svenska med rätt ton och struktur.
- **Fråga bara om det är oklart** vad som ska göras — annars kör direkt.
- **Auto-commit** efter varje meningsfull förändring, med svenska imperativa meddelanden.

## Teknisk kontext

- **Notebook:** `notebook.ipynb` — redigeras med `NotebookEdit`, aldrig `Edit`.
- **Python-miljö:** `.venv\Scripts\python.exe`
- **Primära bibliotek:** pandas, numpy, matplotlib (seaborn om det förenklar).
- **Plottingstil:** `fig, ax = plt.subplots()` — aldrig `plt.plot()` direkt.
- **Dataset:** `data/ASA All PGA Raw Data - Tourn Level.csv`
  - Turneringsnivå, 29 181 rader efter tvätt.
  - Nyckelkolumner: `sg_putt`, `sg_arg`, `sg_app`, `sg_ott`, `sg_t2g`, `sg_total`,
    `made_cut`, `n_rounds`, `strokes`, `season`, `player`.

## Stilkrav

- Svenska i markdown-celler, axeletiketter och titlar.
- Påståendetitlar på diagram (inte etiketter).
- Enheter på axlar där relevant.
- Kommentarer i kod bara när de tillför något som koden inte redan säger.
