## Premier exo vue avec boucle et input

1. Générer une nouvelle page name-list.vue (à laquelle on accédera donc en allant sur localhost:3000/name-list
	
2. Dans le script de cette page, déclarer une ref avec comme valeur un tableau de noms 
	
3. Dans le template, faire un ul et un li dedans et sur le li appliquer un v-for qui va boucler sur la liste de noms
	
4. Créer une nouvelle ref newName qui aura une chaîne de caractère vide comme valeur par défaut
	
5. Créer une fonction addName() qui va push la value de newName dans la value de la liste
	
6. Dans le template, rajouter un input avec un v-model associé à newName (c'est comme ngModel, mais sans les [(...)] ) et rajouter également un button qui au click va lancer la fonction addName

## Si on veut charger le css de bootstrap :
> npm i bootstrap
	
Modifier le nuxt.config.ts pour qu'il ressemble à :
	
	// https://nuxt.com/docs/api/configuration/nuxt-config
	export default defineNuxtConfig({
	  devtools: { enabled: true },
	  
	  css: [
	    '/node_modules/bootstrap/dist/css/bootstrap.min.css'
	  ]
	})






# Nuxt 3 Minimal Starter

Look at the [Nuxt 3 documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

## Setup

Make sure to install the dependencies:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# pnpm
pnpm run dev

# yarn
yarn dev
```

## Production

Build the application for production:

```bash
# npm
npm run build

# pnpm
pnpm run build

# yarn
yarn build
```

Locally preview production build:

```bash
# npm
npm run preview

# pnpm
pnpm run preview

# yarn
yarn preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
