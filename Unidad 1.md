# Fundamentos de Redes

### Actividad 1.1

**¿Qué espero aprender de la materia de Fundamentos de Redes?** En esta materia busco comprender a fondo qué es una red informática, los distintos tipos que existen y cómo operan técnicamente. Asimismo, me interesa dominar herramientas de apoyo como Obsidian y GitHub que me sirvan tanto en el transcurso de mi carrera como en mi futuro profesional. También espero identificar las diversas áreas de oportunidad y campos de especialización en los que podré desarrollarme más adelante.

### Actividad 1.2

**Con mis propias palabras: importancia y razón de ser de las redes informáticas** Las redes de computadoras son fundamentales porque facilitan el intercambio de información y la interconexión entre múltiples dispositivos electrónicos. Sin ellas, actividades cotidianas de la actualidad serían sumamente complejas. Hoy en día son indispensables debido a que la tecnología impregna la mayor parte de nuestras actividades, abarcando la comunicación, el trabajo, la educación y el entretenimiento.

# 5 Pilares de una Red Computacional

### Infraestructura Física y Conexión

- **Nodos (Origen y Destino):** Dispositivos encargados de enviar y recibir los datos dentro del ecosistema de la red.
    
- **Enlaces (El Camino Físico):** Medios materiales o inalámbricos que establecen la ruta de conexión entre los diferentes nodos.
    

### Lógica y Reglas de Comunicación

Una red computacional es un sistema complejo de intercambio de información que combina la infraestructura física con reglas lógicas para garantizar una comunicación fluida.

- **Direcciones (Identidad Digital):** Identificadores únicos (como las direcciones IP y MAC) que permiten ubicar con precisión los dispositivos de origen y destino.
    
- **Protocolos (El Lenguaje Común):** Normas estrictas de formato y sintaxis que estandarizan la comunicación entre aparatos.
    
- **Enrutamiento (Gestión de Rutas):** Proceso de toma de decisiones para determinar el trayecto más óptimo y eficiente para los paquetes de datos.
    

### Actividad 1.4

Para que una red pueda transmitir diferentes tipos de datos de forma eficiente, debe cumplir con cuatro características fundamentales:

- **Tolerancia a fallas**
    
- **Escalabilidad**
    
- **Calidad de servicio (QoS):** Conjunto de mecanismos que priorizan qué tráfico atender primero cuando la red carece de capacidad suficiente para procesarlo todo simultáneamente.
    
- **Seguridad:** Protección de la red y de los datos que circulan en ella frente a accesos, alteraciones o interrupciones no autorizadas.
    

_Principales amenazas:_

- Suplantación de MAC/IP
    
- Ataques de intermediario (Man-in-the-Middle)
    
- Denegación de servicio (DoS)
    
- Accesos no autorizados a puntos de acceso inalámbricos
    

### Actividad 1.5

Una **arquitectura de red** agrupa las reglas y decisiones de diseño que estructuran una red para que la comunicación opere correctamente, definiendo el rol de cada componente.

Esto se logra dividiendo el sistema en capas independientes; cada capa resuelve un problema específico sin necesidad de conocer los detalles internos de las demás. El modelo de referencia describe de forma teórica todas las funciones involucradas en una comunicación de red.

#### Modelo OSI (7 capas)

1. Física
    
2. Enlace de datos (Data Link)
    
3. Red (Network)
    
4. Transporte
    
5. Sesión
    
6. Presentación
    
7. Aplicación
    

#### Modelo TCP/IP

1. Aplicación
    
2. Transporte
    
3. Internet
    
4. Acceso a red
    

### Encapsulamiento

Durante el envío, al descender por las capas, cada una añade su propio encabezado al dato original. Al llegar al destino, el proceso se invierte y cada capa retira el encabezado correspondiente hasta entregar el mensaje final.

