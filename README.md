# Tercera y Última Actividad: Trabajo Colaborativo con Git

En esta actividad vamos a trabajar de manera colaborativa. El objetivo es crear un repositorio en GitHub que contenga un proyecto en PHP, donde podamos visualizar una foto y una descripción de cada usuario participante. Además, el repositorio debe incluir la documentación del proceso realizado (en formato `.md`) junto con todos los archivos necesarios, como imágenes, etc.

Una vez documentado todo el proceso en tu `README.md`, debes entregar la actividad pegando el enlace a tu repositorio de GitHub y adjuntando la carpeta comprimida del repositorio.

## 1.Creación del Repositorio

En esta ocasión, vamos a crear nuestro proyecto a partir de un repositorio ya existente. Los pasos a continuación te guiarán para clonar el proyecto y configurarlo en tu equipo.

1. **Clona el Repositorio Existente**:

    Primero, clona el repositorio proporcionado en una carpeta en tu equipo con el nombre `PPS-ActividadUnidad0-TuNombre`. Esto se logra ejecutando un comando `git clone` que especifica el nombre de la carpeta.

    ```bash
    git clone https://github.com/jmmedinac03vjp/PPS-Unidad0Actividad5-JoseMi.git PPS-ActividadUnidad0-TuNombre
    ```

2. **Accede al Directorio del Proyecto Clonado**:

    Cambia el directorio al proyecto recién clonado para realizar los siguientes pasos:

    ```bash
    cd PPS-ActividadUnidad0-TuNombre
    ```

3. **Inicializa Tu Propio Repositorio y Configura el Remoto**:

    Para configurar el proyecto en tu propio repositorio de GitHub, realiza los siguientes pasos:

    - Crea un archivo `README.md` y añade el nombre del proyecto al inicio:

      ```bash
      echo "# PPS-Unidad0Actividad5-TuNombre" >> README.md
      ```

    - Inicializa el repositorio en el directorio:

      ```bash
      git init
      ```

    - Añade el archivo `README.md` al área de preparación:

      ```bash
      git add README.md
      ```

    - Haz el primer commit para guardar el estado inicial del repositorio:

      ```bash
      git commit -m "First commit"
      ```

    - Configura la rama principal (`main`) y el repositorio remoto de GitHub:

      ```bash
      git branch -M main
      git remote add origin git@github.com:TuNombreDeUsuario/PPSUnidad0Actividad5TuNombre.git
      ```

    - Sube el commit inicial al repositorio remoto:

      ```bash
      git push -u origin main
      ```

## 2. Viendo los Remotos y Visualizando la Página Web

En esta sección, vamos a verificar los repositorios remotos configurados y, posteriormente, a visualizar el contenido de la página web utilizando un servidor PHP local.

## 3. Ver los Remotos Configurados

1. **Ver los Remotos**:

    Utiliza el comando `git remote -v` para visualizar los repositorios remotos configurados en tu proyecto.

    ```bash
    git remote -v
    ```

    Este comando mostrará las URLs de los remotos configurados, lo cual es útil para verificar a qué repositorios estamos conectados para realizar `push` y `pull`.

---

## 4. Visualización de la Página Web

1. **Ejecuta el Servidor PHP**:

    Utiliza el siguiente comando para iniciar un servidor PHP en tu máquina local y visualizar el contenido de la página web en el puerto `8080`.

    ```bash
    php -S 0:8080
    ```

    Abre un navegador web e ingresa la URL `http://localhost:8080` para visualizar la página web.

2. **Agrega una Imagen en la Carpeta `img`**:

    Dentro de tu proyecto, crea una carpeta llamada `img` (si no existe) y coloca en ella una imagen de tu foto o avatar. Asegúrate de nombrar el archivo con tu nombre para facilitar su identificación.

    ```bash
    mkdir -p img
    cp /ruta/de/tu/foto.jpg img/SergioMorato.jpg
    ```

3. **Crea un Perfil HTML Asociado**:

    En la carpeta `profile`, crea un archivo HTML con el mismo nombre que tu imagen (por ejemplo, `SergioMorato.html`). Este archivo contendrá la información o descripción de tu perfil.

    ```bash
    mkdir -p profile
    nano profile/TuNombre.html
    ```

    Dentro del archivo `SergioMorato.html`, puedes agregar contenido como:

    ```html
    <!DOCTYPE html>
    <html lang="es">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Perfil de TuNombre</title>
    </head>
    <body>
        <h1>Hola, soy TuNombre</h1>
        <img src="../img/TuNombre.jpg" alt="Foto de TuNombre">
        <p>Esta es la descripción de mi perfil.</p>
    </body>
    </html>
    ```

4. **Visualiza la Página Web**:

    Asegúrate de que el servidor PHP esté en ejecución (`php -S 0:8080`) y refresca la página en tu navegador (`http://localhost:8080`). Deberías ver los cambios reflejados con la imagen y el perfil en HTML que creaste.

## 5. Colaborando en el Proyecto

En esta sección, colaboraremos en proyectos GitHub compartidos, añadiendo colaboradores y gestionando ramas en los repositorios de nuestros compañeros.

---

### 1. Añadir Colaboradores al Proyecto

1. **Configuración de Colaboradores**:

    Para permitir a otros usuarios realizar cambios en tu repositorio, puedes añadir colaboradores desde la Configuración del Repositorio, en el apartado *Collaborators*.

    - Ve a la página de tu repositorio en GitHub.
    - Dirígete a **Settings > Collaborators** y añade a tus compañeros.
  
    Así, ellos podrán clonar y modificar el proyecto.

