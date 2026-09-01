# 02 - Charte Graphique

## 1. Philosophie de la charte

La charte graphique de Mbhidiya Intelligence doit vehiculer trois qualites fondamentales :

1. **Autorite** : Mbhidiya opere dans un domaine ou la credibilite est non negociable. Chaque choix graphique doit inspirer une confiance immediate.
2. **Precision** : L'intelligence economique repose sur l'exactitude. Le design doit refleter cette rigueur par des alignements parfaits, des espacements controles et une hierarchie claire.
3. **Profondeur** : L'activite de Mbhidiya consiste a reveler ce qui est cache sous la surface. Le design doit evoquer des couches d'information, de la profondeur, des connexions.

## 2. Logo

### Description

Le logo de Mbhidiya Intelligence se compose de deux elements :

**Symbole (pictogramme)** :

- Trois arcs concentriques dans les couleurs panafricaines : rouge (exterieur), vert (intermediaire), or/jaune (interieur)
- Un element central en bleu marine representant un oeil orbital / vortex de connexions
- Symbolisme : les arcs representent les couches d'investigation (du visible vers le cache), l'oeil orbital represente la capacite d'observation et d'analyse

**Logotype** :

- "Mbhidiya" en typographie serif bold de style didone/moderne
- "INTELLIGENCE" en capitales espacees (tracking large), typographie sans-serif light

### Zones de protection

La zone de protection minimale autour du logo est egale a la hauteur du "M" de Mbhidiya sur tous les cotes. Aucun element graphique ou textuel ne doit penetrer cette zone.

### Tailles minimales

| Support     | Taille minimale (largeur) |
| ----------- | ------------------------- |
| Ecran (web) | 120px                     |
| Print       | 30mm                      |
| Favicon     | 32x32px (symbole seul)    |

### Versions du logo

| Version                     | Usage                                        |
| --------------------------- | -------------------------------------------- |
| **Complet couleur**         | Usage principal sur fond blanc/clair         |
| **Complet sur fond sombre** | Logo avec texte blanc sur fonds navy/sombres |
| **Symbole seul**            | Favicon, icone d'app, reseaux sociaux        |
| **Monochrome blanc**        | Impression monochrome, watermarks            |
| **Monochrome noir**         | Impression N&B, fax, documents juridiques    |

### Interdictions

- Ne jamais etirer ou deformer le logo
- Ne jamais modifier les couleurs des arcs
- Ne jamais placer le logo sur un fond visuellement charge sans overlay
- Ne jamais ajouter d'effets (ombre, biseautage, lueur)
- Ne jamais reorganiser les elements du logo

## 3. Palette de couleurs

### Couleurs primaires (derivees du logo)

| Nom                   | Hex       | RGB         | Usage principal                                                                       |
| --------------------- | --------- | ----------- | ------------------------------------------------------------------------------------- |
| **Navy Depth**        | `#0C1B3A` | 12, 27, 58  | Couleur dominante du site : headers, footers, fonds de sections cles, texte principal |
| **Navy Medium**       | `#1A3158` | 26, 49, 88  | Variante pour cartes, backgrounds alternes, hover states                              |
| **Intelligence Blue** | `#1E3A6E` | 30, 58, 110 | CTAs secondaires, liens, bordures actives                                             |

### Couleurs d'accent (panafricaines du logo)

