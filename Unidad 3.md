### **Capa física**

* **Bit:** Unida mínima de información en redes (0 o 1).
* **Señal:** Representación eléctrica, óptica o electromagnética de los datos.
* **Ancho de banda:** Capacidad máxima teórica de transferencia de datos de un medio en un tiempo dado.
* **Rendimiento (throughput):** Tasa real de datos transferidos con éxito a través del medio.
* **Latencia:** Tiempo que tarda un paquete de datos en viajar de su origen a su destino.
* **Medio de transmisión:** Canal físico o inalámbrico por el que viajan las señales.

### **Cables y medios**

* **Par trenzado (UTP / STP):** Cable de pares de hilos de cobre entrelazados para reducir interferencias; UTP sin blindaje, STP blindado.
* **Conector RJ-45:** Interfaz estándar de 8 pines utilizada para terminar cables de red ethernet.
* **Cable directo y cable cruzado:** El directo conecta dispositivos diferentes (ej. PC a Switch); el cruzado conecta dispositivos iguales (ej. PC a PC).
* **Fibra óptica:** Medio de transmisión que envía impulsos de luz a través de hilos de vidrio o plástico.
* **Fibra monomodo y multimodo:** Monomodo usa un solo haz de luz para largas distancias; multimodo usa múltiples haces para distancias cortas.
* **Interferencia electromagnética (EMI):** Distorsión de la señal causada por campos electromagnéticos externos.
* **Wi-Fi (IEEE 802.11):** Estándar para comunicación de redes locales inalámbricas (WLAN).
* **Bandas de 2.4 GHz y 5 GHz:** Frecuencias de Wi-Fi; 2.4 GHz ofrece mayor alcance y menor velocidad, 5 GHz menor alcance y mayor velocidad.
* **Bluetooth:** Protocolo inalámbrico de corto alcance para redes de área personal (PAN).

### **Señalización**

* **Codificación:** Proceso de convertir datos digitales en un patrón de señales eléctricas u ópticas.
* **Señalización:** Método físico utilizado para representar los valores binarios en el medio de transmisión.
* **Sincronización:** Alineación de reloj entre emisor y receptor para interpretar correctamente el inicio y fin de cada bit.
* **Código Manchester:** Método de codificación donde cada bit tiene una transición de voltaje a mitad del intervalo para mantener la sincronización.

### **Ethernet y LAN**

* **Ethernet (IEEE 802.3):** Estándar dominante para redes de área local (LAN) cableadas.
* **Tarjeta de red (NIC):** Componente de hardware que permite a un dispositivo conectarse a la red.
* **Switch:** Dispositivo de Capa 2 que reenvía tramas exclusivamente al puerto del destinatario usando direcciones MAC.
* **Hub:** Dispositivo de Capa 1 obsoleto que retransmite todas las señales recibidas a todos sus puertos.
* **Tabla de direcciones MAC:** Registro en el switch que asocia direcciones MAC específicas con sus respectivos puertos físicos.
* **Dúplex (half y full):** Half envía y recibe datos por turnos; Full envía y recibe datos simultáneamente.
* **Colisión:** Impacto producido cuando dos dispositivos transmiten datos al mismo tiempo en un medio de medio-dúplex compartido.

### **Direccionamiento**

* **Dirección MAC:** Identificador físico único de 48 bits grabado en el hardware de la NIC.
* **OUI:** Primeros 24 bits de una dirección MAC que identifican al fabricante del dispositivo.
* **Hexadecimal:** Sistema numérico en base 16 ($0$-$9$ y $A$-$F$) usado para representar direcciones MAC de forma compacta.
* **Unicast:** Tráfico enviado de un único emisor a un único destinatario específico.
* **Multicast:** Tráfico enviado de un único emisor a un grupo específico de destinatarios.
* **Broadcast:** Tráfico enviado de un emisor a todos los dispositivos de la red local.

### **Enlace de datos**

* **Trama (frame):** Unidad de datos de protocolo (PDU) de la Capa 2 que empaqueta los paquetes de red con encabezado y tráiler.
* **Encabezado y tráiler:** Controladores añadidos al inicio y final de los datos; contienen direccionamiento MAC e información de control/errores.
* **FCS / CRC:** Secuencia de verificación en el tráiler (FCS) que utiliza un cálculo matemático (CRC) para detectar errores en la trama.
* **Subcapa LLC:** Subcapa superior de Capa 2 que gestiona la comunicación con la Capa 3 e identifica el protocolo de red.
* **Subcapa MAC:** Subcapa inferior de Capa 2 que controla el acceso al medio físico y el direccionamiento del hardware.
* **CSMA/CD:** Protocolo de acceso al medio para redes cableadas half-duplex que detecta colisiones y retransmite.
* **CSMA/CA:** Protocolo de acceso al medio para redes inalámbricas que evita colisiones reservando el canal antes de transmitir.
### Actividad 3.1 
![[Pasted image 20261020195027.png]]