---

### 2. Compartir el Proyecto con Compañeros

1. **Invita a tus Compañeros**:

    Asegúrate de añadir al menos dos compañeros como colaboradores en tu repositorio.

2. **Aceptar Invitación y Clonar el Repositorio de los Compañeros**:

    - Acepta la invitación en el repositorio de cada uno de tus compañeros.
    - Crea una nueva carpeta para cada proyecto y clona el repositorio en ella.

    ```bash
    mkdir Proyecto_Companero
    cd Proyecto_Companero
    git clone URL_DEL_REPOSITORIO_DE_TU_COMPANERO
    ```

---

### 3. Crear y Trabajar en una Nueva Rama

1. **Crear y Cambiar de Rama**:

    Crea una nueva rama con tu nombre y cámbiate a esa rama.

    ```bash
    git branch TuNombre
    git checkout TuNombre
    ```

2. **Verificar la Rama Activa**:

    Comprueba en qué rama estás trabajando actualmente.

    ```bash
    git status
    ```

3. **Ver los Remotos Configurados**:

    Utiliza `git remote -v` para ver los remotos asociados al proyecto.

    ```bash
    git remote -v
    ```

4. **Añadir Archivos de Usuario y Subir Cambios**:

    - En la nueva rama, añade tus archivos de usuario (como tu foto y perfil HTML).
    - Haz un commit y sube los cambios al repositorio remoto.

    ```bash
    git add .
    git commit -m "Añadir archivos de usuario en rama TuNombre"
    git push origin TuNombre
    ```

    Visualiza los cambios en la web para confirmar que se han subido correctamente.

---

### 4. Modificaciones en la Rama `main`

1. **Cambiar a la Rama `main`**:

    Cambia a la rama `main` del proyecto de tus compañeros.

    ```bash
    git checkout main
    ```

2. **Sincronizar la Rama `main` en Local**:

    Actualiza tu rama `main` en local para sincronizar los cambios de otros colaboradores.

    ```bash
    git pull origin main
    ```

    Puedes lanzar la aplicación web con PHP para ver los cambios recientes.

3. **Añadir Archivos en la Rama `main`**:

    Añade tus archivos de usuario (foto y perfil) también en la rama `main`, realiza un commit y sube los cambios.

    ```bash
    git add .
    git commit -m "Añadir archivos de usuario en rama main"
    git push origin main
    ```

---

### 5. Verificar el Proyecto Propio

1. **Regresar a Tu Repositorio**:

    Vuelve a tu repositorio en local y verifica en qué rama estás.

    ```bash
    git status
    ```

2. **Comprobar Ramas de los Compañeros**:

    Asegúrate de que tus compañeros hayan creado sus propias ramas en tu repositorio. Utiliza `git branch` para ver las ramas disponibles.

    ```bash
    git branch
    ```

    Si no están, ayúdales a configurar sus ramas.

3. **Comparar Ramas**:

    Utiliza `git diff` para comparar las diferencias entre la rama `main` y las ramas de tus compañeros.

    ```bash
    git diff main TuNombre
    ```

## 6. Erre que Erre con Git Logs

En esta sección, repasaremos algunos de los comandos principales para ver el historial de confirmaciones en Git utilizando `git log`.

---

### 1. Visualizar los Logs

1. **Muestra los Logs Completo**:

    Para ver el historial completo de confirmaciones en el repositorio, utiliza el siguiente comando:

    ```bash
    git log
    ```

    Este comando muestra una lista de commits, incluyendo el autor, la fecha y el mensaje de cada confirmación.

---

### 2. Mostrar los Logs de los Últimos 3 Commits

1. **Visualizar Solo los Últimos 3 Commits**:

    Si solo necesitas ver las últimas tres confirmaciones, puedes limitar el número de commits mostrados utilizando `-n`:

    ```bash
    git log -n 3
    ```

    Esto te permite enfocar tu atención en los cambios más recientes.

---

### 3. Usar el Modificador `--pretty`

1. **Mostrar los Logs con Formato Personalizado**:

    Para una visualización más compacta y estilizada del historial, utiliza el modificador `--pretty`, que permite cambiar el formato de salida de los logs:

    ```bash
    git log --pretty=oneline
    ```

    - **`oneline`**: Muestra cada commit en una sola línea, con el hash y el mensaje.
    - Existen otros formatos como `short`, `medium`, y `full` que también puedes explorar para mayor personalización.

---

### 4. Mostrar los Logs de los Últimos 2 Commits con las Diferencias

1. **Ver los Últimos 2 Commits con Detalles de las Diferencias**:

    Para ver los detalles de las diferencias en los archivos modificados en cada uno de los dos últimos commits, utiliza el siguiente comando:

    ```bash
    git log -p -n 2
    ```

    - **`-p`**: Incluye un "patch" que muestra los cambios específicos en cada archivo.
    - **`-n 2`**: Limita la salida a los últimos dos commits.

---

### 5. Mostrar los Logs de las Modificaciones Realizadas en el Último Día

1. **Ver los Cambios del Último Día**:

    Para ver las confirmaciones realizadas en las últimas 24 horas, puedes especificar un rango de tiempo:

    ```bash
    git log --since="1 day ago"
    ```

    - **`--since`**: Permite limitar el historial a las confirmaciones realizadas después de una fecha o tiempo específico.

---

Este proceso te permite explorar y personalizar el uso de `git log` para visualizar la historia de confirmaciones en tu proyecto.
