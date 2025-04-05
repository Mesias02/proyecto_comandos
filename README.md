# Informe de la Práctica: Servidor Web

## 1. Título
**Creación y Manipulación de Archivos en un Servidor Web con Docker y Nginx**

## 2. Tiempo de Duración
La práctica tuvo una duración aproximada de **60 minutos**. Esto incluye la configuración inicial de los contenedores, la manipulación de archivos y la ejecución de pruebas.

## 3. Fundamentos
La práctica está basada en la creación y gestión de contenedores con Docker y la configuración de un servidor web con Nginx. Docker es una plataforma que permite automatizar la implementación de aplicaciones en contenedores ligeros, proporcionando un entorno consistente para el desarrollo y la ejecución de aplicaciones.

### ¿Qué es Docker?
Docker es una herramienta de contenedores que permite empaquetar aplicaciones y sus dependencias en un contenedor aislado, asegurando que se ejecute de manera uniforme en cualquier entorno, sin importar el sistema operativo o la configuración subyacente. Cada contenedor incluye el código de la aplicación, las bibliotecas y otros archivos necesarios para que funcione correctamente.

### Contenedores vs Máquinas Virtuales
A diferencia de las máquinas virtuales, que emulan un sistema completo con su propio sistema operativo, los contenedores comparten el mismo sistema operativo del host, pero están aislados entre sí. Este enfoque permite un uso más eficiente de los recursos del sistema, ya que los contenedores son más livianos y rápidos de desplegar.

En esta práctica, utilizamos **Nginx**, un servidor web de alto rendimiento utilizado para servir contenido estático, como archivos HTML, imágenes, y archivos de estilo. La combinación de Docker y Nginx nos permite gestionar contenedores con configuraciones personalizadas para proyectos web.

> **Figura 1-1**: Diagrama de contenedores. *(Agregar imagen si aplica)*

## 4. Conocimientos Previos
Para realizar esta práctica es importante estar familiarizado con los siguientes temas:

- Comandos básicos de Linux: uso de la terminal, manejo de directorios y archivos.
- Manejo de Docker: creación de contenedores, uso de imágenes y gestión de puertos.
- Manejo de Nginx: configuración básica de un servidor web para servir archivos estáticos.

Además, es importante tener un conocimiento básico de cómo funcionan los contenedores y los sistemas de archivos.

## 5. Objetivos a Alcanzar

- **Implementar contenedores con Docker**: Crear contenedores para ejecutar aplicaciones y servicios web, específicamente un servidor Nginx.
- **Manipular archivos de configuración de Nginx**: Modificar los archivos de configuración de Nginx para ajustar los parámetros del servidor.
- **Gestionar contenedores y redes de Docker**: Administrar contenedores en ejecución y configurar redes para la comunicación entre ellos.

## 6. Equipo Necesario

- Computador con sistema operativo Windows, Linux o Mac.
- Docker instalado en el sistema (versión Docker `vXX` o superior).
- Cuenta en Docker Hub para acceder a imágenes de contenedores.

## 7. Material de Apoyo

- [Documentación oficial de Docker](https://docs.docker.com/)
- Guía de la asignatura.
- [Cheat sheet de Linux](https://www.cheatography.com/)

## 8. Procedimiento

### Paso 1: Crear la estructura de carpetas

```bash
cd ~
mkdir proyecto_comandos
cd proyecto_comandos
mkdir documentos imagenes scripts

## Paso 2: Manipulación de archivos

### 2.1 Crear `notas.txt` dentro de la carpeta `documentos`

```bash
cd documentos
echo "Primera línea de notas" > notas.txt
echo "Segunda línea de notas" >> notas.txt
echo "Tercera línea de notas" >> notas.txt

from pathlib import Path

# Contenido en formato Markdown del informe solicitado
markdown_content = """
## Paso 2.2: Copiar `notas.txt` a la carpeta `scripts` y renombrarlo

```bash
cp notas.txt ../scripts/backup_notas.txt

#### Paso 2.3: Mover backup_notas.txt a la carpeta imagenes
bash
Mostrar siempre los detalles

Copiar
mv ../scripts/backup_notas.txt ../imagenes/
## Paso 3: Redirección y concatenación
### 3.1 Crear resumen.txt y redireccionar el contenido de notas.txt
bash
Mostrar siempre los detalles

Copiar
cat notas.txt > resumen.txt
### 3.2 Agregar una nueva línea a resumen.txt sin sobrescribir el contenido
bash
Mostrar siempre los detalles

Copiar
echo "Esta es una línea adicional al resumen" >> resumen.txt
Paso 4: Eliminar archivos y carpetas
### 4.1 Eliminar backup_notas.txt de la carpeta imagenes
bash
Mostrar siempre los detalles

Copiar
rm ../imagenes/backup_notas.txt
### 4.2 Eliminar la carpeta imagenes (solo si está vacía)
bash
Mostrar siempre los detalles

Copiar
rmdir ../imagenes
## 9. Resultados Esperados
Al finalizar la práctica, se espera lo siguiente:

Creación de archivos dentro de las carpetas específicas.

Correcta manipulación y redirección de archivos.

Eliminación de archivos y carpetas según lo solicitado.

Archivos generados:
notas.txt

resumen.txt

backup_notas.txt (eliminado en el paso final)

Figura 1-2: Resultado de la manipulación de archivos. (Agregar capturas de pantalla si corresponde)

### 10. Bibliografía
Docker. (2023). Documentación oficial de Docker. Recuperado de https://docs.docker.com/

Linux Command Cheat Sheet. (2023). Recuperado de https://www.cheatography.com/ """