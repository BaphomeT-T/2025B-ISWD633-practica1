# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
# COMPLETAR
docker create --name srv-web nginx:alpine

Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world
# COMPLETAR
docker create hello-world

### Listar los contenedores ejecutándose o no

```
docker ps -a
```
<img width="1327" height="161" alt="image" src="https://github.com/user-attachments/assets/e3e0058b-fc7e-47f0-9135-9518cc437f12" />

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 
# COMPLETAR
docker start srv-web

### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```
<img width="1234" height="102" alt="image" src="https://github.com/user-attachments/assets/d37a0dbc-c78d-4291-afb8-249dc1f63034" />

### Para detener un contenedor

```
docker stop <nombre contenedor>
```

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
# COMPLETAR
docker run --name srv-web2 nginx:alpine

**¿Qué sucede luego de la ejecución del comando?**

# COMPLETAR  
Se ejecuta en primer plano.

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
# COMPLETAR
docker run -d --name srv-web3 nginx:alpine
### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
# COMPLETAR
docker rm cool_lumiere

Verificar que el contenedor que se eliminó
# COMPLETAR
<img width="1370" height="156" alt="image" src="https://github.com/user-attachments/assets/b11be8b7-55e5-4cda-b740-2f96b8e7817f" />

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 
# COMPLETAR
docker rm -f srv-web3

Verificar que el contenedor que se eliminó
# COMPLETAR
docker ps -a

<img width="1426" height="169" alt="image" src="https://github.com/user-attachments/assets/8c839fb5-fd21-45ab-8774-66a12be4dfe0" />

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
# COMPLETAR
inspect srv-web
