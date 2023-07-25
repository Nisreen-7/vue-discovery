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
	_______________________
## Afficher les chiens côté vue	
1. Créer une nouvelle page list-dog.vue et copier-coller le fichier entities.ts du back vers le front, à la racine
	
2. En vous aidant de cette doc (https://nuxt.com/docs/getting-started/data-fetching#usefetch) utiliser le useFetch pour récupérer les chiens et pour le moment afficher juste leur name dans une boucle (on peut typer le useFetch avec des <> comme on type les get/post du httpclient)
	
3. Utiliser nuxi pour générer un component dog-item et lui ajouter une prop dog de type Dog (équivalent des @Input de angular) en suivant cette doc https://vuejs.org/guide/typescript/composition-api.html#typing-component-props
	
4. Utiliser la prop dans le template pour afficher les infos du chien
	
5. Côté list-dog.vue, modifier le template pour boucler sur des DogItem en leur donnant la prop avec :dog 
______________________________

## Formulaire d'ajout de chien	
1. Créer un nouveau component form-dog et dans son template faire un form avec les 3 inputs pour les infos du chien
	
2. Dans le script du component créer une ref<Dog> avec un chien initialisé dedans avec des valeurs vides, liés chaque propriété du chien avec un v-model à son input
	
3. Créer une fonction handleSubmit qui va pour le moment juste faire un console.log du chien et l'assigner au @submit.prevent du form

4. En regardant cette doc (https://vuejs.org/guide/components/events.html#declaring-emitted-events) déclarer un event submitted et faire en sorte de le déclencher dans le handleSubmit en lui donnant le dog comme valeur
	
5. Côté list-dog, créer une async fonction postDog(dog:Dog) et dedans faire un await $fetch pour faire un post en lui donnant dog (https://nuxt.com/docs/api/utils/dollarfetch#fetch)
	
6. A côté du data du useFetch, rajouter le refresh et lancer ce refresh dans le post dog une fois le $fetch terminé
______________________________







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
