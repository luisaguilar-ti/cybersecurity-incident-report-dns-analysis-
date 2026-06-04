# Resumen del incidente

Varios clientes reportaron que no podían acceder al sitio web **[www.yummyrecipesforme.com](http://www.yummyrecipesforme.com)**. Al intentar ingresar, los usuarios recibían el mensaje de error **"Destination Port Unreachable"** después de esperar a que la página cargara.

Para investigar el problema, el equipo de TI reprodujo el incidente y utilizó la herramienta **tcpdump** para capturar y analizar el tráfico de red. Durante el análisis se observó que el navegador enviaba consultas DNS mediante el protocolo **UDP** al puerto **53** del servidor DNS con el fin de obtener la dirección IP del sitio web.

Sin embargo, en lugar de recibir una respuesta DNS válida, el sistema recibía mensajes **ICMP** indicando el error:

**"UDP Port 53 Unreachable"**

Este hallazgo reveló que las consultas DNS no podían ser procesadas correctamente, impidiendo que el navegador resolviera el nombre de dominio a una dirección IP. Como consecuencia, los usuarios no podían acceder al sitio web.

La investigación permitió identificar que el servicio afectado estaba relacionado con **DNS**, específicamente con el puerto **53**, utilizado para la resolución de nombres de dominio.
