
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
