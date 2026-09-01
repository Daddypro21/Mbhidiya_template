# 09 - Principes UX et Strategie d'Experience Utilisateur

## 1. Vision UX

L'experience utilisateur du site Mbhidiya Intelligence doit vehiculer un sentiment unique :

> **"Je suis entre de bonnes mains. Ces gens sont serieux, discrets et competents."**

Chaque micro-interaction, chaque transition, chaque choix de layout doit renforcer cette perception. Le site n'est pas un e-commerce, ni un SaaS playful. C'est la vitrine digitale d'une firme qui manipule des informations sensibles pour des clients exigeants.

## 2. Les 7 principes UX fondamentaux

### Principe 1 : Confiance immediate

**Constat** : les clients potentiels de Mbhidiya grent des millions en capital, des decisions de recrutement critiques ou des partenariats strategiques. Ils ne confieront pas leurs besoins d'investigation a une entreprise dont le site ne les rassure pas en 5 secondes.

**Application** :

- Le hero doit immediatement communiquer ce que fait Mbhidiya, pour qui, et pourquoi c'est different
- Pas de slider, pas de video en autoplay, pas d'animation de chargement longue
- Le logo, les couleurs et la typographie doivent etre visibles instantanement
- Le design doit etre impeccable au pixel pres -- le moindre defaut d'alignement trahit un manque de rigueur

### Principe 2 : Progressivite de l'information

**Constat** : Mbhidiya a 11 services, couvre 25+ pays, sert 7 secteurs. Donner tout d'un coup submerge l'utilisateur.

**Application** :

- Page d'accueil : vue d'ensemble (6 services principaux, pas 11)
- Pages de services : detail complet de chaque service
- Mega-menu : organise en categories logiques, pas une liste plate de 11 items
- "Learn More" comme pattern de progressive disclosure sur les cartes
- Accordions pour les listes detaillees (pays par region, examens par service)

### Principe 3 : Friction minimale vers la conversion

**Constat** : l'objectif #1 du site est de generer des demandes de consultation confidentielle.

**Application** :

- Le CTA "Request a Consultation" est present :
  - Dans le header (toujours visible)
  - Dans le hero de chaque page
  - En bas de chaque page de service
  - Dans une section CTA dediee avant le footer
- Le formulaire est court : 5 champs maximum (Nom, Organisation, Email, Pays, Message)
- Pas de creation de compte, pas de CAPTCHA visible (utiliser un honeypot ou reCAPTCHA invisible)
- Le bouton de soumission indique clairement l'action : "Request a Confidential Consultation"
- Confirmation post-soumission : message clair ("Thank you. We will respond within 24 hours.") + pas de redirection vers une autre page

### Principe 4 : Autorite par la structure

**Constat** : la facon dont l'information est organisee est elle-meme un signal de competence.

**Application** :

- Navigation previsible et coherente
- Breadcrumbs sur toutes les pages sauf l'accueil
- Titres descriptifs dans l'URL (pas /service/3 mais /services/human-risk-intelligence)
- Hierarchie visuelle claire : overline > titre > sous-titre > corps > meta
- Utilisation des overlines en gold pour "etiqueter" chaque section

### Principe 5 : Discretion visuelle

**Constat** : les clients de Mbhidiya valorisent la discretion. Le site ne doit pas etre "bruyant".

**Application** :

