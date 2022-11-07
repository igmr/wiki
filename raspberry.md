# Raspberry Pi 4

<a name="contenido"></a>
## Contenido
- [Sistema](#os)
	- [Actualización de repositorio](#update)
	- [Actualización de sistema](#upgrade)
	- [Instalación de software común](#comun)
- [Software de termianl](#shell)
	- [ufw](#ufw)
	- [neofetch](#neofetch)
	- [zsh](#zsh)
	- [OhMyZsh](#ohmyzsh)
- [Instalación de software](#software)
	- [Simple Screen Recorder](#simplescreenrecorder)
	- [Dia](#dia)
	- [Visual Studio Code](#vscode)
- [Interpretes y compiladores](#code)
- [Apache](#apache)
- [php](#php)
- [Composer](#composer)
- [Mariadb](#mariadb)


<a name="os"></a>
## Sistema

<a name="update"></a>
### Actualización de respositorio
Actualización de lista de paquetes Apt
```sh
sudo apt update
```
[Volver a lista de contenido](#contenido)

<a name="upgrade"></a>
### Actualización de sistema
Busqueda de paquetes que se puedan actualizar, sin eliminar ningun paquete.
```sh
sudo apt upgrade
```
[Volver a lista de contenido](#contenido)

<a name="comun"></a>
### Instalación de software común
```sh
sudo apt install software-properties-common
```
[Volver a lista de contenido](#contenido)

<a name="shell"></a>
## Software de terminal

<a name="ufw"></a>
### ufw
FireWall
```sh
sudo apt install ufw -y
```
[Volver a lista de contenido](#contenido)

<a name="neofetch"></a>
### neofetch
Información del sistema
```sh
sudo apt install neofetch -y
```
[Volver a lista de contenido](#contenido)

<a name="zsh"></a>
### zsh
Instalación de Zsh
```sh
sudo apt install zsh zsh-common zsh-doc -y
```
[Volver a lista de contenido](#contenido)

<a name="ohmyzsh"></a>
### Oh My Zsh
Instalación de Oh My Zsh [github](https://github.com/ohmyzsh/ohmyzsh)
```sh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
**Intalación de plugin de autosuggestions (opcional)**

```sh
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh
```
**Definir zsh como terminal por default**

```sh
chsh -s `which zsh`
echo $SHELL
```

**configuración de OhMyZsh (opcional)**
```sh
nano ~/.zshrc
```

```sh
...
# Cmabio de tema
ZSH_THEME="arrow"

...

# Agregar plugin
plugins=(
	vscode
	git
	zsh-autosuggestions)

...

# Configuración de alias
alias zshrc="nano ~/.zshrc"
alias src="sources ~/.zshrc"
alias cls="reset"
alias spark="reset && php spark serve"
alias dev="reset && npm run dev"
alias start="reset && npm run start"
alias dev="reset && npm run dev"
alias sql="mysql -u root -p1234567890"
```
[Volver a lista de contenido](#contenido)

<a name="software"></a>
## Instalación de software

<a name="simplescreenrecorder"></a>
### Simple Screen Recorder
Programa de grabación de pantalla [github](https://github.com/MaartenBaert/ssr)
```sh
sudo apt install simplescreenrecorder -y
```
[Volver a lista de contenido](#contenido)

<a name="dia"></a>
### Dia
Programa para crear diagramas [web](http://dia-installer.de)
```sh
sudo apt install dia -y
```
[Volver a lista de contenido](#contenido)

<a name="vscode"></a>
### Visual Studio Code
Editar de codigo [web](https://code.visualstudio.com)
```sh
sudo apt install code -y
```
[Volver a lista de contenido](#contenido)

<a name="code"></a>
## Interpretes y compiladores

<a name="apache"></a>
### Apache
```sh
sudo apt install apache2 apache2-utils apache2-doc
a2enconf apache2-doc
```
[Volver a lista de contenido](#contenido)

<a name="php"></a>
### php
**Instalación de php version 7.4**
```sh
# Instalación de php version 7.4
sudo apt install php7.4 libapache2-mod-php7.4 php7.4-mysql php7.4-common php7.4-cli php7.4-common php7.4-json php7.4-opcache php7.4-readline php7.4-mbstring php7.4-gettext php7.4-curl php7.4-intl php7.4-dom -y
```

**Habilitar apache**

```sh
sudo a2enmod php7.4
```

**Reiniciar apache**

```sh
sudo systemctl restart apache2
```
[Volver a lista de contenido](#contenido)

<a name="composer"></a>
### Composer

```sh
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '55ce33d7678c5a611085589f1f3ddf8b3c52d662cd01d4ba75c0ee0459970c2200a51f492d557530c71c15d8dba01eae') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```

**Mover composer**

```sh
sudo mv composer.phar /usr/local/bin/composer
```
[Volver a lista de contenido](#contenido)

<a name="mariadb"></a>
### Mariadb
**Instalación**

```sh
sudo apt install mariadb-server mariadb-client mariadb-common -y
```

**Habilitar Mariadb**

```sh
sudo systemctl enable mariadb
# Configuración de Mariadb
sudo mysql_secure_installation
# Opciones de configuración
[Y]
[Y]
[Y]
1234567890
1234567890
[Y]
[n]
[Y]
[Y]
```

**Configuración Mariadb**
```sh
sudo mysql_secure_installation

[Y]
[Y]
[Y]
<password>
<repeat-password>
[Y]
[n]
[Y]
[Y]
```
[Volver a lista de contenido](#contenido)




