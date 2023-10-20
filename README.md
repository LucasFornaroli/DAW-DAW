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


7. ¿Dónde se encuentran los ficheros de monitorización de Apache2?
• Ubicación principal
• error.log y access.log: Explica la diferencia entre estos dos archivos. Abre y revisa las entradas recientes en cada uno de ellos
• Rotación de logs: Investiga cómo funciona la rotación de logs en Apache2. ¿Por qué es importante? ¿Cómo se configura?
• Monitorización en tiempo real: Utiliza herramientas como tail -f para monitorear en tiempo real los accesos a tu servidor web y posibles errores.
• Análisis de logs: Instala y usa herramientas como goaccess para analizar y obtener estadísticas visuales a partir de tus logs de Apache2.

8. ¿Qué es un Firewall? ¿Para qué sirve? ¿Por qué es necesario? Instale y configure un Firewall en la máquina virtual para que solo permita tráfico HTTP y HTTPS. Bloquee todo el resto de los puertos y demuestre su funcionamiento.

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
