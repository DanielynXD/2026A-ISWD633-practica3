# BIND MOUNT
En un bind mount mapeamos (montar) un directorio o archivo específico del sistema de archivos del host con una parte del sistema de ficheros del contenedor.

```
docker run -d --name <nombre contenedor> -v <ruta carpeta host>:<ruta carpeta contenedor> <imagen> 
```
ó
```
docker run -d --name <nombre contenedor> --mount type=bind,source=<ruta carpeta host>,target=<ruta carpeta contenedor> <imagen>
```
- destination, dst, target: La ruta donde se monta el archivo o directorio en el contenedor.
- source, src: El origen del montaje.
  
### En tu computador crear una carpeta llamada nginx y dentro de esta carpeta crea otra llamada html. Como se aprecia en la figura.
![Volúmenes](directorio.PNG)

### Crear un contenedor con la imagen nginx:alpine, mapear todos por puertos, para la ruta carpeta host colocar el directorio en donde se encuentra la carpeta html en tu computador y para la ruta carpeta contenedor: /usr/share/nginx/html (esta ruta se obtiene al revisar la documentación de la imagen)
![Volúmenes](volumen-host.PNG)
# COMPLETAR CON EL COMANDO
<img width="1441" height="53" alt="image" src="https://github.com/user-attachments/assets/362ad251-5ee1-4dfe-b00b-a03afe04e2a3" />


### ¿Qué sucede al ingresar al servidor de nginx?
Aparece el erro 403 Forbidden, ya que no hay nada en la carpeta nginex/html 
<img width="1204" height="224" alt="image" src="https://github.com/user-attachments/assets/93350169-fac7-42e0-8517-655a87650849" />



### ¿Qué pasa con el archivo index.html del contenedor?
El archivo index.html que viene por defecto queda oculto. Nginx no puede acceder a el mientras el contenedor este usando la carpeta local.

### Ir a https://html5up.net/ y descargar un template gratuito, descomprirlo dentro de tu computador en la carpeta html
### ¿Qué sucede al ingresar al servidor de nginx?
Ahora si tiene un archivo index.html y se ve la página web del template que descargué, esto sin tener que reiniciar el contenedor.

### Eliminar el contenedor
<img width="493" height="144" alt="image" src="https://github.com/user-attachments/assets/f9ed570d-8ff4-4f44-80a3-481d9637b46b" />


### ¿Qué sucede al crear nuevamente un contenedor montado al directorio definidos anteriormente?
<img width="1456" height="96" alt="image" src="https://github.com/user-attachments/assets/25f5ec99-e002-4858-b45b-9b00c33edde8" />

Al ingresar al servidor de nginx se sigue mostrando la página web del template que descargue, lo que quiere decir que al eliminar el contenedor persistieron los datos.


