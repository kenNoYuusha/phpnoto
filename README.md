# **Instalacion** 
- Agregar repositorio app de php, para tener sus versiones mas recientes.
- Actualizar repositorios
- Instalar versiones de php deseadas
- Verificar si la instalacion se hizo correctamente (opcional)
- Instalar apache
- Ajustar configuracion del firewall
- Habilitar php en apache
- Deshabilitar php en apache
- Comandos apache
- Verificar ruta


#### Agregar repositorios

```sh
  $ sudo apt update
  $ sudo apt install lsb-release ca-certificates apt-transport-https software-properties-common -y
  $ sudo add-apt-repository ppa:ondrej/php
```
#### Actualizar repositorios

```sh
  $ sudo apt update
  $ sudo apt upgrade
```

#### Instalar versiones de php 

```sh
  $ sudo apt install php8.0
```

#### Verificar instalacion

```sh
   $ sudo dpkg --get-selections | grep php
```

#### Instalar apache

```sh
  $ sudo apt install apache2
```

#### Ajustar configuracion Firewall

```sh
  $ sudo ufw app list 
  $ sudo ufw allow 'Apache' 
  $ sudo ufw status 
```

| List | 
| ------ | 
| `Apache` | 
| Apache Full | 
| Apache Secure | 

#### Habilitar php en apache

```sh
  $ sudo a2enmod php8.0
```

#### Deshabilitar php en apache

```sh
  $ sudo a2dismod php8.0
```

#### Comandos apache

```sh
  $ sudo systemctl status apache2  
  $ sudo systemctl start apache2
  $ sudo systemctl stop apache2 
  $ sudo systemctl restart apache2 
```

### Verificar ruta

> Ir a /var/www/html crear un index.php con la sentencia phpinfo()

> Ir a localhost en el navegador.

> Configurar php ini para que muestre los errores
