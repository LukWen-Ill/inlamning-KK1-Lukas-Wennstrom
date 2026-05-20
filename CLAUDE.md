# CLAUDE.md

Detta repo är inlämningen för **KK1** i kursen *Artificiell Intelligens – programmering
Python* (MAI25MA).

## Uppdrag

Bygg en Jupyter-notebook som analyserar `data/dog_breeds.csv` (~116 hundraser) och
uppfyller KK1-kraven för **Godkänt (G)**. Inte VG.

Full kravspec (auktoritativ vid tveksamhet):
`C:\Users\lukas\projects\school_repos\ai-python-mai25ma\kunskapskontroll\KK1\README.md`

## Dataset

- **Källa:** `data/dog_breeds.csv` (ursprung: Kaggle — exakt URL fylls i före inlämning)
- **Storlek:** ~116 rader, 8 kolumner
- **En rad =** en hundras
- **Kolumner:** Breed, Country of Origin, Fur Color, Height (in), Color of Eyes,
  Longevity (yrs), Character Traits, Common Health Problems
- **Viktigt:** `Height (in)` och `Longevity (yrs)` är lagrade som strängranges
  (`"21-24"`, `"10-12"`) — måste parsas till numeriska kolumner innan plottning.

## Mål

- Godkänt KK1, inget mer.
- Notebook kör utan fel.
- 3 visualiseringar med matplotlib.
- Inkrementell git-historik (commits löpande genom arbetet, inte en enda final commit).
- Inlämning: publikt GitHub-repo + mejl till kursledaren senast onsdag 20 maj 2026, 09:00.

## Notebook-struktur

1. **Inledning** — kontext om datasetet
2. **Inläsning och inspektion** — `.shape`, `.info()`, `.describe()`
3. **Datatvätt** — parsa range-strängar, hantera NaN, motivera val
4. **Visualiseringar** (3 st med matplotlib Figure/Axes):
   - Stapel: top 10 ursprungsländer efter antal raser
   - Histogram: fördelning av median-livslängd
   - Scatter: höjd vs livslängd
5. **Avslutning** — reflektion över mönster och datans gränser

## Repo-struktur

```
notebook.ipynb
data/dog_breeds.csv
README.md
CLAUDE.md
```

## Stilkrav

- Svenska i markdown-celler, axeletiketter och titlar.
- Kommentarer i kod på svenska där de behövs.
- matplotlib primärt. Seaborn endast om det förenklar.
- Figure/Axes-modellen (`fig, ax = plt.subplots()`), inte `plt.plot()` direkt.

## Vad detta INTE är

- Ingen VG-ambition (inga titlar-som-påståenden, ingen diagramval-reflektion,
  ingen Tufte-tillämpning).
- Ingen ML, ingen prediktion, ingen interaktivitet.
- Inga "imponerande" tillägg som inte tjänar analysen.

## Arbetsregler för Claude

- Följ KK1-readme när tveksamhet uppstår om kraven.
- Föreslå inte VG-tillägg om jag inte ber om det.
- Bare minimum är målet. Tid är knapp (deadline 20 maj 09:00).
- En sektion i taget. Vänta på godkännande innan nästa.
- Användaren gör alla git-commits själv.
