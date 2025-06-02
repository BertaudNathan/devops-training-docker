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