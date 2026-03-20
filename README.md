Proyecto de Red LAN – Edificio de Ingeniería Química y Petrolera.

Objetivo. 
Diseñar e implementar una red de área local (LAN) estructurada para un edificio académico, orientada a proporcionar conectividad, segmentación y servicios de red para las aulas, oficinas administrativas y zonas especiales de la carrera de Ingeniería Química y Petrolera. 
Infraestructura. 
El edificio está dividido en dos alas cada un distribuidas de la siguiente manera:
•	Aulas teóricas: Q201, Q202
•	Laboratorios: P101, P102, Lab
•	Área administrativa: Admin
•	Sala de sistemas: SalaMst

Cada sala cuenta con 8 equipos de computo y un switch de acceso por cada PC, excepto el Lab y SalaMst que tienem un solo Switch para 8 PC’s, cableado estructurado Categoría 6 y estaciones de trabajo conectadas en topología estrella.
La sala de sistemas aloja un router principal.

Topología elegida y justificación
Se adopta una topología jerárquica de tres capas:
•	Capa de Acceso: switches en cada sala para conectar dispositivos finales.
•	Capa de Distribución: enlaces troncales entre los switches de acceso y el núcleo.
•	Capa de Núcleo: switch principal y router en la sala de sistemas.

Justificación:
La topología jerárquica permite escalabilidad, segmentación por VLAN, facilidad de mantenimiento y control del tráfico. Además, soporta crecimiento futuro y redundancia.
Topología lógica
•	Router-on-a-Stick con subinterfaces para inter-VLAN.
•	VLANs definidas para:
1.	Estudiantes (aulas teóricas)
2.	Laboratorios
3.	Administración
•	Voz (VoIP)
•	Servidores
•	Enrutamiento estático y soporte de RIP para pruebas.
•	DHCP con pools independientes por VLAN.
•	NAT para acceso a Internet.

Servicios de red implementados
•	DHCP: asignación automática de direcciones IP.
•	DNS: resolución interna y reenvío externo.
•	HTTP/FTP: acceso a recursos web y transferencia de archivos.
•	VoIP: comunicación interna mediante teléfonos IP.
•	Segmentación por VLANs para separar tráfico de usuarios, administración y servidores.

Seguridad y escalabilidad. 
Se plantea el uso de listas de control de acceso (ACLs) para restringir el tráfico entre segmentos. El diseño modular permite la expansión de la red y puede incluir redundancia mediante protocolos como STP. 
Tenemos la presencia de dispositivos como PCs, La topología incluye varios switches por aula, interconexiones hacia un núcleo, y servidores esperados en la sala de Sistemas. 

Inventario de dispositivos y funciones por área
Área	PCs	Switches	Servidores	Impresoras	Routers	Función principal
Q202	8	8	0	0	1	Aula teórica
Q201	8	8	0	0	1	Aula teórica
P102	8	8	0	0	1	Laboratorio
P101	8	8	0	0	1	Laboratorio
Lab	8	8	0	0	1	Laboratorio
Admin	8	1	0	0	1	Gestión académica y administrativa
SalaMst	8	1 (núcleo)	0	0	1	Centro de red y servicios
Total	56	42	0	0	7	

CISCO:

<img width="555" height="255" alt="image" src="https://github.com/user-attachments/assets/141e92f9-593b-4d0d-bc30-03ff7edae1c2" />


Presupuesto: 

Ítem	Cantidad	Precio unitario aprox. (USD)	Precio unitario aprox. (MXN)†	Total estimado MXN

Cisco Router 2911 (nuevo)	7	$3,245	~MXN $59,000	~MXN 413,000
Cisco Switch 2960 24TT (nuevo)	42	$1,525	~MXN $28,000	~MXN 1,176,000
Computadora de escritorio básica
	64	~~USD 250–300	~MXN 5,000–6,000	~MXN 320,000–384,000
Cable UTP Cat5e cobre puro	1,000 m	-	~MXN 14 por m	~MXN 14,000



Cronograma:

 <img width="589" height="387" alt="image" src="https://github.com/user-attachments/assets/8a699ae0-e723-42c2-a79a-570314ca7ea8" />

 

