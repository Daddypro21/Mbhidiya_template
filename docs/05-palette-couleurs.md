# 05 - Palette de Couleurs - Guide Approfondi

## 1. Origine et logique de la palette

La palette de Mbhidiya Intelligence n'est pas arbitraire. Elle decoule directement de deux sources :

1. **Le logo existant** : qui etablit les couleurs de reference (rouge, vert, or, bleu marine)
2. **Le positionnement de marque** : intelligence B2B, high-stakes, corridor Canada-Afrique

### Pourquoi le bleu marine comme couleur dominante du site (et non les couleurs panafricaines)

Les couleurs panafricaines du logo (rouge, vert, or) sont essentielles a l'identite de la marque, mais elles ne doivent pas dominer l'interface web pour trois raisons :

- **Credibilite corporate** : la clientele cible (fonds d'investissement, cabinets d'avocats, institutions financieres) attend un design qui evoque la confiance et la sobriete. Le bleu marine est la couleur la plus universellement associee a la confiance, la securite et l'autorite dans le monde des affaires.
- **Lisibilite** : un site domine par du rouge, vert et or serait visuellement agressif et fatigant a lire. Le navy fournit une base calme et profonde.
- **Differenciation** : beaucoup de sites "africains" utilisent les couleurs panafricaines de maniere saturee. En les utilisant comme accents strategiques sur une base navy, Mbhidiya se distingue et projette un professionnalisme superieur.

Les couleurs panafricaines interviennent comme des **accents chirurgicaux** : elles rappellent l'ancrage africain sans le rendre "folklorique".

## 2. Palette complete

### 2.1 Couleurs primaires

#### Navy Depth (couleur dominante)

```
HEX: #0C1B3A
RGB: 12, 27, 58
HSL: 220, 66%, 14%
```

- **Utilisation** : background de hero, header, footer, sections d'impact, texte titre sur fond clair
- **Frequence** : presente sur 30-40% de la surface visible
- **Psychologie** : profondeur, autorite, mystere, confiance

#### Navy Medium

```
HEX: #1A3158
RGB: 26, 49, 88
HSL: 218, 54%, 22%
```

- **Utilisation** : backgrounds secondaires navy, cartes sur fond sombre, hover states sombres
- **Frequence** : 10-15% de la surface

#### Intelligence Blue

```
HEX: #1E3A6E
RGB: 30, 58, 110
HSL: 219, 57%, 27%
```

- **Utilisation** : liens, boutons secondaires, bordures actives, icones, elements interactifs
- **Frequence** : 5-10% de la surface

### 2.2 Couleurs d'accent

#### Signal Red

```
HEX: #C0392B
RGB: 192, 57, 43
HSL: 6, 63%, 46%
```

- **Utilisation** : badges d'alerte, indicateurs de risque, elements d'attention
- **Frequence** : < 3% de la surface. C'est un accent, jamais un fond de section.
- **Interdit sur** : boutons principaux, backgrounds larges, texte courant
- **Contraste** : Ratio 5.9:1 sur fond blanc (AA pour texte large)

#### Integrity Green

```
HEX: #1D7A47
RGB: 29, 122, 71
HSL: 147, 62%, 30%
```

- **Utilisation** : etapes completees dans un processus, indicateurs positifs, validation, icones de confiance
- **Frequence** : < 3%
- **Contraste** : Ratio 4.8:1 sur fond blanc (AA pour texte large)

#### Insight Gold

```
HEX: #D4A017
RGB: 212, 160, 23
HSL: 44, 80%, 46%
```

- **Utilisation** : overlines de section, trait decoratif sous les titres, badges premium, focus states
- **Frequence** : < 5%
- **Attention** : Le gold a un contraste faible sur fond blanc (ratio 2.1:1). Ne jamais l'utiliser pour du texte sur fond clair. Sur fond navy, le ratio est de 6.3:1 (acceptable).

### 2.3 Couleurs neutres

