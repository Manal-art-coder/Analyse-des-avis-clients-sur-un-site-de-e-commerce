Objectif du Projet
L'objectif de ce projet est de prédire la note d'un client pour une commande sur un site de e-commerce brésilien. En analysant les avis des clients, nous cherchons à identifier les facteurs influençant les notes afin d'optimiser l'expérience client, augmenter les ventes et attirer davantage de vendeurs sur la plateforme.

Objectifs spécifiques :
Prédire la note d'un client pour une commande.
Identifier les principaux facteurs affectant la satisfaction des clients.
Mettre en œuvre des stratégies d'amélioration des produits et services basées sur les données des avis clients.
Étapes du Projet
1. Extraction et Compréhension des Données
Nous avons commencé par extraire les données et les comprendre. Ce processus inclut :

Fusion des bases de données relationnelles à l'aide de requêtes SQL.
Conversion des dates et création de nouvelles colonnes, telles que la durée de livraison réelle et l'écart entre la date de livraison estimée et réelle.
2. Datavisualisation
Nous avons utilisé des visualisations pour comprendre les tendances des données, notamment :

L'évolution du nombre de commandes entre 2017 et 2018.
Les tendances d'achat des Brésiliens (heures de la journée, jours de la semaine).
L'impact des facteurs tels que le prix et les frais de livraison sur les notes des clients.
3. Feature Engineering
Création de variables comme 'number_review_before' et 'review_score_before' pour intégrer les avis précédents d'un produit avant l'achat.
Enrichissement des données avec des informations comme la catégorie de produit en anglais.
4. Modélisation
Sélection des variables pertinentes pour la prédiction (prix, statut de commande, catégorie de produit, durée de livraison,






Vous avez dit :
le style je veux dire, mettre en gras émoticone
ChatGPT a dit :
D'accord ! Voici un README.md amélioré avec du style pour le rendre plus visuellement attrayant pour GitHub. J'ai ajouté des titres en gras, des émoticônes, des listes et des sections pour une meilleure lisibilité et une présentation plus dynamique.

📊 Projet d'Analyse des Avis Clients - Site de E-Commerce
🎯 Objectif du Projet
Le but de ce projet est de prédire la note d'un client pour une commande sur un site de e-commerce brésilien. Les avis clients jouent un rôle clé pour renforcer la confiance des acheteurs et les encourager à finaliser leurs achats. En analysant ces données, nous cherchons à identifier les facteurs qui influencent les notes des clients afin d'optimiser l'expérience utilisateur et de maximiser les ventes.

🎯 Objectifs spécifiques :
Prédire la note d'un client pour une commande.
Identifier les facteurs influençant la satisfaction des clients.
Déterminer des leviers pour améliorer l'expérience d'achat et optimiser les ventes.
🛠️ Étapes du Projet
1️⃣ Extraction et Compréhension des Données
Nous avons commencé par extraire les données et comprendre leur structure :

Fusion des bases de données relationnelles à l'aide de requêtes SQL.
Conversion des dates et création de nouvelles colonnes :
Durée de livraison réelle
Écart entre la date de livraison estimée et réelle
2️⃣ Datavisualisation
Avant de passer à la modélisation, nous avons utilisé des visualisations pour mieux comprendre les données :

📅 Évolution du nombre de commandes de 2017 à 2018.
📊 Analyse des tendances d'achat : heure de la journée, jour de la semaine.
💰 Impact des facteurs (prix, frais de livraison) sur les notes des clients.
3️⃣ Feature Engineering
Nous avons créé de nouvelles variables pour enrichir nos données :

📝 'number_review_before' : Nombre d'avis laissés avant l'achat d'un article.
⭐ 'review_score_before' : Note moyenne d'un article avant l'achat.
🔄 Enrichissement des données avec des informations telles que la catégorie de produit en anglais.
4️⃣ Modélisation
Nous avons ensuite sélectionné les variables pertinentes pour la prédiction et testé plusieurs modèles :

Utilisation du modèle Random Forest pour prédire la note des clients.
🔀 Fusion des classes pour créer une classification binaire afin de mieux gérer le déséquilibre des classes.
Évaluation de la performance du modèle, y compris la gestion du déséquilibre des classes (classe 5 étant majoritaire).
⚙️ Étapes Préparatoires et Préprocessing
1️⃣ Sélection des Variables
Les variables utilisées pour notre modèle sont :

order_status : Statut de la commande.
product_category_name_english : Catégorie de produit en anglais.
price : Prix du produit.
delivery_duration : Durée de livraison réelle.
difference_between_expected_and_real_delivery_date : Écart entre la livraison estimée et réelle.
freight_value : Frais de livraison.
review_score_before : Note moyenne avant achat.
number_review_before : Nombre d'avis avant achat.
hour : Heure de l'achat.
weekday : Jour de la semaine de l'achat.
2️⃣ Préprocessing
Suppression des valeurs manquantes.
Encodage des variables catégorielles.
🎡 Encodage trigonométrique des variables temporelles (heure, jour de la semaine) pour capturer la périodicité.
🧠 Modélisation et Évaluation
1️⃣ Modèle Random Forest
Nous avons utilisé le modèle Random Forest pour prédire les notes des clients. Ce modèle a montré une bonne performance en termes de précision (accuracy).

2️⃣ Fusion des Classes
Afin d'améliorer la performance du modèle, nous avons fusionné certaines classes pour en faire une classification binaire. Cela a permis de réduire l'impact du déséquilibre des classes.

3️⃣ Matrice de Confusion
Nous avons observé que certaines classes étaient souvent confondues :

Les classes 2 et 3 avec la classe 1.
Les classes 4 et 5 avec la classe 5.
Même avec cette fusion, le modèle reste sujet à un nombre élevé de faux positifs, principalement en raison du déséquilibre des classes.

🏁 Conclusion
Résultats clés :
Durée de livraison : Un facteur majeur influençant la note des clients. Plus la livraison est longue, plus les clients sont susceptibles de laisser une note faible.
Frais de livraison : Les frais plus élevés sont également associés à des notes plus basses.
Prix des produits : Bien que le prix ait un impact moindre, de nombreux produits bien notés sont plus chers.
Optimisation : En optimisant ces facteurs, le site peut améliorer l'expérience client et ainsi augmenter ses ventes et attirer plus de vendeurs sur la plateforme.

📦 Prérequis
Bibliothèques Python nécessaires :
pandas
numpy
matplotlib
seaborn
scikit-learn
sqlite3
google.colab (si vous utilisez Google Colab)
Vous pouvez installer ces bibliothèques avec la commande suivante :
