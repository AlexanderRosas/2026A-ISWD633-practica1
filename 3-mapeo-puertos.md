# Mapeo de puertos
El mapeo de puertos es un mecanismo que permite redirigir el tráfico de red desde un puerto en el host (tu máquina local o servidor) hacia un puerto específico en un contenedor Docker.
Por ejemplo, supongamos que tienes un contenedor que ejecuta un servidor web en el puerto 80 dentro del contenedor, pero quieres acceder a ese servidor desde tu navegador en la máquina host. Puedes usar el mapeo de puertos para redirigir el tráfico del puerto 80 del contenedor al puerto 3000 en el host. De esta manera, cuando accedas a http://localhost:3000 en tu navegador, el tráfico se dirigirá al servidor web dentro del contenedor en el puerto 80.

![mapeo](mapeoPuertos.PNG)

### Para crear un mapeo de puertos (puerto host y puerto contenedor)
El mapeo de puertos se especifica al ejecutar un contenedor Docker utilizando la opción -p o --publish seguida de los puertos que deseas mapear
```
docker run -d --name srv-web-mapeo -p 3000:80 nginx:alpine

```
Crear un contenedor a partir de la imagen nginx version alpine con el mapeo de puertos del ejemplo gráfico, host 3000 y contenedor 80
<img width="1420" height="95" alt="image" src="https://github.com/user-attachments/assets/38f307c6-c19f-4642-ad98-12aab45eef80" />

# COMPLETAR

# COLOCAR UNA CAPTURA DE PANTALLA  DEL ACCESO http://localhost:3000

<img width="1912" height="581" alt="image" src="https://github.com/user-attachments/assets/2604f974-4f96-49cb-9228-39988ba50f2a" />


### Para mapear más de un puerto

```
docker run -d --name <nombre contenedor> -p <puerto host 01>:<puerto contenedor 01> -p <puerto host 02>:<puerto contenedor 02> <nombre imagen>:<tag>
```

Crear un contenedor a partir de la imagen rabbitmq version management-alpine, para este mapeo de puertos usar en el host los mismos puertos del contenedor.
# COMPLETAR

### Usando una forma más semántica cuando se especifican puertos

```
docker run -d --name <nombre contenedor> --publish published=<valorPuertoHost>,target=<valor> <nombre imagen>:<tag> 
```

<img width="1667" height="396" alt="image" src="https://github.com/user-attachments/assets/5d13dc04-b9c8-4432-bb3e-e14a542a1b5c" />
<img width="1672" height="446" alt="image" src="https://github.com/user-attachments/assets/ec977098-a4e6-4b9d-b58a-81dbe6b94852" />


### Publicando todos los puertos
```
docker run -P -d --name <nombre contenedor> <nombre imagen>:<tag> 
```
<img width="1622" height="78" alt="image" src="https://github.com/user-attachments/assets/035640f9-ced1-4a00-a475-cafabf91352b" />

-P: le indica a Docker que asigne automáticamente puertos aleatorios en tu host para todos los puertos expuestos por el contenedor.

**Recordar**
No puedes mapear puertos a un contenedor existente directamente después de su creación con Docker. El mapeo de puertos debe especificarse en el momento de crear y ejecutar el contenedor.

### Crear contenedor de Jenkins puertos contenedor: 8080 (interface web) y 50000 (comunicación entre nodos) imagen: jenkins/jenkins:alpine3.18-jdk11
# COMPLETAR

# COLOCAR UNA CAPTURA DE PANTALLA  DEL ACCESO http://localhost:8080
<img width="1258" height="873" alt="image" src="https://github.com/user-attachments/assets/045416db-d80d-406b-bdbf-3d5885112732" />

<img width="1630" height="967" alt="image" src="https://github.com/user-attachments/assets/b70f9b59-7a7c-4706-bf53-961c878ef3ca" />

### ¿Cómo obtener la contraseña solicitada?
Para obtener la contraseña solicitada es necesario ingresar al contenedor.


![Imagen](jenkins.PNG)

