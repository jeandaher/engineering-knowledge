📘 Engineering — Knowledge Base
Référentiel d’ingénierie complet pour projets multi‑services, multi‑équipes et IA‑assistés
Ce répertoire contient toute la connaissance structurée du système, depuis le business jusqu’à l’architecture, les données, les standards, les décisions et les guidelines IA.

Il est conçu pour être :    
lisible par les humains,    
exploitable par les LLM (Claude Code, Cursor, Devin),    
stable, cohérent et maintenable,    
source de vérité unique pour l’ensemble du cycle de vie du produit.    

📁 Structure des répertoires

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

Chaque dossier est verrouillé :    
👉 Seul l’architecte peut créer, déplacer ou renommer un dossier.     
👉 Les contributeurs ne créent que des fichiers dans les dossiers existants.     

📂 01-business/ — Contexte métier    
Contient les éléments fondamentaux du métier :    
glossary/ — vocabulaire métier    
business-rules/ — règles métier     
use-cases/ — cas d’usage métier    
actors/ — acteurs métier

Objectif : définir le “pourquoi” du système.

📂 02-product/ — Vision produit    
Contient les éléments orientés produit :    
vision.md — vision stratégique    
roadmap.md — roadmap    
requirements/ — exigences produit    
user-stories/ — stories utilisateur     

Objectif : définir le “quoi” du produit.

📂 03-user-experience/ — UX & UI    
Contient les éléments orientés expérience utilisateur :    

navigation.md    
pages/
forms/
workflows/
design-system/

Objectif : définir le “comment l’utilisateur interagit”.

📂 04-domain/ — Modèle de domaine (DDD)
Contient les éléments conceptuels :
domain-model.md
bounded-contexts/
entities/
value-objects/
aggregates/

Objectif : définir le “comment le métier est modélisé”.

📂 05-architecture/ — Architecture (ISO 42010 + C4)    
Contient les vues d’architecture :     
context.md      
containers.md    
components.md    
deployment.md    
principles.md    

Objectif : définir le “comment le système est structuré”.

📂 06-services/ — Interfaces & intégrations
Contient les contrats techniques :    

openapi/ — API REST    
asyncapi/ — événements    
integrations/ — systèmes externes    
    
Objectif : définir le “comment les services communiquent”.

📂 07-data/ — Données & stockage
Contient les éléments orientés données :    

erd.md — diagramme ER    
tables/ — tables SQL    
migrations/ — scripts de migration    
    
Objectif : définir le “comment les données sont structurées”.

📂 08-standards/ — Standards techniques    
Contient les règles transverses :    
frontend/    
backend/    
ui/    
crud/    
logging/    
observability/    
security/    
testing/    
    
Objectif : définir le “comment le code doit être écrit”.
    
📂 09-decisions/ — ADR (Architecture Decision Records)    
Contient les décisions d’architecture :    
adr/ADR-0001.md    
adr/ADR-0002.md    
adr/index.md    
    
Objectif : définir le “pourquoi nous avons choisi cette solution”.

📂 10-ai/ — Guidelines IA    
Contient les instructions pour les assistants IA :    
project-context.md    
claude.md    
codex.md    
cursor.md    
prompts/
    
Objectif : définir le “comment les IA doivent travailler sur ce projet”.    

🧭 Règles de gouvernance    
1. Les dossiers sont verrouillés    
Seul l’architecte peut :    
créer un dossier    
déplacer un dossier    
renommer un dossier    
    
2. Les contributeurs ne créent que des fichiers    
    
3. Chaque fichier doit être :    
atomique    
court    
structuré    
référencé (REQ‑xxxx, ADR‑xxxx)    

4. Les LLM doivent être guidés via :    
10-ai/claude.md    
10-ai/cursor.md    
10-ai/prompts/    

5. Les décisions doivent être liées à :    
04-domain    
05-architecture        
06-services    
07-data    
6. Les liens croisés sont obligatoires    
Exemples :    
une exigence → un cas d’usage    
un cas d’usage → un workflow    
un workflow → une API    
une API → un service    
un service → un ADR    
un ADR → un principe d’architecture    
