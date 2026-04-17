# Imagen
### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull hello-world
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull nginx:alpine
```

Descargar la imagen **hello-world**
# COMPLETAR

**¿Qué es nginx?**
Nginx es un servidor web de código abierto, proxy inverso, balanceador de carga y caché de HTTP. Es conocido por su alto rendimiento, estabilidad y bajo consumo de recursos.
# COMPLETAR 

Descargar la imagen  **nginx** en la versión **alpine**
# COMPLETAR
<img width="1011" height="323" alt="image" src="https://github.com/user-attachments/assets/0882f9b2-1b02-429a-88a8-6b6d203973dd" />

### Listar imágenes
<img width="871" height="185" alt="image" src="https://github.com/user-attachments/assets/15d75d85-97da-44d2-b278-2d03cfb29314" />

```
docker images
```

# COLOCAR UNA CAPTURA DE PANTALLA DEL RESULTADO 

**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect hello-world

```

Inspeccionar la imagen hello-world 
<img width="1143" height="592" alt="image" src="https://github.com/user-attachments/assets/2f2c37e7-c81f-41bf-87ac-f8ce6f74a208" />

# COMPLETAR

**¿Con qué algoritmo se está generando el ID de la imagen**
Se genera mediante el algoritmo SHA-256 (Secure Hash Algorithm 256-bit).

# COMPLETAR

### Filtrar imágenes

```
docker images | grep nginx

```

### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi hello-world
```

Eliminar la imagen hello-world 
# COMPLETAR

<img width="1065" height="105" alt="image" src="https://github.com/user-attachments/assets/21ec08ca-b519-4e9a-bde4-39738b4d8c9a" />


-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```
