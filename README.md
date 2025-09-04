# Analyse de mes parties d'échecs (Chess.com)

Notebook d'analyse de **mes parties personnelles** : répartition des ouvertures, winrate (Blanc/Noir), efficacité par ouverture, et évolution Elo par cadence.

🔗 Notebook Kaggle : [https://www.kaggle.com/code/thomasroux74/chess-analysis]  
📊 Figures clés : voir le dossier `images/`.

## Données
- Export Chess.com (PGN) → parsing & enrichissement (ECO / familles d'ouvertures).
- Fichier utilisé : `my_chess_games_and_openings.csv` (non inclus ici pour taille ; dispo sur Kaggle).
- Période : 2020–2025, cadences Bullet/Blitz/Rapide.

## Principaux résultats (TL;DR)
- **Winrate global** : X% (Blanc Y%, Noir Z%).
- **Ouvertures phares** : A, B, C (winrate respectif…).
- **Elo** : +N points en M mois (pics, creux).

## Méthode
1. Export via API Chess.com (PGN mensuels).
2. Parsing `python-chess` → CSV enrichi (ECO, familles).
3. Analyses avec `pandas` + visualisations `matplotlib`.

## Limites
- ECO parfois manquant → regroupements par familles.
- Pas d’évaluation moteur (qualité des coups non mesurée).
- Données personnelles → biais de sélection (cadences jouées).

## Reproduire
```bash
pip install -r requirements.txt
# ouvrir notebook.ipynb
