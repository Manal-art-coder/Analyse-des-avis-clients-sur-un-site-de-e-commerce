# 📊 Projet d'Analyse des Avis Clients - Site de E-Commerce

## 🎯 Objectif du Projet

L'objectif de ce projet est de **prédire la note d'un client** pour une commande sur un site de **e-commerce brésilien**.  
Les avis clients sont essentiels pour **renforcer la confiance des acheteurs** et augmenter les ventes.  

### 📌 Objectifs spécifiques :
- 🔍 **Prédire** la note d'un client.
- 🧐 **Analyser** les facteurs influençant la satisfaction.
- 📈 **Optimiser** l'expérience utilisateur et les ventes.

---

## 🛠️ Étapes du Projet

### 1️⃣ **Extraction et Compréhension des Données**
- 🔗 **Fusion des bases relationnelles** via SQL.
- 🗂️ **Conversion et création de colonnes** :
  - 📦 `delivery_duration` : Durée réelle de livraison.
  - ⏳ `difference_between_expected_and_real_delivery_date` : Écart entre la date estimée et réelle.

### 2️⃣ **Datavisualisation**
Avant la modélisation, nous avons **visualisé** les données pour identifier les tendances :
- 📅 **Évolution des commandes** (2017-2018).
- 🕒 **Périodes d’achat préférées** (après-midi, lundi).
- 💰 **Impact du prix et des frais de livraison** sur les notes.

### 3️⃣ **Feature Engineering**
- 📝 `number_review_before` : Nombre d’avis laissés avant l’achat.
- ⭐ `review_score_before` : Note moyenne d’un produit avant achat.
- 🔄 **Traduction** des noms de catégories de produits.

### 4️⃣ **Modélisation**
- 🌲 **Modèle : Random Forest**.
- 🔀 **Fusion des classes** pour gérer le déséquilibre des données.
- 📊 **Évaluation** et analyse des erreurs du modèle.

---

## ⚙️ Étapes Préparatoires et Préprocessing

### 📌 Sélection des Variables
| Variable | Description |
|----------|-------------|
| `order_status` | Statut de la commande |
| `product_category_name_english` | Catégorie du produit |
| `price` | Prix du produit |
| `delivery_duration` | Durée de livraison |
| `difference_between_expected_and_real_delivery_date` | Écart entre livraison estimée et réelle |
| `freight_value` | Frais de livraison |
| `review_score_before` | Note moyenne avant achat |
| `number_review_before` | Nombre d'avis avant achat |
| `hour` | Heure de l'achat |
| `weekday` | Jour de la semaine de l'achat |

### 🔄 Préprocessing
- 🚫 **Suppression des valeurs manquantes**.
- 🎡 **Encodage trigonométrique** des variables temporelles :
  ```python
  hour_cos = np.cos(2 * np.pi * hour / 24)
  hour_sin = np.sin(2 * np.pi * hour / 24)
- 🔀 **Séparation des données en train/test**.
  
## 🧠 Modélisation et Évaluation

🌲 **Modèle Random Forest**

Nous avons testé Random Forest, qui offre la meilleure précision pour prédire les notes des clients.

🔀 **Fusion des Classes**
Pour améliorer la classification, nous avons regroupé :

(1, 2, 3) → Classe "Mauvaise note"
(4, 5) → Classe "Bonne note"

📊 **Matrice de Confusion**

Certaines classes sont souvent confondues :
❌ Les notes 2 et 3 sont souvent classées comme 1.
❌ Les notes 4 et 5 sont souvent confondues.

Malgré cela, la fusion des classes a amélioré la précision globale.

## 🏁 Conclusion

🔑 **Résultats clés** :
🚚 Durée de livraison : Impact majeur sur la note client.
💵 Frais de livraison : Plus ils sont élevés, plus la note baisse.
🏷️ Prix des produits : Moins impactant, mais les produits plus chers sont mieux notés.
🎯 En optimisant ces facteurs, on peut améliorer l’expérience client et augmenter les ventes !

📦 **Prérequis**

📌 **Bibliothèques Python nécessaires** :

pip install pandas numpy matplotlib seaborn scikit-learn sqlite3
