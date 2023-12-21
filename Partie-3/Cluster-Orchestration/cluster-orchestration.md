# Cluster et orchestration

## Principe

L'ochestration de conteneur permet de gérer de nombreux conteneurs à la fois sur une machine. C'est une couche par dessus les conteneurs qui permet de les gérer (les lancer, les restart en cas de problème). Lorsque notre application à besoin de beaucoup de service c'est une bonne pratique de créer des cluster de conteneur et de les gérer avec un orchestrateur tel que Docker Swarm.

## Microservices

Le principe de l'architecture en microservice consiste à séparer le plus possible les différents traitements de l'application en différents service. Chaque service correspondra à un container. Des sites comme les sites de e-commerce fonctionnent beaucoup sur ce principe et c'est pourquoi l'orchestration de tous les container est très importante.

## Scalabilité

L'avantage de tous séparer dans des microservice est le fait d'adapter les tailles des application en fonction de ce dont elles ont besoin. Plus les applications sont séparée intelligement, plus on peut optimiser les tailles et maximiser les performances.

## Availability

L'availability représente la capacité d'une application conteneurisée à être accessible et opérationnelle de manière fiable sur une période de temps donnée.

## Load Balancing

Le load balancing représente la distribution équitable du trafic réseau entrant entre plusieurs instances d'une application ou d'un service lorsqu'elle est déployées sur des conteneurs distincts. L'objectif principal est d'optimiser l'utilisation des ressources et d'assurer une répartition uniforme des requêtes pour améliorer la performance, la disponibilité et la résilience de l'application.

## La clusterisation : une solution

La clusterisation est une solution pour ces problématiques. La séparation en microservice permet une meilleur scalabilité des différents conteneurs. Ensuite grâce à un orchestrateur on va gérer les disponibilités des conteneurs et on va aussi gérer le load balancing en repartissant équitablement

## Comment clusteriser

Des outils comme **Docker Swarm**, **Kubernetes** ou encore **Apache Mesos** permettent d'orchestrer un cluster de conteneurs.
