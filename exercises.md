# Análisis de Escenarios
Analizar el escenario y completar las acciones a realizar en cada fase del manejo de la respuesta ante incidentes.


## Escenario 1: Infestación por Gusanos y Denegación Distribuida de Servicio (DDoS)

- Este escenario es una compañía de inversiones pequeña y familiar.
- La organización tiene solo una sede y menos de 100 empleados.
- Es martes por la mañana y se libera un gusano nuevo; se propaga por medios extraíbles, y se puede copiar a sí mismo en recursos compartidos de Windows.
- Cuando el gusano infecta a un host, instala un agente de DDoS.
- Solo hubo firmas de antivirus disponibles varias horas después de que el gusano comenzara a propagarse.
- La organización ya había sufrido infecciones masivas.
- La compañía de inversiones ha contratado a un pequeño grupo de expertos en seguridad que suelen utilizar el modelo diamante para el manejo de incidentes de seguridad.  

### Fase Preparación
¿Tienen un equipo CSIRT definido con roles definidos y responsabilidades asignadas? Sí  
¿Tienen un canal de comunicación propio? Se desconoce.  
¿Quienes son los contactos clave? Se desconoce.  
¿Se han coordinado con las autoridades? No.  
¿Qué sistemas de detección usan? Antivirus.  
¿Tienen un plan de respuesta ante incidentes? Parece que no a tenor que habían sufrido otros incidentes anteriormente.  
¿Están definidos los procedimientos a seguir ante un incidente? No  
¿Existe una guía de actuación? Se desconoce.  
¿Los empleados están concienciados? ¿Se han hecho formaciones? Parece que no a tenor que habían sufrido otros incidentes anteriormente.   
¿Se han realizado simulacros? Se desconoce.  
¿El CSIRT está formado y entrenado? Parece que sí, pues son expertos y utilizan el modelo diamante, pero en esta ocasión no lo pusieron en práctica.  


