# Docker Comandos

**Listando, parando, excluindo containers:**

- `docker ps` **** exibe todos os containers em execução no momento.
- `docker ps -a` **** exibe todos os containers, independentemente de estarem em execução ou não.
- `docker run -it NOME_DA_IMAGEM` **** conecta o terminal que estamos utilizando com o do container.
- `docker start ID_CONTAINER` **** inicia o container com id em questão.
- `docker stop ID_CONTAINER` **** interrompe o container com id em questão.
- `docker start -a -i ID_CONTAINER` **** inicia o container com id em questão e integra os terminais, além de permitir interação entre ambos.
- `docker rm ID_CONTAINER` **** remove o container com id em questão.
- `docker container prune` **** remove todos os containers que estão parados.
- `docker rmi NOME_DA_IMAGEM` **** remove a imagem passada como parâmetro.
- `docker run -d -P --name NOME dockersamples/static-site` **** ao executar, dá um nome ao container.
- `docker run -d -p 12345:80 dockersamples/static-site` **** define uma porta específica para ser atribuída à porta 80 do container, neste caso 12345.
- `docker run -d -P -e AUTHOR="Fulano" dockersamples/static-site` **** define uma variável de ambiente AUTHOR com o valor *Fulano* no container criado.

**docker system prune --all --force --volumes** - Excluir todas as imagens

**Trabalhando com Volumes:**

- `docker run -v "[CAMINHO_VOLUME_LOCAL:]CAMINHO_VOLUME_CONTAINER" NOME_DA_IMAGEM` **** cria um volume no respectivo caminho do container, caso seja
especificado um caminho local monta o volume local no volume do
container.
- `docker inspect ID_CONTAINER` **** retorna diversas informações sobre o container.
    
    `docker  images`lista as imagens instaladas****
    

**Dockerfile buildando, publicando e baixando imagens**

- `docker build -f Dockerfile` **** cria uma imagem a partir de um Dockerfile.
- `docker build -f CAMINHO_DOCKERFILE/Dockerfile -t NOME_USUARIO/NOME_IMAGEM` **** constrói e nomeia uma imagem não-oficial informando o caminho para o Dockerfile.
- `docker login` **** inicia o processo de login no Docker Hub.
- `docker push NOME_USUARIO/NOME_IMAGEM` **** envia a imagem criada para o Docker Hub.
- `docker pull NOME_USUARIO/NOME_IMAGEM` **** baixa a imagem desejada do Docker Hub.

**Trabalhando com redes**

- `hostname -i` **** mostra o ip atribuído ao container pelo docker (funciona apenas dentro do container).
- `docker network create --driver bridge NOME_DA_REDE` **** cria uma rede especificando o driver desejado.
- `docker run -it --name NOME_CONTAINER --network NOME_DA_REDE NOME_IMAGEM` **** cria um container especificando seu nome e qual rede deverá ser usada.
    
    `docker network inspect`<rede> **** Lista as informações da rede inclusive os containers configurados
    

**Docker-compose**

- `docker-compose build` **** Realiza o build dos serviços relacionados ao arquivo docker-compose.yml, assim como verifica a sua sintaxe.
- `docker-compose up` **** Sobe todos os containers relacionados ao docker-compose, desde que o build já tenha sido executado.
- `docker-compose down` **** Para todos os serviços em execução que estejam relacionados ao arquivo docker-compose.yml.
- `docker-compose ps` - lista os serviços que estão rodando.
- `docker exec -it alura-books-1 ping node2`executa o comando `ping node2` dentro do container `alura-books-1`
