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
     
     $ docker container attach servidor-debian


 ## Executando container - Etapa 2
 
   ### Uma vez conectado ao container, verifique o nome da máquina e as configurações de rede: 
      $ hostname 
      $ ip a 
      $ exit

   ### Para remover apenas o container em execução e conservar a imagem base, execute: 
   
      $ docker container rm -f 
      $ (docker ps -qa)
      $ docker container ls -a
      
      
   # GERENCIAR IMAGENS NO DOCKER
   
     ## Comandos de Gerenciamento – ETAPA 1           
         
     ### Liste as imagens e verifique o histórico de comandos utilizados para sua construção: 
        $ docker image ls 
        $ docker history debian


      ### Para inspecionar uma imagem, utilizamos o seguinte comando: 
         $ docker inspect debian2

      ### Antes de criar uma nova imagem, execute os seguintes comandos:
         $ docker container run -dit --name servidor-debian debian 
         $ docker container exec servidor-debian apt-get update 
         $ docker container exec servidor-debian apt-get install apache2 -y
         
      
