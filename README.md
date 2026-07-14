📘 Engineering Knowledge Repository (EKR)
Référentiel d’ingénierie moderne — Optimisé pour BMAD, Claude Code, Cursor et projets multi‑services
Ce répertoire contient toute la connaissance d’ingénierie du système.    

Il est conçu pour être :    

lisible par les humains,    
exploitable par les LLM (Claude Code, Cursor, Devin),
compatible avec BMAD-METHOD,    
stable, cohérent et maintenable,    
source de vérité unique pour l’architecture, les exigences, les API, les décisions et les patterns.

🧩 Structure des répertoires

engineering-knowledge/    
   10-requirements/    
   20-architecture/    
   30-interfaces/    
   40-decisions/    
   50-components/    
   60-patterns/    
   70-llm-guidelines/    
   README.md    

Chaque dossier est verrouillé :    
👉 Seul l’architecte peut créer, déplacer ou renommer un dossier.    
👉 Les contributeurs ne créent que des fichiers dans les dossiers existants.    

📂 10-requirements/ — Exigences (IEEE 29148)    
Contient les exigences du système :

fonctionnelles    
non fonctionnelles    
contraintes    
règles métier    
Format recommandé    
Chaque exigence doit être un fichier atomique :    
REQ-1234-title.md

Avec :    
ID stable (REQ‑xxxx)    
Description     
Rationale     
Acceptance Criteria    

Mapping BMAD
BMAD lit ce dossier pour générer :

PRD

User Stories

Dev Stories

Architecture Requirements

Mapping Claude Code
Claude Code utilise ces exigences pour :

générer du code conforme

produire des tests

vérifier la cohérence des API

respecter les contraintes métier

📂 20-architecture/ — Architecture (ISO 42010 + C4)
Contient les vues d’architecture :

context-view

container-view

component-view

deployment-view

principes d’architecture

Mapping BMAD
BMAD consolide ces vues pour produire :

architecture shardée

architecture-summary.md

diagrams textuels

Mapping Claude Code
Claude Code s’appuie sur ces vues pour :

structurer les services

respecter les relations entre composants

générer du code aligné sur l’architecture

📂 30-interfaces/ — API & Events (OpenAPI + AsyncAPI)
Contient les contrats d’interface :

OpenAPI (REST)

AsyncAPI (events)

résumés textuels

Mapping BMAD
BMAD lit ces specs pour générer :

API documentation shardée

API summaries

Event catalogs

Mapping Claude Code
Claude Code utilise ces specs pour :

générer les endpoints

produire les DTO

créer les clients API

générer les producers/consumers Kafka

📂 40-decisions/ — ADR (Architecture Decision Records)
Contient les décisions d’architecture :

ADR‑0001

ADR‑0002

adr-index.md

Mapping BMAD
BMAD indexe les ADR pour :

produire adr-index.md

relier les décisions aux exigences et à l’architecture

Mapping Claude Code
Claude Code respecte les ADR pour :

choisir les technologies

appliquer les patterns

éviter les contradictions

📂 50-components/ — Composants standards
Contient les briques techniques transverses :

logging

observability

security

crud

ui

Mapping BMAD
BMAD utilise ces fichiers pour générer :

component-guidelines.md

engineering standards

Mapping Claude Code
Claude Code applique ces règles pour :

structurer les services

générer du code conforme

respecter les conventions techniques

📂 60-patterns/ — Patterns d’ingénierie
Contient les patterns réutilisables :

event-sourcing

domain-events

repository-pattern

api-versioning

Mapping BMAD
BMAD relie les patterns aux composants et aux ADR.

Mapping Claude Code
Claude Code applique ces patterns dans :

la génération de code

les tests

les refactorings

📂 70-llm-guidelines/ — Règles pour les IA
Contient les instructions pour :

Claude Code

Cursor

Devin

BMAD

Contenu typique
claude-code.md

cursor.md

project-context.md

bmad.md

Mapping BMAD
BMAD génère les skills dans .claude/skills.

Mapping Claude Code
Claude Code utilise ces guidelines comme system prompts internes.

🧭 Règles de gouvernance
1. Les dossiers sont verrouillés
Seul l’architecte peut :

créer un dossier

déplacer un dossier

renommer un dossier

2. Les contributeurs ne créent que des fichiers dans les dossiers existants
3. Chaque fichier doit être :
atomique

court

structuré

référencé (REQ‑xxxx, ADR‑xxxx)

4. Les LLM doivent être guidés via :
70-llm-guidelines/claude-code.md

.claude/skills/ généré par BMAD

5. BMAD lit uniquement :
10-requirements/

20-architecture/

30-interfaces/

40-decisions/

50-components/

60-patterns/

6. Claude Code lit :
tout le EKR

les skills BMAD

les artefacts BMAD dans _bmad-output/

🧠 Objectif du EKR
Ce référentiel permet :

une cohérence totale du système

une génération automatique d’artefacts via BMAD

une génération de code fiable via Claude Code

une documentation vivante

une réduction massive des erreurs

une accélération du développement