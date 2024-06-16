Proyecto Final de ciclo 

Estudio de la migración del Cortafuegos Titán 

Índice 

1. Introducción .............................................................................................................................. 3 
1. Consideraciones Previas ............................................................................................................ 3 
1. Alternativa 1: Migración del Cortafuegos a una Máquina Virtual en Calisto ............................ 4 
1. Alternativa 2: Migración del Cortafuegos a una Máquina Virtual en Luna ............................... 4 
1. Alternativa 3: Migración del Cortafuegos al Servidor Físico Jupiter.......................................... 5 
1. Comparación de Alternativas .................................................................................................... 6 
1. Introducción 

En el contexto presente, se plantea la necesidad de reestructurar la infraestructura de red de informática y del router de fibra óptica propia en un centro educativo. Este proyecto se enmarca dentro de la realidad de la institución, que cuenta con limitaciones específicas en cuanto a configuraciones de red, ubicación física de equipos y recursos tecnológicos disponibles. 

El centro educativo  dispone  de dos conexiones  de fibra óptica:  una propia con 600 Mbps destinada  a  las  aulas  de  informática,  despachos  directivos y  áreas  de  restaurantes, y otra compartida de 4 Gbps, conocida como Andared, para uso general. Además, cuenta con distintos armarios de comunicaciones distribuidos en el edificio, cada uno con su función y equipamiento específico. 

Entre los objetivos del proyecto se encuentran la optimización de la gestión de direcciones de red para las máquinas virtuales de los hipervisores, la mejora de la disponibilidad de acceso a Internet desde las redes de informática aprovechando ambas conexiones de fibra óptica, y la migración de servidores y cortafuegos para mejorar la eficiencia y redundancia del sistema. 

Dentro de este marco, se plantea la necesidad de explorar diversas alternativas para migrar el cortafuegos  Titán  a  una  nueva  infraestructura,  considerando  distintos  enfoques  como  la virtualización en los servidores Calisto o Luna, así como la migración al servidor físico Jupiter. Estas alternativas serán evaluadas en función de su viabilidad técnica, recursos necesarios y la optimización general de la red del centro educativo. 

2. Consideraciones Previas 

Antes de adentrarnos en las alternativas específicas para la migración del cortafuegos Titán, es crucial tener en cuenta una serie de consideraciones que influirán en la viabilidad y efectividad de dicha migración. Estas consideraciones incluyen: 

- Ubicación Física de los Equipos: Evaluar la ubicación física de los servidores Calisto, Luna y Júpiter, así como del cortafuegos Titán. La distancia entre estos equipos puede afectar la latencia y la velocidad de la red, así como los recursos de red necesarios para la migración. 
- Capacidad  de  los  Servidores:  Analizar  la  capacidad  de  procesamiento,  memoria  y almacenamiento de los servidores Calisto, Luna y Júpiter. Es fundamental asegurarse de que tienen los recursos suficientes para alojar y ejecutar el cortafuegos Titán de manera eficiente, además de otras cargas de trabajo existentes o futuras. 
- Configuración de Red Existente: Comprender la topología de red actual, incluyendo las direcciones IP, las subredes, las puertas de enlace y los dispositivos de red involucrados. Cualquier cambio en la configuración de red debe realizarse cuidadosamente para evitar interrupciones en el servicio y conflictos de direcciones IP. 
- Requisitos de Seguridad: Considerar los requisitos de seguridad de la red, incluyendo políticas de acceso, filtrado de tráfico y protección contra amenazas. Es fundamental garantizar que el cortafuegos migrado mantenga los mismos niveles de seguridad o los mejore. 
- Disponibilidad del Servicio: Minimizar el tiempo de inactividad durante la migración del cortafuegos para evitar interrupciones en el acceso a Internet y otros servicios críticos. 

Se deben planificar estrategias de respaldo y recuperación en caso de fallas durante el proceso de migración. 

3. Alternativa 1: Migración del Cortafuegos a una Máquina Virtual en Calisto 

   Esta alternativa implica migrar el cortafuegos Titán a una máquina virtual alojada en el servidor Calisto. Calisto es un servidor ubicado en el armario de Andared, con una conexión a la red del router de fibra óptica propia y la capacidad suficiente para ejecutar aplicaciones críticas como un cortafuegos. A continuación, se detallan los pasos y consideraciones clave de esta alternativa: 

