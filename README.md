# Projet-IT-UNEO

# Simulateur Comptabilité PageTurner

## 📄 Description

`simulateur_comptabilite_page_turner.py` est un script Python qui simule des données comptables pour une librairie fictive, **PageTurner Books**, basée à Genève, Suisse.  
Le script génère des données financières synthétiques sur une période personnalisable *(par défaut : 2021–2025)* et produit un fichier Excel structuré selon un **schéma comptable suisse strict** (inspiré de UNEO AbaReport pour PowerBI).

Les données incluent :
- Le **grand livre**
- Les **factures fournisseurs et clients**
- Le **plan comptable**
- Les **états financiers** (bilan et compte de résultat)
- Les **taux de change des devises**

---

## 🎯 Objectifs

- Simuler des transactions financières réalistes pour une librairie suisse.
- Générer des états financiers avec une colonne **"Solde"** pour le suivi des comptes.
- Produire un fichier Excel prêt à l’emploi pour analyse comptable ou intégration dans PowerBI.

---

## 📊 Scénarios de simulation

Le script simule divers types de transactions sur 5 ans (2021–2025) :

- **Factures fournisseurs** :  
  ~50 factures/an, montants entre 500–5000 CHF, TVA 7.7 % ou 8.1 %, frais de transport (~20 %), 90 % payées.
  
- **Factures clients** :  
  ~60 factures/an, montants :
  - 200–2000 CHF (2021–2022)
  - 500–5000 CHF (2023–2025)  
  85 % sont payées, avec reprise post-COVID.

- **Salaires** :  
  Mensuels pour 5 employés (3000–5000 CHF). Charges sociales réparties (AVS/AC/AMAT, LAA, IJM, LPP, IS) sur les comptes 2270–2279. Paiement net via 2299. Frais de repas (~30 % des mois).

- **Règlements TVA** :  
  Équilibrage trimestriel des comptes 1170, 1171, 1172, 2200.

- **Écritures diverses** :  
  - Mensuelles : loyers, frais admin.
  - Trimestrielles : publicité, amortissements.
  - Annuelles : impôts, frais bancaires (<18 fois/an).  
  Impacts COVID-19 inclus pour 2021–2022 (subventions, sécurité).

- **États financiers** :  
  - Bilan et compte de résultat avec colonne "Solde"
  - Résultat intégré au compte 2979 (Bénéfice/Perte)

---

## 📁 Sortie

Un fichier **Excel unique** : `BookstoreAccountingData.xlsx`  
Contient les feuilles suivantes :

- `GrandLivre`  
- `PlanComptable`  
- `CodesAnalytiques`  
- `Fournisseurs`, `FacturesFournisseurs`  
- `Clients`, `FacturesClients`  
- `Monnaies`, `CotationsDevises`  
- `BalanceDesComptes`, `Bilan`, `EtatDeResultat`

---

## 📚 À propos de PageTurner Books

**PageTurner Books** est une chaîne de librairies indépendantes basée à Genève, fondée en 2015. Elle se spécialise dans :

- La littérature
- Les matériels éducatifs
- La vente de livres en ligne

Elle a surmonté la crise COVID-19 (2021–2022), qui a réduit les ventes en magasin mais stimulé l’e-commerce (compte 3410). L’entreprise compte 5 employés et collabore avec des partenaires locaux (écoles, clubs de lecture).

Sa stratégie financière comprend :
- Des règlements TVA trimestriels
- Une gestion rigoureuse des dépenses
- Des réinvestissements ciblés  
**Objectif : rentabilité dès 2025**.

---

## ✅ Prérequis

- Python **3.8** ou supérieur
- Bibliothèques Python :
  - `pandas`
  - `numpy`
  - `openpyxl`

---

## 🔧 Installation

Clonez ce dépôt :

```bash
git clone https://github.com/<votre-nom-utilisateur>/simulateur-comptabilite-page-turner.git
cd simulateur-comptabilite-page-turner
