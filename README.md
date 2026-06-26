# 📊 Projet Power BI – Analyse des Performances d'un Établissement Scolaire

## 📌 Contexte du projet

La direction d'un établissement scolaire souhaite disposer d'un tableau de bord décisionnel permettant d'analyser les performances académiques des élèves, l'absentéisme, la charge de travail des enseignants ainsi que l'efficacité des cours dispensés.

L'objectif de ce projet est de transformer des données brutes en indicateurs pertinents afin d'aider les responsables pédagogiques à prendre des décisions stratégiques.

---

# 🎯 Objectifs

* Nettoyer et préparer les données.
* Construire un modèle de données optimisé.
* Développer des mesures DAX avancées.
* Concevoir un tableau de bord interactif sous Power BI.
* Identifier des insights et proposer des recommandations.

---

# 📁 Jeux de données

Le projet repose sur trois fichiers CSV.

## 1. students.csv

Informations concernant les élèves.

| Colonne         | Description          |
| --------------- | -------------------- |
| student_id      | Identifiant unique   |
| full_name       | Nom complet          |
| birth_date      | Date de naissance    |
| gender          | Genre                |
| enrollment_date | Date d'inscription   |
| class_level     | Niveau scolaire      |
| section         | Section              |
| status          | Statut de l'élève    |
| average_grade   | Moyenne générale     |
| absences_count  | Nombre d'absences    |
| teacher_id      | Professeur principal |

---

## 2. teachers.csv

Informations concernant les enseignants.

| Colonne            | Description          |
| ------------------ | -------------------- |
| teacher_id         | Identifiant unique   |
| full_name          | Nom complet          |
| hire_date          | Date d'embauche      |
| subject            | Matière enseignée    |
| department         | Département          |
| classlevelassigned | Niveau affecté       |
| contract_type      | Type de contrat      |
| weekly_hours       | Heures hebdomadaires |
| city               | Ville                |
| performance_rating | Note d'évaluation    |

---

## 3. courses.csv

Informations relatives aux cours et aux résultats.

| Colonne         | Description          |
| --------------- | -------------------- |
| course_id       | Identifiant du cours |
| course_name     | Nom du cours         |
| teacher_id      | Enseignant           |
| student_id      | Élève                |
| semester        | Semestre             |
| year            | Année scolaire       |
| scheduled_hours | Heures prévues       |
| completed_hours | Heures réalisées     |
| grade           | Note obtenue         |
| pass_fail       | Réussi / Échoué      |

---

# 🛠 Technologies utilisées

* Microsoft Power BI Desktop
* Power Query
* DAX
* CSV
* Git / GitHub (optionnel)

---

# 🔄 Étapes du projet

## 1. Exploration des données

* Import des trois fichiers CSV.
* Profilage des colonnes.
* Détection :

  * valeurs manquantes
  * doublons
  * erreurs de type
  * valeurs aberrantes
  * incohérences.

---

## 2. Nettoyage des données

Les traitements réalisés comprennent :

* suppression des doublons
* gestion des valeurs manquantes
* remplacement des notes manquantes par la médiane
* remplacement des valeurs texte par **"Inconnu"**
* correction des formats de dates
* uniformisation des textes
* suppression des espaces inutiles
* correction des valeurs du genre.

### Colonnes calculées

* Âge de l'élève
* Ancienneté enseignant
* Taux de réalisation des cours
* Année d'inscription

---

## 3. Modélisation

Relations créées :

```
Teachers
    │
    ├──────── Students
    │              │
    │              │
    └──────── Courses
```

Relations :

* Teachers → Students
* Teachers → Courses
* Students → Courses

Ajout d'une table calendrier :

* Année
* Mois
* Trimestre
* Semaine

---

## 4. Mesures DAX

Mesures développées :

* Total Élèves
* Moyenne Générale
* Taux de Réussite
* Élèves à Risque
* Heures Moyennes par Enseignant
* Top Matières
* Évolution des Inscriptions

---

# 📈 Tableau de bord

## Page 1 — Vue Élèves

KPIs

* Total élèves
* Moyenne générale
* Taux de réussite
* Élèves à risque

Visualisations

* Répartition par niveau
* Répartition par section
* Évolution des inscriptions
* Corrélation Absences / Moyenne
* Répartition par statut

---

## Page 2 — Vue Enseignants

KPIs

* Total enseignants
* Ancienneté moyenne
* Heures hebdomadaires moyennes
* Performance moyenne

Visualisations

* Répartition par matière
* Répartition par contrat
* Histogramme des évaluations
* Top 5 enseignants
* Flop 5 enseignants

---

## Page 3 — Vue Cours & Résultats

KPIs

* Total cours
* Taux de réalisation
* Taux de réussite par semestre

Visualisations

* Réussite / Échec par matière
* Évolution des notes
* Tableau des matières avec moyenne ≥ 12

---

# 🎛 Interactivité

Le rapport comprend :

* Slicer Année scolaire
* Slicer Niveau
* Slicer Matière
* Slicer Contrat enseignant
* Slicer Semestre
* Interactions entre visuels
* Bouton de réinitialisation des filtres

---

# 📊 Principaux indicateurs

* Nombre total d'élèves
* Nombre total d'enseignants
* Moyenne générale
* Taux de réussite
* Élèves à risque
* Ancienneté moyenne
* Charge horaire moyenne
* Performance des enseignants
* Taux de réalisation des cours

---

# 💡 Conclusions et recommandations

Le rapport permet d'identifier :

* les matières présentant le plus fort taux d'échec ;
* les enseignants sous-chargés ou surchargés ;
* les élèves en difficulté selon leurs absences et leurs résultats ;
* l'évolution des inscriptions au fil des années ;
* les performances académiques par niveau scolaire.

Ces analyses facilitent la prise de décision en matière de suivi pédagogique, de répartition des ressources et d'amélioration des résultats scolaires.

---

# 📂 Structure du projet

```
Projet Power BI/
│
├── Dataset/
│   ├── students.csv
│   ├── teachers.csv
│   └── courses.csv
│
├── Rapport/
│   └── School_Analytics.pbix
│
├── Images/
│   ├── Dashboard_Students.png
│   ├── Dashboard_Teachers.png
│   └── Dashboard_Courses.png
│
└── README.md
```
# 📸 Captures d’Écran

## 🖥️Dashboard_Students

<img width="1298" height="730" alt="Dashboard_Students" src="https://github.com/user-attachments/assets/b63b17c7-38db-460e-9bab-58fbb7f6a5f9" />

## 🖥️Dashboard_Teachers
<img width="1115" height="801" alt="Dashboard_Teachers" src="https://github.com/user-attachments/assets/563a6ed6-09c7-4fb7-abfb-39ec42bf5846" />

## Dashboard_Courses
<img width="1295" height="733" alt="Dashboard_Courses" src="https://github.com/user-attachments/assets/6ba50b6a-156c-4bd1-8c9b-83ad9aa179c7" />

