
# Cómo instalar NS3 👨‍💻👨‍💻

Instalar **ns-3** puede es una tarea compleja, pero en este README te guiaré para que la instalación sea lo más sencilla posible. **ns-3** es un potente simulador de redes que no cuenta con una interfaz gráfica, por lo que todas las simulaciones se programan mediante scripts.

Pero esta instalacion te puede presentar varios problemas.

## 1. Selección de versión: **ns-3.34** ♟️

Es crucial seleccionar la versión adecuada de **ns-3**, ya que esto afectará la elección del archivo de construcción. En la mayoría de los tutoriales en línea, se utiliza el archivo de construcción `./waf`, pero **las versiones más recientes** utilizan **CMake** o **MakeWaf** para compilar el simulador.  ⏬⏬⏬

Para facilitar el proceso de instalación y evitar posibles problemas con dependencias, en este repositorio se proporciona un contenedor **Docker** que incluye **ns-3** y todas las dependencias necesarias preconfiguradas. De esta forma, podrás ejecutar **ns-3** sin complicaciones.

Más información en la documentación oficial de ns-3:  

## [Documentación de ns-3](https://www.nsnam.org/documentation/) 🔴🔴🔴

Si encuentras problemas con **ns-3**, recuerda que una buena práctica es consultar la documentación para depurar cualquier inconveniente. 🚀🚀

### Nota importante:

* Una de las principales diferencias entre versiones es que la ejecución de scripts en **Python** puede no estar habilitada, pero **C++** es totalmente compatible.  🎖️

**IMPORTANTE:**  
**ns-3** está diseñado para ejecutarse en sistemas operativos **Linux**.

## 2. Instalación de Docker 🌟🐳🐳🐳

**Docker** es una plataforma de código abierto que automatiza la implementación de aplicaciones en contenedores de software. Estos contenedores permiten una mayor flexibilidad y consistencia, asegurando que el software funcione de manera predecible en cualquier entorno.

Para instalar Docker, sigue los pasos en la página oficial de Docker:  
[Guía de instalación de Docker en Linux](https://docs.docker.com/desktop/install/linux/)

Cuando descargues el repositorio de este proyecto, encontrarás un archivo **Dockerfile** que contiene todas las configuraciones necesarias para instalar **ns-3** y sus dependencias. Esto te permitirá ejecutar **ns-3** de manera sencilla y sin complicaciones.

## 3. Instalación de ns-3  📶📶📶

Una vez que tengas Docker instalado, sigue estos pasos para ejecutar **ns-3.34**:

1. Abre una terminal en la carpeta donde se encuentran los archivos del repositorio.
2. Ejecuta el siguiente comando en la terminal para construir el contenedor con **ns-3**:

```bash
$ docker build -t ns3-dce:v1 .
```

Este comando creará una imagen de Docker con **ns-3** y sus dependencias listas para usar.

3. Ejecuta el run para abrir el contenedor de ns3 

```bash
$ docker run -it ns3-dce:v1 bash
```

4. Desde la terminal del contenedor, ns-3 ya estará instalado y podrás comenzar a utilizarlo ejecutando scripts y simulaciones directamente desde esta terminal.

   Si tienes dudas como abrir y ejecutar archivos en ns3 recuerda revisar la documentacion oficial o apoyarte de videos de youtube de otros creadores. 🎨🎨

## Creditos 👨‍💻👩‍💻

# Docker creado por: 
- EmanuelM153 (Estudiante de Ciencias de la computacion e inteligencia artificial)

# Manual escrito por:   
- Karen (Estudiante de Ciencias de la computacion e inteligencia artificial)










