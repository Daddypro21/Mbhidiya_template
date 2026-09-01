# 06 - Systeme de Composants UI

## 1. Principes de conception des composants

Chaque composant du design system de Mbhidiya suit ces regles :

- **Sobre par defaut** : un composant au repos doit etre discret. L'interaction (hover, focus) revele plus de detail.
- **Fonctionnel d'abord** : aucun composant purement decoratif. Chaque element a une raison d'etre.
- **Coherent** : memes espacements, memes couleurs, memes border-radius partout.

## 2. Boutons

### Bouton primaire (CTA principal)

```
Fond :          #0C1B3A (Navy Depth)
Texte :         #FFFFFF
Police :        Inter Semi-Bold 600, 15px
Letter-spacing: 0.03em
Padding :       14px 32px
Border-radius : 6px
Transition :    background 200ms ease-out

Hover :         Fond #1A3158 (Navy Medium)
Active :        Fond #0C1B3A + translateY(1px)
Focus :         Outline #D4A017 2px, offset 2px
Disabled :      Opacity 0.5, cursor not-allowed
```

### Bouton primaire Gold (CTA premium - usage rare)

```
Fond :          #D4A017 (Insight Gold)
Texte :         #0C1B3A (Navy Depth)
Padding :       14px 32px
Border-radius : 6px

Hover :         Fond #E8B830
Focus :         Outline #0C1B3A 2px
```

Usage reserve au CTA principal du hero et au bouton "Request a Consultation" dans le header. Maximum 1-2 par page.

### Bouton secondaire (outline)

```
Fond :          transparent
Bordure :       1.5px solid #0C1B3A
Texte :         #0C1B3A
Padding :       14px 32px
Border-radius : 6px

Hover :         Fond #0C1B3A, Texte #FFFFFF
```

### Bouton secondaire sur fond sombre

```
Fond :          transparent
Bordure :       1.5px solid #FFFFFF
Texte :         #FFFFFF
Padding :       14px 32px

Hover :         Fond #FFFFFF, Texte #0C1B3A
```

### Bouton texte (lien stylise)

```
Fond :          transparent
Texte :         #1E3A6E (Intelligence Blue)
Police :        Inter Semi-Bold 600, 15px
Padding :       0
Decoration :    none

Hover :         Underline, couleur #0C1B3A
```

Accompagne d'une fleche droite (svg inline) qui se decale de 4px vers la droite au hover.

### Tailles de boutons

| Taille | Padding | Font-size |
|---|---|---|
| **Small** | 10px 20px | 13px |
| **Medium (defaut)** | 14px 32px | 15px |
| **Large** | 18px 40px | 17px |

## 3. Cartes

### Carte de service

```
Fond :          #FFFFFF
Bordure :       1px solid #E8ECF1
Border-radius : 8px
Padding :       32px
Shadow :        0 1px 3px rgba(12,27,58,0.08)
Cursor :        pointer
Position :      relative (la carte entiere est cliquable via un lien en ::after)

Hover :
  Shadow :      0 4px 12px rgba(12,27,58,0.12)
  Border :      1px solid rgba(30,58,110,0.3)
  Transform :   translateY(-2px)
  Transition :  all 200ms ease-out

Structure interne :
  [Icone] .......... 24x24px, couleur #1E3A6E, margin-bottom 16px
  [Titre] .......... Inter SemiBold 600, 22px, #0A0F1A, margin-bottom 12px
  [Description] .... Inter Regular 400, 15px, #3D4F63, margin-bottom 20px, max 3 lignes
  [Lien] ........... Inter SemiBold 600, 15px, #1E3A6E + fleche
                     Le lien utilise un pseudo-element ::after en position absolute
                     couvrant toute la carte (Loi de Fitts : zone cliquable maximale)
```

### Carte de secteur

```
Fond :          #F7F8FA
Bordure :       none
Border-radius : 8px
Padding :       24px

Structure interne :
  [Titre secteur] .. Inter Bold 700, 18px, #0A0F1A
  [Liste items] .... Bullet list, Inter 400, 15px, #3D4F63
```

### Carte equipe (membre)

