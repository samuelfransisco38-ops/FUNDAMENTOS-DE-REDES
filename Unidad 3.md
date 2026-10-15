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