- Evaluación  de  Recursos:  Se  debe  evaluar  la  capacidad  de  Calisto  para  alojar  el cortafuegos Titán junto con otras cargas de trabajo existentes. Es necesario garantizar que Calisto tenga suficiente capacidad de procesamiento, memoria y almacenamiento para ejecutar el cortafuegos de manera eficiente. 
- Configuración de Red: Se debe configurar la red de la máquina virtual del cortafuegos en Calisto para asegurar la conectividad adecuada con las redes internas y externas. Esto incluye  la  asignación  de  direcciones  IP,  la  configuración  de  reglas  de  firewall  y  la integración con el router de fibra óptica propia. 
- Migración de Configuraciones: Se deben migrar las configuraciones del cortafuegos Titán al nuevo entorno en Calisto. Esto incluye las reglas de firewall, las políticas de seguridad y cualquier configuración específica de la red. Es fundamental asegurarse de que todas las configuraciones se apliquen correctamente y no se pierdan durante el proceso de migración. 
- Pruebas de Funcionalidad: Antes de poner en producción el cortafuegos migrado en Calisto,  se  deben  realizar  pruebas  exhaustivas  para  garantizar  su  funcionalidad  y seguridad. Esto incluye pruebas de conectividad, pruebas de rendimiento y pruebas de penetración para identificar posibles vulnerabilidades. 
- Implementación y Monitorización: Una vez completada la migración y las pruebas de funcionalidad, se puede implementar el cortafuegos migrado en producción en Calisto. Es importante establecer un proceso de monitorización continua para supervisar el rendimiento y la seguridad del cortafuegos en su nuevo entorno. 
- Respaldo  y  Recuperación:  Se  deben  establecer  procedimientos  de  respaldo  y recuperación para el cortafuegos migrado en Calisto. Esto garantizará la disponibilidad del servicio en caso de fallas o incidentes de seguridad. 

La migración del cortafuegos a una máquina virtual en Calisto ofrece la ventaja de aprovechar la capacidad de procesamiento y almacenamiento del servidor existente, así como la flexibilidad y escalabilidad de la virtualización. Sin embargo, es crucial realizar una planificación cuidadosa y pruebas exhaustivas para garantizar una migración exitosa y sin problemas. 

4. Alternativa 2: Migración del Cortafuegos a una Máquina Virtual en Luna 

   La segunda alternativa consiste en migrar el cortafuegos Titán a una máquina virtual alojada en el servidor Luna. Luna es un servidor ubicado en el armario de Informática, conectado a la red del router de fibra óptica propia y con capacidad para ejecutar aplicaciones críticas como un cortafuegos. A continuación, se detallan los pasos y consideraciones clave de esta alternativa: 

- Evaluación de Recursos: Se debe evaluar la capacidad de Luna para alojar el cortafuegos Titán junto con otras cargas de trabajo existentes. Es fundamental garantizar que Luna tenga suficiente capacidad de procesamiento, memoria y almacenamiento para ejecutar 

  el cortafuegos de manera eficiente. 

- Configuración de Red: Se debe configurar la red de la máquina virtual del cortafuegos en Luna para asegurar la conectividad adecuada con las redes internas y externas. Esto incluye  la  asignación  de  direcciones  IP,  la  configuración  de  reglas  de  firewall  y  la integración con el router de fibra óptica propia. 
- Migración de Configuraciones: Se deben migrar las configuraciones del cortafuegos Titán al nuevo entorno en Luna. Esto implica trasladar las reglas de firewall, las políticas de seguridad y cualquier configuración específica de la red. Es esencial asegurarse de que todas las configuraciones se apliquen correctamente y no se pierdan durante el proceso 

  de migración. 

- Pruebas de Funcionalidad: Antes de poner en producción el cortafuegos migrado en Luna,  se  deben  realizar  pruebas  exhaustivas  para  garantizar  su  funcionalidad  y seguridad. Esto incluye pruebas de conectividad, pruebas de rendimiento y pruebas de penetración para identificar posibles vulnerabilidades. 
- Implementación y Monitorización: Una vez completada la migración y las pruebas de funcionalidad, se puede implementar el cortafuegos migrado en producción en Luna. Se debe establecer un proceso de monitorización continua para supervisar el rendimiento 

  y la seguridad del cortafuegos en su nuevo entorno. 

- Respaldo  y  Recuperación:  Se  deben  establecer  procedimientos  de  respaldo  y recuperación para el cortafuegos migrado en Luna. Esto garantizará la disponibilidad del servicio en caso de fallas o incidentes de seguridad. 

La migración del cortafuegos a una máquina virtual en Luna ofrece la ventaja de aprovechar la capacidad  de  procesamiento  y  almacenamiento  del  servidor  existente  en  el  armario  de Informática. Sin embargo, es crucial realizar una planificación cuidadosa y pruebas exhaustivas para garantizar una migración exitosa y sin problemas. 

