
### construire l'image docker
docker build . -t rpalvair/spring-boot:latest

### vérifier que l'image est bien construite
docker images

### lancer le container
docker run -p 8080:8080 spring-boot/initial

### vérifier que le conteneur est lancé
docker container ls

### arreter le container
docker stop <id>

### connaitre l'adresse ip de la docker-machine
docker-machine ip default
