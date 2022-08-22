# DevOPs
#!/bin/bash

echo "atualizando o servidor"
sudo apt update 
sudo apt upgrade -y
sudo apt install apache2 -y
sudo apt install unzip -y

echo "Baixando o arquivo para o servidor"

cd /tmp
wget https://github.com/denilsonbonatti/linux-site-dio/archive/refs/heads/main.zip
unzip main.zip
cd /linux-site-dio
cp -R * /var/www/html/
