# kubedev
repositório para documentar as tarefas do desafio docker do curso kubedev

# Kubedev - Desafio Docker Questão 01 e 02 - MongoDB + Mongo Express

Execute os comandos para criar os 4 bancos de dados listados com containers, e use
como se tivesse instalado eles localmente na sua máquina (Não esquece de garantir
que não vai perder os dados caso o container seja excluido).

MongoDB
MariaDB
PostgreSQL
Redis

## 🚀 Começando

Através dessa questão iremos ver como executar o MongoDB em um contêiner Docker

- Iremos configurar o MongoDB como um contêiner Docker
- Configurar o Docker com docker-compose
- Criar um arquivo docker-compose para criar o contêiner MongoDB
- Instalar o Mongo Express em um contêiner para gerenciarmos o MongoDB pela interface Web
- Criar uma rede dedicada e um volume para o projeto
- Adicionar uma verificação de saúde do contêiner

### 📋 Pré-requisitos

Para este projeto utilizei o ubuntu 20.04 rodando via WSL no Windows10, os passos a seguir podem ser feitos no Ubuntu ou no WSL

### 🔧 Instalação

1. Atualizar os pacotes existentes:

sudo apt update && sudo apt upgrade -y

2. Instalar os pacotes de pré requisitos

sudo apt install apt-transport-https ca-certificates curl software-properties-common

3. Adicionar a chave GPG do repositório oficial do Docker

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

4. Adicionar o repositório docker oficial às fontes APT.

sudo add-apt-repository \
"deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

 5. Atualize a lista de pacotes do Ubuntu

 sudo apt update

 6. Instale o Docker

 sudo apt install docker

 7. Instale o docker-compose

 sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

8. Aplique as permissões necessárias ao executável do docker-compose

sudo chmod +x /usr/local/bin/docker-compose


Finalizado os pré requisitos agora vamos a instalação do Mongo

Para este exercício foi criado um arquivo docker-compose.yml que levanta todo o ambiente necessário do mongodb e o mongo express com volume criado e acesso pela url http://localhost:8081
## ⚙️ Executando os testes

- Para verificar a execução do contêiner rode o comando na pasta onde o projeto foi baixado:

sudo docker-compose up -d

- Acesse pela url http://localhost:8081 o usuário e senha para login estão no arquivo docker-compose nas variáveis de ambiente do Mongo
### 🛠️ Construído com

* [Docker]
* [Docker-Compose]
* [MongoDB]
## ✒️ Autores

* **Thiago dos Santos** - (https://www.linkedin.com/in/tdsantos1981/)

## 📄 Licença

Este projeto está sob a licença (Unlicense) - veja o arquivo [LICENSE.md](https://github.com/tdsantoscursos/mongo/blob/main/LICENSE) para detalhes.
