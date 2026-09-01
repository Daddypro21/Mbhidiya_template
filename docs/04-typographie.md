# 04 - Systeme Typographique

## 1. Philosophie typographique

La typographie de Mbhidiya Intelligence repose sur un **contraste delibere entre tradition et modernite** :

- **Serif pour les titres** : evoque l'autorite, la tradition, la gravite. Les institutions financieres, cabinets d'avocats et firmes de conseil de premier plan utilisent des serifs pour leurs headlines. C'est un signal de serieux et d'expertise.
- **Sans-serif pour le corps** : assure une lisibilite optimale sur ecran, projette la modernite et la precision technique.

Ce contraste serif/sans-serif est un classique du design institutionnel haut de gamme. Il fonctionne particulierement bien pour Mbhidiya car il reflete la dualite de l'entreprise : des methodes d'investigation eprouvees (tradition) combinees a des techniques OSINT/SOCMINT modernes (innovation).

## 2. Polices selectionnees

### Police de titres : DM Serif Display

| Propriete              | Detail                                         |
| ---------------------- | ---------------------------------------------- |
| **Nom**                | DM Serif Display                               |
| **Fonderie**           | Colophon Foundry (pour Google Fonts)           |
| **Licence**            | Open Font License (gratuite, usage commercial) |
| **Graisses utilisees** | Regular (400) uniquement                       |
| **Source**             | Google Fonts                                   |

**Justification du choix** :

- Serif de style transitionnel avec une elegance moderne qui rappelle la typographie du logo
- Caracteres aux contrastes de pleins/delies prononces, projettant autorite et raffinement
- Excellente lisibilite en grande taille (titres, hero statements)
- Alternative open-source credible aux polices commerciales comme Freight Display ou Canela
- L'italique est disponible pour les citations et mises en avant

**Alternatives en cas de non-disponibilite** :

1. Playfair Display (Google Fonts)
2. Libre Baskerville (Google Fonts)
3. Georgia (system font, fallback ultime)

### Police de corps : Inter

| Propriete              | Detail                                                   |
| ---------------------- | -------------------------------------------------------- |
| **Nom**                | Inter                                                    |
| **Createur**           | Rasmus Andersson                                         |
| **Licence**            | Open Font License                                        |
| **Graisses utilisees** | Regular (400), Medium (500), Semi-Bold (600), Bold (700) |
| **Source**             | Google Fonts / bundles npm                               |

**Justification du choix** :

- Concue specifiquement pour les ecrans d'ordinateur avec une hauteur d'x optimisee
- Lisibilite exceptionnelle en petite taille (meta-donnees, labels, captions)
- Large eventail de graisses permettant une hierarchie fine sans changer de police
- Support de caracteres etendus (accents francais, caracteres africains)
- Chiffres tabulaires disponibles (important pour les tableaux de donnees/stats)
- Adoptee massivement par les produits SaaS B2B et les institutions (credibilite par association)

**Alternatives en cas de non-disponibilite** :

1. Source Sans 3 (Adobe, open source)
2. DM Sans (Google Fonts)
3. system-ui, -apple-system, sans-serif (system stack)

### Police monospace (usage limite) : JetBrains Mono

| Propriete              | Detail                                             |
| ---------------------- | -------------------------------------------------- |
| **Nom**                | JetBrains Mono                                     |
| **Licence**            | Open Font License                                  |
| **Graisses utilisees** | Regular (400) uniquement                           |
| **Usage**              | References de dossiers, codes, elements techniques |

**Justification** : Si le site doit afficher des references de cas, des identifiants de rapport ou des elements techniques, une police monospace ajoute une couche de credibilite "investigative".

## 3. Echelle typographique

L'echelle suit un ratio de **1.25** (Major Third) qui produit une progression harmonieuse adaptee aux longs contenus textuels du site.

### Desktop (>= 1024px)

| Element        | Taille           | Hauteur de ligne | Graisse | Police           | Espacement lettres |
| -------------- | ---------------- | ---------------- | ------- | ---------------- | ------------------ |
| **Hero Title** | 56px / 3.5rem    | 1.1              | 400     | DM Serif Display | -0.02em            |
| **H1**         | 44px / 2.75rem   | 1.15             | 400     | DM Serif Display | -0.01em            |
| **H2**         | 36px / 2.25rem   | 1.2              | 400     | DM Serif Display | -0.01em            |
| **H3**         | 28px / 1.75rem   | 1.3              | 600     | Inter            | 0                  |
| **H4**         | 22px / 1.375rem  | 1.35             | 600     | Inter            | 0                  |
| **H5**         | 18px / 1.125rem  | 1.4              | 600     | Inter            | 0.01em             |
| **H6**         | 16px / 1rem      | 1.5              | 700     | Inter            | 0.04em             |
| **Body Large** | 20px / 1.25rem   | 1.6              | 400     | Inter            | 0                  |
| **Body**       | 17px / 1.0625rem | 1.7              | 400     | Inter            | 0                  |
| **Body Small** | 15px / 0.9375rem | 1.6              | 400     | Inter            | 0.01em             |
| **Caption**    | 13px / 0.8125rem | 1.5              | 500     | Inter            | 0.02em             |
| **Overline**   | 12px / 0.75rem   | 1.5              | 600     | Inter            | 0.08em             |
| **Button**     | 15px / 0.9375rem | 1                | 600     | Inter            | 0.03em             |

### Mobile (<= 639px)

