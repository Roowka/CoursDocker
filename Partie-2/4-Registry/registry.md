# Registry

## Utilisation en entreprise

L'utilisation d'un registry interne en entreprise a plusieurs avantages. Tout d'abord cela a un intérêt en terme de sécurité, car cela permet de limiter les images disponible à celles du registry. Ensuite cela permet de garder la confidentialité des images créer par l'entreprise. En terme de performance il peut être plus rapide de télécharger une image depuis un registry interne privé que depuis le docker hub. De plus on peut personnaliser notre registry pour l'optimiser selon nos besoins.

## Push d'une image

Tout d'abord je commence par retag mon image en mettant <monpseudo>/<monimage>:<version>

```
docker tag <monimage> <monpseudo>/<monimage>:<version>
```

Ensuite je me connecte avec la commande

```
docker login
```

Ensuite, il suffit de push l'image de la manière suivante

```
docker push <monpseudo>/<monimage>:<version>
```

Lien de mon image

```
docker pull lucasgoi/site-vuejs:1.0.0
```