```
Fond :          #FFFFFF
Border-radius : 8px
Shadow :        0 1px 3px rgba(12,27,58,0.08)
Overflow :      hidden

Structure interne :
  [Photo] .......... Ratio 4:5, object-fit cover, border-radius 8px 8px 0 0
  [Padding zone] ... 24px
    [Nom] .......... Inter Bold 700, 18px, #0A0F1A
    [Poste] ........ Inter Regular 400, 14px, #8896A7
    [Bio truncated]  Inter Regular 400, 15px, #3D4F63, max 3 lignes + "Lire plus"
```

### Carte insight / article

```
Fond :          #FFFFFF
Border-radius : 8px
Shadow :        0 1px 3px rgba(12,27,58,0.08)

Structure interne :
  [Image] .......... Ratio 16:9, overlay #0C1B3A a 5%
  [Category badge]   Overline style, #D4A017
  [Titre] .......... DM Serif Display 400, 22px, #0A0F1A
  [Excerpt] ........ Inter 400, 15px, #3D4F63, 2 lignes max
  [Date] ........... Inter 400, 13px, #8896A7
```

## 4. Navigation

### Header (desktop)

```
Position :      fixed, top 0
Fond :          #0C1B3A (opaque au scroll, transparent en haut de page avec gradient)
Hauteur :       80px
Padding :       0 80px
Z-index :       1000
Transition :    background 300ms ease

Structure :
  [Logo] ......................... Gauche, hauteur 40px
  [Navigation links] ............ Centre, Inter Medium 500, 15px, #FFFFFF/80%
    Lien actif :                  #FFFFFF 100% + underline #D4A017 2px, offset 8px
    Lien hover :                  #FFFFFF 100%
    Espacement entre liens :      32px
  [CTA Button] .................. Droite, style bouton Gold
```

### Menu mobile

```
Trigger :       Icone hamburger (3 lignes), 24px, #FFFFFF
Overlay :       Fond #0C1B3A, plein ecran, z-index 2000
Animation :     Slide from right, 300ms ease
Fermeture :     Icone X, 24px, #FFFFFF, coin superieur droit

Liens :         Inter Medium 500, 24px, #FFFFFF, espacement vertical 24px
CTA :           Bouton Gold, pleine largeur, en bas du menu
```

### Breadcrumb

```
Police :        Inter Regular 400, 13px
Couleur :       #8896A7
Separateur :    "/"  ou chevron droit, #E8ECF1
Lien hover :    #1E3A6E
Element actif : #3D4F63, non cliquable
```

## 5. Sections de page

### Hero section (page d'accueil)

```
Hauteur :       100vh (min 600px, max 900px)
Fond :          Image + overlay gradient
                linear-gradient(135deg, rgba(12,27,58,0.85) 0%, rgba(12,27,58,0.6) 50%, rgba(12,27,58,0.4) 100%)
Padding :       vertical 128px, horizontal 80px
Contenu :       Aligne a gauche, max-width 700px

Elements :
  [Overline]          12px, Inter 600, #D4A017, tracking 0.08em, uppercase
  [Titre principal]   56px, DM Serif Display, #FFFFFF, margin-top 16px
  [Sous-titre]        20px, Inter 400, #FFFFFF/90%, margin-top 24px, max-width 600px
  [Boutons]           margin-top 40px, gap 16px
    - Primaire Gold
    - Secondaire outline blanc
```

### Section standard (fond clair)

```
Padding :       96px 80px (desktop), 64px 20px (mobile)
Max-width :     1200px, centre
Background :    #FFFFFF

Elements :
  [Overline]    Centre, #D4A017
  [Titre H2]    Centre, DM Serif Display, max-width 800px
  [Sous-titre]  Centre, Inter 400, 17px, #3D4F63, max-width 700px
  [Contenu]     margin-top 64px
```

### Section fond sombre (mise en avant)

```
Padding :       96px 80px
Background :    #0C1B3A
Fond decoratif: Network lines a 5-10% opacite

Texte :         #FFFFFF pour titres, #FFFFFF/80% pour corps
Accent :        #D4A017 pour overlines et elements de mise en avant
```

### Section statistiques / chiffres cles

```
Layout :        Grid 3 ou 4 colonnes, gap 32px
Fond :          #0C1B3A
Padding :       80px

Chaque stat :
  [Chiffre]     DM Serif Display 400, 48px, #D4A017
  [Label]       Inter 500, 15px, #FFFFFF/80%, uppercase, tracking 0.04em
  [Separateur]  Ligne verticale #FFFFFF/10% entre les stats
```

## 6. Formulaire de contact

### Structure

