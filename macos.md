# Mac Os
<a name="contenido"></a>
## Contenido
- [Homebrew](#homebrew)
	- [Instalación](#instalacion)
	- [Software de terminal](#shell)
		- [git](#git)
		- [zsh](#zsh)
		- [curl](#curl)
		- [wget](#wget)
		- [tree](#tree)
		- [neofetch](#neofetch)
	- [Software](#software)
		- [1Password](#1password)
		- [iTerm 2](#iterm)
		- [Google Chrome](#chrome)
		- [Hyper Term](#hyper)
		- [Notion](#notion)
		- [Android file transfer](#androidfile)
		- [Sublime Text](#sublime)
		- [Visual Studio Code](#vscode)
		- [vlc](#vlc)
		- [Postman](#postman)
		- [Star Uml](#staruml)
		- [Brave brower](#brave)
		- [MySql Workbench](#workbench)
		- [Clean My Mac](#cleanmymac)
		- [MacDown](#macdown)
		- [Microsoft Office](#microsoftoffice)
		- [WhatApp](#whatapp)
	- [Interpretes y compiladores](#code)
		- [php](#php)
		- [composer](#composer)
- [MySQL](#mysql)
- [ohmyzsh](#ohmyzsh)

<a name="homebrew"></a>
### Homebrew
Administrador de paquetes de MacOs [Sitio oficial](https://brew.sh/index_es).

<a name="instalacion"></a>
#### Instalación
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
[Volver a lista de contenido](#contenido)

<a name="shell"></a>
### Software de terminal

<a name="git"></a>
#### git
```sh
brew install git
```
[Volver a lista de contenido](#contenido)

<a name="zsh"></a>
#### zsh
```sh
brew install zsh

# Establecer zsh por defecto
chsh -s $(which zsh)

echo $SHELL
```
[Volver a lista de contenido](#contenido)

<a name="curl"></a>
#### curl
```sh
brew install curl
```
[Volver a lista de contenido](#contenido)

<a name="wget"></a>
#### wget
```sh
brew install wget
```
[Volver a lista de contenido](#contenido)

<a name="tree"></a>
#### tree
```sh
brew install tree
```
[Volver a lista de contenido](#contenido)

<a name="neofetch"></a>
#### Neofetch
```sh
brew install neofetch
```
[Volver a lista de contenido](#contenido)

<a name="software"></a>
### Software

<a name="1password"></a>
#### 1Password
```sh
brew install --cask 1password
```
[Volver a lista de contenido](#contenido)

<a name="iterm"></a>
#### iTerm 2
```sh
brew install --cask iterm2
```
[Volver a lista de contenido](#contenido)

<a name="chrome"></a>
#### Google Chrome
```sh
brew install --cask google-chrome
```
[Volver a lista de contenido](#contenido)

<a name="hyper"></a>
#### Hyper Term
```sh
brew install --cask hyper
```
[Volver a lista de contenido](#contenido)

<a name="notion"></a>
#### Notion
```sh
brew install --cask notion
```
[Volver a lista de contenido](#contenido)

<a name="androidfile"></a>
#### Android File Transfer
```sh
brew install --cask android-file-transfer
```
[Volver a lista de contenido](#contenido)

<a name="sublime"></a>
#### Sublime Text
```sh
brew install --cask sublime-text
```
[Volver a lista de contenido](#contenido)

<a name="vscode"></a>
#### Visual Studio Code
```sh
brew install --cask visual-studio-code
```
[Volver a lista de contenido](#contenido)

<a name="vlc"></a>
#### vlc
```sh
brew install --cask vlc
```
[Volver a lista de contenido](#contenido)

<a name="postman"></a>
#### Postman
```sh
brew install --cask postman
```
[Volver a lista de contenido](#contenido)

<a name="staruml"></a>
#### Star Uml
```sh
brew install --cask staruml
```
[Volver a lista de contenido](#contenido)

<a name="brave"></a>
#### Brave Brower
```sh
brew install --cask brave-brower
```
[Volver a lista de contenido](#contenido)

<a name="workbench"></a>
#### MySql workbench
```sh
brew install --cask mysqlworkbeanch
```
[Volver a lista de contenido](#contenido)

<a name="cleanmymac"></a>
#### CleanMyMac
```sh
brew install --cask cleanmymac
```
[Volver a lista de contenido](#contenido)

<a name="macdown"></a>
#### MacDown
```sh
brew install --cask macdown
```
[Volver a lista de contenido](#contenido)

<a name="microsoftoffice"></a>
#### Microsoft Office
```sh
brew install --cask microsoft-office
```
[Volver a lista de contenido](#contenido)

<a name="whatapp"></a>
#### Whatapp
```sh
brew install --cask whatapp
```
[Volver a lista de contenido](#contenido)
<a name="code"></a>
### Interpretes y compiladores

<a name="php"></a>
#### php
```sh
brew install php
```
[Volver a lista de contenido](#contenido)

<a name="composer"></a>
#### Composer
```sh
brew install composer
```
[Volver a lista de contenido](#contenido)


<a name="mysql"></a>
#### MySql

Descargar desde su [sitio oficial](https://dev.mysql.com/downloads/mysql/)

Agregar al PATH
```sh
echo 'export PATH="/usr/local/mysql/bin:$PATH"' >> ~/.zshrc
```

[Volver a lista de contenido](#contenido)


<a name="ohmyzsh"></a>
### OhMyZsh

```sh
# Instalación
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
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
	sublime
	react-native
	postgres
	node
	brew
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