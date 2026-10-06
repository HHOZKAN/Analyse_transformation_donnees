# Analyse_transformation_donnees

Analyse des comptages routiers permanents de Paris

Analyse exploratoire du trafic sur trois axes parisiens, à partir des données ouvertes de la Ville de Paris (comptages routiers permanents, mesures horaires).

Axes étudiés
Bd_Vincent_Auriol
Av_de_l'Opera
St_Jacques

Période : du 1er mars 2026 au 1er septembre 2026 (exclu).

Structure du projet
Analyse_transformation_donnees/
├── data/
│   └── raw/
│       └── comptages.csv      # généré par download_data.py (ignoré par Git)
├── download_data.py           # téléchargement des 3 axes sur la période
├── analyse.ipynb              # chargement, exploration et graphiques
└── README.md

Graphiques produits
Distribution du débit horaire 
Profil horaire moyen 
Répartition de l'état du trafic