# devops-training-docker

## Par Nathan Bertaud, B3 dev A

- 3 
    - a) la commande est : docker run -d --name mon-nginx -p 80:80 nginx 
    - b) la commande est : docker ps

    - c) les commandes sont :
        1. docker exec -it mon-nginx bash
        2. cd usr/share/nginx/html
        3. echo "Hello World" > index.html
        4. exit
    
    - d) la commande est : docker run -d --name mon-nginx-volume -p 80:80 -v C:/Users/"Nathan Bertaud"/Desktop/devops-training-docker/html:/usr/share/nginx/html nginx

    - e) la commande est : docker remove mon-nginx-volume

    - f) la commande est : docker cp C:/Users/"Nathan Bertaud"/Desktop/devops-training-docker/html/index.html d46dcc07ad6d:/usr/share/nginx/html/index.html

- 4
    - a) voir Dockerfile

    - b) COPY html/index.html /usr/share/nginx/html/index.html dans le Dockerfile
    - c1) la différence est que dans la question 3, on utilise un volume monté qui permet de modifier le fichier index.html en temps réel, tandis que dans la question 4, on utilise une image Docker qui contient le fichier index.html au moment de sa création. L'avantage du volume est qu'il permet de modifier le fichier sans avoir à reconstruire l'image, tandis que l'avantage de l'image est qu'elle est plus portable et peut être déployée sur n'importe quel serveur Docker.

    - c2) les avantages de la méthode COPY sont que l'image est plus légère et que le fichier index.html est inclus dans l'image, ce qui permet de ne pas avoir à le copier manuellement. Les inconvénients sont que si le fichier index.html change, il faut reconstruire l'image pour que les changements soient pris en compte. La méthode mount volume permet de modifier le fichier index.html sans avoir à reconstruire l'image, mais l'image est plus lourde car elle inclut le volume monté.