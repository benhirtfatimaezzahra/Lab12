# Lab12 – Statistiques avec NumPy

Application pratique des fonctions statistiques de NumPy sur un jeu de données de notes d'étudiants. Ce lab explore le calcul de statistiques globales et par axe, l'identification de performances, le filtrage conditionnel et l'enrichissement de tableaux.

Le programme démontre l'utilisation des fonctions d'agrégation NumPy, la manipulation d'axes, les masques booléens et la construction de tableaux de synthèse.

---

## Fonctionnalités

### Statistiques Globales
- **Moyenne générale** : calcul sur tous les éléments avec `np.mean()`
- **Min/Max globaux** : valeurs extrêmes avec `np.min()` et `np.max()`
- **Somme totale** : agrégation complète avec `np.sum()`
- **Écart-type global** : mesure de dispersion avec `np.std()`

### Statistiques par Axe
- **Par épreuve (axis=0)** : moyenne, min, max et écart-type de chaque colonne
- **Par étudiant (axis=1)** : moyenne, min, max et écart-type de chaque ligne
- **Agrégations directionnelles** : comprendre axis=0 vs axis=1
- **Dispersion individuelle** : analyse de la régularité des performances

### Identification de Performances
- **Meilleur étudiant** : recherche avec `np.argmax()` sur les moyennes
- **Épreuve la plus difficile** : identification avec `np.argmin()` sur les moyennes d'épreuves
- **Indexation avancée** : récupération des noms correspondants

### Filtrage Conditionnel
- **Seuil d'admission** : sélection des étudiants avec moyenne ≥ 12
- **Critère par épreuve** : filtrage selon performance à une épreuve spécifique
- **Masques booléens** : extraction de sous-ensembles avec conditions
- **Filtrage multi-critères** : combinaison de conditions

### Enrichissement de Tableaux
- **Ajout de colonnes** : moyenne individuelle avec `np.hstack()`
- **Ajout de lignes** : moyennes globales avec `np.vstack()`
- **Écart-type individuel** : colonne supplémentaire de dispersion
- **Reshape stratégique** : transformation (n,) → (n, 1) pour concaténation

### Rapport Formaté
- **Synthèse visuelle** : affichage structuré avec formatage
- **Tableau enrichi** : combinaison de toutes les statistiques
- **Présentation professionnelle** : alignement et précision décimale

---

## Architecture
```
Lab12.ipynb → Notebook Jupyter contenant :

1. Étape 1 : Mise en place du dataset
   - Tableau des noms (4 étudiants)
   - Matrice de notes (4 étudiants × 3 épreuves)
   - Vérification de la forme (shape)

2. Étape 2 : Statistiques globales
   - Moyenne générale : np.mean(notes)
   - Min/Max globaux : np.min(), np.max()
   - Somme et écart-type globaux

3. Étape 3 : Statistiques par axe
   - Task 3.1 : Par épreuve (axis=0)
     * Moyennes, min, max, écart-type de chaque colonne
   - Task 3.2 : Par étudiant (axis=1)
     * Moyennes, min, max, écart-type de chaque ligne

4. Étape 4 : Identification de performances
   - Task 4.1 : Meilleur étudiant avec np.argmax()
   - Task 4.2 : Épreuve la plus difficile avec np.argmin()

5. Étape 5 : Sélection conditionnelle
   - Task 5.1 : Étudiants avec moyenne ≥ 12
   - Task 5.2 : Étudiants avec ≥15 à l'épreuve E2

6. Étape 6 : Enrichissement du tableau
   - Task 6.1 : Ajout colonne moyenne avec np.hstack()
   - Task 6.2 : Ajout ligne moyennes globales avec np.vstack()
   - Task 6.3 : Ajout colonne écart-type (optionnel)

7. Étape 7 : Synthèse visuelle
   - Rapport formaté avec alignement
   - Affichage structuré du tableau final
```

---

## Installation

Cloner le projet :
```bash
git clone https://github.com/benhirtfatimaezzahra/Lab12.git
```

Installer NumPy (si nécessaire) :
```bash
pip install numpy
```

Ouvrir le notebook avec Jupyter :
```bash
cd Lab12
jupyter notebook Lab12.ipynb
```

Ou utilisez JupyterLab :
```bash
jupyter lab Lab12.ipynb
```

---



## Notes Techniques

### Concepts NumPy utilisés
- **Fonctions d'agrégation** : `np.mean()`, `np.min()`, `np.max()`, `np.sum()`, `np.std()`
- **Paramètre axis** : axis=0 (colonnes), axis=1 (lignes), axis=None (global)
- **Fonctions argmin/argmax** : `np.argmin()`, `np.argmax()` pour indices
- **Masques booléens** : filtrage avec conditions
- **Concaténation horizontale** : `np.hstack()` pour ajouter colonnes
- **Concaténation verticale** : `np.vstack()` pour ajouter lignes
- **Reshape** : transformation (n,) → (n, 1) avec `.reshape(-1, 1)`
- **Indexation avancée** : `array[masque]` pour extraction conditionnelle


## Démonstration

<img width="1641" height="815" alt="image" src="https://github.com/user-attachments/assets/aee65e50-289d-497c-806e-c403361a09aa" />
<img width="1645" height="685" alt="image" src="https://github.com/user-attachments/assets/5b458f54-3547-4ec9-b73c-0847b2d1cad6" />
<img width="1649" height="620" alt="image" src="https://github.com/user-attachments/assets/c8eb22ee-b022-4e2c-baa7-09b87cb430fb" />
<img width="1650" height="910" alt="image" src="https://github.com/user-attachments/assets/f5912095-b516-4381-b80e-5b7a264e7968" />
<img width="1649" height="801" alt="image" src="https://github.com/user-attachments/assets/bbc38d03-6af4-451a-b164-b486b6ca9fd9" />
<img width="1612" height="682" alt="image" src="https://github.com/user-attachments/assets/7909e31a-70ca-447d-b2d6-69d3eaee90eb" />
<img width="908" height="438" alt="image" src="https://github.com/user-attachments/assets/752ae553-ab3c-496b-b046-a9dd676c96da" />
<img width="1649" height="953" alt="image" src="https://github.com/user-attachments/assets/89ac187c-eb16-4f55-9077-199af6d80d54" />

---

## Auteur

**Nom :** Benhirt Fatima Ezzahra  
**Cours :** Introduction à Python  
**Date :** Décembre 2025  
**Encadré par :** Pr. Mohamed LACHGAR
