# Comandos essenciais do Docker

   ## Comandos Nativos

   ### Logue com usuário suporte e execute o comando que exibe informações do ambiente: 
    $ docker system info 

   ### Para listar containers, imagens e redes no Docker, execute os comandos: 
    $ docker container ls 
    $ docker image ls 
    $ docker network ls

   ### Para pesquisar imagem Debian no Docker Hub, execute o comando: 
    $ docker search debian
    

 ## Executando container - Etapa 1
 
 ### Baixe a imagem do servidor Debian e verifique se o mesmo aparece na lista de imagens: 
 
      $ docker image pull debian 
      $ docker image ls

   ### Execute um container debian e verifique se o mesmo aparece na lista de containers em execução: 
     
     $ docker container run -dit --name servidor-debian --hostname servidor-debian debian 
     $ docker container ls

   ### Para se conectar ao container em execução, execute o seguinte comando:
     
     $ docker container attach servidor-debian3
