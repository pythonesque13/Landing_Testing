# Projet d'A/B Testing : Optimisation d'une Landing Page

Ce projet met en œuvre une analyse statistique complète d'un test A/B afin de déterminer si une nouvelle version d'une page de destination ("landing page") est plus performante que l'ancienne en termes de taux de conversion.

---

## Contexte et Objectifs

L'objectif est d'utiliser une approche "data-driven" pour prendre une décision business : faut-il remplacer l'ancienne page par la nouvelle ? Pour cela, nous allons :

1.  **Nettoyer et préparer les données** issues de l'expérimentation.
2.  **Formuler des hypothèses statistiques** claires (hypothèse nulle H0 et alternative H1).
3.  **Réaliser un test statistique** (Z-test pour deux proportions) pour évaluer la significativité des résultats.
4.  **Interpréter les résultats** (notamment la p-value) et formuler une recommandation business concrète.

---

## Technologies et Librairies

- **Langage :** Python 3.9+
- **Analyse de données :** Pandas, NumPy
- **Tests statistiques :** `statsmodels` (pour le Z-test)
- **Analyse exploratoire :** Jupyter Lab, Matplotlib, Seaborn

---

## Installation et Lancement de l'Analyse

Suivez ces étapes pour reproduire l'analyse sur votre machine.

### 1. Prérequis

- Avoir [Git](https://git-scm.com/) et [Python](https://www.python.org/downloads/) (version 3.9+) installés.

### 2. Cloner le Dépôt

```bash
git clone https://github.com/pythonesque13/Landing_Testing.git
cd Landing_Testing
```
----

### 3. Créer l'Environnement et Installer les Dépendances

```bash     
    # Créer un environnement virtuel
    python -m venv venv

    # Activer l'environnement
    # Sur Windows : venv\Scripts\activate
    # Sur macOS/Linux : source venv/bin/activate

    # Installer les librairies
    pip install -r requirements.txt

```  

### 4. Lancer Jupyter Lab

Pour explorer le notebook contenant l'analyse :

```bash     
    jupyter lab
```
    
 
### Naviguez ensuite vers le dossier notebooks/ et ouvrez 01-Analyse-AB-Testing.ipynb.
    Résultats et Conclusion
Analyse

Après un nettoyage rigoureux des données pour éliminer les utilisateurs dupliqués et les assignations incorrectes, nous avons calculé les taux de conversion :

    Groupe Contrôle (ancienne page) : ~12.02%

    Groupe Traitement (nouvelle page) : ~11.87%

À première vue, la nouvelle page semble légèrement moins performante.
Test Statistique

Un Z-test pour deux proportions a été réalisé pour vérifier si cette différence était statistiquement significative.

    Hypothèse Nulle (H0) : Il n'y a pas de différence de conversion entre les deux pages.

    Hypothèse Alternative (H1) : Il y a une différence de conversion.

Le test a donné une p-value d'environ 0.19.
Conclusion

Étant donné que la p-value (0.23) est largement supérieure à notre seuil de significativité de 0.05, nous ne pouvons pas rejeter l'hypothèse nulle.

Recommandation Business :
Il n'y a pas de preuve statistique que la nouvelle page apporte une amélioration. Par conséquent, il est recommandé de ne pas lancer la nouvelle page et de conserver l'ancienne version, qui reste la plus performante et la moins risquée.