| Nom                 | Hex       | RGB          | Usage principal                                                                              |
| ------------------- | --------- | ------------ | -------------------------------------------------------------------------------------------- |
| **Signal Red**      | `#C0392B` | 192, 57, 43  | Accents strategiques (risque, alertes, elements d'attention). Usage modere : jamais dominant |
| **Integrity Green** | `#1D7A47` | 29, 122, 71  | Accents positifs (validation, confiance, etapes de processus)                                |
| **Insight Gold**    | `#D4A017` | 212, 160, 23 | Accents premium (highlights, badges, elements distinctifs)                                   |

### Couleurs neutres

| Nom            | Hex       | RGB           | Usage                                                |
| -------------- | --------- | ------------- | ---------------------------------------------------- |
| **White Pure** | `#FFFFFF` | 255, 255, 255 | Fonds principaux, texte sur fonds sombres            |
| **Off-White**  | `#F7F8FA` | 247, 248, 250 | Fonds de sections alternees, backgrounds de cartes   |
| **Light Gray** | `#E8ECF1` | 232, 236, 241 | Bordures, separateurs, fonds de champs de formulaire |
| **Mid Gray**   | `#8896A7` | 136, 150, 167 | Texte secondaire, placeholders, icones inactives     |
| **Dark Gray**  | `#3D4F63` | 61, 79, 99    | Texte de corps sur fond clair                        |
| **Near Black** | `#0A0F1A` | 10, 15, 26    | Titres sur fond clair                                |

### Regles d'application des couleurs

**Ratio dominant : 70 / 20 / 10**

- **70% Navy + Neutres** : fonds, texte, structure
- **20% Intelligence Blue** : elements interactifs, navigation, cartes
- **10% Accents panafricains** : touches strategiques, jamais dominantes

**Contraste et accessibilite (WCAG 2.1 AA minimum)** :

- Texte sur fond blanc : utiliser `#0A0F1A` ou `#3D4F63` (ratio > 7:1)
- Texte sur fond Navy : utiliser `#FFFFFF` (ratio > 12:1)
- Liens : `#1E3A6E` sur fond clair (ratio > 4.5:1)
- Ne jamais placer du texte Signal Red sur fond Navy (contraste insuffisant)

### Gradients autorises

| Nom               | Definition                        | Usage                                     |
| ----------------- | --------------------------------- | ----------------------------------------- |
| **Navy Gradient** | `#0C1B3A` vers `#1A3158` (135deg) | Hero sections, header, footer             |
| **Subtle Light**  | `#FFFFFF` vers `#F7F8FA` (180deg) | Transitions entre sections sur fond clair |
| **Gold Shimmer**  | `#D4A017` vers `#E8B830` (90deg)  | Boutons premium (usage tres limite)       |

## 4. Typographie

_(Detaillee dans le document 04-typographie.md)_

**Resume rapide :**

- Titres : **DM Serif Display** (serif elegant, autorite)
- Corps : **Inter** (sans-serif, lisibilite maximale)
- Accent/Data : **JetBrains Mono** (monospace, pour elements techniques)

## 5. Iconographie

### Style

Les icones de Mbhidiya Intelligence suivent un style **outline** (contour fin) avec les specifications suivantes :

| Propriete                   | Valeur                        |
| --------------------------- | ----------------------------- |
| **Epaisseur du trait**      | 1.5px                         |
| **Coins**                   | Arrondis (2px radius)         |
| **Taille de reference**     | 24x24px                       |
| **Couleur par defaut**      | `#3D4F63` (Dark Gray)         |
| **Couleur sur fond sombre** | `#FFFFFF`                     |
| **Couleur hover**           | `#1E3A6E` (Intelligence Blue) |

### Bibliotheque recommandee

**Lucide Icons** (fork moderne de Feather Icons) : open-source, style coherent, excellent support Symfony/Twig.

### Icones cles par service

| Service                   | Icone suggeree   |
| ------------------------- | ---------------- |
| Human Risk Intelligence   | `user-search`    |
| Corporate Intelligence    | `building-2`     |
| Cross-Border Intelligence | `globe`          |
| Transaction Intelligence  | `handshake`      |
| Executive Vetting         | `shield-check`   |
| Reputation Intelligence   | `scan-eye`       |
| Network Intelligence      | `network`        |
| Market Entry              | `map-pin`        |
| Third-Party Intelligence  | `link-2`         |
| Fraud Intelligence        | `alert-triangle` |
| Continuous Monitoring     | `radar`          |

## 6. Photographie et imagerie

### Direction artistique

| Critere                  | Directive                                                                                                            |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------- |
| **Tonalite**             | Scenes professionnelles, sobres, eclairage naturel ou studio                                                         |
| **Sujets**               | Skylines urbaines (villes africaines et canadiennes), salles de reunion, documents, mains serrees, ecrans de donnees |
| **Traitement**           | Leger filtre desature navy (overlay `#0C1B3A` a 15-25% d'opacite) pour uniformiser                                   |
| **Ce qu'il faut eviter** | Photos generiques de "happy business people", images de cadenas/serrures (trop cliche securite), drapeaux            |
| **Diversite**            | Representation equilibree Canada-Afrique, diversite des profils                                                      |

### Elements graphiques abstraits

Pour les sections ou la photographie n'est pas appropriee (ex: services, processus), utiliser :

- **Lignes de connexion** : fines lignes `#1E3A6E` a 20% d'opacite, evoquant des reseaux
- **Points nodaux** : petits cercles aux intersections, rappelant l'element orbital du logo
- **Couches de profondeur** : formes geometriques superposees avec opacite variable

## 7. Grille et espacements

### Grille de mise en page

| Propriete                  | Valeur                                         |
| -------------------------- | ---------------------------------------------- |
| **Colonnes**               | 12 colonnes                                    |
| **Gouttiere**              | 24px (desktop), 16px (mobile)                  |
| **Marge exterieure**       | 80px (desktop), 48px (tablette), 20px (mobile) |
| **Largeur max de contenu** | 1200px                                         |

### Systeme d'espacement (base 8)

| Token       | Valeur | Usage typique                             |
| ----------- | ------ | ----------------------------------------- |
| `space-xs`  | 4px    | Micro-espacement (icone-texte)            |
| `space-sm`  | 8px    | Espacement interne compact                |
| `space-md`  | 16px   | Espacement standard entre elements        |
| `space-lg`  | 24px   | Espacement entre groupes d'elements       |
| `space-xl`  | 32px   | Espacement entre composants               |
| `space-2xl` | 48px   | Espacement entre blocs de contenu         |
| `space-3xl` | 64px   | Espacement entre sections                 |
| `space-4xl` | 96px   | Espacement hero / sections majeures       |
| `space-5xl` | 128px  | Padding vertical des sections principales |

## 8. Ombres et elevations

| Niveau          | Valeur CSS                        | Usage                      |
| --------------- | --------------------------------- | -------------------------- |
| **Elevation 1** | `0 1px 3px rgba(12,27,58,0.08)`   | Cartes au repos            |
| **Elevation 2** | `0 4px 12px rgba(12,27,58,0.12)`  | Cartes au hover, dropdowns |
| **Elevation 3** | `0 8px 24px rgba(12,27,58,0.16)`  | Modales, popups            |
| **Elevation 4** | `0 16px 48px rgba(12,27,58,0.20)` | Elements flottants majeurs |

## 9. Bordures et arrondis

| Element              | Border-radius |
| -------------------- | ------------- |
| Boutons              | 6px           |
| Cartes               | 8px           |
| Champs de formulaire | 6px           |
| Badges / tags        | 4px           |
| Images (dans cartes) | 8px (top)     |
| Avatars              | 50% (cercle)  |
| Modales              | 12px          |

## 10. Animations et transitions

### Principes

- **Subtilite** : les animations doivent etre a peine perceptibles. Un site d'intelligence ne doit pas "danser".
- **Fonctionnalite** : chaque animation a un but (feedback, orientation, hierarchie). Aucune animation decorative.
- **Performance** : utiliser exclusivement `transform` et `opacity` pour rester sur le GPU.

### Durees

| Type                   | Duree | Easing                          |
| ---------------------- | ----- | ------------------------------- |
| Hover (boutons, liens) | 200ms | `ease-out`                      |
| Apparition d'elements  | 300ms | `ease-out`                      |
| Transitions de page    | 250ms | `ease-in-out`                   |
| Modales (ouverture)    | 300ms | `cubic-bezier(0.16, 1, 0.3, 1)` |
| Scroll reveal          | 500ms | `ease-out`                      |

### Scroll reveal

Les elements apparaissent avec un leger `translateY(20px)` vers `translateY(0)` avec fade-in. Declenchement a 15% de visibilite dans le viewport. Pas de stagger superieur a 100ms entre elements freres.

### Respect de prefers-reduced-motion

Toutes les animations doivent etre desactivees pour les utilisateurs qui ont active la reduction de mouvement dans leur systeme d'exploitation :

```css
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```

Cela concerne le parallax du hero, les scroll reveals, les transitions de carte et le header transparent/opaque.
