Analyse Olist : Ce que les données racontent sur l'e-commerce brésilien
J'ai travaillé sur le dataset d'Olist (100 000 commandes entre 2016 et 2018) pour comprendre comment la logistique impacte réellement la satisfaction client dans un pays aussi vaste que le Brésil.

Ce projet est le résultat d'un pipeline complet : du nettoyage brut en Python à la création d'un outil d'aide à la décision sur Power BI.

📊 Aperçu des Dashboards

🧠 Ma démarche de travail

1. Préparation (Python & SQL)
Les données étaient réparties sur plusieurs fichiers CSV. J'ai utilisé Pandas pour fusionner les tables (orders, customers, reviews) et nettoyer les types de données (notamment les timestamps). L'idée était d'arriver à un fichier maître propre, sans doublons, prêt pour l'analyse.

2. Visualisation & Stratégie (Power BI)
L'objectif n'était pas de faire de "beaux graphiques", mais de trouver des leviers de croissance.

Volume vs Qualité : J'ai mis en opposition le Chiffre d'Affaires total (13,53 M€) et le Panier Moyen (120,4 €) pour situer le positionnement prix d'Olist.

Analyse Géographique : J'ai utilisé une arborescence de décomposition pour explorer comment le CA se répartit par État, avec une domination sans surprise de São Paulo (SP).

💡 Les découvertes (Insights)

C'est la partie la plus intéressante de l'analyse :

Le poids de la logistique : En croisant les frais de port (freight_value) et les notes de satisfaction, j'ai pu démontrer visuellement que le prix de livraison est un frein majeur à l'expérience client. Plus les frais montent, plus la note chute.

L'effet Black Friday : On observe un pic massif de ventes en novembre 2017, ce qui valide la cohérence temporelle du dataset.

Gestion des litiges : J'ai intégré une table des commandes à 1 étoile pour isoler les transactions les plus problématiques et permettre une analyse granulaire des échecs de livraison.

## 📂 Structure du dépôt

* 📊 **[Analyse interactive (Power BI)](./Olist_Dashboard.pbix)** : Le fichier source de mes tableaux de bord.
* 🐍 **[Nettoyage des données (Notebook Python)](./Olist_Ecommerce_Analyse.ipynb)** : Mon script Google Colab pour la fusion et le traitement des tables.
* 🖼️ **[Captures d'écran](./images)** : Dossier contenant les visuels du projet pour une consultation rapide.