### Fase Detección y análisis
¿Qué alerta/s saltaron en el SIEM? Se desconoce.  
¿Cuál es el vector del ataque? Medios extraíbles y recursos compartidos.
¿Se revisaron los logs? Se desconoce.  
¿Hubo alguna señal precursora antes del incidente? Infecciones masivas anteriores.  
¿Se analizó el incidente? Sí.  
¿A que sistemas afectan? ¿Cuál es el alcance? Recursos compartidos, se instala en host y se replica mediante agente DDoS.   
¿Qué gravedad tiene? Muy grave.  
¿Se ha notificado a todos los equipos implicados (responsables, equipo interno, stakeholders? Parece que no.  


### Fase Contención, erradicación y recuperación
¿Se aislaron los equipos implicados? Se desconoce.  
¿Se bloquearon los accesos? Se desconoce.  
¿Se cortaron las conexiones/comunicaciones? Se desconoce.  
¿Se pudo eliminar el malware? Sí.  
¿Se pudo aplicar algún tipo de parche? Sí, horas más tarde.  
¿Se corrigió la vulnearabidad? Sí.   
¿Se pudo restaurar el sistema?  
¿Tenían backups? ¿Se pudieron recuperar los datos? Se desconoce.  
¿Funciona todo con normalidad tras la recuperación? Se desconoce.

### Fase Actividad posterior al incidente
¿Cómo entraron? Medio extraíble  
¿Qué falló? Antivurs.
¿Qué sistemas afectó? Varios hosts.  
¿Fue rápida la respuesta del CSIRT? Se desconoce.
¿El CSIRT estuvo coordinado? Se desconoce.  
¿Se siguieron los procedimientos? Se desconoce.  
¿Los procedimientos fueron adecuados y suficientes?¿Se pueden mejorar? Sí  
¿Funcionaron los controles de seguridad? No  
¿Qué se debe reforzar? Accesos, Permisos y Antivirus.

===============

## Escenario 2: Acceso no autorizado a registros de nómina

- Este escenario se trata de un hospital de mediana magnitud con varios consultorios y servicios médicos externos.
- La organización tiene decenas de sedes y más de 5000 empleados.
- Debido al tamaño de la organización, han adoptado un modelo CSIRT con equipos distribuidos de respuesta ante incidentes. También tienen un equipo de coordinación que controla a los CSIRT y les ayuda a comunicarse entre sí.
- Son las últimas horas de la tarde de un miércoles, el equipo de seguridad física de la organización recibe una llamada de una administradora de nómina que vio salir de su oficina a un desconocido, correr por el pasillo y salir del edificio.
- La administradora se había alejado de su estación de trabajo solo durante unos pocos minutos y la había dejado desbloqueada.
- El programa de nóminas sigue con la sesión abierta y en el menú principal, tal como ella lo había dejado, pero cree que han movido el mouse.
- Se le ha solicitado al equipo de respuesta ante incidentes que reúna evidencia relacionada con el incidente y determine qué medidas se deben tomar.
- Los equipos de seguridad ponen en práctica el modelo de la cadena de eliminación y saben utilizar la base de datos VERIS.
- A modo de nivel de protección adicional, han tercerizado parcialmente el personal a una MSSP para tener monitoreo las 24 horas del día, los 7 días de la semana.

### Fase Preparación
¿Tienen un equipo CSIRT definido con roles definidos y responsabilidades asignadas? Sí  
¿Tienen un canal de comunicación propio? Sí.  
¿Quienes son los contactos clave? Se desconoce.  
¿Se han coordinado con las autoridades? Sí a través del equipo de coordinación.  
¿Qué sistemas de detección usan? Se desconoce.   
¿Tienen un plan de respuesta ante incidentes? Sí.  
¿Están definidos los procedimientos a seguir ante un incidente? Se desconoce.  
¿Existe una guía de actuación? Se desconoce.  
¿Los empleados están concienciados? ¿Se han hecho formaciones? Según lo ocurrido no, pues la administradora se dejó la sesión abierta, y además un extraño pudo acceder al edificio.  
¿Se han realizado simulacros? Se desconoce.  
¿El CSIRT está formado y entrenado? Sí.  


### Fase Detección y análisis
¿Qué alerta/s saltaron en el SIEM? Ninguna. Fue robo de información física.  
¿Cuál es el vector del ataque? Error humano.
¿Se revisaron los logs? Se desconoce.  
¿Hubo alguna señal precursora antes del incidente? Ninguna  
¿Se analizó el incidente? Sí.  
¿A que sistemas afectan? ¿Cuál es el alcance? Software de nóminas.  
¿Qué gravedad tiene? Muy grave, pues se habrían exfiltrado datos personales confidenciales.  
¿Se ha notificado a todos los equipos implicados (responsables, equipo interno, stakeholders? Sí.  


### Fase Contención, erradicación y recuperación
¿Se aislaron los equipos implicados? Se desconoce.  
¿Se bloquearon los accesos? No.  
¿Se cortaron las conexiones/comunicaciones? No.  
¿Se pudo eliminar el malware? No aplica.  
¿Se pudo aplicar algún tipo de parche? No aplica. 
¿Se corrigió la vulnearabidad? No aplica.   
¿Se pudo restaurar el sistema? No aplica.  
¿Tenían backups? ¿Se pudieron recuperar los datos? No aplica.  
¿Funciona todo con normalidad tras la recuperación? Parece que sí.

### Fase Actividad posterior al incidente
¿Cómo entraron? Acceso físico.  
¿Qué falló? Error humano con sesión abierta.
¿Qué sistemas afectó? Nóminas.  
¿Fue rápida la respuesta del CSIRT? Se desconoce.
¿El CSIRT estuvo coordinado? Sí  
¿Se siguieron los procedimientos? Se desconoce.  
¿Los procedimientos fueron adecuados y suficientes?¿Se pueden mejorar?  
¿Funcionaron los controles de seguridad? No.  
¿Qué se debe reforzar? Control de acceso.
