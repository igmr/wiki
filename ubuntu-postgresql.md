
# PostgreSQL

PostgreSQL es un gestor de base de datos relacional open source.

<details>

<summary>Contenido</summary>

- [Instalación de PostgreSQL](#postgresql)
- [Instalación de pgAdmin 4](#pgadmin-4)
- [Cambiar contraseña](#change-password)

</details>

---

<a name="postgresql"></a>

## Instalación de PostgreSQL <a href="https://www.postgresql.org/download/linux/ubuntu/" target="_blank">#</a>

Crear archivo de configuración de repositorio.

```bash
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
```

Importar clave del repositorio.

```bash
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
```

Actualizar lista de repositorios.

```Bash
sudo apt-get update
```

Instalar la ultima versión de postgreSQL.
```bash
sudo apt install postgresql -y
```

<a name="pgadmin-4"></a>

## Instalación de pgAdmin 4 <a href="https://www.pgadmin.org/download/pgadmin-4-apt/" target="_blank">#</a>

Instalar clave publica del repositorio.

```bash
curl -fsS https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo gpg --dearmor -o /usr/share/keyrings/packages-pgadmin-org.gpg
```

Crear archivo de configuración del repositorio
```bash
sudo sh -c 'echo "deb [signed-by=/usr/share/keyrings/packages-pgadmin-org.gpg] https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'
```

Instalar pgAdmin 4

```bash
sudo apt install pgadmin4
```

Instalar solo aplicación de escritorio.

```bash
sudo apt install pgadmin4-desktop
```

Instalar solo aplicación de web.

```bash
sudo apt install pgadmin4-web 
```

Configuración de webserver para la instalación de pgadmin4-web

```bash
sudo /usr/pgadmin4/bin/setup-web.sh
```


<a name="change-password"></a>

## Cambio de contraseña

Accedemos con el usuario **postgres** desde la linea de comandos.

```bash
sudo su postgres
```

Accedemos al gestor de base de datos por medio de **psql**.

```bash
psql
```

Cambiamos la contraseña con el siguiente comando.

```sql
ALTER user postgres WITH password <new-password>
```

Salimos de psql

```sql
\q
```