#### White Pure

```
HEX: #FFFFFF
RGB: 255, 255, 255
```

- Fond principal, texte sur fond sombre

#### Off-White

```
HEX: #F7F8FA
RGB: 247, 248, 250
```

- Fond alterne des sections, fond de cartes

#### Light Gray

```
HEX: #E8ECF1
RGB: 232, 236, 241
```

- Bordures, separateurs, fond de champs de formulaire

#### Mid Gray

```
HEX: #8896A7
RGB: 136, 150, 167
```

- Texte tertiaire, placeholders, icones desactivees

#### Dark Gray

```
HEX: #3D4F63
RGB: 61, 79, 99
```

- Texte de corps principal sur fond clair

#### Near Black

```
HEX: #0A0F1A
RGB: 10, 15, 26
```

- Titres sur fond clair, footer background

## 3. Combinaisons validees (avec ratios de contraste)

### Fond clair

| Texte                       | Fond                  | Ratio  | Verdict                               |
| --------------------------- | --------------------- | ------ | ------------------------------------- |
| Near Black sur White        | `#0A0F1A` / `#FFFFFF` | 18.5:1 | AAA                                   |
| Dark Gray sur White         | `#3D4F63` / `#FFFFFF` | 7.6:1  | AAA                                   |
| Dark Gray sur Off-White     | `#3D4F63` / `#F7F8FA` | 7.2:1  | AAA                                   |
| Intelligence Blue sur White | `#1E3A6E` / `#FFFFFF` | 9.4:1  | AAA                                   |
| Signal Red sur White        | `#C0392B` / `#FFFFFF` | 5.9:1  | AA                                    |
| Integrity Green sur White   | `#1D7A47` / `#FFFFFF` | 4.8:1  | AA (large text)                       |
| Insight Gold sur White      | `#D4A017` / `#FFFFFF` | 2.1:1  | ECHEC - ne pas utiliser pour du texte |
| Mid Gray sur White          | `#8896A7` / `#FFFFFF` | 3.4:1  | AA (large text only)                  |

### Fond sombre (Navy)

| Texte                       | Fond                                | Ratio  | Verdict |
| --------------------------- | ----------------------------------- | ------ | ------- |
| White sur Navy Depth        | `#FFFFFF` / `#0C1B3A`               | 15.8:1 | AAA     |
| White 90% sur Navy Depth    | `rgba(255,255,255,0.9)` / `#0C1B3A` | ~13:1  | AAA     |
| Insight Gold sur Navy Depth | `#D4A017` / `#0C1B3A`               | 6.3:1  | AA      |
| Light Gray sur Navy Depth   | `#E8ECF1` / `#0C1B3A`               | 12.1:1 | AAA     |

### Combinaisons interdites

| Combinaison            | Raison                                |
| ---------------------- | ------------------------------------- |
| Gold sur White         | Contraste insuffisant (2.1:1)         |
| Mid Gray sur Off-White | Contraste insuffisant (3.2:1)         |
| Signal Red sur Navy    | Contraste insuffisant et clash visuel |
| Green sur Red          | Inaccessible pour daltoniens          |

## 4. Application par composant

### Navigation (header)

| Element                      | Couleur                         |
| ---------------------------- | ------------------------------- |
| Fond                         | `#0C1B3A` (Navy Depth)          |
| Liens inactifs               | `#FFFFFF` a 80%                 |
| Lien actif                   | `#FFFFFF` 100%                  |
| Indicateur actif (underline) | `#D4A017` (Insight Gold)        |
| Bouton CTA header            | Fond `#D4A017`, texte `#0C1B3A` |

### Hero sections

| Element           | Couleur                            |
| ----------------- | ---------------------------------- |
| Fond              | Gradient `#0C1B3A` vers `#1A3158`  |
| Overline          | `#D4A017`                          |
| Titre             | `#FFFFFF`                          |
| Sous-titre        | `#FFFFFF` a 90%                    |
| Bouton primaire   | Fond `#D4A017`, texte `#0C1B3A`    |
| Bouton secondaire | Bordure `#FFFFFF`, texte `#FFFFFF` |

