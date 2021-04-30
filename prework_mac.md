# Prework para Mac

## Instalación de Node

**1. Ejecutar en terminal este comando** "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

Esto es un manejador de paquetes, es un repositorio de paquetes de donde puede descargar dependencias (homebrew y NPM son dos ejemplos)

-**Homebrew** Maneja paquetes para instalar software en el sistema operativo

-**npm** Instala paquetes para el entorno web (node)

**2. instalar node** _brew install node_

### Actualizaciones y versiones

**Atualizar brew** _brew update_

**Consultar versión node** _node -v_

**Consultar versión npm** _npm -v_

---

## Comandos terminal

**cd** = change directory
**cd folder_name** = entro a la carpeta folder_name

**Regresarme un nivel** = cd ..

**ls** = listar

**nueva carpeta** = mkdir new_folder

**Nuevo archivo** = touch new_file.extension

`Tip` **Abrir VS Code desde terminal** En VS Code poner Command shift P y buscar _shell Command: Install 'code' command in PATH_ Luego enter, dar permisos y en terminal escribir _code ._

**open demo_liveserver.html** = Abre el archivo en el navegador (o programa según extensión) por defecto

**sudo** = Super User DO (Super usuario hace algo) Da permisos de superadministrador (Mac)

**reset** = Resetea la terminal

**Ctrl C** = Termina cualquier proceso en la terminal

---

## Primer Demo en react

**Crear nuevo proyecto** = _npx create-react-app app-name_

**Iniciar app** = cd app-name => _npm start_

**Terminar proceso** = ^ C

---

## Manejo de repos en Git

### Generando llaves

**Crear la llave** ssh-keygen -t rsa -b 4096 -C "correo@dominio.com"

**Copiar llave** pbcopy < ~/.ssh/id_rsa.pub

Luego en github en sttings del perfil

seleccionar SSH and GPG >> creo una nueva llave SSH

Agrego el nombre del equipo y pego la llave

### Creando repo

En git nuevo repositorio, escribo nombre y descripción

#### **En terminal**

**Configurar usuario de github** = git config --global --edit

Eso abrirá el editor de texto vim, para poder escribir debe estar en estado INSERT
salgo y guardo con _:wq_

**1. Inicializaar repo** = git init

**2. Agregar archivos a traking de github** = git add .

**3. Guardar puntos de avance** = git commit -m "message"

**4. Añadiendo repositorio remoto** = git remote add origin https://github.com/github_user/repo_name.git

**Mostrar info del repo** = git remote -v

**5. subir cambios a la rama** = git push -u origin main `anteriormente (git push -f origin master)`

`Github me recomendó esta` _git push --set-upstream origin master_

#### **Subiendo desde VS Code**

1. Presionar en el ícono del fork donde hay un batch con el número de cambios

2. En el campo de texto se ingresa el commit y se presiona el check ✔️

3. se presionan los puntos ••• y se oprime push
