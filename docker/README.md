
### construire l'image docker
docker build . -t rpalvair/spring-boot:initial

### vérifier que l'image est bien construite
docker images

### lancer le container
docker run -p 8080:8080 rpalvair/spring-boot:initial

### vérifier que le conteneur est lancé
docker container ls

### arreter le container
docker stop <id>

### connaitre l'adresse ip de la docker-machine
docker-machine ip default


### Demarrer un registry en local
docker run -d -p 5000:5000 --restart=always --name registry registry:2
 
### Taguer une image avec le format 'local registry'
docker tag a880a54fa6cc localhost:5000/spring-boot:initial

### Pusher une image dans le registry
docker push localhost:5000/spring-boot

### Effacer les images en local
docker image remove a880a54fa6cc

### Recuperer une image du local registry
docker pull localhost:5000/spring-boot:initial
