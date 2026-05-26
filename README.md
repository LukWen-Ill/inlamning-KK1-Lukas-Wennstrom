# KK1 – PGA Tour-spelarstatistik

Inlämning för **KK1** i kursen *Artificiell Intelligens – programmering Python* (MAI25MA).

## Dataset

`data/pga_tour.csv` – PGA Tour-spelarsäsonger 2015–2022. En rad per spelare och säsong,
med numeriska statistik som drive-längd, drive-precision, greens in regulation, putting
och scoring average, samt prestationsindikatorer (vinster, topp-10, prispengar).

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
python -m nbconvert --to notebook --execute notebook.ipynb
```
