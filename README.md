Projet Mairie de Cergy - Site Web Connecté :

Ce projet est une application web moderne pour la Mairie de Cergy, offrant aux citoyens un accès facile aux actualités, services municipaux et permettant de signaler des incidents. L'application dispose également d'une interface d'administration pour la gestion du contenu.

Interface Utilisateur :
- **Page d'accueil** : Présentation des principales sections du site
- **Actualités** : Consultation des dernières nouvelles de la ville avec filtrage par catégorie
- **Services Municipaux** : Accès aux informations sur les services disponibles
- **Signalement d'Incidents** : Possibilité de signaler et suivre des incidents dans la ville

Système d'Authentification :
- Inscription et connexion des utilisateurs
- Différents niveaux d'accès (utilisateur, super-utilisateur, administrateur)
- Protection des routes et composants selon les droits d'accès

Interface d'Administration :
- Gestion des utilisateurs
- Publication et gestion des actualités
- Suivi des incidents signalés

Frontend :
- **Next.js 15** : Framework React avec rendu du côté du serveur
- **React 19** : Bibliothèque UI
- **Tailwind CSS** : Framework CSS utilitaire
- **Shadcn UI** : Composants UI basés sur Radix UI
- **Axios** : Client HTTP pour les requêtes API
- **date-fns** : Manipulation des dates

Backend :
- **Next.js API Routes** : API REST
- **Prisma** : ORM pour la gestion de la base de données
- **PostgreSQL** : Base de données relationnelle
- **bcrypt** : Hachage des mots de passe

 Prérequis :
- Node.js (version recommandée : 20.x ou supérieure)
- PostgreSQL (version recommandée : 15.x ou supérieure)

Étapes d'installation :

1. Cloner le dépôt :

git clone [https://github.com/AlexLcq/mairie.git]
cd mairie

2. Installer les dépendances :

npm install


4. Exécuter les migrations Prisma :
npx prisma migrate dev

5. Générer le client Prisma :
npx prisma generate

Mode développement :
npm run dev

L'application sera accessible à l'adresse [http://localhost:3000]

Mode production :
npm run build
npm start


Structure du Projet :

├── app/                    # Routes et pages Next.js
│   ├── actualites/         # Page des actualités
│   ├── admin/              # Interface d'administration
│   ├── api/                # Routes API
│   ├── incidents/          # Page de signalement d'incidents
│   ├── login/              # Page de connexion
│   ├── register/           # Page d'inscription
│   ├── services/           # Page des services municipaux
│   ├── globals.css         # Styles globaux
│   ├── layout.tsx          # Layout principal
│   └── page.tsx            # Page d'accueil
├── components/             # Composants React réutilisables
│   ├── ui/                 # Composants UI de base
│   ├── AdminPostNews.tsx   # Composant de publication d'actualités
│   ├── AdminUser.tsx       # Composant de gestion des utilisateurs
│   ├── header.tsx          # En-tête du site
│   ├── protectedComponent.tsx # Protection des composants
│   └── protectedPage.tsx   # Protection des pages
├── context/                # Contextes React
│   └── AuthContext.tsx     # Contexte d'authentification
├── hook/                   # Hooks personnalisés
│   └── useAuth.tsx         # Hook d'authentification
├── lib/                    # Utilitaires et types
│   ├── type.tsx            # Définitions de types TypeScript
│   └── utils.ts            # Fonctions utilitaires
├── prisma/                 # Configuration Prisma
│   ├── migrations/         # Migrations de base de données
│   └── schema.prisma       # Schéma de la base de données
└── provider/               # Fournisseurs de contexte
    └── AuthProvider.tsx    # Fournisseur d'authentification
```

Utilisateur (User) :
- Gestion des comptes utilisateurs avec différents niveaux d'accès

Service Municipal (MunicipalService) :
- Informations sur les services disponibles dans la ville

Objet Connecté (ConnectedObject) :
- Gestion des objets connectés de la ville (capteurs, etc.)

Incident (Incident) :
- Signalements d'incidents par les utilisateurs

Actualité (News) :
- Publications et événements de la ville


