# Image de base Node.js
FROM node:alpine AS build

# Installation des dépendances
COPY package.json  /app/
WORKDIR /app
RUN npm install

# Ajout des fichiers du projet
COPY . /app

# Build de l'application Vue.js
RUN npm run build

FROM nginx:alpine

# Copie des fichiers de build vers le dossier de Nginx
COPY --from=build /app/dist /usr/share/nginx/html

EXPOSE 80
# Démarrage de Nginx
CMD ["nginx", "-g", "daemon off;"]