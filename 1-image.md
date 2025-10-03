# Imagen
### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull <nombre imagen> 
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull <nombre imagen>:<tag>
```

Descargar la imagen **hello-world**
# COMPLETAR
docker pull hello-world

**¿Qué es nginx?**
# COMPLETAR 
Es un servidor web de alto rendimiento y bajo consumo de recursos. Su función principal es servir páginas web. Es utilizado como servidor web estático, proxy inverso, balaceador de carga, servidor de correo, gestor de conexiones etc.

Descargar la imagen  **nginx** en la versión **alpine**
# COMPLETAR
docker pull nginx:alpine
### Listar imágenes

```
docker images
```
# COLOCAR UNA CAPTURA DE PANTALLA DEL RESULTADO 
<img width="792" height="146" alt="image" src="https://github.com/user-attachments/assets/28fb0d52-625a-4b4c-95df-cf9e8587f2a3" />
**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```
Inspeccionar la imagen hello-world 
# COMPLETAR
docker inspect hello-world
**¿Con qué algoritmo se está generando el ID de la imagen**
# COMPLETAR
sha256

### Filtrar imágenes

```
docker images | grep <termino a buscar>

```

### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi <nombre imagen>:<tag>
```

Eliminar la imagen hello-world 
# COMPLETAR
docker rmi hello-world:latest

-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```
docker rmi -f hello-world:latest
