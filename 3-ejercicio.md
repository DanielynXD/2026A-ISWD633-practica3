## Esquema para el ejercicio
![Imagen](esquema-ejercicio3.PNG)

### Crear red net-wp
<img width="779" height="233" alt="image" src="https://github.com/user-attachments/assets/c9e08d73-d35b-43db-9aa3-058c0a095ce2" />


### Para que persista la información es necesario conocer en dónde mysql almacena la información.
# COMPLETAR LA SIGUIENTE ORACIÓN. REVISAR LA DOCUMENTACIÓN DE LA IMAGEN EN https://hub.docker.com/
En el esquema del ejercicio carpeta del contenedor (a) es /var/lib/mysql

Ruta carpeta host: C:/docker/ejercicio3/db

### ¿Qué contiene la carpeta db del host?
No contiene nada al inicio.

### Crear un contenedor con la imagen mysql:8  en la red net-wp, configurar las variables de entorno: MYSQL_ROOT_PASSWORD, MYSQL_DATABASE, MYSQL_USER y MYSQL_PASSWORD
<img width="1448" height="82" alt="image" src="https://github.com/user-attachments/assets/2797b409-c603-4f2c-810f-2c578a9e9f45" />


### ¿Qué observa en la carpeta db que se encontraba inicialmente vacía?
Ahora aparecieron muchos archivos del contenedor.

### Para que persista la información es necesario conocer en dónde wordpress almacena la información.
# COMPLETAR LA SIGUIENTE ORACIÓN. REVISAR LA DOCUMENTACIÓN DE LA IMAGEN EN https://hub.docker.com/
En el esquema del ejercicio la carpeta del contenedor (b) es /var/www/html/

Ruta carpeta host: C:/docker/ejercicio3/www

### Crear un contenedor con la imagen wordpress en la red net-wp, configurar las variables de entorno WORDPRESS_DB_HOST, WORDPRESS_DB_USER, WORDPRESS_DB_PASSWORD y WORDPRESS_DB_NAME (los valores de estas variables corresponden a los del contenedor creado previamente)
<img width="1455" height="124" alt="image" src="https://github.com/user-attachments/assets/ab776fbe-019a-4059-a43d-ca6d4c8f078e" />

<img width="806" height="856" alt="image" src="https://github.com/user-attachments/assets/3527bcd5-76ed-4a78-b708-5abe563f369f" />

### Personalizar la apariencia de wordpress y agregar una entrada
<img width="1909" height="1077" alt="image" src="https://github.com/user-attachments/assets/f4ba7c52-ad1e-4756-b426-e9433a041831" />

### Eliminar el contenedor y crearlo nuevamente, ¿qué ha sucedido?
<img width="1462" height="235" alt="image" src="https://github.com/user-attachments/assets/dfaf5125-3411-465e-a8e0-36f0831796ea" />
<img width="1459" height="99" alt="image" src="https://github.com/user-attachments/assets/4c5895d2-68ca-4687-b20a-f6b0bb7370e5" />
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/bd5110fc-4d95-4553-a2ad-ab0a9863308a" />


-Los datos estan a salvo, se ve la persistencia de los datos, al eliminar el contenedor y volverlo a crear no afecta en nada xq los archivos de los contenedores estan en local y al crear uno nuevo y vincularlo seguirá funcionando igual.