### Cartes de services (fond clair)

| Element         | Couleur         |
| --------------- | --------------- |
| Fond carte      | `#FFFFFF`       |
| Bordure         | `#E8ECF1`       |
| Icone           | `#1E3A6E`       |
| Titre           | `#0A0F1A`       |
| Description     | `#3D4F63`       |
| Lien            | `#1E3A6E`       |
| Hover : fond    | `#F7F8FA`       |
| Hover : bordure | `#1E3A6E` a 30% |

### Formulaire de contact

| Element             | Couleur                         |
| ------------------- | ------------------------------- |
| Label               | `#0A0F1A`                       |
| Champ fond          | `#F7F8FA`                       |
| Champ bordure       | `#E8ECF1`                       |
| Champ bordure focus | `#1E3A6E`                       |
| Champ outline focus | `#D4A017` a 30% (glow)          |
| Placeholder         | `#8896A7`                       |
| Bouton submit       | Fond `#0C1B3A`, texte `#FFFFFF` |
| Bouton submit hover | Fond `#1A3158`                  |
| Message d'erreur    | `#C0392B`                       |
| Message de succes   | `#1D7A47`                       |

### Footer

| Element            | Couleur         |
| ------------------ | --------------- |
| Fond               | `#0A0F1A`       |
| Titres de colonnes | `#FFFFFF`       |
| Liens              | `#FFFFFF` a 70% |
| Liens hover        | `#FFFFFF` 100%  |
| Separateur         | `#FFFFFF` a 10% |
| Copyright          | `#8896A7`       |

## 5. Mode sombre

Le site Mbhidiya Intelligence etant deja a dominante sombre dans ses sections cles (hero, header, footer, sections d'impact), un mode sombre complet n'est pas prioritaire pour la V1. Les sections sur fond clair offrent le contraste et le repos visuel necessaire.

Si un mode sombre est implemente ulterieurement :

| Element         | Mode clair | Mode sombre     |
| --------------- | ---------- | --------------- |
| Fond principal  | `#FFFFFF`  | `#0A0F1A`       |
| Fond secondaire | `#F7F8FA`  | `#0C1B3A`       |
| Texte principal | `#3D4F63`  | `#E8ECF1`       |
| Texte titre     | `#0A0F1A`  | `#FFFFFF`       |
| Cartes          | `#FFFFFF`  | `#1A3158`       |
| Bordures        | `#E8ECF1`  | `#1E3A6E` a 30% |

## 6. Variables CSS

```css
:root {
  /* Primaires */
  --color-navy-depth: #0c1b3a;
  --color-navy-medium: #1a3158;
  --color-intelligence-blue: #1e3a6e;

  /* Accents */
  --color-signal-red: #c0392b;
  --color-integrity-green: #1d7a47;
  --color-insight-gold: #d4a017;

  /* Neutres */
  --color-white: #ffffff;
  --color-off-white: #f7f8fa;
  --color-light-gray: #e8ecf1;
  --color-mid-gray: #8896a7;
  --color-dark-gray: #3d4f63;
  --color-near-black: #0a0f1a;

  /* Semantiques */
  --color-text-primary: var(--color-dark-gray);
  --color-text-heading: var(--color-near-black);
  --color-text-secondary: var(--color-mid-gray);
  --color-text-on-dark: var(--color-white);
  --color-bg-primary: var(--color-white);
  --color-bg-secondary: var(--color-off-white);
  --color-bg-dark: var(--color-navy-depth);
  --color-border: var(--color-light-gray);
  --color-link: var(--color-intelligence-blue);
  --color-focus: var(--color-insight-gold);
  --color-error: var(--color-signal-red);
  --color-success: var(--color-integrity-green);
}
```
