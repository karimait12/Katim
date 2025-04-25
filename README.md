# Anime Seven Admin Assistant

Un assistant MCP (Model Context Protocol) pour les administrateurs de l'application mobile Anime Seven. Cet outil facilite la gestion des animes et des épisodes sur la page Facebook officielle de l'application.

## Fonctionnalités

- **Gestion d'anime** : Recherche, publication et mise à jour d'animes via l'API Facebook
- **Gestion d'épisodes** : Ajout et organisation des épisodes sous forme de commentaires
- **Traduction** : Traduction automatique des descriptions et titres d'animes
- **Guides pratiques** : Instructions détaillées pour les différentes tâches d'administration

## Configuration requise

- Node.js v18 ou supérieur
- Un compte Facebook avec accès à la page d'Anime Seven
- Un token d'accès Facebook avec les permissions appropriées
- Une clé API Gemini pour les fonctionnalités de traduction

## Installation

1. Clonez ce dépôt :
```bash
git clone https://github.com/anime-seven/admin-assistant.git
cd admin-assistant
```

2. Installez les dépendances :
```bash
npm install
```

3. Créez un fichier `.env` à la racine du projet avec les variables suivantes :
```
FACEBOOK_ACCESS_TOKEN=votre_token_acces_facebook
FACEBOOK_PAGE_ID=votre_id_page_facebook
GEMINI_API_KEY=votre_cle_api_gemini
```

4. Compilez le projet :
```bash
npm run build
```

## Utilisation

Pour démarrer l'assistant :

```bash
npm start
```

Pour le mode développement (recompilation automatique) :

```bash
npm run dev
```

## Configuration pour Cline AI

Pour configurer le projet `A7-admin-assistant` dans Cline AI, ajoutez la section suivante à votre fichier de configuration :

```json
"A7-admin-assistant": {
  "autoApprove": [
  ],
  "disabled": false,
  "timeout": 60,
  "command": "node",
  "args": [
    "c:/Users/HP/Documents/Cline/MCP/A7-admin-assistant/build/index.js"
  ],
  "env": {
    "FACEBOOK_ACCESS_TOKEN": "EAAIkB3nvYhUBO8ug20kUilXK6nOC2c9WbCow4Mf0F1VIFp39ZCqVIE3LgmI9eNgXX9rty98HWOpSANEZCNfmv2lf4WUwWjBqQAzfouLM4WkLTapcUrmup6Q9NjJrSEVbVuNrFV0y1oUvJE1lxbEe1ERvwFzsAYhvtkeWcHZCiVv5ZBJrlXq4ZAqpZBhXAlUm8W",
    "FACEBOOK_PAGE_ID": "547656128434943",
    "GEMINI_API_KEY": "AIzaSyAsuiXiwTIArv7o8MwELEXTNus5v-AjneQ"
  },
  "transportType": "stdio"
}
```

## Configuration pour Cursor AI

Pour configurer le projet `A7-admin-assistant` dans Cursor AI, ajoutez la section suivante à votre fichier de configuration `mcp.json` :

```json
"A7-admin-assistant": {
  "command": "node",
  "args": [
    "C:/Users/HP/Documents/Cline/MCP/A7-admin-assistant/build/index.js"
  ],
  "env": {
    "FACEBOOK_ACCESS_TOKEN": "EAAIkB3nvYhUBO8ug20kUilXK6nOC2c9WbCow4Mf0F1VIFp39ZCqVIE3LgmI9eNgXX9rty98HWOpSANEZCNfmv2lf4WUwWjBqQAzfouLM4WkLTapcUrmup6Q9NjJrSEVbVuNrFV0y1oUvJE1lxbEe1ERvwFzsAYhvtkeWcHZCiVv5ZBJrlXq4ZAqpZBhXAlUm8W",
    "FACEBOOK_PAGE_ID": "547656128434943",
    "GEMINI_API_KEY": "AIzaSyAsuiXiwTIArv7o8MwELEXTNus5v-AjneQ"
  },
  "disabled": false,
  "autoApprove": [
    "get_facebook_page_posts",
    "get_post_comments",
    "search_anime",
    "add_episode_comment",
    "translate_text",
    "guide_ajout_anime"
  ]
}
```


## Outils disponibles

### Outils Facebook

- `get_facebook_page_posts` : Récupère les publications de la page Facebook
- `get_post_comments` : Récupère les commentaires d'une publication Facebook
- `delete_facebook_comment` : Supprime un commentaire d'une publication Facebook

### Outils d'anime

- `post_anime_to_facebook` : Publie des informations d'anime sur Facebook avec image
- `search_anime` : Recherche des informations d'anime par titre via l'API Jikan
- `add_episode_comment` : Ajoute un épisode en tant que commentaire sur une publication

### Outil de traduction

- `translate_text` : Traduit un texte vers une langue cible en utilisant l'API Gemini

### Guides et instructions

- `get_add_anime_process_overview` : Vue d'ensemble du processus d'ajout d'anime
- `get_add_anime_detailed_steps` : Étapes détaillées pour l'ajout d'anime
- `get_add_anime_practical_tips` : Conseils pratiques pour l'ajout d'anime
- `get_add_anime_comprehensive_example` : Exemple complet d'ajout d'anime et d'épisodes

## Contribution

Les contributions sont les bienvenues ! Veuillez soumettre une pull request ou ouvrir une issue pour discuter des changements proposés.

## Licence

Ce projet est sous licence MIT.