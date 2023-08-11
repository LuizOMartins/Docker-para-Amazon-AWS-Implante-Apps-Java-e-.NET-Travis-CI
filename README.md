# Docker-para-Amazon-AWS-Implante-Apps-Java-e-.NET-Travis-CI

o que é Docker: empresa/teclogia.
- Open Source
- Containers são mais leves que maquinas virtuais.

Uma vez Dockenizada a aplicação, ela pode ser executada em qualquer lugar, sem problemas de compatibilidade.

DockerFile: arquivo de configuração do Docker.
Docker Composer: arquivo de configuração do Docker para multi-container.
- combina containers para execução de uma aplicação.
Docker Hub: repositório de imagens Docker.


Errata:
Docker para Windows (Docker Desktop)
Em 27 de maio de 2020, a Microsoft lançou o Windows 10 build 2004 (primavera de 2020) que permite executar o Docker Deskop em todas as edições do Windows 10, incluindo Home graças ao WSL 2.

A partir de agosto de 2020, a Microsoft habilitou o suporte WSL 2 para versões 1903 + 1909 do Windows 10.

Nos anos anteriores, você só podia executá-lo no Windows Pro, Enterprise ou qualquer edição que tivesse o Hyper-V disponível, mas desde agosto de 2020 praticamente todas as versões com suporte do Windows 10 podem usar o Docker Desktop.

Você também pode executar o VirtualBox 6+ ao lado do Docker Desktop, caso tenha projetos mais antigos usando o VirtualBox (talvez com o Vagrant também).

_______________________________________________________________________

- Aplicação Java:

mvn clean package: gera o arquivo .jar da aplicação.
no caso foi para pasta target onde o dockerfile identifica o jar gerado da aplicação.

Exemplo no DockerFile:

ADD app/target/docker-to-aws-with-java-0.0.1-SNAPSHOT.jar app.jar

docker-to-aws-with-java-0.0.1-SNAPSHOT.jar: o noem fica configurado no pom.xml da aplicação.

Docker Compose:
ports:
    - "3308:3306"
- porta do container: porta do host.

Comando:
docker-compose up -d --build
- build: para construir a imagem.
- up: para subir o container.
- -d: para rodar em background.

docker ps -a
- lista todos os containers.
ps: processos.
-a : all.


docker-compose down
- para desligar o container.

Conectar em uma imagem (container): mysql
docker exec -it <ID> mysql -u docker -p

_______________________________

CCP: Certificate of Cloud Practitioner;
- Certificação da AWS.
- Como é a prova: 65 questões, 90 minutos, 70% de acerto.

Ideia de roteiro de Certificações:
Pratictioner -> Solutions Architect -> Developer -> SysOps -> DevOps Engineer -> Solutions Architect Professional -> DevOps Professional:

AWS Certified Cloud Practitioner.
Código de desconto: AWLA276F0E59 (aplicar no checkout, última etapa).

_______________________________

Atenção ao utilizar a AWS:

- não esquecer maquinas rodando.
- Certificar que o serviço é FREE.
- Estude aprenda e apague maquinas e instâncias.

Travis

_______________________________

Instalando AWS  CLI: (Command Line Interface)   
Local onde fica : C:\Users\<usuario>\.aws
- aws configure: para configurar a AWS.

_______________________________

EC2: Elastic Compute Cloud.
- Serviço de computação em nuvem que permite a criação e utilização de máquinas virtuais na AWS.
SSH: Secure Shell.

_______________________________


RDS: Relational Database Service.
- Serviço de banco de dados relacional na AWS.
- MySQL, PostgreSQL, Oracle, SQL Server, MariaDB, Amazon Aurora.

_______________________________

http://localhost:8080/swagger-ui.html#/PersonEndpoint/findAllUsingGET

_______________________________

Principais Comandos Docker:

docker ps -a: lista todos os containers.
docker images: lista todas as imagens.
docker rm <ID>: remove um container.
docker rmi <ID>: remove uma imagem.
docker exec -it <ID> bash: entra no container.
docker stop <ID>: para o container.
docker start <ID>: inicia o container.
docker logs <ID>: mostra os logs do container.
docker-compose up -d --build: sobe o container.
docker-compose down: desliga o container.

docker run -d -p 80:8080  docker-to-aws-with-java
- -d: para rodar em background.
- -p: para mapear a porta do container com a porta do host.
- docker-to-aws-with-java: nome da imagem.

Contianer: é uma instancia de uma imagem.
Imagem: é um template para criar um container.

uma imagem é uma representação estática e autossuficiente de uma aplicação, enquanto um container é uma instância em execução dessa imagem, com seu próprio ambiente isolado. O uso de imagens e containers no Docker facilita a implantação, o gerenciamento e a escalabilidade de aplicativos, tornando a distribuição de software mais consistente e eficiente em diferentes ambientes.



_______________________________

ECR: Elastic Container Registry.
- Serviço de registro de imagens de containers na AWS.


ECS: Elastic Container Service.
- Serviço de orquestração de containers na AWS.

Cluster ECS: é um grupo de instâncias EC2 que são executadas em um ou mais locais de disponibilidade. Um cluster pode conter vários serviços e tarefas. 

Cluster: é um grupo de instâncias EC2 que são executadas em um ou mais locais de disponibilidade. Um cluster pode conter vários serviços e tarefas.

Task Definition: é um arquivo JSON que descreve uma ou mais tarefas, definindo parâmetros como CPU, memória, porta de contêiner, imagem de contêiner, etc.
