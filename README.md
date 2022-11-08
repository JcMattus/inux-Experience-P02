# :penguin: Linux Experience - Projeto 02
Projeto do Bootcamp Linux Experience - Script de Provisionamento de um Servidor Web (Apache).


## :page_with_curl:

#!/bin/bash

echo "Atualizando o servidor..."
apt-get update
apt-get upgrade -y
apt-get install apache2 -y
apt-get install unzip -y


echo "Baixando e copiando os arquivos da aplicação..."

cd /tmp
wget https://github.com/denilsonbonatti/linux-site-dio/archive/refs/heads/main.zip

unzip main.zip

cd linux-site-dio-main

cp -R * /var/www/html/
