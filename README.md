# SARIMA-Time-Series-Forecasting
# SARIMA Time Series Forecasting Project

#  Modélisation SARIMA - Prévisions de Production Laitière

Ce projet implémente un modèle **SARIMA (Seasonal AutoRegressive Integrated Moving Average)** pour prévoir la production mensuelle de lait en utilisant des données historiques entre **1962 et 1975**.

## 📚 Sommaire

- [Objectif](#objectif)
- [Données Utilisées](#données-utilisées)
- [Principales Étapes](#principales-étapes)
- [Modèle Retenu](#modèle-retenu)
- [Résultats](#résultats)
- [Installation & Exécution](#installation--exécution)
- [Bibliothèques Utilisées](#bibliothèques-utilisées)
- [Auteur](#auteur)


##  Objectif

Prédire la production mensuelle de lait à l’aide du modèle **SARIMA**, en analysant les tendances, la saisonnalité et les fluctuations des données historiques.

---

##  Données Utilisées

Le jeu de données contient la **production mensuelle de lait** entre **janvier 1962** et **décembre 1975**.

- Source : Fichier CSV (`monthly-milk-production(1).csv`)
- Colonnes :
  - `Month` : Date (format YYYY-MM-DD)
  - `Milk Production` : Quantité produite (en unités arbitraires)

---

##  Principales Étapes

1. **Chargement et visualisation des données**
2. **Nettoyage et division des données** (train/test)
3. **Analyse exploratoire** (tendance, saisonnalité, résidus)
4. **Stationnarisation** via différenciation simple et saisonnière
5. **Calcul des coefficients saisonniers**
6. **Identification des paramètres avec ACF/PACF**
7. **Construction et évaluation du modèle SARIMA**

---

## Modèle Retenu

- **Type de modèle** : SARIMA(p,d,q)(P,D,Q)s
- **Paramètres optimaux** : `(1,1,0)(0,1,1)12`
- Justification :
  - Meilleurs résultats en termes de **MAE** et **RMSE**
  - Diagnostics validés (normalité des résidus, stationnarité, homoscédasticité)

---

## Résultats

- **MAE (Mean Absolute Error)** : 7.71
- **RMSE (Root Mean Squared Error)** : 90.47
- Les résidus sont bien distribués et le modèle montre une bonne capacité de prédiction.

---

## ⚙ Installation & Exécution

### Prérequis

Assurez-vous d'avoir installé les bibliothèques nécessaires :

```bash
pip install pandas numpy matplotlib statsmodels scikit-learn
```

### Lancer le Projet

1. Clonez le dépôt :

```bash
git clone https://github.com/votre-pseudo/milk-production-forecast.git
```

2. Accédez au dossier et exécutez le script principal :

```bash
cd milk-production-forecast
python model_sarima.py
```

> Remplacez `model_sarima.py` par le nom réel de votre script Python si différent.

---

##  Bibliothèques Utilisées

- `pandas`, `numpy` : Manipulation des données
- `matplotlib`, `statsmodels.graphics.tsaplots` : Visualisation
- `statsmodels.tsa.statespace.sarimax.SARIMAX` : Modélisation SARIMA
- `statsmodels.tsa.stattools.adfuller` : Test de Dickey-Fuller
- `seasonal_decompose` : Décomposition de la série temporelle
- `sklearn.metrics` : Évaluation des prévisions

---



👤 **Mourad Bahaddou**  
📧 Email: moradbahddou@gmail.com  
🔗 GitHub: [mourad-bahaddou](https://github.com/mourad-bahaddou)



