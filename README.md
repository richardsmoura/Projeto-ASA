# Projeto-ASA

O projeto ASA consiste em um projeto realizado para a disciplina de Administração de Sistemas Abertos(ASA), o qual consiste em realizar um laboratório para realizar um conjunto de serviços em Containers Docker. De resumo, a infraestrutura foi realizada em 3 Sprints:

| Sprint | Tarefas                                                                                                           |
|--------|--------------------------------------------------------------------------------------------------------------------|
| 1      | - Configuração de Proxy Reverso (Nginx) com um virtualhost para o Web Content                                     |
|        | - Criação da primeira zona direta "ifrn.asa.br" no BIND                                                           |
|        | - Criação de um Web Content com um Conjunto de Wordpress e DB (MySQL)                                             |
| 2      | - Configuração de Proxy Reverso (Nginx) com um segundo virtualhost para um segundo Web Content                  |
|        | - Criação da segunda zona direta "diaren.ifrn.asa.br" no BIND                                                     |
|        | - Criação do segundo Web Content em Wordpress com as especificações do Sprint 1                                    |
| 3      | - Configuração de Proxy Reverso (Nginx) com mais um virtualhost para o Serviço de e-mail                           |
|        | - Configuração de um container com Postfix e Dovecote                                                              |
|        | - Implementação de Webmail para a transmissão de mensagens no servidor de e-mail                                   |
|        | - Configuração de um servidor SSH para acesso remoto seguro                                                         |

## Antes de Testar os Serviços:

Importantante criar/modificar algumas coisas, como por exemplo o endereço IP dos arquivos DNS, logo que os nomes serão de extrema importância, caso algo acontece de errado verifique os volumes ou o caminho de diretórios que está apontando o Dockerfile do determinado container.
Para a realização e testagem do Projeto é necessário ter o Docker e o Docker Compose instalado no seu SO. Caso não tenha, poderá acessar a documentação oficial: https://docs.docker.com/engine/install/
Após realizar as instalações e dependências, podemos prosseguir e fazer algumas verificações:

1 - Para utilizar os serviços confirme que o DNS está funcionando. Caso tenha resposta prossiga para o passo 2.

2 - Ao confirmar os endereços de DNS, pode acessar o Web Content 01 utilizando o endereço: ifrn.asa.br (ou endereço que chegou a escolher). Para o Web Content 02: www.diaren.ifrn.asa.br (ou o que você escolheu).

3 - Para entrar no webmail, basta acessar: mail.ifrn.asa.br/rainloop/ - Caso seja a primeira vez configurando, terá que acessar: mail.ifrn.asa.br/rainloop/?admin - Poderá ter mais informações sobre configurações do Webmail em: https://www.rainloop.net/docs/

4 - Para utilizar o SSH, baixar realizar o acesso via terminal ou putty informando o para o ip e a porta 22. O logon dos users, pode ser acessado/modificado dentro do Dockerfile.ssh.

## Subindo os serviços:

Para Clonar os arquivos do GitHub:
```bash
git clone https://github.com/richardsmoura/Projeto-ASA.git
```
Para build e subir os containers:
```bash
docker-compose up --build
```
Para kill containers:
```bash
docker-compose down
```


Outras documentações que poderão te ajudar:

DNS BIND: https://bind9.readthedocs.io/en/v9.18.21/

NGINX HTTP: https://nginx.org/en/docs/

POSTFIX: https://www.postfix.org/documentation.html

DOVECOTE: https://www.dovecot.org/


Espero que tenha gostado do projeto ou te ajudado em algum que esteja desenvolvendo.
