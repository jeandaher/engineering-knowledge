# 📘 Engineering Knowledge Repository (EKR)    
## Référentiel d’ingénierie pour projets IA
L’Engineering Knowledge Repository (EKR) est la <strong>source de vérité du système.</strong>

Il contient uniquement les connaissances nécessaires au <strong>développement</strong>, à la <strong>maintenance</strong> et à l’évolution du produit :
* métier    
* produit    
* expérience utilisateur    
* domaine    
* architecture    
* interfaces    
* données    
* standards    
* décisions    
* contexte IA    
    
    
Il est conçu pour être :    
* lisible par les humains    
* exploitable par les assistants IA (Claude Code, Codex, Cursor, Gemini, etc.)    
* versionné avec le code source    
* indépendant des outils    
* maintenable dans le temps    
* structuré pour éviter les duplications    

<strong>Principe fondamental</strong>    
<i>Une information doit exister une seule fois, au bon endroit.</i>    

## 📁 Structure
```text
engineering/    
├── 01-business/    
├── 02-product/    
├── 03-user-experience/    
├── 04-domain/    
├── 05-architecture/    
├── 06-services/    
├── 07-data/    
├── 08-standards/    
├── 09-decisions/    
├── 10-ai/    
└── README.md    
```

| Dossier            | Contenu      | Source de vérité                      |
| ------------------ | ------------ | ------------------------------------- |
| 01-business        | Métier       | Glossaire, règles métier, cas d'usage |
| 02-product         | Produit      | Vision, exigences, user stories       |
| 03-user-experience | UX/UI        | Pages, navigation, design system      |
| 04-domain          | Domaine      | Modèle métier, entités, agrégats      |
| 05-architecture    | Architecture | C4, principes, déploiement            |
| 06-services        | Interfaces   | OpenAPI, AsyncAPI, intégrations       |
| 07-data            | Données      | Modèle de données, migrations         |
| 08-standards       | Standards    | Règles techniques communes            |
| 09-decisions       | Décisions    | ADR                                   |
| 10-ai              | IA           | Contexte et instructions IA           |


## 📂 01-business — Métier
```Code
01-business/
├── glossary/
├── business-rules/
├── use-cases/
└── actors/
```
Contient :    
* vocabulaire métier    
* règles métier    
* cas d’utilisation    
* acteurs    

<b>Source de vérité</b> :      
Les concepts métier et leurs définitions.

## 📂 02-product — Produit
```Code
02-product/
├── vision.md
├── roadmap.md
├── requirements/
└── user-stories/
```
Contient :    
* vision produit
* exigences
* stories utilisateur

<b>Source de vérité :</b>  
<i>Les besoins du produit et leur priorisation.</i>

## 📂 03-user-experience — UX/UI
```Code
03-user-experience/
├── navigation.md
├── pages/
├── forms/
├── workflows/
└── design-system/
```

Contient :
* navigation
* pages applicatives
* composants UI
* parcours utilisateur

<b>Source de vérité :</b>  
<i>L’expérience utilisateur.</i>

## 📂 04-domain — Domaine (DDD)
```Code
04-domain/
├── domain-model.md
├── bounded-contexts/
├── entities/
├── value-objects/
└── aggregates/
```

Contient :
* modèle métier
* entités
* objets valeur
* agrégats
* contextes délimités

<b>Source de vérité :</b>  
<i>Le modèle conceptuel du système.</i>

## 📂 05-architecture — Architecture
```Code
05-architecture/
├── context.md
├── containers.md
├── components.md
├── deployment.md
└── principles.md
```

Référence architecture :
* ISO/IEC/IEEE 42010
* C4 Model

<b>Source de vérité :</b>  
<i>La structure du système.</i>

## 📂 06-services — Interfaces & intégrations
```Code
06-services/
├── openapi/
├── asyncapi/
└── integrations/
```
Sources de vérité :
* OpenAPI : API REST
* AsyncAPI : événements
* intégrations externes

## 📂 07-data — Données
```Code
07-data/
├── erd.md
├── tables/
└── migrations/
```
Contient :
* modèle de données
* structures SQL
* migrations

<b>Source de vérité :</b>  
<i>La structure des données persistées.</i>

## 📂 08-standards — Standards techniques
```Code
08-standards/
├── frontend/
├── backend/
├── ui/
├── crud/
├── logging/
├── observability/
├── security/
└── testing/
```

Définit les règles communes applicables aux projets.

<b>Source de vérité :</b>  
<i>Les conventions techniques.</i>

## 📂 09-decisions — ADR
```Code
09-decisions/
└── adr/
    ├── ADR-0001.md
    ├── ADR-0002.md
    └── index.md
```

Les ADR expliquent :
* le contexte
* la décision
* les conséquences

<b>Source de vérité :</b>  
<i>Les choix structurants.</i>

## 📂 10-ai — IA
```Code
10-ai/
├── project-context.md
├── claude.md
├── codex.md
├── cursor.md
└── prompts/
```
Contient :

* contexte projet pour les IA
* règles d’utilisation
* instructions spécifiques

<b>Source de vérité :</b>  
<i>Le comportement attendu des assistants IA.</i>

## 🧭 Gouvernance
<b>Structure</b>    
La structure des dossiers est <b>stable</b>.     
Seul l’architecte peut : 
* créer un dossier
* supprimer un dossier
* déplacer un dossier
* renommer un dossier    

Les contributeurs ajoutent uniquement des <b>fichiers</b> dans les dossiers existants.   

--- 

### Qualité documentaire
Chaque document doit être :
* court
* ciblé
* structuré
* versionné
* référencé si nécessaire

Identifiants recommandés
```Code
REQ-0001
ADR-0001
API-0001
PAGE-0001
STD-0001
```

--- 

### Source de vérité
Une information ne doit <b>pas</b> être dupliquée.

Exemples :
* API → OpenAPI
* événements → AsyncAPI
* décisions → ADR
* standards → 08-standards
* architecture → 05-architecture

---

### Traçabilité minimale
```Code
Requirement
      ↓
Use Case
      ↓
Page
      ↓
API
      ↓
Service
      ↓
ADR
```
La traçabilité doit apporter une <b>valeur opérationnelle.</b>

---

### Philosophie
L’EKR n’est pas un wiki.    
C’est un <b>référentiel de connaissance</b> exploitable par :
* les architectes
* les développeurs
* les équipes QA
* les assistants IA

Le code décrit l’implémentation.    
Les contrats décrivent les interfaces.    
Les standards décrivent les règles.    
Les ADR expliquent les choix.    
L’EKR décrit la connaissance du système.    

<b>Tous les outils utilisent la même source de vérité.</b>

---