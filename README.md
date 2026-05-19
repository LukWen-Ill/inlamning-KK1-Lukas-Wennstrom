# KK1 – Analys av hundraser

Inlämning för **KK1** i kursen *Artificiell Intelligens – programmering Python* (MAI25MA).

## Dataset

`data/dog_breeds.csv` – 117 hundraser, en rad per ras, 8 kolumner: ras, ursprungsland,
pälsfärg, höjd, ögonfärg, livslängd, karaktärsdrag och vanliga hälsoproblem.

Källa: Kaggle – https://www.kaggle.com/datasets/marshuu/dog-breeds

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
