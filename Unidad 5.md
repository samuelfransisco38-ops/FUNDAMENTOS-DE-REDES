
### ### DHCP
El cliente obtiene su configuración en cuatro pasos, DORA: Discover, Offer, Request y
Acknowledge. El primer mensaje es un broadcast.
El servidor entrega I, mascara, puerta de enlace y DNS.

Para que sirve DHCP 
DHCP (protocolo de config dinamica de host )
es un servicio que asigna dirreccciones IP automaticamente a los equipos de la red
Evita configurar cada equipo a mano y los confligtos por direcciones duplicadas }
## Proceso DHCP (DORA)

| Mensaje | Acrónimo | Flujo | Destino (L3 / L2) | Función principal |
| :--- | :---: | :--- | :--- | :--- |
| **1. DHCP Discover** | **D** | Cliente $\rightarrow$ Servidor(es) | Broadcast (`255.255.255.255` / `FF:FF:FF:FF:FF:FF`) | El cliente busca servidores DHCP disponibles en la subred al no tener IP configurada (usa origen `0.0.0.0`). |
| **2. DHCP Offer** | **O** | Servidor $\rightarrow$ Cliente | Unicast o Broadcast | El servidor ofrece una configuración de red (IP disponible, máscara, *gateway*, DNS y tiempo de *lease*). |
| **3. DHCP Request** | **R** | Cliente $\rightarrow$ Servidor(es) | Broadcast (`255.255.255.255` / `FF:FF:FF:FF:FF:FF`) | El cliente acepta formalmente una oferta (indicando el servidor elegido con la opción 54) y descarta el resto. |
| **4. DHCP Ack** | **A** | Servidor $\rightarrow$ Cliente | Unicast o Broadcast | El servidor confirma la asignación, registra el *lease* y autoriza al cliente a usar la dirección IP. |

> [!note] Unicast vs. Broadcast en Offer y Ack
> Aunque el cliente aún no tiene la IP asignada durante el **Offer** y el **Ack**, el servidor suele enviarlos por **Unicast** apuntando a la MAC del cliente y a la IP ofrecida. Si el cliente activa el *Broadcast Flag* (porque su pila TCP/IP no acepta unicast sin interfaz configurada), el servidor responde por **Broadcast**.

### Mensajes adicionales del ciclo de vida
- **DHCP NAK:** El servidor rechaza la solicitud (ej. renovación de una IP que ya no corresponde a la subred).
- **DHCP Release:** El cliente libera voluntariamente su IP antes de que expire el *lease*.
- **DHCP Decline:** El cliente avisa al servidor que la IP ofrecida ya está en uso en la red (detectado vía *Gratuitous ARP*).



Tiempo de concesión 

La dirrección  se entrega en préstamo por un tiémpo de concesión (laase), no de forma permanente .

El cliente renueva a la mitad del tiempo; en Windows,ipconfig/release libera la dirección e ipconfig/renew pide otra 



### Actividad 5.1
| Capa       | ¿Qué es?                                                                                                                                           | ¿Para qué sirve?                                                                                                                                        |
| :--------- | :------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Capa 2** | Es donde los dispositivos se hablan por su dirección física (la MAC) dentro de la misma red local. Aquí entran los switches y las tramas (frames). | Para mover datos de un dispositivo a otro dentro de la misma red (como en tu casa u oficina) sin hacerse bolas y detectando si algún dato llegó dañado. |
| **Capa 3** | Es la capa de las direcciones IP y los routers. Aquí los datos ya se llaman paquetes y dejan de estar encerrados en la red local.                  | Para encontrar el mejor camino y mandar los datos de una red a otra hasta que lleguen a su destino final (básicamente, hace que funcione el internet).  |
| **Capa 4** | Es la capa que controla la entrega de los datos de aplicación a aplicación usando puertos (como TCP y UDP).                                        | Para asegurar que los datos lleguen completos y en orden (si usas TCP) o mandarlos rápido sin importar si se pierde algo en el camino (si usas UDP).    |