- Pas d'animations invasives ou de transitions spectaculaires
- Pas de pop-ups, pas de chatbot visible, pas de banniere cookie intrusive
- Banniere cookies : design integre au footer, sobre, conforme RGPD mais discrete
- Pas de compteurs sociaux, pas de "X personnes consultent cette page"
- Formulaire de newsletter : optionnel, en bas de page Insights uniquement
- Pas de telechargement force (pas de "Telechargez notre brochure" en echange d'un email)

### Principe 6 : Performance comme signal de qualite

**Constat** : un site lent communique l'inverse de ce que Mbhidiya promet (precision, efficacite).

**Application** :

- Time to Interactive (TTI) : < 3 secondes sur desktop, < 5 sur mobile 4G
- Largest Contentful Paint (LCP) : < 2.5 secondes
- Cumulative Layout Shift (CLS) : < 0.1
- Images optimisees (WebP avec fallback JPEG, lazy loading)
- Polices en swap (texte visible immediatement)
- Server-Side Rendering via Symfony/Twig (pas de SPA avec hydration lente)

### Principe 7 : Coherence cross-page

**Constat** : l'utilisateur peut atterrir sur n'importe quelle page (SEO, lien direct). Chaque page doit fonctionner independamment tout en s'inscrivant dans un tout coherent.

**Application** :

- Chaque page de service commence par un hero qui recontextualise le service
- Le CTA est present sur chaque page
- Le footer est identique partout
- Le breadcrumb situe l'utilisateur dans l'arborescence
- Les couleurs, typographies et espacements sont identiques page a page

## 3. Micro-interactions

### 3.1 Navigation

| Interaction         | Comportement                                                      |
| ------------------- | ----------------------------------------------------------------- |
| Scroll down         | Header passe de transparent a fond navy opaque (transition 300ms) |
| Lien hover          | Texte passe a 100% d'opacite + legere underline                   |
| Mega-menu ouverture | Fade-in 200ms + slideDown 200ms                                   |
| Menu mobile         | Slide depuis la droite, 300ms, overlay fond navy                  |

### 3.2 Cartes de services

| Interaction         | Comportement                                                     |
| ------------------- | ---------------------------------------------------------------- |
| Hover               | Elevation augmente (shadow 2), translateY(-2px), bordure bleutee |
| Fleche "Learn More" | Se decale de 4px vers la droite                                  |
| Clic                | Transition standard vers la page de service                      |

### 3.3 Boutons

| Interaction     | Comportement                                                |
| --------------- | ----------------------------------------------------------- |
| Hover           | Changement de couleur de fond (200ms ease-out)              |
| Active          | translateY(1px), retour de 100ms                            |
| Focus (clavier) | Outline gold 2px, offset 2px                                |
| Chargement      | Texte remplace par spinner (cercle anime), bouton desactive |

### 3.4 Formulaire

| Interaction         | Comportement                                             |
| ------------------- | -------------------------------------------------------- |
| Focus champ         | Bordure passe a Intelligence Blue + glow gold subtil     |
| Erreur              | Bordure rouge + message d'erreur apparait avec slideDown |
| Soumission reussie  | Formulaire fade-out, message de confirmation fade-in     |
| Soumission en cours | Bouton en etat "loading", champs desactives              |

### 3.5 Scroll

| Interaction   | Comportement                                                    |
| ------------- | --------------------------------------------------------------- |
| Scroll reveal | Elements apparaissent avec translateY(20px) -> 0 + fade-in      |
| Parallax hero | Image de fond se deplace a 50% de la vitesse du scroll (subtil) |
| Back to top   | Bouton apparait apres 2 ecrans de scroll, coin inferieur droit  |

## 4. Strategie de contenu UX (UX Writing)

### Ton de voix du site

| Attribut         | Description                                 | Exemple                                                                                |
| ---------------- | ------------------------------------------- | -------------------------------------------------------------------------------------- |
| **Direct**       | Phrases courtes, affirmatives               | "We help organisations identify risk." (pas "Our mission is to potentially assist...") |
| **Questionneur** | Questions rhetoriques qui interpellent      | "Can you afford to trust this person?"                                                 |
| **Factuel**      | Pas de superlatifs, pas de promesses vagues | "30+ years of investigative experience" (pas "world-class team")                       |
| **Inclusif**     | "We help" plutot que "We are the best"      | Positionne le client comme l'acteur principal                                          |

### Labels des CTAs

| Page     | CTA primaire                            | CTA secondaire          |
| -------- | --------------------------------------- | ----------------------- |
| Accueil  | "Request an Intelligence Consultation"  | "Explore Our Services"  |
| Service  | "Discuss This Intelligence Requirement" | "View Related Services" |
| About    | "Start a Conversation"                  | "View Our Process"      |
| Contact  | "Request a Confidential Consultation"   | --                      |
| Insights | "Read More"                             | "Back to Insights"      |

### Messages systeme

| Situation          | Message                                                                                                                                                                                                                                                            |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Formulaire soumis  | Icone check animee + "Thank you. Your enquiry has been received. We will respond within one business day. Your enquiry is treated with full confidentiality." + lien "Explore Our Intelligence Insights" (Peak-End Rule : fin d'experience positive et rassurante) |
| Erreur formulaire  | "Please complete the required fields below."                                                                                                                                                                                                                       |
| Page 404           | "This page does not exist. You may have followed an outdated link." + lien vers l'accueil                                                                                                                                                                          |
| Erreur serveur 500 | "Something went wrong. Please try again or contact us directly."                                                                                                                                                                                                   |

## 5. Accessibilite (a11y)

### Standards

- **WCAG 2.1 niveau AA** comme objectif minimum
- **WCAG 2.1 niveau AAA** pour les contrastes de texte

### Checklist

| Critere            | Implementation                                                        |
| ------------------ | --------------------------------------------------------------------- |
| Navigation clavier | Tous les elements interactifs accessibles via Tab                     |
| Focus visible      | Outline gold sur tous les elements focusables                         |
| Roles ARIA         | Landmarks (nav, main, footer, aside), roles sur les composants custom |
| Alt text           | Toutes les images ont un texte alternatif descriptif                  |
| Formulaires        | Labels associes, messages d'erreur lies par aria-describedby          |
| Contraste          | Minimum 4.5:1 pour le texte normal, 3:1 pour le texte large           |
| Animations         | Respecter prefers-reduced-motion (desactiver parallax, transitions)   |
| Langue             | `lang="en"` sur la balise html                                        |
| Structure          | Hierarchie de titres logique (h1 > h2 > h3, pas de saut)              |
| Liens              | Texte de lien descriptif (pas de "cliquez ici")                       |

### Skip to content

Un lien "Skip to main content" est disponible au premier Tab sur chaque page, visible uniquement au focus.

## 6. Performance UX

### Budget de performance

| Metrique             | Objectif | Justification                                |
| -------------------- | -------- | -------------------------------------------- |
| **LCP**              | < 2.5s   | Standard Google "Good"                       |
| **FID**              | < 100ms  | Reactivite aux interactions                  |
| **CLS**              | < 0.1    | Pas de saut visuel au chargement             |
| **TTI**              | < 3.5s   | Site utilisable rapidement                   |
| **Poids total page** | < 1.5 MB | Connexions africaines potentiellement lentes |
| **Requetes HTTP**    | < 30     | Minimiser les allers-retours                 |

### Optimisations specifiques au contexte

Mbhidiya a une clientele potentiellement repartie entre le Canada (excellente connectivite) et l'Afrique (connectivite variable). Le site doit fonctionner correctement sur des connexions 3G/4G africaines :

- Images en WebP avec compression aggressive (qualite 75-80%)
- Lazy loading sur toutes les images sous le fold
- Polices en `font-display: swap` (texte visible immediatement)
- CSS critique inline dans le `<head>`
- JavaScript minimal (pas de framework JS lourd, Symfony + Twig + JS vanilla ou Stimulus)
- CDN avec points de presence en Afrique si possible (Cloudflare)

## 7. Metriques de succes UX

| Metrique                          | Objectif                | Outil de mesure     |
| --------------------------------- | ----------------------- | ------------------- |
| **Taux de rebond**                | < 40%                   | Google Analytics    |
| **Temps moyen sur site**          | > 2 min                 | Google Analytics    |
| **Pages par session**             | > 2.5                   | Google Analytics    |
| **Taux de conversion contact**    | > 2%                    | Suivi formulaire    |
| **Taux de completion formulaire** | > 60%                   | Analytics evenement |
| **Scroll depth page accueil**     | > 60% atteignent le CTA | Scroll tracking     |
| **Core Web Vitals**               | Tous "Good"             | PageSpeed Insights  |
