# Instalación

## Configuracion del sistema de virtualitzacion (IsardVDI)
---
Instal·la Apache

sudo apt install apache2 -y

Activa i inicia el servei:

sudo systemctl enable apache2
sudo systemctl start apache2

Verifica l’estat:

sudo systemctl status apache2
---
Instal·la MySQL

Ubuntu 24.04 ja inclou el paquet mysql-server als repositoris oficials (versió 8.0 o superior):

sudo apt install mysql-server mysql-client -y

Inicia i habilita el servei:

sudo systemctl enable mysql
sudo systemctl start mysql

Configura de MySQL:
Accés a la consola de MySQL

sudo mysql

Creació de la base de dades

CREATE DATABASE bbdd;

Creació de l’usuari local

CREATE USER 'usuario'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
GRANT ALL PRIVILEGES ON bbdd.* TO 'usuario'@'localhost';
FLUSH PRIVILEGES;
EXIT;
---
Instal·la PHP i extensions comunes

Ubuntu 24.04 inclou PHP 8.3 als repositoris estàndard:

sudo apt install php libapache2-mod-php php-mysql php-curl php-gd php-mbstring php-xml php-zip php-json php-cli -y

Reinicia Apache per carregar PHP:

sudo systemctl restart apache2

Verifica la versió de PHP:

php -v

Crea un fitxer de prova:

echo "<?php phpinfo(); ?>" | sudo tee /var/www/html/info.php

Visita http://localhost/info.php per veure la informació de PHP.

    🔒 Mesura de seguretat: Un cop hagis verificat que funciona, elimina el fitxer:

    sudo rm /var/www/html/info.php
