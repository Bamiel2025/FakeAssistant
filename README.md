# Fake ou Science ? - Chatbot Pédagogique Sécurisé

Chatbot pédagogique pour développer l'esprit critique scientifique, déployé de manière sécurisée sur Vercel avec une architecture frontend/backend.

Test commit for Vercel deployment.

## Architecture

- **Frontend** : Interface HTML/CSS/JS statique
- **Backend** : Fonction serverless Vercel (Node.js) qui proxy les requêtes vers l'API Gemini
- **Sécurité** : Clé API stockée côté serveur dans les variables d'environnement

## Déploiement sur Vercel

1. Créez un compte sur [Vercel](https://vercel.com).
2. Installez la CLI Vercel : `npm install -g vercel`
3. Clonez ou téléchargez ce projet.
4. Obtenez une clé API Gemini depuis [Google AI Studio](https://makersuite.google.com/app/apikey).
5. Dans votre projet Vercel, ajoutez la variable d'environnement : `GEMINI_API_KEY` = votre clé API.
6. Déployez : `vercel --prod`

## Développement Local

1. Installez les dépendances : `npm install`
2. Configurez la variable d'environnement : `export GEMINI_API_KEY=votre_clé`
3. Lancez le serveur de développement : `npm run dev`
4. Ouvrez `http://localhost:3000`

## Utilisation

- Les élèves peuvent poser leurs questions dans le champ de saisie.
- L'agent répond en suivant la méthodologie pédagogique définie.
- L'historique de la conversation est maintenu côté client.

## Fonctionnalités

- Interface de chat simple et intuitive
- Intégration sécurisée avec Gemini 1.5 Flash via proxy backend
- Respect des principes pédagogiques (questionnement socratique, etc.)
- Modes : analyse d'information, débat simulé, quiz, formation méthodologique

## Sécurité

- Clé API Gemini stockée côté serveur, non exposée au client
- CORS configuré pour les communications frontend-backend
- Architecture serverless pour une scalabilité sécurisée