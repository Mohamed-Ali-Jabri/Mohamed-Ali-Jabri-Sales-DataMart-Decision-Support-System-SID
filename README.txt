Mini-projet SID – DataMart de Vente

Présentation du projet
Ce mini-projet a été réalisé dans le cadre du module Systèmes
d’Information Décisionnels (SID).

L’objectif du projet est de concevoir et mettre en place un DataMart
permettant l’analyse des ventes selon différentes dimensions
(Client, Produit et Date) afin de faciliter la prise de décision.

------------------------------------------------------

Objectifs du projet
- Concevoir un DataMart orienté analyse des ventes
- Mettre en place une modélisation dimensionnelle
- Implémenter un processus ETL
- Analyser les indicateurs de performance commerciale
- Visualiser les résultats à l’aide de tableaux de bord

------------------------------------------------------

Modélisation du DataMart
Le DataMart est basé sur un schéma en étoile composé de :

Table de faits
- Fact_Vente
  - Id_Fact
  - ID_DimClient
  - ID_DimProduit
  - ID_DimDate
  - QTEPRD
  - MNTHT

Tables de dimensions
- Dim_Client
  - ID_DimClient
  - Num_Client
  - Nom_Client
  - Type_Client
  - Secteur_Client
  - Gouvernorat

- Dim_Produit
  - ID_DimProduit
  - Code_Produit
  - Libelle_Produit
  - Categorie_Produit

- Dim_Date
  - ID_DimDate
  - Mois
  - Annee
  - Periode

------------------------------------------------------

Architecture du projet
- Source de données : fichiers Excel
- Zone de staging
- DataMart (schéma en étoile)
- Outil ETL : SSIS
- Outil de visualisation : Power BI

------------------------------------------------------

Processus ETL
- Extraction des données depuis des fichiers Excel
- Nettoyage et transformation des données
- Chargement des dimensions
- Chargement de la table de faits
- Gestion des clés primaires et étrangères

------------------------------------------------------

Analyse et visualisation
Des tableaux de bord ont été développés pour analyser :
- Le montant des ventes
- Les quantités vendues
- Les ventes par client
- Les ventes par produit
- Les ventes par période

------------------------------------------------------

Technologies utilisées
- SQL Server
- SSIS (SQL Server Integration Services)
- Power BI
- Microsoft Excel

------------------------------------------------------

Conclusion
Ce mini-projet a permis de mettre en pratique les concepts fondamentaux
des systèmes d’information décisionnels, notamment la modélisation
dimensionnelle, l’ETL et la visualisation des données pour l’aide
à la décision.
