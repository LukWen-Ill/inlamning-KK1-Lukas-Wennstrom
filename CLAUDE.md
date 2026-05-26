# CLAUDE.md

Detta repo är inlämningen för **KK1** i kursen *Artificiell Intelligens – programmering
Python* (MAI25MA).

## Uppdrag

Bygg en Jupyter-notebook som analyserar `data/pga_tour.csv` (PGA Tour-spelarsäsonger
2015–2022) och uppfyller KK1-kraven på **mellanting G/VG** — solid G-grund med VG-finish
där det passar naturligt (påståendetitlar, diagramvalsförsök, annoteringar).

Full kravspec (auktoritativ vid tveksamhet):
`C:\Users\lukas\projects\school_repos\ai-python-mai25ma\kunskapskontroll\KK1\README.md`

## Dataset

- **Källa:** Kaggle – https://www.kaggle.com/datasets/robikscube/pga-tour-golf-data-20152022
- **Fil:** `data/pga_tour.csv`
- **Storlek:** ~400–560 rader (8 säsonger × ~50–70 spelare/säsong)
- **En rad =** en spelare en säsong
- **Förväntade kolumner:** drive distance (yards), drive accuracy (%), greens in
  regulation (%), putting average, scoring average, wins, top 10, money/earnings
  (faktiska kolumnnamn bekräftas vid inläsning)
- **Förväntade kvirkar:** money troligen som textsträng (`"$1,234,567"`),
  procent kan vara strängar, NaN för spelare som inte kvalificerat för en stat

## Mål

- KK1 mellanting G/VG.
- Notebook kör utan fel.
- 4–5 visualiseringar med matplotlib (seaborn där det förenklar).
- Tre frågor som tråd genom analysen:
  1. Vad kännetecknar de bästa spelarna?
  2. Hur har spelet förändrats över tid?
  3. Finns det en trade-off mellan drive-längd och precision?
- Inkrementell git-historik (många små commits).
- Inlämning: publikt GitHub-repo + mejl till kursledaren senast onsdag 20 maj 2026, 09:00.

## Notebook-struktur

1. **Inledning** — kontext, källa, en-rad-definition, population, de tre frågorna
2. **Inläsning och inspektion** — `.shape`, `.info()`, `.describe()`, `.head()`
3. **Datatvätt** — money-parsing, procent-parsing, NaN-hantering, motivera val
4. **Visualiseringar** (4–5 st med matplotlib Figure/Axes), varje med formulerad fråga:
   - Topp vs resten: boxplot/histogram-jämförelse av nyckelstats
   - Drive-längd över tid: linjediagram med annoterad trend
   - Distance vs accuracy: scatter med färglagd grupp + kvadrantlinjer
   - Diagramvalsförsök för EN fråga (VG-punkt: synligt prövat)
   - (Optional) Korrelationsranking mot scoring
5. **Avslutning** — reflektion över alla tre frågor + epistemisk gräns

## Repo-struktur

```
notebook.ipynb
data/pga_tour.csv
README.md
CLAUDE.md
```

## Stilkrav

- Svenska i markdown-celler, axeletiketter och titlar.
- Kommentarer i kod på svenska där de behövs.
- matplotlib primärt. Seaborn endast om det förenklar.
- Figure/Axes-modellen (`fig, ax = plt.subplots()`), inte `plt.plot()` direkt.
- Påståendetitlar där det passar (inte forcerat överallt).
- Enheter på axlar (yards, %, USD, scoring).

## VG-punkter som tillämpas (mellanting)

- Påståendetitlar där det passar
- Annoteringar på minst två visualiseringar
- Ett synligt diagramvalsförsök med markdown-reflektion
- Reell reflektion i avslutningen (inte bara "här är grafer")

## Vad detta INTE är

- Ingen ML, ingen prediktion, ingen interaktivitet.
- Inga "imponerande" tillägg som inte tjänar analysen.
- Inte full VG-checklist överallt — bara där det naturligt tillför värde.

## Arbetsregler för Claude

- Följ KK1-readme när tveksamhet uppstår om kraven.
- En sektion i taget. Vänta på godkännande innan nästa sektion.
- **Auto-commit på branch `i3-pga-tour`:** Claude commit:ar löpande efter varje litet
  steg, med svenska imperativa meddelanden. Många små commits, inte stora klumpar.
- Inom en sektion commit:as flera små steg sekventiellt. Mellan sektionerna stannar
  Claude och väntar på godkännande.
- Frågan bestämmer diagramtypen — börja alltid med "vad ska betraktaren kunna jämföra?".
