# Índice

   [Introducción](#tercera-y-última-actividad-trabajo-colaborativo-con-git)
- [Índice](#índice)
- [Tercera y Última Actividad: Trabajo Colaborativo con Git](#tercera-y-última-actividad-trabajo-colaborativo-con-git)
  - [1.Creación del Repositorio](#1creación-del-repositorio)
  - [2. Viendo los Remotos y Visualizando la Página Web](#2-viendo-los-remotos-y-visualizando-la-página-web)
  - [3. Ver los Remotos Configurados](#3-ver-los-remotos-configurados)
  - [4. Visualización de la Página Web](#4-visualización-de-la-página-web)
  - [5. Colaborando en el Proyecto](#5-colaborando-en-el-proyecto)
    - [1. Añadir Colaboradores al Proyecto](#1-añadir-colaboradores-al-proyecto)
    - [2. Compartir el Proyecto con Compañeros](#2-compartir-el-proyecto-con-compañeros)
    - [3. Crear y Trabajar en una Nueva Rama](#3-crear-y-trabajar-en-una-nueva-rama)
    - [4. Modificaciones en la Rama `main`](#4-modificaciones-en-la-rama-main)
    - [5. Verificar el Proyecto Propio](#5-verificar-el-proyecto-propio)
  - [6. Erre que Erre con Git Logs](#6-erre-que-erre-con-git-logs)
    - [1. Visualizar los Logs](#1-visualizar-los-logs)
    - [2. Mostrar los Logs de los Últimos 3 Commits](#2-mostrar-los-logs-de-los-últimos-3-commits)
    - [3. Usar el Modificador `--pretty`](#3-usar-el-modificador---pretty)
    - [4. Mostrar los Logs de los Últimos 2 Commits con las Diferencias](#4-mostrar-los-logs-de-los-últimos-2-commits-con-las-diferencias)
    - [5. Mostrar los Logs de las Modificaciones Realizadas en el Último Día](#5-mostrar-los-logs-de-las-modificaciones-realizadas-en-el-último-día)

# Tercera y Última Actividad: Trabajo Colaborativo con Git

En esta actividad vamos a trabajar de manera colaborativa. El objetivo es crear un repositorio en GitHub que contenga un proyecto en PHP, donde podamos visualizar una foto y una descripción de cada usuario participante. Además, el repositorio debe incluir la documentación del proceso realizado (en formato `.md`) junto con todos los archivos necesarios, como imágenes, etc.

Una vez documentado todo el proceso en tu `README.md`, debes entregar la actividad pegando el enlace a tu repositorio de GitHub y adjuntando la carpeta comprimida del repositorio.

## 1.Creación del Repositorio

En esta ocasión, vamos a crear nuestro proyecto a partir de un repositorio ya existente. Los pasos a continuación te guiarán para clonar el proyecto y configurarlo en tu equipo.

1. **Clona el Repositorio Existente**:

    Primero, clona el repositorio proporcionado en una carpeta en tu equipo con el nombre `PPS-ActividadUnidad0-SergioMorato`. Esto se logra ejecutando un comando `git clone` que especifica el nombre de la carpeta.

    ```bash
    git clone https://github.com/jmmedinac03vjp/PPS-Unidad0Actividad5-JoseMi.git PPS-Unidad0Actividad5-SergioMorato
    ```

2. **Accede al Directorio del Proyecto Clonado**:

    Cambia el directorio al proyecto recién clonado para realizar los siguientes pasos:

    ```bash
    cd  PPS-Unidad0Actividad5-SergioMorato
    ```

3. **Inicializa Tu Propio Repositorio y Configura el Remoto**:

    Para configurar el proyecto en tu propio repositorio de GitHub, realiza los siguientes pasos:

    - Crea un archivo `README.md` y añade el nombre del proyecto al inicio:

      ```bash
      echo "# PPS-Unidad0Actividad5-SergioMorato" >> README.md
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
      git remote add origin git@github.com:SergioMP04/PPS-Unidad0Actividad5-SergioMorato.git
      ```

    - Sube el commit inicial al repositorio remoto:

      ```bash
      git push -u origin main
      ```

        <p align="center">
          <img src="imagenes\Creación_Repo.png" alt="Config Nano">
          <img src="imagenes\Creación_Repo2.png" alt="Config Nano">
        </p>
---

*Lo que haremos después de esto será editar el archivo html y añadir una imagen .png diferente dentro de la carpeta.
        <p align="center">
        <img src="imagenes\Creación_Repo3.png" alt="Config Nano">
        </p>

## 2. Viendo los Remotos y Visualizando la Página Web

En esta sección, vamos a verificar los repositorios remotos configurados y, posteriormente, a visualizar el contenido de la página web utilizando un servidor PHP local.
        <p align="center">
          <img src="imagenes\PHP1.png" alt="Config Nano">
          <img src="imagenes\PHP2.png" alt="Config Nano">
        </p>

## 3. Ver los Remotos Configurados

1. **Ver los Remotos**:

    Utiliza el comando `git remote -v` para visualizar los repositorios remotos configurados en tu proyecto.

    ```bash
    git remote -v
    ```
    Se adjunta imagen del comando:
        <p align="center">
          <img src="imagenes\Git_Remote.png" alt="Config Nano">
        </p>

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
    nano profile/SergioMorato.html
    ```

    Dentro del archivo `SergioMorato.html`, puedes agregar contenido como:

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>SergioMorato</title>
    </head>
    <body>
      <h1>Hola!</h1>
      <p>Me llamo Sergio Morato Prieto</p>
      <p>Soy alumno de CECETI</p>
    </body>
    </html>
    ```

4. **Visualiza la Página Web**:

    Asegúrate de que el servidor PHP esté en ejecución (`php -S 0:8080`) y refresca la página en tu navegador (`http://localhost:8080`). Deberías ver los cambios reflejados con la imagen y el perfil en HTML que creaste.

*Estos pasos los hize al principio para que sea todo mas fácil las imágenes con la demostración se encuentran el segundo punto.

## 5. Colaborando en el Proyecto

En esta sección, colaboraremos en proyectos GitHub compartidos, añadiendo colaboradores y gestionando ramas en los repositorios de nuestros compañeros.

---

### 1. Añadir Colaboradores al Proyecto

1. **Configuración de Colaboradores**:

    Para permitir a otros usuarios realizar cambios en tu repositorio, puedes añadir colaboradores desde la Configuración del Repositorio, en el apartado *Collaborators*.

    - Ve a la página de tu repositorio en GitHub.
    - Dirígete a **Settings > Collaborators** y añade a tus compañeros.
        <p align="center">
          <img src="imagenes\Colaboradores.png" alt="Config Nano">
        </p>

---

### 2. Compartir el Proyecto con Compañeros

1. **Invita a tus Compañeros**:

    Asegúrate de añadir al menos dos compañeros como colaboradores en tu repositorio.

2. **Aceptar Invitación y Clonar el Repositorio de los Compañeros**:

    - Acepta la invitación en el repositorio de cada uno de tus compañeros.
    - Crea una nueva carpeta para cada proyecto y clona el repositorio en ella.

    ```bash
    git clone https://github.com/jmtatop01/PPS-Actividad5Unidad0-JulioManuelTatoPulido.git
    git clone https://github.com/Clealg01/PPS-Unidad0Actividad5-Cristian.git
    ```

    - Clonación de los repositorios de ambos compañeros.
        <p align="center">
          <img src="imagenes\Git_Clone.png" alt="Config Nano">
        </p>

---

### 3. Crear y Trabajar en una Nueva Rama

1. **Crear y Cambiar de Rama**:

    Crea una nueva rama con tu nombre y cámbiate a esa rama.

    ```bash
    git branch SergioMorato
    git checkout SergioMorato
    ```

    <p align="center">
    <img src="imagenes\Checkout.png" alt="Config Nano">
    </p>

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
    git commit -m "Añadir archivos de usuario en rama SergioMorato"
    git remote set-url origin git@github.com:jmtatop01/PPS-Actividad5Unidad0-JulioManuelTatoPulido.git
    git push origin SergioMorato
    ```

    <p align="center">
    <img src="imagenes\Rama_Julio_Sergio.png" alt="Config Nano">
    <img src="imagenes\Rama_Julio_Sergio2.png" alt="Config Nano">
    </p>

    - Visualiza los cambios en la web para confirmar que se han subido correctamente.
    - Ahora repetiremos el proceso con el repositorio de Cristian.
      - Aqui se adjunta captura de los comandos, a la hora de mover archivos de una carpeta a otra se ha hecho a mano y no en terminal.

    <p align="center">
    <img src="imagenes\Checkout_Cristian.png" alt="Config Nano">
    </p>

    - A continuación adjunto las diferentes capturas de los comando empleandos en la práctica, recalco el siguiente ya que sin el me habria dado un fallo.

    ```bash
    git remote set-url origin git@github.com:jmtatop01/PPS-Actividad5Unidad0-JulioManuelTatoPulido.git
    git remote set-url origin git@github.com:Clealg01/PPS-Unidad0Actividad5-Cristian.git
    ```

    <p align="center">
    <img src="imagenes\Rama_Cristian_Sergio.png" alt="Config Nano">
    <img src="imagenes\Rama_Cristian_Sergio2.png" alt="Config Nano">
    </p>

---

### 4. Modificaciones en la Rama `main`

1. **Cambiar a la Rama `main`**:

    Cambia a la rama `main` del proyecto de tus compañeros(Haré el miso proceso tanto para el proyecto de Cristian como el de Julio).

    ```bash
    git checkout main
    ```

2. **Sincronizar la Rama `main` en Local**:

    Actualiza tu rama `main` en local para sincronizar los cambios de otros colaboradores.

    ```bash
    git pull origin main
    ```

    <p align="center">
    <img src="imagenes\Rama_Cristian_Sergio3.png" alt="Config Nano">
    <img src="imagenes\Rama_Julio_Sergio3.png" alt="Config Nano">
    </p>
    Puedes lanzar la aplicación web con PHP para ver los cambios recientes.

3. **Añadir Archivos en la Rama `main`**:

    Añade tus archivos de usuario (foto y perfil) también en la rama `main`, realiza un commit y sube los cambios.

    ```bash
    git add .
    git commit -m "Actualización de rama main, Sergio Morato"
    git push origin main
    ```

    <p align="center">
    <img src="imagenes\Rama_Cristian_Sergio4.png" alt="Config Nano">
    <img src="imagenes\Rama_Julio_Sergio4.png" alt="Config Nano">
    </p>

---

### 5. Verificar el Proyecto Propio

1. **Regresar a Tu Repositorio**:

    Vuelve a tu repositorio en local y verifica en qué rama estás.

    ```bash
    git status
    ```

    <p align="center">
    <img src="imagenes\Git_Status1.png" alt="Config Nano">
    </p>

2. **Comprobar Ramas de los Compañeros**:

    Asegúrate de que tus compañeros hayan creado sus propias ramas en tu repositorio. Utiliza `git branch` para ver las ramas disponibles, aunque primero actualizaremos nuestro repositorio y después las visualizaremos.

    ```bash
    git fetch
    git branch -a
    ```

    <p align="center">
    <img src="imagenes\Git_Fetch.png" alt="Config Nano">
    </p>

3. **Comparar Ramas**:

    Utiliza `git diff` para comparar las diferencias entre la rama `main` y las ramas de tus compañeros.

    ```bash
    git diff main
    ```

    <p align="center">
    <img src="imagenes\Git_Diff.png" alt="Config Nano">
    </p>

## 6. Erre que Erre con Git Logs

En esta sección, repasaremos algunos de los comandos principales para ver el historial de confirmaciones en Git utilizando `git log`.

---

### 1. Visualizar los Logs

1. **Muestra los Logs Completo**:

    Para ver el historial completo de confirmaciones en el repositorio, utiliza el siguiente comando:

    ```bash
    git log
    ```

    <p align="center">
    <img src="imagenes\Git_Log1.png" alt="Config Nano">
    </p>

    Este comando muestra una lista de commits, incluyendo el autor, la fecha y el mensaje de cada confirmación.

---

### 2. Mostrar los Logs de los Últimos 3 Commits

1. **Visualizar Solo los Últimos 3 Commits**:

    Si solo necesitas ver las últimas tres confirmaciones, puedes limitar el número de commits mostrados utilizando `-n`:

    ```bash
    git log -n 3
    ```

    <p align="center">
    <img src="imagenes\Git_Log2.png" alt="Config Nano">
    </p>

    Esto te permite enfocar tu atención en los cambios más recientes.

---

### 3. Usar el Modificador `--pretty`

1. **Mostrar los Logs con Formato Personalizado**:

    Para una visualización más compacta y estilizada del historial, utiliza el modificador `--pretty`, que permite cambiar el formato de salida de los logs:

    ```bash
    git log --pretty=oneline
    ```

    <p align="center">
    <img src="imagenes\Git_Log3.png" alt="Config Nano">
    </p>

    - **`oneline`**: Muestra cada commit en una sola línea, con el hash y el mensaje.
    - Existen otros formatos como `short`, `medium`, y `full` que también puedes explorar para mayor personalización.

---

### 4. Mostrar los Logs de los Últimos 2 Commits con las Diferencias

1. **Ver los Últimos 2 Commits con Detalles de las Diferencias**:

    Para ver los detalles de las diferencias en los archivos modificados en cada uno de los dos últimos commits, utiliza el siguiente comando:

    ```bash
    git log -p -n 2
    ```

    <p align="center">
    <img src="imagenes\Git_Log4.png" alt="Config Nano">
    <img src="imagenes\Git_Log5.png" alt="Config Nano">
    </p>

    - **`-p`**: Incluye un "patch" que muestra los cambios específicos en cada archivo.
    - **`-n 2`**: Limita la salida a los últimos dos commits.

---

### 5. Mostrar los Logs de las Modificaciones Realizadas en el Último Día

1. **Ver los Cambios del Último Día**:

    Para ver las confirmaciones realizadas en las últimas 24 horas, puedes especificar un rango de tiempo:

    ```bash
    git log --since="1 day ago"
    ```

    <p align="center">
    <img src="imagenes\Git_Log6.png" alt="Config Nano">

    </p>

    - **`--since`**: Permite limitar el historial a las confirmaciones realizadas después de una fecha o tiempo específico.

---
