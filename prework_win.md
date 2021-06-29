# Prework para Windows

## Extensiones VS Code

**Prettier** = Mejora la visualización e indentado del código

**Color highlight** = Previsualiza el color a los hexa en css

**Live Server** = Lanza un servidor local que actualiza automáticamente al guardar el archivo

**Path Intellisense** = Autocompleta las rutas de imágenes

**Auto Rename Tag** = Autocompleta los tags de html (mi vscode ya lo hace)

**Material Icon Theme** = Agrega íconos tipo material design a los formatos de archivo

---

## Configuración windows subSystem for Linux

1. Abrir CMD >> Escribir comando winver

   `Si la versión de compilación de SO es mayor a 19041 puedo continuar`

2. Abrir powershell como administrador

3. revisar la guía de Instalación de Windows Subsystem for Linux [Acá](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

4. Pegar eso en el powershell que había abierto como admin
   `dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart` y enter

5. Luego pegar esto
   `dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart` y enter

6. Pegar esto `wsl --set-default-version 2` y enter
   Acá aparece un error que se arregla ingresando a la bios del equipo y en seguridad, habilitar la virtualización

- Si al ingresar el mismo comando sale el `error: 0x1bc`, entonces...

  descargar _WSL2 Linux kernel update package for x64 machines_  [Acá](https://docs.microsoft.com/es-es/windows/wsl/install-win10#step-4---download-the-linux-kernel-update-package)

7. consultar la versión del WSL con _wsl -l -v_ esto dira que no tengo distros instaladas

8. Abro la tienda de aplicaciones de microsoft y busco Ubuntu 20 LTS (Long Time Support), Instalo/adquiero

9. En la microsoft store busco e instalo windows terminal

10. **Abro Ubuntu:** Ubuntu es un sistema operativo sin interfaz gráfica viviendo dentro de windows

11. tratar de dejar los archivos en ubuntu dentro de /home/usuario

---

## Manejo de archivos y directorios en termial

Se manejan los siguientes comandos:

**ls** muestra archivos

**ls -a** muestra archivos ocultos

**ls -l** muestra los permisos de los archivos

**ls -la** Lista y muestra archivos ocultos

**Clear** Limpia pantalla, da lo mismo que Ctrl + L

**ls -lat** Organiza la lista por fecha de modificación

**pwd** Retorna la ruta en la que estoy ubicado

**mkdir folder_name** Crea una carpeta

**(Ubuntu) sudo mkdir folder_name** creo carpeta con permisos de admin

**cd** change directory

**cd folder_name** Entra a esa carpeta

**cd ..** Subo un nivel de carpetas

**cd** Me voy a la carpeta raiz del usuario

---

### Linux Ubuntu

**cd mnt** me voy desde Ubuntu a carpetas de windows

**cd ~** me devuelvo al subsistema de Ubuntu

**sudo apt-get update** actualiza paquetes de Ubuntu

**sudo apt-get upgrade** Ejecuta los paquetes de Ubuntu

---

**cd route/folder_name** Me voy a una ruta específica

**history** Historial de comandos ejecutados, como cada item de la lista tiene un número de índice, escribo `!1` y ejecuta el comando número 1

**touch new_file.txt** Crea un nuevo archivo

**code .** Abre VS Code desde Ubuntu

**sudo chown -R user-name ~/folder-name** Para habilitar las carpetas creadas con sudo (permisos de admin)

**man cat** muestra el manual del comando cat, Me salgo del manual oprimiendo Q

**cat new_file.txt** Permite visualizar el archivo

**nano new_file.txt** Permite editar archivos

**mv new_file.txt/subfolder_name folder_name** Mueve el archivo a una carpeta

**rm new_file.txt** Borra el archivo

**rm -rf folder_name/** Elimina carpetas

**more new_file.txt** Permite visualizar el archivo, por partes, para navegarlo, se usan las flechas. Para salir de esa vista se presiona Q

**tail new_file.txt** Muestra las ultimas 10 líneas de un archivo

**tail -5 new_file.txt** Muestra las ultimas n (5) líneas de un archivo

**cat new_file.txt > copy_new_file.txt** Copia el archivo

**open** Abre un archivo con su programa por defecto

---

**sudo apt install npm** descarga el gestor de paquetes de node

**npx** es similar a npm, solo que no instala local sino baja lo que necesite

### Crear nuevo proyecto de react

1. ir a la carpeta donde lo voy a crear

2. Ahí dentro escribir `npx create-rect-app project-name`

### Git

**git --version** me muestra la versión de git

**sudo apt install git** instala git

```
Tip siempre antes de instalar algo, actualizar paquetes con: sudo apt-get update y sudo apt-get upgrade
```

### Generando llaves

1. **Crear la llave** ssh-keygen -t rsa -b 4096 -C "micorreo@dominio.com"

2. Esto me devolverá el directorio donde se guarda

3. luego me pedirá un pass

4. escribir _eval "$(ssh-agent -s)"_ esto devolverá el agente (agent pid 12345)

5. escribir _ssh-copy-id micorreo@dominio.com_ para copiar la llave publica

6. ir a directorio donde está la llave cd ~/.ssh

7. Abrir la llave con _cat id_rsa.pub_ copio todo

8. luego pego la llave por fuera

9. ir a github >> settings >> SSH and GPG keys, pegar la llave y ponerle un nombre

---

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

---

### Cambiar contraseña en ubuntu

1. Abrir powershell como admin

2. escribir _wsl -u root_

3. escribir passwd _nombre-usuario_

4. escribir nueva contraseña

---

## Definiciones

**Nodejs** run time enviroment
Ambiente de ejecución para comandos de javascript
