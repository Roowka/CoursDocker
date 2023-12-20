# Concept de conteneur

## Principe de conteneurisation

La conteneurisatioon consiste à rassembler le code du logiciel et tous ses composants. En fait on va sauvegarder un "environnement" dans un conteneur, isolé entre autre du reste sur la machine.

## Avantage de la conteneurisation

Lorsque que l'on conteneurise notre application, tout le nécessaire pour son fonctionnement (modules, language...) est pris et sauvegardé dans l'image. Cette image peut être télécharger n'importe ou et cela permet un déploiement et un lacement du projet en quelques secondes sans aucun soucis.

## VM vs Docker

![VM-vs-Docker](./vm-vs-docker.webp)

Comme nous pouvons voir sur le schéma ci-dessus, une machine virtuelle, contrairement à Docker, embarque un système d'exploitation. Docker lui partage le même OS entre ses différentes images, ce qui rend chaque conteneur beaucoup plus léger qu'une VM.

Le partage d'image Docker d'un système à un autre est de ce fait plus rapide, et le démarrage sur un autre OS se fait très rapidement. De plus, un conteneur Docker démarre en quelques secondes.
