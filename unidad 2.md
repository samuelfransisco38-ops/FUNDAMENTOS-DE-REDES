## UNIDAD 2: Clasificación de Redes
### CLASE DIA 22 /09/26

- **Red de Área Personal (PAN):** Conecta dispositivos pertenecientes a un mismo usuario a una distancia muy corta (alcance máximo de unos 10 metros).
    
- **Red de Área Local (LAN):** Conecta equipos dentro de un espacio físico delimitado: una casa, una oficina, un salón de clases o un edificio único. Se caracteriza por ser administrada por una sola organización, ofrecer altas velocidades y mantener un bajo costo debido a su limitado alcance.
    
- **Red Inalámbrica de Área Local (WLAN):** Es una variante de la LAN que emplea el espectro radioeléctrico en lugar de cables para interconectar los dispositivos. El acceso se realiza a través de uno o más puntos de acceso (AP), compartiendo el medio y siendo más sensible a las interferencias.
    
- **Red de Área de Campus (CAN):** Conecta varios edificios de una misma organización ubicados en una zona cercana.
    
- **Red de Área Amplia (WAN):** Conecta redes separadas geográficamente entre distintas ciudades, países o continentes. No suele depender de una sola organización, sino de proveedores de telecomunicaciones, lo que implica mayores costos y latencias en comparación con una LAN.
    

#### Comparación de Alcances (de Menor A Mayor)


1. **PAN:** Una persona / escala personal.
    
2. **WLAN / LAN:** Un espacio físico o edificio.
    
3. **CAN:** Varios edificios de una organización.
    
4. **WAN:** Distintas ciudades, países o continentes.   


ACTIVIDAD 2.1 


|**Tipo de Red**|**Definición**|**3 Características**|**2 Ejemplos**|
|---|---|---|---|
|**PAN**<br><br>  <br>  <br><br>_(Personal Area Network)_|Red de área personal diseñada para conectar dispositivos alrededor de un solo usuario en un espacio muy reducido.|1. Alcance muy corto (típicamente hasta 10 metros).<br><br>  <br>  <br><br>2. Baja velocidad de transferencia comparada con redes más grandes.<br><br>  <br>  <br><br>3. Generalmente usa tecnologías de bajo consumo como Bluetooth o infrarrojos.|1. Conexión de un teléfono celular a unos auriculares inalámbricos.<br><br>  <br>  <br><br>2. Sincronización de un smartwatch con el teléfono móvil.|
|**LAN**<br><br>  <br>  <br><br>_(Local Area Network)_|Red de área local que interconecta equipos en un espacio geográfico limitado, como una casa, oficina o escuela, mediante cables físicos.|1. Altas velocidades de transmisión de datos.<br><br>  <br>  <br><br>2. Propiedad y administración privada.<br><br>  <br>  <br><br>3. Baja tasa de errores y alta seguridad por su aislamiento físico.|1. Red de computadoras en una oficina conectadas por cable Ethernet a una impresora compartida.<br><br>  <br>  <br><br>2. Red interna de un laboratorio de informática escolar.|
|**WLAN**<br><br>  <br>  <br><br>_(Wireless Local Area Network)_|Variante de la LAN que cumple la misma función pero utiliza ondas de radio (Wi-Fi) en lugar de cables para la comunicación.|1. Proporciona movilidad y flexibilidad dentro del área de cobertura.<br><br>  <br>  <br><br>2. Su alcance está limitado por la potencia del punto de acceso (Router).<br><br>  <br>  <br><br>3. Requiere protocolos de seguridad estrictos (como WPA3) debido a la exposición del medio inalámbrico.|1. Red Wi-Fi doméstica que conecta laptops, smartphones y consolas.<br><br>  <br>  <br><br>2. Red inalámbrica abierta en una cafetería o aeropuerto.|
|**CAN**<br><br>  <br>  <br><br>_(Campus Area Network)_|Red de área de campus que interconectan múltiples redes LAN dentro de un área geográfica delimitada y de una sola entidad.|1. Tamaño y alcance intermedio entre una LAN y una WAN.<br><br>  <br>  <br><br>2. Generalmente interconecta varios edificios cercanos mediante fibra óptica.<br><br>  <br>  <br><br>3. Controlada por una sola organización o institución.|1. La red que conecta las distintas facultades y la biblioteca dentro de un campus universitario.<br><br>  <br>  <br><br>2. Red de un gran complejo industrial o corporativo con varios edificios.|
|**WAN**<br><br>  <br>  <br><br>_(Wide Area Network)_|Red de área amplia que cubre grandes distancias geográficas, conectando ciudades, países o continentes enteros.|1. Cobertura geográfica masiva (nacional o global).<br><br>  <br>  <br><br>2. Utiliza infraestructura de múltiples proveedores de servicios de internet (ISPs) y enlaces satelitales o submarinos.<br><br>  <br>  <br><br>3. Velocidades y latencias variables según la congestión y la distancia.|1. Internet (la red de redes a nivel mundial).<br><br>  <br>  <br><br>2. La red privada virtual (VPN) que conecta las oficinas centrales de una multinacional en diferentes continentes.|


### CLASE DIA 29 /09/26 

Actividad 2.2
# Estándares de Red Inalámbrica IEEE 802.11

---

## 1. IEEE 802.11a (Wi-Fi 2)
> [!info] 
> **Año:** 1999  
> **Frecuencia:** 5 GHz  
> **Velocidad máxima:** 54 Mbps  

