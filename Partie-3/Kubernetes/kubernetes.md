# Liste des différents noeuds kubernetes

kubelet : C'est le responsable des conteneurs sur un ordinateur. Il s'assure que les conteneurs sont en cours d'exécution et qu'ils fonctionnent correctement.

kube-proxy : C'est le responsable du réseau sur les ordinateurs. Il permet aux conteneurs de communiquer entre eux et avec le monde extérieur.

Container Runtime : C'est le moteur qui exécute les conteneurs. Il existe différents runtimes, mais Docker est le plus courant.

Pod : C'est la plus petite unité de travail dans Kubernetes. Il contient un ou plusieurs conteneurs, qui partagent le même espace réseau et de stockage.

Kubelet : Kubelet est également responsable de l'exécution d'add-ons sur les ordinateurs. Ces add-ons peuvent fournir des fonctionnalités supplémentaires, telles que la gestion des volumes ou la surveillance des ressources.

cAdvisor : C'est un outil qui collecte des informations sur l'utilisation des ressources et les performances des conteneurs sur un ordinateur. Ces informations peuvent être utilisées pour la surveillance et le diagnostic.

Pause container : Chaque pod contient un conteneur "pause" dédié. Ce conteneur partage le réseau et le stockage avec les autres conteneurs du pod. Il est utilisé pour fournir un point de vue commun du réseau et de l'espace de stockage aux conteneurs du pod.

Kube-Proxy : Il maintient les règles de réseau sur les ordinateurs, permettant aux services de communiquer entre eux. Il peut également effectuer du réacheminement pour permettre l'accès aux services depuis l'extérieur du cluster.

Container Network Interface : C'est une interface standard qui permet de configurer le réseau des conteneurs. Les plugins CNI permettent de configurer les interfaces réseau des conteneurs, facilitant la communication entre les pods sur différents ordinateurs.
