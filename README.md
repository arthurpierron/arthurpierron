<h1 align="center">Salut, moi c'est Arthur 👋</h1>

<p align="center">
  Étudiant en 3<sup>e</sup> année à <b>Epitech Lille</b> (Programme Grande École, promo 2029)<br>
  <b>Je veux devenir ingénieur en intelligence artificielle.</b>
</p>

<p align="center">
  J'ai écrit un réseau de neurones sans aucune librairie, construit un agent LLM qui tourne 100 % en local<br>
  et passé des heures à attaquer et défendre des prompts. J'aime comprendre comment les modèles marchent, pas seulement les utiliser.
</p>

---

## 🎯 Ce qui m'intéresse

- **Agents LLM** : outils, MCP, mémoire, planification, humain dans la boucle
- **Sécurité et évaluation des LLM** : prompt injection, red teaming, détection d'hallucinations
- **Deep learning** : comprendre les fondamentaux en les réimplémentant
- **IA locale** : faire tourner des modèles sur sa machine, sans envoyer de données

---

## 🧰 Stack

**IA et data**<br>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white" alt="NumPy">
<img src="https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white" alt="pandas">
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white" alt="scikit-learn">
<img src="https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white" alt="Jupyter">
<img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white" alt="OpenCV">
<img src="https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white" alt="Ollama">
<img src="https://img.shields.io/badge/MCP-555555?style=flat" alt="MCP">
<img src="https://img.shields.io/badge/n8n-EA4B71?style=flat&logo=n8n&logoColor=white" alt="n8n">

**Développement**<br>
<img src="https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white" alt="C">
<img src="https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white" alt="C++">
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white" alt="TypeScript">
<img src="https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white" alt="Node.js">
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white" alt="PostgreSQL">
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white" alt="Docker">
<img src="https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black" alt="Linux">

---

## 🤖 Projets IA

### SENSAI · copilote BI 100 % local
*Python · Ollama (qwen3:8b) · MCP · SQLite · interface web*

Un agent qui répond en français aux questions métier d'une entreprise en interrogeant sa base de données. Les chiffres sont **vérifiés contre les données** et l'agent **ne modifie rien sans confirmation explicite**. Rien ne quitte la machine.
- Client **MCP écrit à la main** (JSON-RPC sur stdio) et serveur SQL maison
- Mémoire structurée (glossaire, entités, faits) et compression du contexte quand il se remplit
- Un juge LLM évalue chaque réponse, avec un contrôle numérique déterministe contre les hallucinations
- **77 attaques adversariales** (prompt injection) rejouées en CI, golden set pour comparer les versions de prompts
- Profils d'agent avec des droits différents, questions de précision quand la demande est ambiguë

### my_torch · réseau de neurones from scratch
*Python · NumPy, sans aucune librairie de deep learning*

Un module de réseaux de neurones écrit de zéro, utilisé pour analyser des positions d'échecs (FEN) et prédire *échec*, *mat* ou *rien*.
- Propagation avant, rétropropagation, entraînement et sauvegarde des réseaux, tout écrit à la main
- **92,8 % d'accuracy** (macro-F1 0,915) sur 71 554 positions jamais vues à l'entraînement

### Codename · attaque et défense de prompts
*Prompt engineering · Granite 3.1 MoE · Ollama*

Concevoir un prompt de défense qui protège un secret, et un prompt d'attaque qui arrache celui des autres équipes.
- Défense construite par itérations : de règles en langage naturel (contournées par l'ingénierie sociale) à un modèle qui joue le rôle d'un **interpréteur de code**, insensible à la manipulation
- Tests déterministes (temperature 0) et analyse du comportement « trop serviable » du modèle

### CVRIE · apprentissage supervisé et non supervisé
*Python · scikit-learn · OpenCV · pandas · Jupyter*

- **Supervisé** : classification de radiographies pulmonaires (normal / pneumonie) sur un dataset rééquilibré
- **Non supervisé** : analyse et segmentation d'un dataset d'étudiants

### Persona · agrégateur d'actualités piloté par l'IA
*n8n · LLM · PostgreSQL · Docker*

Un assistant qu'on configure uniquement par chat. Il cherche les actualités qui correspondent à vos centres d'intérêt, **les résume avec un LLM**, vérifie la fiabilité des sources et envoie une newsletter par e-mail à l'heure choisie. Conçu en respectant le RGPD.

---

## 🛠️ Bases en ingénierie logicielle

L'IA en production, c'est aussi du système, du réseau et de l'architecture. Ce que j'ai construit en C, C++ et TypeScript :

| Projet | Description | Stack |
|---|---|---|
| **Horde.io** | Jeu multijoueur en ligne (navigateur et mobile) : serveur autoritaire, **protocole binaire**, bots, config rechargée à chaud | TypeScript · Node.js · PixiJS |
| **my_pgp** | XOR, AES, RSA, ElGamal et PGP réimplémentés à la main, avec génération de nombres premiers et signatures | Python |
| **Raytracer** | Moteur de rendu par lancer de rayons, chaque primitive est un plugin chargé à l'exécution | C++ |
| **Arcade** | Borne qui charge jeux (Snake, Pac-Man) et rendus (ncurses, SDL2, Allegro 5) à la volée | C++ |
| **Zappy** | Jeu en réseau : serveur, client graphique et **IA qui joue de façon autonome** | C++ · SFML · Python |
| **Plazza** | Pizzeria simulée sur plusieurs processus et threads, communication par named pipes | C++17 |
| **MyTeams** | Messagerie d'équipe client/serveur avec un protocole binaire maison | C · sockets |
| **CartePro** | Application web full-stack avec plusieurs rôles, authentification et base de données | TypeScript · Express · PostgreSQL · React |
| **Corewar** | Machine virtuelle où des programmes en assembleur s'affrontent en mémoire partagée | C |
| **42sh** | Shell inspiré de `tcsh` : pipes, redirections, alias, historique | C |

---

## 📫 Me contacter

<!-- Remplace les liens ci-dessous par les tiens -->
- 💼 [LinkedIn](https://www.linkedin.com/in/TON-PROFIL)
- ✉️ ton.email@exemple.com

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=arthurpierron&show_icons=true&hide_border=true&include_all_commits=true&count_private=true" alt="Stats GitHub" height="160">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=arthurpierron&layout=compact&hide_border=true" alt="Langages" height="160">
</p>
