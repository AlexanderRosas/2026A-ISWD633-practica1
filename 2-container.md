# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
```
docker create --name srv-web nginx:alpine
```

<img width="1180" height="67" alt="image" src="https://github.com/user-attachments/assets/1666fcef-01ea-4883-8817-d3cb9d7db8b7" />


# COMPLETAR

Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world

<img width="1000" height="158" alt="image" src="https://github.com/user-attachments/assets/a4feaf82-75bc-4254-a061-809fc3bad6b7" />

# COMPLETAR

### Listar los contenedores ejecutándose o no

```
docker ps -a
```
<img width="1396" height="132" alt="image" src="https://github.com/user-attachments/assets/4cb74e33-29bf-4eb4-bcbe-c29ff3403623" />

### Para iniciar un contenedor

```
docker start srv-web
```
Iniciar el contenedor srv-web 

<img width="958" height="75" alt="image" src="https://github.com/user-attachments/assets/98e36781-46e9-44c1-bbad-902c5f7a6379" />

# COMPLETAR

### Listar los contenedores ejecutándose
```
docker ps 
```
<img width="1280" height="92" alt="image" src="https://github.com/user-attachments/assets/6b0c88ea-30d6-402f-b7d1-c309c1331865" />

### Para detener un contenedor

```
docker stop srv-web
```

<img width="977" height="87" alt="image" src="https://github.com/user-attachments/assets/50d38453-10cc-41aa-a7e7-7400928d7445" />

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name srv-web2 nginx:alpine
```
![Ecosistema de Docker](dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
# COMPLETAR
<img width="1168" height="572" alt="image" src="https://github.com/user-attachments/assets/b78c0601-8e1c-45fb-a7c0-e81fc8105787" />

**¿Qué sucede luego de la ejecución del comando?**
El contenedor captura la entrada estándar (stdin) del terminal, por lo que el terminal queda bloqueado y no permite introducir más comandos hasta que el contenedor se detenga.
# COMPLETAR  

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
<img width="1205" height="90" alt="image" src="https://github.com/user-attachments/assets/6a795332-9839-4a24-8ec7-74d79b3563c8" />


# COMPLETAR

### Para eliminar un contenedor

```
docker rm ef8554b3032e
```

Eliminar el contenedor que se creó a partir de la imagen hello-world 

<img width="963" height="103" alt="image" src="https://github.com/user-attachments/assets/21bc038a-8b8b-436a-80a8-0d7228358acc" />

# COMPLETAR

Verificar que el contenedor que se eliminó

<img width="1587" height="135" alt="image" src="https://github.com/user-attachments/assets/a59e0c25-93ef-4dca-a148-37f3a741da71" />

# COMPLETAR

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f srv-web3
```
Eliminar el contenedor **srv-web3** 
<img width="962" height="62" alt="image" src="https://github.com/user-attachments/assets/cedc8993-3dd4-43ef-a779-34d043cba5be" />


# COMPLETAR

Verificar que el contenedor que se eliminó
<img width="1475" height="121" alt="image" src="https://github.com/user-attachments/assets/fa54b4cc-7058-4c2c-a9e7-a5c8db31c027" />


# COMPLETAR

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 

<img width="1057" height="510" alt="image" src="https://github.com/user-attachments/assets/519fd390-9a74-4193-afac-356e4fd8a951" />

# COMPLETAR
