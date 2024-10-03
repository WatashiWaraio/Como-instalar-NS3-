
# Cómo instalar NS3 👨‍💻👨‍💻

Instalar **ns-3** puede es una tarea compleja, pero en este README te guiaré para que la instalación sea lo más sencilla posible. **ns-3** es un potente simulador de redes que no cuenta con una interfaz gráfica, por lo que todas las simulaciones se programan mediante scripts.

Pero esta instalacion te puede presentar varios problemas.

## 1. Selección de versión: **ns-3.34** ♟️

Es crucial seleccionar la versión adecuada de **ns-3**, ya que esto afectará la elección del programa de construcción. En la mayoría de los tutoriales en línea, se utiliza el programa de construcción **Waf** desde el archivo `./waf`, pero **las versiones más recientes** utilizan **CMake** o **MakeWaf** para compilar el simulador.  ⏬⏬⏬

Para facilitar el proceso de instalación y evitar posibles problemas con dependencias, este repositorio proporciona un **Dockerfile** para la descarga, compilación y configuración de **ns-3** y todas sus dependencias necesarias. De esta forma, podrás utilizar **ns-3** sin complicaciones.

Además, el **Dockerfile** instala el módulo **DCE** (Direct Code Execution, o ejecución directa de código en español).

   La Ejecución Directa de Código (DCE) es un framework para ns-3 que proporciona facilidades para ejecutar, dentro de ns-3, implementaciones existentes de protocolos de red o aplicaciones en espacio de usuario y espacio de kernel sin necesidad de cambios en el código fuente. (Nsnam, traducción propia)

De esta manera, podrás ejecutar herramientas como `Iperf` y `ping` directamente desde una simulación de **ns-3**.

Más información en la documentación oficial de ns-3:  

## [Documentación de ns-3](https://www.nsnam.org/documentation/) 🔴🔴🔴

Si encuentras problemas con **ns-3**, recuerda que una buena práctica es consultar la documentación para depurar cualquier inconveniente. 🚀🚀 (RTFM 😉)

### Nota importante:

* El Dockerfile no compila los **Python** bindings para la ejecución de scripts en este lenguaje, pero **C++** esta totalmente habilitado.  🎖️

**IMPORTANTE:**  
**ns-3** está diseñado para ejecutarse en sistemas operativos **Linux** Sin embargo con el docker se puede instalar desde cualquier sistema operativo.

## 2. Instalación de Docker 🌟🐳🐳🐳

**Docker** es una plataforma de código abierto que automatiza la implementación de aplicaciones en contenedores de software. Estos contenedores permiten una mayor flexibilidad y consistencia, asegurando que el software funcione de manera predecible en cualquier entorno.

Para instalar Docker, sigue los pasos en la página oficial de Docker:  
[Guía de instalación de Docker en Linux](https://docs.docker.com/desktop/install/linux/)

[Guía de instalación de Docker en Windows](https://www.youtube.com/watch?v=ZO4KWQfUBBc)

[Guía de instalación de Docker en MacOs](https://www.youtube.com/watch?v=-EXlfSsP49A)

Cuando descargues el repositorio de este proyecto, encontrarás un archivo **Dockerfile** que contiene todas las configuraciones necesarias para instalar **ns-3** y sus dependencias. Esto te permitirá utilizar **ns-3** de manera sencilla y sin complicaciones.

## 3. Instalación de ns-3  📶📶📶

Una vez que tengas Docker instalado, sigue estos pasos para utilizar **ns-3.34**:

1. Abre una terminal en la carpeta donde se encuentran los archivos del repositorio. El Dockerfile no debe terminar en la extensión _.txt_. Si tienes el archivo con esta extensión cambia el nombre. El siguiente comando se puede utilizar desde Windows en **Powershell**, o en Linux desde cualquier shell, para renombrar el archivo:

```bash
$ mv Dockerfile.txt Dockerfile
```
   
3. Ejecuta el siguiente comando en la terminal para construir el contenedor con **ns-3**:

```bash
$ docker build -t ns3-dce:v1 .
```

Este comando creará una imagen de Docker con **ns-3** y sus dependencias listas para usar.

3. Ejecuta el run para abrir el contenedor de ns3 

```bash
$ docker run -it ns3-dce:v1 bash
```

4. Desde la terminal del contenedor, **ns-3** ya estará instalado y podrás comenzar a utilizarlo ejecutando scripts y simulaciones directamente desde esta terminal.

   Si tienes dudas de como abrir y ejecutar archivos en ns3 recuerda revisar la documentacion oficial o apoyarte de videos de youtube de otros creadores. 🎨🎨

## Creditos 👨‍💻👩‍💻

# Dockerfile creado por: 
- @EmanuelM153 (Estudiante de Ciencias de la computacion e inteligencia artificial)

# Manual escrito por:   
- Karen (Estudiante de Ciencias de la computacion e inteligencia artificial)










