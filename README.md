# 📊 Sales DataMart – Decision Support System ( SID )

## 📖 Présentation du projet
Ce mini-projet a été réalisé dans le cadre du module **Systèmes d'Information Décisionnels (SID)**. 

L’objectif principal est de concevoir et de mettre en place un **DataMart** permettant l’analyse des ventes selon différentes dimensions (Client, Produit et Date) afin de faciliter la prise de décision en entreprise.

---

## 🎯 Objectifs du projet
- Concevoir un DataMart orienté analyse des ventes.
- Mettre en place une modélisation dimensionnelle (Schéma en étoile).
- Implémenter un processus ETL robuste pour le traitement de la donnée.
- Analyser les indicateurs de performance commerciale (KPI).
- Visualiser les résultats à l’aide de tableaux de bord interactifs.

---

## 🗄️ Modélisation du DataMart
Le DataMart repose sur un modèle classique en **schéma en étoile**, composé de la manière suivante :

### 🌟 Table de faits
**`Fact_Vente`**
- `Id_Fact` (Clé Primaire)
- `ID_DimClient` (Clé technique)
- `ID_DimProduit` (Clé technique)
- `ID_DimDate` (Clé technique)
- `QTEPRD` (Quantité de produit vendue)
- `MNTHT` (Montant de la vente Hors Taxe)

### 📌 Tables de dimensions
- **`Dim_Client`** : `ID_DimClient`, `Num_Client`, `Nom_Client`, `Type_Client`, `Secteur_Client`, `Gouvernorat`
- **`Dim_Produit`** : `ID_DimProduit`, `Code_Produit`, `Libelle_Produit`, `Categorie_Produit`
- **`Dim_Date`** : `ID_DimDate`, `Mois`, `Annee`, `Periode`

---

## 🏗️ Architecture du projet
L'architecture de la solution s'articule autour des éléments suivants :
- **Sources de données** : Fichiers Excel / CSV 📄
- **Zone de Staging (ODS)** : Chargement et préparation intermédiaire des données brutes.
- **DataMart (DWH)** : Base de données finale, optimisée pour l'analyse (Schéma en étoile).
- **Outil ETL** : SQL Server Integration Services (SSIS).
- **Outil de visualisation** : Power BI.

---

## ⚙️ Processus ETL
Le flux d'intégration de données a été construit ainsi :
1. **Extraction** des données depuis la source (Excel/CSV).
2. **Nettoyage et Transformation** via les control flows / data flows de SSIS.
3. **Chargement (Load)** des dimensions.
4. **Chargement** de la table de faits pour y associer les Surrogate Keys des dimensions.

---

## 📈 Analyse et Visualisation
Des tableaux de bord Power BI ont été développés afin d'analyser dynamiquement :
- 💰 Le montant total des ventes
- 📦 Les quantités vendues
- 👥 Les ventes réparties par client (selon leur secteur, localisation, etc.)
- 🏷️ Les ventes segmentées par types de produit
- 📅 L'évolution des ventes dans le temps (par mois, entreprise)

🎥 **[▶️ Cliquez ici pour visionner une démonstration vidéo du Tableau de Bord Microsoft Power BI](https://drive.google.com/file/d/1k1vr1mYiMvrHLAybGXPZILM7rqSbOwEa/view?usp=sharing)**

---

## 💻 Technologies Utilisées
- ![SQL Server](https://img.shields.io/badge/SQL_Server-_?style=for-the-badge&logo=microsoftsqlserver&logoColor=white&color=CC2927) SGBD hébergeant la base ODS et DWH.
- ![SSIS](https://img.shields.io/badge/SSIS-_?style=for-the-badge&logo=visualstudio&logoColor=white&color=5C2D91) Orchestration de l'ETL.
- ![Power BI](https://img.shields.io/badge/Power_BI-_?style=for-the-badge&logo=powerbi&logoColor=white&color=F2C811) Visualisation et Reporting.
- ![Excel](https://img.shields.io/badge/Excel-_?style=for-the-badge&logo=microsoftexcel&logoColor=white&color=217346) Système et fichiers source.

---

## Conclusion
Ce mini-projet a permis de mettre en pratique les concepts fondamentaux de bout en bout des Systèmes d’Information Décisionnels : depuis les données sources, la modélisation dimensionnelle au niveau logique et physique, la tuyauterie de la donnée (ETL), jusqu'à l'exploration analytique et la Data Visualization pour l’aide à la décision.
