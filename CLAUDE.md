# CLAUDE.md

## Roll

Tar emot naturlig-språks-instruktioner och översätter dem till Python-kod i `notebook.ipynb`
eller formulerar markdown-celler. Fråga bara om det är oklart — annars kör direkt.
Auto-commit efter varje meningsfull förändring med svenska imperativa meddelanden.

## Kontext

- **Notebook:** `notebook.ipynb` — redigeras med `NotebookEdit`, aldrig `Edit`.
- **Python:** `.venv\Scripts\python.exe`
- **Bibliotek:** pandas, numpy, matplotlib. Seaborn bara om det förenklar.
- **Plot-modell:** `fig, ax = plt.subplots()` — aldrig `plt.plot()` direkt.
- **Dataset:** `data/ASA All PGA Raw Data - Tourn Level.csv` — turneringsnivå, 29 181 rader.
  Nyckelkolumner: `player`, `season`, `made_cut`, `n_rounds`, `strokes`,
  `sg_putt`, `sg_arg`, `sg_app`, `sg_ott`, `sg_t2g`, `sg_total`.

## Pandas (pandas-pro skill är aktiv)

- Vektoriserat — inga `.iterrows()`-loopar.
- `.copy()` när du modifierar en subset — undviker SettingWithCopyWarning.
- `.loc[]` för indexering — aldrig kedjad (`df['A']['B']`).
- `groupby(..., observed=True)` för kategoriska kolumner (pandas 2.0+).
- Validera efter transformation: `.shape`, `.isna().sum()`, dtypes.

## Spårbarhet

Konversationsloggar (användarens input + Claudes output) sparas automatiskt i:
`%USERPROFILE%\.claude\projects\C--Users-lukas-projects-school-repos-data-notebook\`

## Stil

- Svenska i markdown, axeletiketter och titlar.
- Påståendetitlar på diagram — inte etiketter.
- Enheter på axlar där relevant.
- Kommentarer i kod bara när de tillför något koden inte redan säger.
