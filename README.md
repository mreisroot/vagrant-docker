# Máquina Vagrant provisionada pelo shell com container do NGINX 

Neste projeto, há a criação de uma máquina virtual Vagrant que irá hospedar um container do servidor web NGINX.

O provisionamento da máquina virtual e do container será feito através de um shell script.

## Executando o provisionamento

Após a criação da máquina, será executado o arquivo script.sh, que realizará as seguintes etapas:

1. Atualizar os repositórios do Ubuntu

2. Adicionar o repositório do Docker

3. Instalar o Docker

4. Criar o container do NGINX com o diretório /site montado no diretório /usr/share/nginx/html do container.

## Resultados

Após a criação e provisionamento, a máquina virtual terá:

1. O Docker instalado

2. Um diretório que irá conter o arquivo index.html

3. Um container do servidor NGINX que servirá a API do site [VIACEP](https://viacep.com.br/)

## Como usar este projeto

Para criar a máquina virtual Vagrant, execute o comando:

`vagrant up`

Para acessar a API servida pelo NGINX, digite na barra de pesquisa de um navegador web:

`192.168.56.11`

Para destruir a máquina virtual, execute:

`vagrant destroy -f`
