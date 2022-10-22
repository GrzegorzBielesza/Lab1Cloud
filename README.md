# Lab1Cloud

Aby zbudować obraz:
* eval $(ssh-agent)
* ssh-add <ścieżka do klucza prywatnego>
* docker build --ssh default=<ścieżka do klucza prywatnego> . -f Dockerfile-webApp -t gbielesza/lab2.v1

Aby uruchomić aplikację
* docker run -d -it --name lab2-container -p 8080:8080 -t gbielesza/lab2.v1 

Aby zastopować działanie aplikacji
* docker stop lab2-container

Aby wypushować do Docker Huba
* docker commit lab2-container gbielesza/lab2.v1
* docker push gbielesza/lab2.v1

Linki do repozytoriów:
* Github: https://github.com/GrzegorzBielesza/Lab1Cloud
* DockerHub: https://hub.docker.com/repository/docker/gbielesza/lab2.v1