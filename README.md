# cybersecurity-incident-report-dns-analysis-

# Análisis de Tráfico de Red e Informe de Incidente de Ciberseguridad

## Descripción del proyecto

Este proyecto documenta el análisis de un incidente de red relacionado con la resolución DNS de un sitio web. El objetivo fue investigar por qué los usuarios no podían acceder al sitio web `www.yummyrecipesforme.com` y determinar qué protocolos y servicios estaban involucrados en el incidente.

La investigación se realizó mediante el análisis de tráfico de red utilizando la herramienta **tcpdump**, identificando paquetes UDP e ICMP relacionados con el servicio DNS.

---

## Objetivos

* Analizar registros de tráfico de red capturados con tcpdump.
* Identificar los protocolos involucrados en el incidente.
* Determinar el servicio afectado.
* Identificar el puerto relacionado con el error.
* Documentar los hallazgos en un informe de incidente de ciberseguridad.

---

## Herramientas utilizadas

* tcpdump
* DNS
* UDP
* ICMP

---

## Hallazgos principales

* Servicio afectado: DNS
* Puerto afectado: 53
* Protocolo utilizado para la consulta: UDP
* Protocolo que devolvió el error: ICMP
* Mensaje observado: "UDP Port 53 Unreachable"
* Impacto: Los usuarios no pudieron acceder al sitio web.

---

## Archivos incluidos

| Archivo             | Descripción                         |
| ------------------- | ----------------------------------- |
| incident-report.md  | Informe completo del incidente      |
| traffic-analysis.md | Análisis técnico del tráfico de red |
| assets/             | Evidencias visuales y diagramas     |

---

## Conceptos aplicados

* Análisis de tráfico de red
* Resolución DNS
* Protocolos UDP e ICMP
* Investigación de incidentes
* Documentación de incidentes de ciberseguridad

---

## Conclusión

La investigación permitió identificar que las consultas DNS enviadas al puerto 53 no podían completarse correctamente. Los mensajes ICMP indicaban que el puerto UDP 53 era inalcanzable, impidiendo la resolución del nombre de dominio y el acceso al sitio web por parte de los usuarios.
