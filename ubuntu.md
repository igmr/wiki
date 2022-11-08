# Ubuntu

<a name="subir"></a>
## Lista de contenido
- [Sistema](#actualizacion)
	- [Actualización de repositorios](#repositorio)
	- [Actualización de sistema](#sistema)
	- [Instalación de software común](#comun)
- [Instalación de software para terminal](#terminal) 
	- [snap](#snap)
	- [zsh](#zsh)
	- [ohmyzsh](#ohmyzsh)
	- [neofetch](#neofetch)
	- [git](#git)
- [Instalación de software](#software)
	- [Simple Screen Recorder](#simplescreenrecorder)
	- [ufw](#ufw)
	- [Ghostwrite](#ghost)
	- [Dia](#dia)
	- [StarUml](#staruml)
	- [Visual Studio Code](#vscode)
	- [Sublime Text 3](#sublime)
	- [Chrome](#chrome)
	- [1Password](#password)
	- [Postman](#postman)
	- [Hyper](#hyper)
	- [Workbench](#workbench)
	- [Vlc](#vlc)
	- [Libre Office](#libreoffice)
	- [gParted](#gparted)
	- [Filezilla](#filezilla)
- [Instalación de interpretes y compiladores](#code)
	- [apache](#apache)
	- [php8.1](#php)
	- [composer](#composer)
	- [node](#node)
	- [mysql](#mysql)
	- [Postgresql](#postgresql)
	- [C++](#c)
---

<a name="actualizacion"></a>
## Sistema

<a name="repositorio"></a>
### Actualización de repositorios

Actualización de lista de paquetes Apt.

```sh
sudo apt update
```

[Volver a lista de contenido](#subir)

<a name="sistema"></a>
### Actualización del sistema

Busqueda de paquetes que se puedan actualizar, sin eliminar ningun paquete.

```sh
sudo apt upgrade -y
```

[Volver a lista de contenido](#subir)

<a name="comun"></a>
### Instalación de software común

```sh
sudo apt install software-properties-common
sudo apt install ubuntu-restricted-extras
```

[Volver a lista de contenido](#subir)

<a name="terminal"></a>
## Instalación de software de terminal

[Volver a lista de contenido](#subir)

<a name="snap"></a>
### snap

Gestor de paquetes Snap

```sh
sudo apt install snapd -y
# Depues de terminar la instación se debe reinicar el equipo
sudo reboot
# Depues de iniciar sesión, instalamos el core de snap
sudo snap install core
```

[Volver a lista de contenido](#subir)

<a name="zsh"></a>
### zsh

Instalación de shell Zsh

```sh
sudo apt install zsh zsh-common zsh-doc -y
```

[Volver a lista de contenido](#subir)

<a name="ohmyzsh"></a>
### OhMyZsh

```sh
# Instalación
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# Establecer zsh por defecto
chsh -s `which zsh`

echo $SHELL
```
**Instalación de plugin autosuggestions**
```sh
# Instalación de plugin autosuggestions
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions

source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh
```

**Configuración de ~/.zshrc (opcional)**
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

[Volver a lista de contenido](#subir)

<a name="neofetch"></a>
### neofetch

Muestra información del sistema

```sh
sudo apt install neofetch -y
```

[Volver a lista de contenido](#subir)

<a name="git"></a>
### git

Sistema de control de versiones.

```sh
sudo apt install git -y
```

[Volver a lista de contenido](#subir)

<a name="software"></a>
### Instalación de software

<a name= "simplescreenrecorder"></a>
### Simple Screen Recorder

Programa para grabar pantalla.

```sh
sudo apt install simplescreenrecorder -y
```

[Volver a lista de contenido](#subir)

<a name="ufw"></a>
### ufw

Fireware

```sh
sudo apt install ufw -y
```

[Volver a lista de contenido](#subir)

<a name = "ghost"></a>
### Ghostwrite [web](https://kde.github.io/ghostwriter/)

Editor de archivos markdown

```sh
sudo add-apt-repository ppa:wereturtle/ppa
sudo apt update
sudo apt install ghostwriter -y
```

[Volver a lista de contenido](#subir)

<a name="dia"></a>
### Dia [web](http://dia-installer.de/index.html.es)

Programa para crear diagramas Uml

```sh
sudo apt install dia -y
```

[Volver a lista de contenido](#subir)

<a name="staruml"></a>
### starUml [web](https://staruml.io/)

Programa para crear diagramas Uml

```sh
# Descargar .deb
# Instalación del software
sudo dpkg -i StarUML_5.0.2_amd64.deb
```

[Volver a lista de contenido](#subir)

<a name="vscode"></a>
### Visual Studio Code [web](https://code.visualstudio.com/)

Editor de codigo

```sh
# Descargar .deb
# Instalación del software
sudo dpkg -i code_1.72.2-1665614327_amd64.deb
```

[Volver a lista de contenido](#subir)

<a name="sublime"></a>
### sublime Text 3 [web](https://www.sublimetext.com/3)

Editor de código

```sh
# Descargar .deb
# Instalación de software
sudo dpkg -i sublime-text_build-3211_amd64.deb
```

[Volver a lista de contenido](#subir)

<a name="chrome"></a>
### Chrome

Navegador web

```sh
# Descargar .deb
# Instalación del software
sudo dpkg -i google-chrome-stable_current_amd64.deb
```

[Volver a lista de contenido](#subir)

<a name="password"></a>
### 1password [web](https://1password.com/es/)

Gestor de contraseñas

```sh
# Descargar .deb
# Instalación del software
sudo dpkg -i 1password-latest.deb
```

[Volver a lista de contenido](#subir)

<a name="postman"></a>
### Postman [web](https://snapcraft.io/postman)

Cliente Http

```sh
sudo snap install postman
```

[Volver a lista de contenido](#subir)

<a name="hyper"></a>
### Hyper [web](https://hyper.is/)

Terminal

```sh
# Descargar .deb
# Instalación de software
sudo dpkg -i hyper_3.3.0_amd64.deb
```

[Volver a lista de contenido](#subir)

<a name="workbench"></a>
### Workbench [web](https://snapcraft.io/mysql-workbench-community)

Administrador de base de datos MySql

```sh
sudo snap install mysql-workbench-community
```

[Volver a lista de contenido](#subir)

<a name="vlc"></a>
### vlc [web](https://www.videolan.org/vlc/)

Reproductor de media

```sh
sudo apt install vlc -y
```


[Volver a lista de contenido](#subir)

<a name="libreoffice"></a>
### Libre Office [web](https://www.libreoffice.org/discover/libreoffice/)

Programa de ofimatica

```sh
sudo apt install libreoffice -y
```

[Volver a lista de contenido](#subir)

<a name="gparted"></a>
### gParted [web](https://gparted.org/)

Administración de unidades de almacenamiento

```sh
sudo apt install gparted -y
```

[Volver a lista de contenido](#subir)

<a name="filezilla"></a>
### Filezilla [web](https://filezilla-project.org/)

Cliente FTP

```sh
sudo apt install filezilla -y
```

[Volver a lista de contenido](#subir)

<a name="code"></a>
### Instalación de interpretes y compiladores

<a name="apache"></a>
### apache

```sh
sudo apt install apache2 apache2-utils apache2-doc -y 
a2enconf apache2-doc
```

[Volver a lista de contenido](#subir)

<a name="php"></a>
### php8.1

```sh
# Instalación
sudo apt install php8.1 libapache2-mod-php8.1 php8.1-pgsql php8.1-sqlite3 php8.1-interbase php8.1-odbc php8.1-sybase php8.1-mysql php8.1-common php8.1-cli php8.1-common php8.1-cli php8.1-opcache php8.1-readline php8.1-mbstring php-pear php8.1-intl php8.1-dom php8.1-curl php8.1-cgi php-json

# Activar módulo de apache con php
sudo a2enmod php8.1

# Reiniciar apache
sudo systemctl restart apache2
```

[Volver a lista de contenido](#subir)

<a name="composer"></a>
### composer

```sh
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '55ce33d7678c5a611085589f1f3ddf8b3c52d662cd01d4ba75c0ee0459970c2200a51f492d557530c71c15d8dba01eae') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"

# Mover composer
sudo mv composer.phar /usr/local/bin/composer
```

[Volver a lista de contenido](#subir)

<a name="node"></a>
### node (Zsh)

```sh

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | zsh

source ~/.zshrc

nvm list-remote

nvm install v16.17.1

nvm list

```

[Volver a lista de contenido](#subir)

<a name="mysql"></a>
### mysql

```sh
# Instalación de Mariadb
sudo apt install mariadb-server mariadb-client mariadb-common -y

# Iniciar Mariadb al encender el equipo
sudo systemctl enable mariadb

# Configuración de Mariadb
sudo mysql_secure_installation
# Opciones de configuración
[Y]
[Y]
[Y]
<pasword>
<repeat-passsword>
[Y]
[n]
[Y]
[Y]
```

[Volver a lista de contenido](#subir)



<a name="postgresql"></a>
### PostgreSql

Instalación de **posgresql** [sitio oficial](https://www.postgresql.org/download/linux/ubuntu/)
```sh
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'

wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -

sudo apt-get update

sudo apt-get -y install postgresql
```

Instalación de **pgAdmin4** [sitio oficial](https://www.pgadmin.org/download/pgadmin-4-apt/)
```sh

curl -fsS https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo gpg --dearmor -o /usr/share/keyrings/packages-pgadmin-org.gpg

sudo sh -c 'echo "deb [signed-by=/usr/share/keyrings/packages-pgadmin-org.gpg] https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'


sudo apt install pgadmin4

# Solo escritorio.
sudo apt install pgadmin4-desktop

# Solo web.
sudo apt install pgadmin4-web 

# Configuracion de uso web.
sudo /usr/pgadmin4/bin/setup-web.sh

```

[Volver a lista de contenido](#subir)


<a name="c"></a>
### C++

```sh
sudo apt install build-essential -y
```

[Volver a lista de contenido](#subir)

