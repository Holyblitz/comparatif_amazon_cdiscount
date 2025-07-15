# comparatif_amazon_cdiscount

Ce projet explore les différences de notation et de popularité entre :

    des produits électroniques vendus sur Amazon (dataset Kaggle),

    et des produits tech en France via Cdiscount (scraping maison).

L’objectif est de :
Construire une base PostgreSQL propre (plus de 1 million de lignes côté Amazon, ~30k côté Cdiscount),
Calculer des agrégats pertinents (moyennes de notes, distribution des reviews, évolution dans le temps),
Visualiser ces résultats via des dashboards Python (Matplotlib + Pandas).
⚙️ Pipeline du projet

    Scraping & nettoyage

        Amazon : dataset Kaggle déjà nettoyé.

        Cdiscount : scraping semi-automatique avec Selenium + BeautifulSoup, nettoyage des notes 4,5/5 ➔ 4.5.

    Stockage

        Base PostgreSQL structurée avec 2 tables principales (amazon_reviews et cdiscount).

    Requêtes SQL

        Calcul des moyennes par catégorie.

        Évolution des scores Amazon par année.

        Top 10 produits les mieux notés.

    Visualisation

        Graphiques Matplotlib sauvegardés localement pour communication LinkedIn + GitHub.

Pour lancer le projet

# Installer les dépendances Python
pip install pandas matplotlib psycopg2-binary sqlalchemy selenium beautifulsoup4

# Exécuter les scripts d'import + nettoyage
python import_amazon.py
python import_cdiscount.py

# Exécuter les dashboards
python dashboard_amazon_cdiscount.py

Ce que j’ai appris

    Nettoyage avancé de données hétérogènes (CSV > PostgreSQL).

    Manipulation et agrégation SQL (avg, count, cast, replace…).

    Création de dashboards clairs et impactants avec Matplotlib.

    Automatisation du scraping dynamique via Selenium.

Prêt à explorer d'autres projets (IA, NLP, nettoyage de boîtes mail…) pour renforcer le portfolio et proposer plus de valeur aux entreprises.