```
Layout :        2 colonnes sur desktop (infos + formulaire), 1 colonne mobile
Fond section :  #F7F8FA ou #0C1B3A (selon la page)

Colonne gauche (infos) :
  [Titre]       DM Serif Display, 36px
  [Description] Inter 400, 17px
  [Contact channels] Liste avec icones

Colonne droite (formulaire) :
  Fond carte :  #FFFFFF, padding 40px, border-radius 8px, shadow elevation 2
```

### Champs de formulaire

```
Hauteur :       48px (input), 120px (textarea)
Fond :          #F7F8FA
Bordure :       1px solid #E8ECF1
Border-radius : 6px
Padding :       12px 16px
Police :        Inter 400, 16px, #0A0F1A

Focus :
  Bordure :     1px solid #1E3A6E
  Box-shadow :  0 0 0 3px rgba(212,160,23,0.15)
  Outline :     none

Erreur :
  Bordure :     1px solid #C0392B
  Message :     Inter 400, 13px, #C0392B, margin-top 4px

Label :
  Police :      Inter Medium 500, 14px, #0A0F1A
  Margin-bottom: 6px
  Position :    Au-dessus du champ (jamais en placeholder-only)
```

### Champs requis

- Nom : text, required
- Organisation : text, required
- Email : email, required
- Pays : select (dropdown), required
- Message : textarea, required, placeholder "How can we help?"

## 7. Footer

```
Fond :          #0A0F1A
Padding :       80px 80px 32px

Layout :        4 colonnes (desktop), 2 colonnes (tablette), 1 colonne (mobile)

Colonne 1 :    Logo (version blanche) + tagline courte + valeurs (Discretion - Loyalty - Precision)
Colonne 2 :    Services (liens vers les 11 pages de services)
Colonne 3 :    Company (About, Process, Sectors, Why Us, Insights)
Colonne 4 :    Contact (email, formulaire, LinkedIn)

Separateur :    1px solid rgba(255,255,255,0.1), margin 32px 0

Bas de page :   Copyright + mentions legales + politique de confidentialite
                Inter 400, 13px, #8896A7
```

## 8. Elements speciaux

### Timeline du processus (page Process)

```
Layout :        Horizontal sur desktop, vertical sur mobile
6 etapes connectees par une ligne

Chaque etape :
  [Numero]      Cercle 48px, fond #0C1B3A, texte #D4A017, DM Serif Display
  [Titre]       Inter SemiBold 600, 18px, #0A0F1A
  [Description] Inter 400, 15px, #3D4F63

Ligne de connexion :
  2px solid #E8ECF1 entre les cercles
  Segment actif/passe : 2px solid #1E3A6E
```

### Carte geographique (page Markets)

```
Type :          SVG stylisee (pas Google Maps)
Couleurs :
  Pays couverts :    Fill #1E3A6E
  Pays non couverts: Fill #E8ECF1
  Hover pays :       Fill #D4A017
  Canada :           Fill #1E3A6E
  Ligne de connexion Canada-Afrique : Dotted #D4A017

Tooltip au hover :   Nom du pays + region, fond #0C1B3A, texte #FFFFFF
```

### Accordion (FAQ / details de services)

```
Fond :          transparent
Bordure :       1px solid #E8ECF1 (bottom only)
Padding :       20px 0

Titre :
  Inter SemiBold 600, 17px, #0A0F1A
  Icone chevron droite, rotation 90deg au clic

Contenu :
  Inter 400, 15px, #3D4F63
  Padding-top 16px
  Animation : slideDown 250ms ease
```

### Badge de region

```
Display :       inline-flex
Fond :          #F7F8FA
Bordure :       1px solid #E8ECF1
Border-radius : 4px
Padding :       4px 12px
Police :        Inter Medium 500, 13px, #3D4F63, uppercase, tracking 0.04em

Hover :         Fond #0C1B3A, Texte #FFFFFF, Bordure #0C1B3A
```

## 9. Etats des composants

Tous les composants interactifs doivent gerer ces 5 etats :

| Etat | Description | Retour visuel |
|---|---|---|
| **Default** | Etat au repos | Style de base |
| **Hover** | Survol souris | Changement de couleur/ombre subtil |
| **Focus** | Navigation clavier | Outline gold `#D4A017` 2px, offset 2px |
| **Active** | Clic en cours | Legere depression (translateY +1px) |
| **Disabled** | Non disponible | Opacite 50%, cursor not-allowed |
