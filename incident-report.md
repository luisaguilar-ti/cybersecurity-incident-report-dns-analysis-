# Informe de Incidente de Ciberseguridad

## Análisis de Tráfico de Red

### Parte 1: Proporcione un resumen del problema encontrado en el registro de tráfico DNS e ICMP

**El protocolo UDP revela que:**

El navegador envió una consulta DNS mediante el protocolo UDP al puerto 53 con el fin de obtener la dirección IP correspondiente al dominio del sitio web.

**Esto se basa en los resultados del análisis de red, los cuales muestran que la respuesta ICMP devolvió el siguiente mensaje de error:**

"UDP Port 53 Unreachable" (Puerto UDP 53 inalcanzable).

**El puerto indicado en el mensaje de error se utiliza para:**

El puerto 53 se utiliza para el servicio DNS, encargado de traducir nombres de dominio en direcciones IP para permitir el acceso a los sitios web.

**El problema más probable es:**

El servicio DNS no estaba disponible o no estaba escuchando en el puerto 53, impidiendo que las consultas DNS fueran procesadas correctamente.

---

### Parte 2: Explique su análisis de los datos y proporcione al menos una causa del incidente

**Hora en que ocurrió el incidente:**

13:24:32

**Explique cómo el equipo de TI tuvo conocimiento del incidente:**

El equipo de TI tuvo conocimiento del incidente después de que varios clientes reportaran que no podían acceder al sitio web.

**Explique las acciones realizadas por el departamento de TI para investigar el incidente:**

El equipo de TI recibió los reportes de los clientes, reprodujo el problema y utilizó la herramienta tcpdump para capturar y analizar el tráfico de red. Posteriormente revisó los paquetes UDP e ICMP involucrados en la comunicación y detectó mensajes de error relacionados con el puerto 53 utilizado por DNS.

**Indique los hallazgos clave de la investigación realizada por el departamento de TI (por ejemplo, detalles relacionados con el puerto afectado, el servidor DNS, los protocolos involucrados, etc.):**

* Servicio afectado: DNS.
* Puerto afectado: 53.
* Protocolo utilizado para la consulta: UDP.
* Protocolo que devolvió el error: ICMP.
* Mensaje identificado: "UDP Port 53 Unreachable".
* Los usuarios no podían resolver el nombre de dominio ni acceder al sitio web.

**Indique una causa probable del incidente:**

La causa probable del incidente fue que el servicio DNS no estaba disponible o no estaba escuchando en el puerto 53. Como consecuencia, las consultas DNS no pudieron completarse correctamente y los usuarios no pudieron acceder al sitio web.



