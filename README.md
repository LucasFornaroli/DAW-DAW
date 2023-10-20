1. Instale en una máquina virtual un sistema operativo con base Linux (se recomienda Debian o Ubuntu) e instale apache2.
![Respuesta 1](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/7a526bdc-d96b-47a0-a058-04f95137fdb4)

2. Explique con sus palabras que es una petición GET, POST, PUT y DELETE, remarcando sus diferencias. 
GET: Le pide al servidor informacion que necesite.
POST: Se utiliza cuando tienes que enviarle datos al servidor.
PUT: Se utiliza para actualizar los datos que envias al servidor.
DELETE: Elimina una informacion especifica.

3. Cambie del puerto 80 al puerto 4444 el servidor apache2. Muestra desde el navegador su funcionamiento adjuntando una captura de pantalla. 
![Respuesta 3](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/e8dcb978-e694-444d-8fe3-27d7d0e65c1f)

4. Instale un certificado SSL y configure su Apache para servir contenido a través de HTTPS en el puerto 4444. Muestre desde el navegador cómo se muestra el sitio web como "seguro" (aunque sea un certificado autofirmado).
![Respuesta 4](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/c36bc944-f4ef-49b4-8913-71197f4b26e5)

5. ¿Dónde se encuentran los ficheros de configuración de Apache2?
• Ubicación principal.
La ubicacion es /etc/apache2/apache2.conf
• Explora el archivo apache2.conf. Identifica las secciones principales y describe su propósito.
Global configuration: Es la seccion principal y tiene configuraciones para el servidor web.
ServerRoot: Especifica la ubicacion del directorio
Timeout: Es el tiempo maximo que espera el servidor antes de denegar la solicitud.
• sites-available y sites-enabled: Explica la diferencia entre estos dos directorios y cómo funcionan juntos.
En el sites-available se encuentran todos los sitios web del servidor, en cambio en el sites-enabled solo se encuentran los sitios habilitados.
• mods-available y mods-enabled: Explica la diferencia entre estos dos directorios.
La diferencia es que mods-available es el directorio en el que estan los modulos disponibles en la instalacion actual, mientras que en mods-enabled se incluyen mediante enlaces el directorio anterior.

6. ¿Dónde se encuentran los ficheros de ejecución de Apache2?
• Ubicación principal
![Respuesta 6](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/b25592de-e32a-47f8-b83d-80d8c18618b5)

• Control del servicio: Utiliza el binario de ejecución para iniciar, detener, recargar y reiniciar el servidor Apache2 explicando la diferencia entre cada uno de los comandos utilizados.
![Respuesta 6 1](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/8cd1098f-bfd7-4f54-9b4d-2552dac93bda)

El caso del entre recargar y reiniciar es que que al recargar no se reinicia apache y preserva todas las conexiones del usuario, por otro lado iniciar y detener sirven para lo que su mismo nombre indica, y la diferencia entre ellos es que son lo opuesto.
• Comprobación de sintaxis: Usa el binario de Apache para verificar la sintaxis de tu configuración. Esto es útil para asegurarse de que no haya errores antes de reiniciar el servidor.
![Respuesta 6 2](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/647afa4f-6e8e-4f09-ac35-bdc81822ef5f)

7. ¿Dónde se encuentran los ficheros de monitorización de Apache2?
• Ubicación principal
La ubicacion es /var/log/apache2
• error.log y access.log: Explica la diferencia entre estos dos archivos. Abre y revisa las entradas recientes en cada uno de ellos
La diferencia entre estos es que error.log registra mensajes de error y errores relacionados con el servicio web, en cambio access.log registra las solicitudes de acceso al servidor web.
![Respuesta 7 1](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/e41295da-61f9-4473-9072-520d16b98837)

![Respuesta 7 2](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/c4ac1776-492f-494f-85b6-6edf61f0f252)

• Rotación de logs: Investiga cómo funciona la rotación de logs en Apache2. ¿Por qué es importante? ¿Cómo se configura?
La rotacion de logs en apache2 es importante porque gestiona el espacio en disco al limitar el tamaño de los archivos, mantiene los registros organizados y faciles de buscar y mejora el rendimiento del servidor.
![Respuesta 7 3](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/733d4433-1eed-4c7c-8655-8542eac86399)

• Monitorización en tiempo real: Utiliza herramientas como tail -f para monitorear en tiempo real los accesos a tu servidor web y posibles errores.
![Respuesta 7 4](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/7a8dca0e-0e0e-47d3-9802-0801bbc5ca20)

• Análisis de logs: Instala y usa herramientas como goaccess para analizar y obtener estadísticas visuales a partir de tus logs de Apache2.
![Respuesta 7 5](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/dea1175b-4341-4cb9-8f84-4500c4731625)

8. ¿Qué es un Firewall? ¿Para qué sirve? ¿Por qué es necesario? Instale y configure un Firewall en la máquina virtual para que solo permita tráfico HTTP y HTTPS. Bloquee todo el resto de los puertos y demuestre su funcionamiento.
El firewall es un sistema que se encarga de la seguridad de la red en los ordenadores, y restringe el trafico de red que ingresa al ordenador y el que sale del mismo. Funciona bloqueando o permitiendo paquetes de datos de forma selectiva.
![Respuesta 8](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/700f9bdd-c155-4863-acfa-d43eda72f74c)
![Respuesta 8 1](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/d80715ab-b716-4882-9d8b-1a1fc280ba29)
![Respuesta 8 2](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/5ca58bc6-b24e-4c2c-a6a3-562fb65b9936)
![Respuesta 8 3](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/829621f6-8aea-4088-a157-889b30836445)
![Respuesta 8 4](https://github.com/LucasFornaroli/DAW-DAW/assets/144775513/10c9ea9a-fa2f-42d3-a6a8-28c556e625fa)

9. Explica con tus palabras las diferentes partes de una URL.
Protocolo: El HTTPS es el encargado de permitir la transferencia de informacion en internet, es el encargado de permitir la comunicacion entre en cliente y el servidor.
Subdominio: Por lo general es www, estos permiten que se adquiera un dominio adicional para crear divisiones en el sitio web.
Dominio: Es el que muestra el nombre unico del sitio web, por eso no hay que utilizar ip, estos pueden ser adquiridos gracias a empresas que los venden.
TLD: Es la extension del dominio, es la parte final del dominio e indica su origen.
Carpeta o subcarpeta: Esta se utiliza para organizar la estructura de la web, y nos dice que dentro existe algun archivo.
Pagina: Este hace referencia a algun archivo del sitio web.
Etiqueta: Es una referencia al contenido de una pagina

10. Explica el funcionamiento del protocolo HTTP con tus palabras.
El cliente envia una peticion, el servidor la recibe y le envia una respuesta y el cliente recibe la respuesta.

11. ¿Qué es un archivo .htaccess? Proporcione un ejemplo de cómo se puede utilizar para reescribir URL o restringir el acceso a ciertas partes de su sitio web.
El archivo .htaccess es un archivo que se utiliza en servidores web y se encarga de controlar y configurar un directorio.

Si queremos que mipagina.com muestre el contenido de mipagina.com/pagina.php hay que poner en .htaccess:
RewriteEngine On
RewriteRule ejemplo$ pagina.php?seccion=ejemplo

Esto hace que te redirija  a mipagina.com/ejemplo
