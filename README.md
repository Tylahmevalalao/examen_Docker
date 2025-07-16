# examen_Docker
### RAKOTONJANAHARY Mevalalao Tylah
### 164/LA/24/25
# Cheat Sheet Docker

### Vérifier la version de Docker

docker --version

### lister les conteneurs actifs

docker ps

### lister tous les conteneurs 

docker ps -a

### Lister les images locales

docker images

### exécuter un conteneur Nginx

docker run -d -p 8080:80 --name web nginx
#qui pull + create + start + exec le conteneur

### supprimer un conteneur

docker rm -f web

### Supprimer une image

docker rmi nginx



### Créer un volume

docker volume create mon_volume

### Lister les volumes

docker volume ls

### supprimer un volume

docker volume rm mon_volume

### Lancer les services en arrière-plan

docker-compose up -d

### arrêter les services

docker-compose down

### rebuild des images et démarrage

docker-compose up --build

### afficher les logs

docker-compose logs -f

### Initialiser le Swarm

docker swarm init

### créer un service Nginx

docker service create --name web -p 80:80 nginx

### Lister les services Swarm

docker service ls

### Mettre à jour un service (changer l'image)

docker service update --image nginx:alpine web

### supprimer un service

docker service rm web

### Déployer une stack depuis un fichier Compose

docker stack deploy -c docker-compose.yml mystack

### supprimer une stack

docker stack rm mystack
