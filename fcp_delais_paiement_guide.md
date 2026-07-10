---
title: "Guide Professionnel : Application Excel FCP Délais de Paiement"
source: "https://youtu.be/BPDTnv8L7ZE?si=TmydNn4xw28RrRqG"
category: Knowledge Management
project: yt-notes-vault
tags:
  - #ComptabilitéMaroc
  - #Fiscalité
  - #DélaisDePaiement
  - #ExcelVBA
  - #EDI-DGI
date_created: 2026-07-10
last_modified: 2026-07-10
status: Completed
type: Video Note
---

# 📋 Guide Professionnel : FCP Délais de Paiement (Excel VBA)

L'application **FCP Délais de Paiement** est un outil d'automatisation avancée 100% VBA, conçu pour préparer, calculer et générer la déclaration des délais de paiement conformément aux exigences réglementaires de la **Direction Générale des Impôts (DGI)** au Maroc (Loi 69.21 / 15-95). L'absence de formules apparentes garantit la fluidité, la performance et la sécurité des calculs face aux modifications accidentelles.

---

## 1. Fonctionnalités Clés & Conformité DGI

L'outil prend en charge l'intégralité du processus de déclaration fiscale lié aux retards de paiement :
* **Génération EDI (XML & ZIP) :** Production instantanée du fichier XML conforme au cahier des charges de la plateforme *Simpl-Regularisation* de la DGI, encapsulé automatiquement dans une archive ZIP prête pour le téléversement.
* **Calcul Automatique des Pénalités :** Application stricte de la réglementation avec calcul des amendes et pénalités de retard selon les seuils légaux.
* **Intégration du Taux BAM :** Récupération et mise à jour automatique en ligne des taux directeurs de **Bank Al-Maghrib (BAM)** pour un calcul précis, actualisé et opposable.
* **Gestion du VISA Professionnel :** Intégration complète des données réglementaires du Comptable Agréé ou de l'Expert-Comptable (Visa, Convention, Codification DGI).

---

## 2. Structure et Modules de l'Application

### 🛠️ Configuration Initiale & Données de Base
Avant de lancer les calculs, l'application s'appuie sur des tables de référence structurées :
* **Fiches Tiers :** Base de données dédiée à la gestion et au suivi des **Fournisseurs** et des **Clients** (Identifiant Fiscal, ICE, Raison Sociale).
* **Paramètres de Période :** Permet de basculer facilement entre les déclarations trimestrielles (**T1, T2, T3, T4**) ou annuelles selon le régime d'imposition et le chiffre d'affaires de l'entreprise.

### 📊 Traitement des Factures & Moteur de Calcul
* **État des Factures :** Module central où sont répertoriées les factures non payées dans les délais légaux.
* **Moteur VBA :** Aucun risque de suppression accidentelle de formules. Le code VBA analyse dynamiquement les dates d'émission, les dates d'échéance et les dates de paiement effectif pour isoler les retards et appliquer le barème.

### 📉 Tableau de Bord & Pilotage (Dashboard)
* **Indicateurs Clés (KPIs) :** Visualisation immédiate du montant total des factures en retard, du montant des pénalités dues et du nombre de pièces concernées.
* **Graphiques Dynamiques :** Analyse visuelle de l'évolution des délais et des risques financiers par période ou par fournisseur pour faciliter l'audit interne.

---

## 3. Flux de Travail Standard (Workflow)

Pour réussir votre déclaration avec l'outil, suivez cette séquence méthodique :

1. **Alimentation :** Saisissez ou importez les données de vos factures (Montant TTC, Date de facturation, Date de règlement réglementaire).
2. **Actualisation :** Lancez la mise à jour des taux Bank Al-Maghrib en un clic via le connecteur web intégré.
3. **Génération des Livrables :**
   * Cliquez sur le bouton de génération EDI pour créer le fichier `.xml` et son `.zip` d'un coup.
   * Utilisez la fonction **Export PDF & Excel** : l'application classe et archive automatiquement les documents générés dans une structure de dossiers logique (ex: `Société / Année / Période`).
4. **Sécurité & Traçabilité :** L'outil intègre une fonction de **Sauvegarde automatique** et conserve un historique rigoureux des déclarations pour sécuriser vos travaux antérieurs face aux contrôles fiscaux.
