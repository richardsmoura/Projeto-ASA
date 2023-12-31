# Projeto-ASA

O projeto ASA consiste em um projeto realizado para a disciplina de Administração de Sistemas Abertos(ASA), o qual consiste em realizar um laboratório para realizar um conjunto de serviços em Containers Docker. De resumo, a infraestrutura foi realizada em 3 Sprints:


1º Sprint - Proxy Reverso (Nginx) com um virtualhost para redirecionamento para o Web Content, primeira zona direta "ifrn.asa.br" (BIND), Criação de um Web Content o qual foi criado com um Conjunto de Wordpress e DB (MySQL).

2º Sprint - Proxy Reverso (Nginx) com um segundo virtualhost para um Web Contente 02, segunda zona direta "diaren.ifrn.asa.br"(BIND), Criação do 2 Web Contente em Wordpress com as especificações anteriores do Sprint 1.

3ª Sprint - Proxy Reverso (Nginx) com mais um virtualhost para o Serviço de email, um container com o Postfix e Dovecote, Webmail para realização de transmissão de mensagens do servidor de e-mail, servidor SSH para acesso remoto seguro.


Para a realização e testagem do Projeto é necessário ter o Docker e o Docker Compose instalado no seu SO. Caso não tenha, poderá acessar acessar a documentação oficial: https://docs.docker.com/engine/install/
Após realizar as instalações e dependências, podemos prosseguir para levantar a infraestrutura.

Para Clonar os arquivos do GitHub:
git clone https://github.com/richardsmoura/Projeto-ASA.git

Para build e subir os containers:
docker compose up --build

Para kill containers:
docker compose down
