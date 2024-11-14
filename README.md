# Tercera y Última Actividad: Trabajo Colaborativo con Git

En esta actividad vamos a trabajar de manera colaborativa. El objetivo es crear un repositorio en GitHub que contenga un proyecto en PHP, donde podamos visualizar una foto y una descripción de cada usuario participante. Además, el repositorio debe incluir la documentación del proceso realizado (en formato `.md`) junto con todos los archivos necesarios, como imágenes, etc.

Una vez documentado todo el proceso en tu `README.md`, debes entregar la actividad pegando el enlace a tu repositorio de GitHub y adjuntando la carpeta comprimida del repositorio.

## Creación del Repositorio

En esta ocasión, vamos a crear nuestro proyecto a partir de un repositorio ya existente. Los pasos a continuación te guiarán para clonar el proyecto y configurarlo en tu equipo.

1. **Clona el Repositorio Existente**:

    Primero, clona el repositorio proporcionado en una carpeta en tu equipo con el nombre `PPS-ActividadUnidad0-TuNombre`. Esto se logra ejecutando un comando `git clone` que especifica el nombre de la carpeta. 

    ```bash
    git clone https://github.com/jmmedinac03vjp/PPS-Unidad0Actividad5-JoseMi.git PPS-ActividadUnidad0-SergioMorato
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

---

## Documentación en `README.md`

Asegúrate de documentar todo el proceso en el archivo `README.md`, incluyendo cada paso realizado para crear y configurar el proyecto. Agrega también las instrucciones para la instalación y ejecución del proyecto, así como una breve descripción de cada colaborador, incluyendo foto y descripción.

---

## Entrega de la Actividad

1. **Entrega en la Plataforma**:

    - Pega el enlace a tu repositorio de GitHub en la plataforma de entrega.
    - Adjunta también la carpeta comprimida del repositorio con todos los archivos necesarios.

---

Este proceso garantiza que has clonado un proyecto existente y lo has configurado como un repositorio propio, preparado para el trabajo colaborativo y para la documentación adecuada del proyecto.