5. Alternativa 3: Migración del Cortafuegos al Servidor Físico Júpiter 

La tercera alternativa implica migrar el cortafuegos Titán al servidor físico Júpiter. Júpiter es un servidor ubicado en el armario de Informática, con capacidad para ejecutar aplicaciones críticas como un cortafuegos y conectado a la red del router de fibra óptica propia. A continuación, se detallan los pasos y consideraciones clave de esta alternativa: 

- Evaluación  de  Recursos:  Se  debe  evaluar  la  capacidad  de  Júpiter  para  alojar  el cortafuegos Titán junto con otras cargas de trabajo existentes. Es fundamental garantizar que Júpiter tenga suficiente capacidad de procesamiento, memoria y almacenamiento para ejecutar el cortafuegos de manera eficiente. 
- Configuración de Red: Se debe configurar la red del cortafuegos en Júpiter para asegurar la conectividad adecuada con las redes internas y externas. Esto incluye la asignación de direcciones IP, la configuración de reglas de firewall y la integración con el router de fibra óptica propia. 
- Migración de Configuraciones: Se deben migrar las configuraciones del cortafuegos Titán al nuevo entorno en Júpiter. Esto implica trasladar las reglas de firewall, las políticas de seguridad y cualquier configuración específica de la red. Es esencial asegurarse de que todas las configuraciones se apliquen correctamente y no se pierdan durante el proceso de migración. 
- Pruebas de Funcionalidad: Antes de poner en producción el cortafuegos migrado en Júpiter,  se  deben  realizar  pruebas  exhaustivas  para  garantizar  su  funcionalidad  y seguridad. Esto incluye pruebas de conectividad, pruebas de rendimiento y pruebas de penetración para identificar posibles vulnerabilidades. 
- Implementación y Monitorización: Una vez completada la migración y las pruebas de funcionalidad, se puede implementar el cortafuegos migrado en producción en Júpiter. Se  debe  establecer  un  proceso  de  monitorización  continua  para  supervisar  el rendimiento y la seguridad del cortafuegos en su nuevo entorno. 
- Respaldo  y  Recuperación:  Se  deben  establecer  procedimientos  de  respaldo  y recuperación para el cortafuegos migrado en Júpiter. Esto garantizará la disponibilidad del servicio en caso de fallas o incidentes de seguridad. 

La  migración  del  cortafuegos  al  servidor  físico  Júpiter  ofrece  la  ventaja  de  aprovechar  la capacidad  de  procesamiento  y  almacenamiento  del  servidor  existente  en  el  armario  de Informática. Sin embargo, es crucial realizar una planificación cuidadosa y pruebas exhaustivas para garantizar una migración exitosa y sin problemas. 

6. Comparación de Alternativas 

A  continuación,  se  realiza  un  análisis  comparativo  de  las  tres  alternativas  para  migrar  el cortafuegos  Titán,  con  el  objetivo  de  determinar  cuál  opción  es  más  adecuada  para  las necesidades del centro educativo: 

- Viabilidad Técnica: Todas las alternativas son técnicamente viables, ya que los servidores Calisto,  Luna  y  Júpiter  tienen  la  capacidad  de  alojar  el  cortafuegos  Titán  y  están conectados a  la  red  del router de fibra óptica propia. Sin embargo, es  importante considerar la capacidad de procesamiento, memoria y almacenamiento de cada servidor para garantizar un rendimiento óptimo del cortafuegos. 
- Recursos  Necesarios:  La  migración  del  cortafuegos  requerirá  recursos  de  tiempo  y personal capacitado en administración de redes y virtualización. Las alternativas que involucran máquinas virtuales (Calisto y Luna) requerirán configuraciones adicionales de virtualización, mientras que migrar a un servidor físico (Jupiter) puede implicar menos configuraciones en términos de virtualización, pero puede requerir más recursos de hardware. 
- Complejidad: La complejidad de cada alternativa varía en función de la infraestructura existente y los conocimientos técnicos disponibles en el centro educativo. La migración a una máquina virtual puede ser más compleja debido a la configuración adicional de virtualización,  mientras  que  migrar  a  un  servidor  físico  puede  ser  más  directo  en términos de configuración. 
- Riesgos:  Todos  los  enfoques  de  migración  conllevan  riesgos  potenciales,  como interrupciones en el servicio, pérdida de datos o vulnerabilidades de seguridad. Es crucial realizar pruebas exhaustivas y establecer medidas de respaldo y recuperación para mitigar estos riesgos. 
Pablo Valencia 