| Element        | Taille           | Hauteur de ligne |
| -------------- | ---------------- | ---------------- |
| **Hero Title** | 36px / 2.25rem   | 1.15             |
| **H1**         | 32px / 2rem      | 1.2              |
| **H2**         | 26px / 1.625rem  | 1.25             |
| **H3**         | 22px / 1.375rem  | 1.3              |
| **H4**         | 19px / 1.1875rem | 1.35             |
| **Body Large** | 18px / 1.125rem  | 1.6              |
| **Body**       | 16px / 1rem      | 1.7              |

## 4. Regles d'utilisation

### Titres (DM Serif Display)

- **Toujours en Regular (400)** : ne jamais utiliser de bold artificiel sur DM Serif Display
- **Casse** : Sentence case pour les titres longs, Title Case pour les titres courts (3-5 mots)
- **Couleur sur fond clair** : `#0A0F1A` (Near Black)
- **Couleur sur fond sombre** : `#FFFFFF` (White Pure)
- **Longueur maximale** : Les titres ne doivent pas depasser 2 lignes en desktop. Si c'est le cas, reduire ou reformuler.
- **Usage de l'italique** : Reserve aux citations et aux titres d'articles/insights

### Corps de texte (Inter)

- **Taille minimale** : 16px en toute circonstance (accessibilite)
- **Longueur de ligne optimale** : 60-75 caracteres par ligne (environ 600-700px de large)
- **Espacement entre paragraphes** : 1em (egale a la taille du texte)
- **Couleur sur fond clair** : `#3D4F63` (Dark Gray) pour le corps, `#0A0F1A` pour les elements importants
- **Couleur sur fond sombre** : `#FFFFFF` a 90% d'opacite pour le corps, `#FFFFFF` 100% pour les elements importants

### Texte en majuscules (Overline)

- Usage reserve aux **labels de section**, **categories**, **badges**
- Toujours avec letter-spacing augmente (`0.08em` minimum)
- Toujours en Inter Semi-Bold ou Bold
- Taille maximale : 14px. Ne jamais utiliser de grandes capitales pour les titres.
- Exemple : `OUR SERVICES`, `CASE STUDY`, `SOUTHERN AFRICA`

### Listes

- Puce : tiret em (--) ou bullet point standard
- Espacement entre items : 8px
- Indentation : 24px
- Police : meme que le corps de texte environnant

## 5. Combinaisons typographiques cles

### Hero de page d'accueil

```
Overline :    "CROSS-BORDER INTELLIGENCE" - Inter 600, 12px, #D4A017, tracking 0.08em
Titre :       "Know Who You're Dealing With." - DM Serif Display 400, 56px, #FFFFFF
Sous-titre :  "We help organisations investigate the people..." - Inter 400, 20px, #FFFFFF/90%
Bouton :      "Request an Intelligence Consultation" - Inter 600, 15px, tracking 0.03em
```

### Titre de section (fond clair)

```
Overline :    "OUR SERVICES" - Inter 600, 12px, #D4A017, tracking 0.08em
Titre :       "Intelligence for High-Stakes Decisions" - DM Serif Display 400, 36px, #0A0F1A
Paragraphe :  "Business decisions often depend on trust..." - Inter 400, 17px, #3D4F63
```

### Carte de service

```
Icone :       24x24px, #1E3A6E
Titre :       "Human Risk Intelligence" - Inter 600, 22px, #0A0F1A
Description : "Understand the people you are considering..." - Inter 400, 15px, #3D4F63
Lien :        "Learn More" - Inter 600, 15px, #1E3A6E
```

## 6. Chargement et performance

### Strategie de chargement des polices

```html
<!-- Preconnexion aux serveurs de polices -->
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />

<!-- Chargement optimise : uniquement les graisses necessaires -->
<link
  href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=Inter:wght@400;500;600;700&display=swap"
  rel="stylesheet"
/>
```

### Font-display strategy

- `font-display: swap` pour les deux polices
- Cela signifie que le texte s'affiche immediatement en police systeme, puis bascule quand la police custom est chargee
- Le "flash" est acceptable et preferable a un texte invisible

### Stack de fallback

```css
:root {
  --font-heading: "DM Serif Display", Georgia, "Times New Roman", serif;
  --font-body: "Inter", system-ui, -apple-system, "Segoe UI", sans-serif;
  --font-mono: "JetBrains Mono", "Fira Code", "Courier New", monospace;
}
```

## 7. Variables CSS / SCSS

```scss
// Typographie - Variables SCSS
$font-heading: "DM Serif Display", Georgia, "Times New Roman", serif;
$font-body:
  "Inter",
  system-ui,
  -apple-system,
  "Segoe UI",
  sans-serif;
$font-mono: "JetBrains Mono", "Fira Code", "Courier New", monospace;

// Echelle typographique
$text-hero: 3.5rem; // 56px
$text-h1: 2.75rem; // 44px
$text-h2: 2.25rem; // 36px
$text-h3: 1.75rem; // 28px
$text-h4: 1.375rem; // 22px
$text-h5: 1.125rem; // 18px
$text-h6: 1rem; // 16px
$text-body-lg: 1.25rem; // 20px
$text-body: 1.0625rem; // 17px
$text-body-sm: 0.9375rem; // 15px
$text-caption: 0.8125rem; // 13px
$text-overline: 0.75rem; // 12px

// Graisses
$font-regular: 400;
$font-medium: 500;
$font-semibold: 600;
$font-bold: 700;
```
