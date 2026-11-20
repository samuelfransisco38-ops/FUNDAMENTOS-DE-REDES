
### Capa 3

**IPV4:**
es el protocolo de la capa de red que direcciona y enruta los paquetes entre las redes, usando direcciones de 32 bits.
Se definio en 1981 dentro de la familia TCP/IP, desanada por Vint Cerf y Bob Kahn
En 1983 ARPANET adopto TCP/IP, el origen de lo que hoy es el internet

**Diferencias entre ip publica y privada:**

| **Característica**    | **IP Pública**                                                                                        | **IP privada**                                                                                                                                                                 |
| --------------------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Definición**        | Identificador único asignado a un dispositivo conectado directamente a internet.                      | Identificador asignado a dispositivos dentro de una red local (LAN).                                                                                                           |
| **Visibilidad**       | Global y accesible desde cualquier punto de internet.                                                 | Local; solo es visible dentro de la misma red privada (hogar, oficina).                                                                                                        |
| **Enrutamiento**      | Enrutable directamente a través de la red pública de internet (ISP).                                  | No enrutable en internet; el tráfico externo requiere NAT (_Network Address Translation_).                                                                                     |
| **Asignación**        | Proveedores de Servicios de Internet (ISP) a los routers, o administradores para servidores públicos. | Routers locales mediante DHCP de forma automática, o configurada de forma estática.                                                                                            |
| **Rangos Reservados** | Cualquiera que no esté reservado para uso privado (ej. IPv4 públicas).                                | - **Clase A:** `10.0.0.0` – `10.255.255.255`<br><br>  <br><br>- **Clase B:** `172.16.0.0` – `172.31.255.255`<br><br>  <br><br>- **Clase C:** `192.168.0.0` – `192.168.255.255` |
| **Duplicidad**        | Debe ser **única** a nivel mundial.                                                                   | Puede repetirse en diferentes redes locales independientes (ej. tu casa y un café pueden usar la misma `192.168.1.50` sin conflicto).                                          |

Características de IPv4
 Es sin conexión (cada paquete viaja por separado), de mejor esfuerzo (no garantiza la entrega) e independiente del medio (funciona sobre cobre, fibra o Wi-Fi).
IPv6
 IPv6 usa direcciones de 128 bits y se creó porque las direcciones IPv4 se agotaron; permite un número prácticamente ilimitado de dispositivos.
 Ventajas de IPv6
Ofrece un espacio de direcciones enorme, un encabezado simplificado de 40 bytes, autoconfiguración de direcciones y no usa broadcast: lo reemplaza el multicast División de la red en grupos
Una red grande se divide en subredes: grupos de dispositivos organizados por ubicación, función o departamento, cada uno con su propio rango de direcciones.

Por que dividir una red 

al dividir se reduce el trafico de broadcast, mejora el rndimiento , se aplican politicas de seguridad por grupo y se facilita  la administracion.

**Red y host**:

Toda direccion tiene dos partes: la parte de red, igual para todos los equipos del grupo, y la parte de host, identifica a cada equipo

La direccion sola no dice donde termina una y empieza la otra.

**Direcciones publicas:**

Las direcciones publicas son unicas en todo Internet y las asigna el **proveedor de servicio** (ISP).

Un equipo con direccion publica es alcanzable desde internet; las privadas no

**Direcciones privadas:**
Se usan solo dentro de una red y no se enrutan en Internet: 10.0.0.0/8, 172.16.0.0/12 y 192.168.0.0/16. para salir a Internet usan **NAT**

Direcciones especiales 

127.0.0.1 es el loopback (el propio equipo) y 169.254.0.0/16 es la asignación automatica (APIPA)ncuando falla el DHCP.

Direcciones IPv4
una dirección IPv4 tiene 32 bits escritos en 4 octetos decimales separados por puntos, como 192.169.1.10;
una parte identifica la red y la otra el host.

### DHCP
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

El cliente renueva a la mitad del tiempo; en Windows,ipconfig/release libera la dirección e ipconfig/renew pide otra ,