# Arthur Pierron

Étudiant en 3<sup>e</sup> année du Programme Grande École d'**Epitech Lille** (promotion 2029), je me destine à l'**ingénierie en intelligence artificielle**.

Mes projets m'ont amené à réimplémenter un réseau de neurones sans librairie, à concevoir un agent LLM fonctionnant entièrement en local et à travailler sur la robustesse des modèles face aux attaques par prompt. Je cherche à comprendre le fonctionnement des modèles autant qu'à les utiliser.

## Domaines d'intérêt

- **Agents LLM** : appel d'outils, protocole MCP, mémoire, validation humaine
- **Sécurité et évaluation des LLM** : prompt injection, red teaming, détection d'hallucinations
- **Deep learning** : compréhension des fondamentaux par la réimplémentation
- **IA locale** : inférence sur machine, sans transmission de données

## Compétences techniques

**Langages**<br>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white" alt="C">
<img src="https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white" alt="C++">
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white" alt="TypeScript">
<img src="https://img.shields.io/badge/Rust-000000?style=flat&logo=rust&logoColor=white" alt="Rust">
<img src="https://img.shields.io/badge/Haskell-5D4F85?style=flat&logo=haskell&logoColor=white" alt="Haskell">

**IA et données**<br>
<img src="https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white" alt="NumPy">
<img src="https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white" alt="pandas">
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white" alt="scikit-learn">
<img src="https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white" alt="Jupyter">
<img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white" alt="OpenCV">
<img src="https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white" alt="Ollama">
<img src="https://img.shields.io/badge/MCP-555555?style=flat" alt="MCP">
<img src="https://img.shields.io/badge/n8n-EA4B71?style=flat&logo=n8n&logoColor=white" alt="n8n">

**Outils et infrastructure**<br>
<img src="https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white" alt="Node.js">
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white" alt="PostgreSQL">
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white" alt="Docker">
<img src="https://img.shields.io/badge/CMake-064F8C?style=flat&logo=cmake&logoColor=white" alt="CMake">
<img src="https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white" alt="Git">
<img src="https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black" alt="Linux">

## Projets en intelligence artificielle

### SENSAI : copilote d'aide à la décision, exécuté en local
*Python, Ollama (qwen3:8b), MCP, SQLite, interface web*

Agent conversationnel qui répond en français aux questions métier d'une entreprise en interrogeant sa base de données. Les chiffres annoncés sont vérifiés contre les données, aucune modification n'est effectuée sans confirmation explicite et aucune donnée ne quitte la machine.
- Client MCP implémenté sans librairie (JSON-RPC sur stdio) et serveur SQL dédié
- Mémoire structurée (glossaire, entités, faits) et compression du contexte
- Évaluation de chaque réponse par un juge LLM, doublée d'un contrôle numérique déterministe contre les hallucinations
- 77 scénarios d'attaque par prompt injection rejoués en intégration continue ; jeu de référence pour comparer les versions de prompts
- Profils d'agent aux droits distincts et demandes de précision en cas d'ambiguïté

### my_torch : réseau de neurones implémenté de zéro
*Python, NumPy, sans librairie de deep learning*

Module de réseaux de neurones appliqué à l'analyse de positions d'échecs (notation FEN) pour prédire l'échec, le mat ou l'absence des deux.
- Propagation avant, rétropropagation, entraînement et sérialisation des réseaux écrits à la main
- Accuracy de 92,8 % (macro-F1 de 0,915) sur 71 554 positions exclues de l'entraînement et de la sélection du modèle

### Codename : attaque et défense de prompts
*Prompt engineering, Granite 3.1 MoE, Ollama*

Conception d'un prompt de défense protégeant un secret et d'un prompt d'attaque visant ceux des autres équipes.
- Défense élaborée par itérations successives : de règles en langage naturel, contournées par ingénierie sociale, à un modèle cantonné au rôle d'interpréteur de code et insensible à la manipulation
- Protocole de test déterministe (température nulle) et analyse de la complaisance du modèle

### CVRIE : apprentissage supervisé et non supervisé
*Python, scikit-learn, OpenCV, pandas, Jupyter*

- Apprentissage supervisé : classification de radiographies pulmonaires (sain ou pneumonie) sur un jeu de données rééquilibré
- Apprentissage non supervisé : analyse et segmentation d'un jeu de données d'étudiants

### Persona : veille d'actualités automatisée par LLM
*n8n, LLM, PostgreSQL, Docker*

Assistant configurable uniquement par conversation. Il collecte les actualités correspondant aux centres d'intérêt de l'utilisateur, les résume à l'aide d'un LLM, évalue la fiabilité des sources et envoie une lettre d'information par e-mail à l'heure choisie. Conçu dans le respect du RGPD.

## Projets d'ingénierie logicielle

| Projet | Description | Technologies |
|---|---|---|
| **Horde.io** | Jeu multijoueur en ligne (navigateur et mobile) : serveur autoritaire, protocole binaire, bots, configuration rechargée à chaud | TypeScript, Node.js, PixiJS |
| **my_pgp** | Implémentation de XOR, AES, RSA, ElGamal et PGP, avec génération de nombres premiers et signature de messages | Python |
| **Raytracer** | Moteur de rendu par lancer de rayons dont chaque primitive est un plugin chargé à l'exécution | C++ |
| **Arcade** | Plateforme chargeant dynamiquement jeux (Snake, Pac-Man) et bibliothèques graphiques (ncurses, SDL2, Allegro 5) | C++ |
| **Zappy** | Jeu en réseau composé d'un serveur, d'un client graphique et d'une IA autonome | C++, SFML, Python |
| **Plazza** | Simulation d'une pizzeria répartie sur plusieurs processus et threads, communiquant par tubes nommés | C++17 |
| **MyTeams** | Messagerie d'équipe client/serveur reposant sur un protocole binaire conçu pour le projet | C |
| **CartePro** | Application web complète avec gestion de plusieurs rôles, authentification et base de données | TypeScript, Express, PostgreSQL, React |
| **Corewar** | Machine virtuelle dans laquelle des programmes en assembleur s'affrontent en mémoire partagée | C |
| **42sh** | Shell inspiré de tcsh : pipes, redirections, alias, historique | C |

## Contact

- [LinkedIn](https://www.linkedin.com/in/arthur-pierron-221905352)
- [arthur.pierron21@gmail.com](mailto:arthur.pierron21@gmail.com)