### La capa 
La **Capa física** es el primer nivel del **modelo OSI**, encargado de la transmisión de datos binarios brutos (bits) sobre un canal de comunicación.

Funciones principales

- **Transmisión de bits**: Envía los bits de un nodo al siguiente a través de un medio físico sin interpretar su significado.
- **Codificación de señales**: Convierte los bits en señales eléctricas, ópticas o de radiofrecuencia (por ejemplo, mediante cables de cobre, **fibra óptica** o conexiones inalámbricas).
- **Definición de hardware**: Especifica las características eléctricas, mecánicas y funcionales de los cables, conectores (como el RJ45) y tarjetas de red.
### principios  : componentes 

La capa física se compone de tres elementos: los medios físicos (cables, conectores y dispositivos), * la codificación de los datos y la señalización que los transmite.
### Principios : parametos

su desempeño se mide con tres parametros:el ancho de banda(capacidad maxima ), el rendimiento (lo que realmente se transfiere )y la latencia (el retardo en llegar)

### Actividad 3.2
Básicamente, los puntos de intercambio de internet (IXP) reducen la latencia porque **cortan los intermediarios y acortan drásticamente la distancia física** que tienen que recorrer los paquetes de datos.

Visto desde la perspectiva de redes, el funcionamiento se resume en lo siguiente:

- **Menos saltos de router:** En lugar de que el tráfico entre dos operadores o ISPs tenga que dar una vuelta enorme pasando por múltiples proveedores de tránsito intermediarios (lo que añade un montón de saltos innecesarios en la ruta), en un IXP las redes se conectan directamente cara a cara en un mismo centro de datos.
    
- **Rutas locales directas:** Permiten que el tráfico local se quede local. Si dos usuarios de diferentes proveedores en una misma región quieren comunicarse, sus datos se cruzan directamente en el punto de intercambio de la zona en lugar de ir a dar la vuelta a servidores o nodos en otros países.
    

Menos saltos, rutas optimizadas y menor distancia física se traducen directamente en un tiempo de respuesta (**ping / latencia**) mucho más bajo.

### Tipos de cable : cobre

el cable de par trenzado (UTP) transmite señales electricas con conector RJ-45, alcanza hasta 100 metros y es el mas usado en LAN ; el trenzado reduce la interferencia }

### UTP: ¿por qué los cables van en pares?
Los 8 hilos del UTP forman 4 pares trenzados.
Cada par envía la señal con polaridad opuesta en sus dos hilos; la interferencia afecta a ambos por igual y el receptor la cancela al comparar los dos.
Cada par tiene un trenzado distinto para reducir la diafonía entre pares vecinos.

### Tipos de cable : fibra optica 

la  fibra optica transmite pulsos de luz :llega a mayores distancias y es inmune a la interferencia electromagnetica, pero es mas costosa y delicada de instalar .

### Medios inalámbricos 
transmiten por ondas de radio (wifi,bluetooth,celular);dan movilidad , pero  el medio es compartido, sufre interferencias y requiere medidas de seguridad

### La capa física:
Una señal es una variación de una propiedad física que representa bits: cambios de voltaje en cobre, pulsos de luz en fibra u ondas de radio en el aire.
![[Pasted image 20261020195328.png]]

### La señalizacion  y codificacion fisica 
La codificacion convierte los bits en un patron predefinido que faciita la sincronia y la detección de errores; la señalización define cómo se representa ese patrón en el medio .

### Medios fisicos : conexión de la comunicación 
Un dispositivo se conecta mediante su tarjeta de red(NIC), un puerto ,un conector y el medio; la NIC convierte los bit 
### Ethernet capa 1 y 2 
Ethernet (IEEE 802.3) es el estandar dominante en el LAN y trabaja en dos capas : en la capa 1 define medios y señalización , y en la capa 2 define las tramas y las direcciones MAC.

### ARP : de dirección IP a dirección Mac
 El protocolo ARP permite descubrir la dirección MAC de un dispositivo a partir de su dirección IP .Envia una petición por broadcast ; solo el dueño de esa IP responde por UNICAST y el resultado se guarda en la tabla ARP.
### Envenenamiento ARP (ARP POISONING)
ARP no verifica quién responde : un atacante envia respuestas ARP falsas para que otros equipos aasocien su MAC con la IP de otro dispositivo , por ejemplo la del router, y asi intercepta el trafico (ataque de intermediario)

se mitiga con inspección dinámica de ARP (DAI) en el switch con entradas ARP estaticas en los equipos críticos .