- **Definición:** Estándar de red inalámbrica diseñado para entornos empresariales que introdujo la modulación **OFDM** (*Orthogonal Frequency Division Multiplexing*) para lograr mayor transferencia de datos.
- **Característica principal:** Operó por primera vez en la banda de **5 GHz**, lo que ofrecía menor interferencia que la saturada banda de 2.4 GHz, aunque con menor alcance y menor capacidad para atravesar obstáculos físicos.

---

## 2. IEEE 802.11b (Wi-Fi 1)
> [!info] 
> **Año:** 1999  
> **Frecuencia:** 2.4 GHz  
> **Velocidad máxima:** 11 Mbps  

- **Definición:** El primer estándar de red inalámbrica de consumo masivo y bajo costo que popularizó el uso del Wi-Fi en hogares y oficinas.
- **Característica principal:** Utiliza modulación **DSSS/HR-DSSS** (*Direct-Sequence Spread Spectrum*) en la banda libre de **2.4 GHz**, ofreciendo mayor alcance a costa de velocidades reducidas.

---

## 3. IEEE 802.11g (Wi-Fi 3)
> [!info] 
> **Año:** 2003  
> **Frecuencia:** 2.4 GHz  
> **Velocidad máxima:** 54 Mbps  

- **Definición:** Estándar que combinó la alta velocidad de transferencia de 802.11a con la banda de frecuencia y alcance de 802.11b.
- **Característica principal:** Mantuvo la **retrocompatibilidad completa con 802.11b** al tiempo que adoptó la tecnología **OFDM** en la banda de 2.4 GHz.

---

## 4. IEEE 802.11n (Wi-Fi 4)
> [!info] 
> **Año:** 2009  
> **Frecuencia:** Doble banda (2.4 GHz y 5 GHz)  
> **Velocidad máxima:** Hasta 600 Mbps  

- **Definición:** Estándar que revolucionó el desempeño de las redes inalámbricas mediante la transmisión simultánea a través de múltiples antenas.
- **Característica principal:** Incorporó la tecnología **MIMO** (*Multiple-Input Multiple-Output*) y la unión de canales (*Channel Bonding* a 40 MHz), permitiendo procesar múltiples flujos espaciales en paralelo.

---

## 5. IEEE 802.11ac (Wi-Fi 5)
> [!info] 
> **Año:** 2013 (Wave 1) / 2016 (Wave 2)  
> **Frecuencia:** 5 GHz  
> **Velocidad máxima:** Hasta 6.9 Gbps  

- **Definición:** Estándar enfocado exclusivamente en la banda de 5 GHz, optimizado para aplicaciones de alto ancho de banda como streaming 4K y transferencia rápida de datos.
- **Característica principal:** Introdujo **MU-MIMO** (*Multi-User MIMO*), modulación **256-QAM** y canales extendidos (80 MHz y hasta 160 MHz).

---

## 6. IEEE 802.11ax (Wi-Fi 6 / Wi-Fi 6E)
> [!info] 
> **Año:** 2019 (Wi-Fi 6) / 2020 (Wi-Fi 6E)  
> **Frecuencia:** 2.4 GHz, 5 GHz y 6 GHz (Wi-Fi 6E)  
> **Velocidad máxima:** Hasta 9.6 Gbps  

- **Definición:** Estándar enfocado en maximizar la eficiencia y rendimiento de la red en entornos de alta densidad de clientes conectados simultáneamente.
- **Característica principal:** Incorpora **OFDMA** (*Orthogonal Frequency-Division Multiple Access*), modulación **1024-QAM** y la extensión a la banda de **6 GHz** (Wi-Fi 6E) para reducir la latencia al mínimo.

---

## Tabla Resumen Comparativa

| Estándar     | Nombre Comercial |     Año     | Frecuencia(s)   | Velocidad Máx. Teórica | Tecnología Clave                      |
| :----------- | :--------------- | :---------: | :-------------- | :--------------------: | :------------------------------------ |
| **802.11a**  | —                |    1999     | 5 GHz           |        54 Mbps         | Uso de OFDM en 5 GHz                  |
| **802.11b**  | Wi-Fi 1          |    1999     | 2.4 GHz         |        11 Mbps         | Modulación DSSS / Masificación        |
| **802.11g**  | Wi-Fi 3          |    2003     | 2.4 GHz         |        54 Mbps         | OFDM en 2.4 GHz + Retrocompatibilidad |
| **802.11n**  | Wi-Fi 4          |    2009     | 2.4 GHz / 5 GHz |        600 Mbps        | MIMO + Canales de 40 MHz              |
| **802.11ac** | Wi-Fi 5          |    2013     | 5 GHz           |       ~6.9 Gbps        | MU-MIMO + Canales de 80/160 MHz       |
| **802.11ax** | Wi-Fi 6 / 6E     | 2019 / 2020 | 2.4 / 5 / 6 GHz |       ~9.6 Gbps        | OFDMA + Rendimiento en alta densidad  |


#### ¿Que es el internet ?

ninguna empresa ni gobierno administra internet como un todo; cada red que la compone es administrada de forma independiente y se conecta a las demas por acuerdo mutuo.

#### ¿Que la hace funcionar?
TCP/IP(Protocolo)

#### ¿Como se conectan las redes entre si?

A travez de provedores de servicios de internet (ISP), Organizados en niveles : los ISP locales se conectan a otros mas grandes, y estos entre si , hasta formar la red global

Puntos de intercambio (XP) Sitios fisicos donde distintos ISP conectan su trafico directamente entre si, en lugar de enviarlo por una ruta mas larga . Reducen latencia y costo de trafico

### PREGUNTA DE EXAMEN : los ixp sirven para crear rutas mas cortas para el trafico de internet