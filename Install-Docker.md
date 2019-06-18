Instalar o Docker no CentOS Server
-Etapa 1

        Logue com usuário suporte e instale yum-utils, que fornece o utilitário yum-config-manager: 
        $ sudo yum install yum-utils device-mapper-persistent-data lvm2 -y1

       -- Em seguida, configure o repositório estável, através do seguinte comando: 
        $ sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

        -- Instale o Docker, através do seguinte comando: 
        $ sudo yum install docker-ce docker-ce-cli containerd.io -y3

Desinstalar versões antigas
Versões mais antigas do Docker eram chamadas docker ou docker-engine. Se estes estiverem instalados, desinstale-os juntamente com as dependências associadas.
        $ sudo yum remove docker \
        docker-client \
        docker-client-latest \
        docker-common \
        docker-latest \
        docker-latest-logrotate \
        docker-logrotate \
        motor de encaixe 
 O conteúdo de /var/lib/docker/ incluindo imagens, contêineres, volumes e redes, é preservado. O pacote do Docker CE agora é chamado de docker-ce.
 
Kleber Jose Vilarim

Instalar o Docker no CentOS Server

-Etapa 2

        Execute o comando para ativar e iniciar o Docker na inicialização do sistema: 
                $ sudo systemctl enable docker 
                $ sudo systemctl start docker
        
        Adicione o usuário suporte ao grupo do Docker: 
                $ sudo gpasswd -a suporte docke

        Verifique qual é a versão instalada do Docker: 
                $ sudo docker version
        
        


