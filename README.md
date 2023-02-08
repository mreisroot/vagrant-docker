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

Caso sua máquina tenha mais de uma placa de rede, o Vagrant perguntará qual interface pretende usar como ponte entre a VM e o host.

Digite o número correspondente à placa que utiliza para se conectar à Internet.

Por exemplo,

```
0: eth0
1: wlan0
```

Digite 0 caso utilize a placa eth0 (placa de conexão Ethernet, conexão cabeada) para se conectar à Internet;

Digite 1 caso utilize a placa wlan0 (placa de Wi-Fi, conexão sem fio) para se conectar à Internet.

Para acessar a API servida pelo NGINX, digite na barra de pesquisa de um navegador web:

`<ip_do_servidor>:8080`

No caso deste projeto, a pesquisa ficará assim:

`192.168.15.55:8080`

Altere o endereço IP de acordo com a sua rede no arquivo **Vagrantfile**.
