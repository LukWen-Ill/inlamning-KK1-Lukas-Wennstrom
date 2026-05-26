# KK1 – PGA Tour-spelarstatistik

Inlämning för **KK1** i kursen *Artificiell Intelligens – programmering Python* (MAI25MA).

## Dataset

`data/ASA All PGA Raw Data - Tourn Level.csv` – PGA Tour, turneringsnivå 2015–2022.
En rad per spelare och turnering. Aggregeras i notebooken till spelar-säsong-nivå.

Källa: Kaggle – https://www.kaggle.com/datasets/robikscube/pga-tour-golf-data-20152022

## Kör notebooken

```
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebook.ipynb
```

Verifiera att notebooken kör utan fel från början till slut:

```
.venv\Scripts\python -m nbconvert --to notebook --execute notebook.ipynb
```

## AI-användning

Detta projekt använder **Claude Code** (Anthropic) som kodassistent. Arbetsflödet:

1. Jag formulerar vad jag vill analysera eller visualisera på naturligt språk.
2. Claude översätter instruktionen till Python-kod och skriver den direkt i notebooken.
3. Jag granskar resultatet, justerar vid behov och godkänner varje steg.

Analysfrågorna, tolkningarna och de skriftliga reflektionerna är mina. Claude skriver
koden; jag styr vad koden ska göra och varför.

Hela konversationshistoriken (mina instruktioner + Claudes svar) sparas lokalt i:
`%USERPROFILE%\.claude\projects\C--Users-lukas-projects-school-repos-data-notebook\`

Git-historiken på denna branch visar varje steg i arbetet med commit-meddelanden som
beskriver vad som gjordes.
