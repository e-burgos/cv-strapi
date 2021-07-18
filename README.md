# ACERCA DEL PROYECTO
CV Personal utilizando como backend Strapi headless CMS.

### PROJECTO ONLINE
https://www.estebanburgos.com.ar/


## PRIMEROS PASOS PARA USAR STRAPI EN TUS PROYECTOS (MacOS)

1. Debes tener al menos instalado node version >= 10 y npm version >=6

2. Asegurate de tener instalado y corriendo un servidor MySQL local o con la base de datos con la que generalmente trabajes, en este caso utilizare mysql.

3. Si no instalaste un servidor MySQL local te recomendo MAMP, solo ten presente que para correr mysql por consola sea necesario modificar tu .bash_profile, para ello abre tu consola en el directorio raíz de tu mac y escribe lo siguiente:

        nano .bash_profile
        export PATH=/Applications/MAMP/Library/bin:$PATH 
        > pegar esta linea dentro de archivo
        > pulsa control + o para guardar
        > pulsa control + x para salir 

4. Genera una DB MySQL (en este ejemplo llamada miproyecto) por consola utilizando los siguientes comandos:

        mysql -u root -p
        > ingresa la password en caso de tener ua configurada
        mysql> CREATE DATABASE miproyecto;
        mysql> show databases;
        mysql> exit

> **Nota:** debes conocer el usuario y password que configuraste al momento de instalar el servidor local.

5. Ahora si, ubicate en el directorio donde deseas inicializar el proyecto strapi en consola y sigue las siguientes instrucciones:
        
        npx create-strapi-app miproyecto
        > selecciona mysql 
        > Database name: miproyecto
        > Host: 127.0.0.1
        > Port: 3306 (o ingresa el puerto de tu configuración local)
        > Username: tu usuario local 
        > Password: tu password local
        > Enable SSL connection: n

6. Esto creará el proyecto, luego debes inicializarlo ingresando a la carpeta creada por strapi:

        cd miproyecto
        npm run develop

7. Esto abrirá una página donde puedes registrar tu usuario, de lo contrario ingresa a http://localhost:1337/admin o la url mostrada por consola.

8. Genera tu usuario, y comienza a crear tu contenido agregando Content-Types.  




