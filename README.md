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

