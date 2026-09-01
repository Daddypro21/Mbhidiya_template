# 07 - Architecture de l'Information

## 1. Principes d'architecture

L'architecture du site Mbhidiya Intelligence est concue selon trois principes :

1. **Profondeur progressive** : l'utilisateur decouvre l'information du general vers le specifique, sans etre submerge. La page d'accueil donne une vue d'ensemble, chaque page de service va dans le detail.

2. **Acces rapide au CTA** : un decision-maker en C-suite ne passera pas 10 minutes a naviguer. Le CTA "Request a Consultation" doit etre accessible en maximum 2 clics depuis n'importe quelle page.

3. **Credibilite par la structure** : une navigation bien organisee est en soi un signal de competence. Un site confus inspire la mefiance -- exactement le contraire de ce que Mbhidiya vend.

## 2. Arborescence du site

```
mbhidiya.com/
|
|-- Accueil (/)
|
|-- A propos (/about)
|   |-- Notre mission
|   |-- Notre approche (5 etapes)
|   |-- L'equipe dirigeante
|
|-- Services (/services)
|   |-- Vue d'ensemble (/services)
|   |-- Human Risk Intelligence (/services/human-risk-intelligence)
|   |-- Corporate & Counterparty Intelligence (/services/corporate-counterparty-intelligence)
|   |-- African Cross-Border Counterparty Intelligence (/services/african-cross-border-intelligence)
|   |-- Pre-Investment & Transaction Intelligence (/services/pre-investment-transaction-intelligence)
|   |-- Executive Vetting & Leadership Due Diligence (/services/executive-vetting)
|   |-- Reputation & Digital Footprint Intelligence (/services/reputation-digital-footprint)
|   |-- Network & Influence Intelligence (/services/network-influence-intelligence)
|   |-- Market Entry & Strategic Intelligence (/services/market-entry-strategic-intelligence)
|   |-- Third-Party & Supplier Integrity (/services/third-party-supplier-integrity)
|   |-- Fraud & Integrity Intelligence (/services/fraud-integrity-intelligence)
|   |-- Continuous Intelligence Monitoring (/services/continuous-monitoring)
|
|-- Secteurs (/sectors)
|   |-- Private Equity & Investment
|   |-- Corporate Development & M&A
|   |-- Law Firms
|   |-- Financial Institutions & Fintech
|   |-- Mining & Natural Resources
|   |-- Infrastructure, Energy & Logistics
|   |-- Technology & Digital Businesses
|
|-- Pourquoi Mbhidiya (/why-mbhidiya)
|
|-- Canada & Afrique (/canada-africa)
|
|-- Notre processus (/process)
|
|-- Insights (/insights)
|   |-- [Article 1] (/insights/slug-article)
|   |-- [Article 2]
|   |-- ...
|
|-- Contact (/contact)
|
|-- Mentions legales (/legal)
|-- Politique de confidentialite (/privacy)
```

## 3. Navigation principale (header)

### Desktop

```
[Logo]   Services v   A propos   Canada & Afrique   Secteurs   Insights   [CTA: Contact]
```

**Justification de l'ordre** (Loi de la Position Serielle) :
- **Services en premier** : c'est ce que les prospects cherchent en priorite (primacy effect -- les premiers elements sont mieux retenus)
- **Insights en dernier** : contenu de credibilite, retenu par le recency effect (les derniers elements sont aussi mieux retenus)
- **Canada & Afrique au centre** : positionnement geographique distinctif
- **"Accueil" retire** : le logo remplit deja cette fonction (convention universelle, Loi de Jakob). Cela reduit la navigation a 6 items, conforme a la Loi de Miller (7 +/- 2)

**"Services"** est le seul item avec un menu deroulant (mega-menu) car il contient 11 sous-pages.

### Mega-menu Services

Le mega-menu s'ouvre au hover/clic sur "Services" et presente les 11 services organises en 3 colonnes :

```
+-----------------------------------------------------------------+
| INTELLIGENCE DES PERSONNES    | INTELLIGENCE CORPORATE         |
|                               |                                |
| Human Risk Intelligence       | * African Cross-Border (phare) |
| Executive Vetting             | Corporate & Counterparty       |
| Reputation & Digital Footprint| Pre-Investment & Transaction   |
| Network & Influence           | Third-Party & Supplier         |
|                               |                                |
| INTELLIGENCE STRATEGIQUE      | [CTA]                          |
|                               |                                |
| Market Entry & Strategic      | Besoin d'aide pour choisir ?   |
| Fraud & Integrity             | Request a Consultation >       |
| Continuous Monitoring         |                                |
+-----------------------------------------------------------------+
```

**Note** : Le service phare "African Cross-Border" est place en **premiere position** de sa colonne (Loi de la Position Serielle + Effet Von Restorff) avec un badge visuel "Flagship Service".

### Mobile

Le menu mobile est un overlay plein ecran avec la navigation empilee verticalement. Les services sont accessibles via un accordion.

## 4. Parcours utilisateur principaux

### Parcours 1 : "Je cherche un service specifique"

```
Accueil --> Services (mega-menu) --> Page du service --> CTA Consultation
                                                    ou
                                                    --> Contact
```
**Nombre de clics jusqu'au formulaire : 2-3**

### Parcours 2 : "Je veux comprendre qui ils sont avant de les contacter"

```
Accueil --> A propos --> Pourquoi Mbhidiya --> Notre processus --> Contact
```
**Nombre de clics : 4 (avec CTA disponible sur chaque page)**

### Parcours 3 : "Je suis une entreprise canadienne qui veut aller en Afrique"

```
Accueil --> Canada & Afrique --> Services (African Cross-Border) --> Contact
```
**Nombre de clics : 3**

### Parcours 4 : "Je veux lire du contenu pour evaluer leur expertise"

```
Accueil --> Insights --> Article --> (CTA en bas d'article) --> Contact
```
**Nombre de clics : 3**

## 5. Structure de chaque page

### 5.1 Page d'accueil

| Section | Contenu | Objectif |
|---|---|---|
| **Hero** | Phrase d'accroche + 2 CTAs | Capter l'attention, definir le positionnement |
| **Problem statement** | "Les decisions critiques dependent de la confiance..." | Creer l'urgence, le besoin |
| **Core intelligence areas** | 6 services principaux en grille | Montrer l'etendue des competences |
| **Geographic coverage** | Carte Canada + Afrique | Ancrer le positionnement geographique |
| **Why Mbhidiya** | 5 differenciateurs | Convaincre de la valeur unique |
| **Process teaser** | Timeline 5 etapes | Rassurer sur la methode |
| **CTA section** | "Make Your Next Decision..." | Convertir |
| **Footer** | Navigation + contact | Informations pratiques |

### 5.2 Page de service (template)

| Section | Contenu |
|---|---|
| **Hero** | Titre percutant + question rhetorique + courte description |
| **Le probleme** | Pourquoi ce service est necessaire (contexte) |
| **Ce que nous examinons** | Liste structuree des domaines d'investigation |
| **Cas d'usage types** | Situations concretes avec icones |
| **Livrable** | Ce que le client recoit (assessment, rapport, recommandations) |
| **Services lies** | 2-3 services complementaires (cross-sell) |
| **CTA** | "Discuss your intelligence requirement" |

### 5.3 Page A propos

| Section | Contenu |
|---|---|
| **Hero** | "Intelligence Beyond What Is Obvious" |
| **Mission** | Statement de mission |
| **Approche** | Les 5 etapes de la methodologie |
| **Equipe** | Portraits + bios des 3 dirigeants |
| **Valeurs** | Discretion, Loyaute, Precision |
| **CTA** | Vers contact |

### 5.4 Page Contact

| Section | Contenu |
|---|---|
| **Hero compact** | "Make Your Next Decision With Better Intelligence" |
| **Situations** | Liste des cas ou Mbhidiya peut aider |
| **Formulaire** | Nom, Organisation, Email, Pays, Message + CTA |
| **Confidentialite** | Note sur la securite des communications |
| **Coordonnees** | Email securise, ligne directe |

## 6. SEO et meta-structure

### Strategie de titres (balises title)

```
Accueil :     "Mbhidiya Intelligence | Cross-Border Intelligence for High-Stakes Decisions"
A propos :    "About Us | Mbhidiya Intelligence"
Services :    "Our Services | Intelligence & Investigations | Mbhidiya Intelligence"
[Service] :   "[Nom du service] | Mbhidiya Intelligence"
Secteurs :    "Who We Work With | Mbhidiya Intelligence"
Canada-Afrique: "Canada-Africa Intelligence | Mbhidiya Intelligence"
Process :     "How We Work | Mbhidiya Intelligence"
Insights :    "Intelligence Insights & Articles | Mbhidiya Intelligence"
Contact :     "Contact Us | Confidential Consultation | Mbhidiya Intelligence"
```

### Meta descriptions (exemples)

```
Accueil :     "Cross-border intelligence, due diligence and investigative services for
               organisations making critical decisions about people, companies and
               opportunities across Canada and Africa."

Services :    "From human risk intelligence to continuous monitoring — 11 specialised
               intelligence services for high-stakes business decisions."

Contact :     "Start a confidential conversation about your intelligence requirement.
               Mbhidiya Intelligence supports decisions across Canada and Africa."
```

### Structure des URLs

- Toutes en minuscules
- Mots separes par des tirets
- Pas de trailing slash
- Pas de parametre de query pour le contenu permanent
- Pas de /page/2 pour la pagination (infinite scroll ou "Load more")

## 7. Fil d'Ariane (breadcrumb)

Present sur toutes les pages sauf la page d'accueil :

```
Accueil > Services > Human Risk Intelligence
Accueil > A propos
Accueil > Insights > [Titre de l'article]
```

Schema markup `BreadcrumbList` pour le SEO.

## 8. Gestion du contenu dynamique

### Blog / Insights

Le systeme de blog est simple pour la V1 :

- **Listing** : grille de cartes 3 colonnes, triees par date, avec categorie badge
- **Article** : layout a une colonne centree (max-width 720px), avec sidebar optionnelle (articles lies)
- **Categories suggerees** : Due Diligence, Cross-Border, Executive Risk, Market Intelligence, AfCFTA, Methodology

### Internationalisation (V2)

Le site est en anglais pour la V1. Si une version francaise est prevue :
- Structure : sous-domaines (fr.mbhidiya.com) ou prefixes (/fr/)
- Symfony supporte nativement le multilingue via le composant Translation
- Chaque route aura un parametre `_locale`
