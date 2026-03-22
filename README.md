# Diseño e Implementación de Red LAN: Edificio de Ingeniería Química y Petrolera

![Estado del Proyecto](https://img.shields.io/badge/Estado-Completado-green?style=for-the-badge)
![Tecnología](https://img.shields.io/badge/Herramienta-Cisco_Packet_Tracer-blue?style=for-the-badge&logo=cisco)
![VLANs](https://img.shields.io/badge/Segmentación-VLANs_&_Inter--VLAN-orange?style=for-the-badge)

Este proyecto detalla el diseño de una red de área local (LAN) estructurada para un entorno académico. El sistema está orientado a proporcionar conectividad robusta, segmentación de tráfico y servicios de red integrados para aulas, laboratorios y oficinas administrativas.

## Infraestructura y Distribución

El edificio se divide en dos alas funcionales distribuidas de la siguiente manera:
* **Aulas teóricas:** Q201, Q202.
* **Laboratorios:** P101, P102, Lab.
* **Área administrativa:** Admin.
* **Sala de sistemas (MDT):** SalaMst.

### Estándares de Conexión
* **Densidad:** Cada sala cuenta con 8 equipos de cómputo.
* **Hardware de Acceso:** Un switch por PC en aulas y laboratorios (excepto Lab y SalaMst que utilizan un switch centralizado para 8 terminales).
* **Medios:** Cableado estructurado Categoría 6 en topología estrella.
* **Core:** El Router principal se aloja en la sala de sistemas.

---

## Arquitectura de Red

### Topología Jerárquica
Se ha implementado un diseño de tres capas para asegurar escalabilidad y redundancia:
1. **Capa de Acceso:** Switches locales para la conexión de dispositivos finales.
2. **Capa de Distribución:** Enlaces troncales para la agregación de tráfico hacia el núcleo.
3. **Capa de Núcleo:** Switch principal y Gateway (Router) central.

### Configuración Lógica
* **Inter-VLAN Routing:** Implementación de Router-on-a-Stick con subinterfaces.
* **VLANs Segmentadas:** Estudiantes, Laboratorios, Administración, Voz (VoIP) y Servidores.
* **Protocolos:** Enrutamiento estático, RIP para entornos de prueba, DHCP por VLAN y NAT para salida a Internet.
* **Seguridad:** Listas de Control de Acceso (ACLs) para restricción de tráfico inter-segmento y Spanning Tree Protocol (STP).

---

## Servicios de Red Implementados
* **DHCP:** Asignación dinámica de direccionamiento IP por pools independientes.
* **DNS:** Resolución de nombres interna y reenvío de consultas externas.
* **HTTP/FTP:** Servidores para acceso a recursos web y transferencia de archivos.
* **VoIP:** Infraestructura de comunicación interna mediante telefonía IP.

---

## Inventario de Dispositivos

| Área | PCs | Switches | Routers | Función Principal |
| :--- | :--- | :--- | :--- | :--- |
| Q201/Q202 | 16 | 16 | 2 | Aula teórica |
| P101/P102 | 16 | 16 | 2 | Laboratorio |
| Lab | 8 | 8 | 1 | Laboratorio |
| Admin | 8 | 1 | 1 | Gestión administrativa |
| SalaMst | 8 | 1 | 1 | Centro de red |
| **Total** | **56** | **42** | **7** | |

---

## Evidencias de Diseño (Cisco Packet Tracer)

![Topología Cisco](https://github.com/user-attachments/assets/141e92f9-593b-4d0d-bc30-03ff7edae1c2)

---

## Análisis de Presupuesto

| Ítem | Cantidad | Precio Unitario (MXN) | Total Estimado (MXN) |
| :--- | :--- | :--- | :--- |
| Cisco Router 2911 | 7 | $59,000 | $413,000 |
| Cisco Switch 2960 24TT | 42 | $28,000 | $1,176,000 |
| Estación de Trabajo | 64 | $6,000 | $384,000 |
| Cable UTP Cat5e (1000m) | 1 | $14,000 | $14,000 |
| **Inversión Total** | | | **$1,987,000** |

---

## Cronograma de Implementación

![Cronograma](https://github.com/user-attachments/assets/8a699ae0-e723-42c2-a79a-570314ca7ea8)

---
**Institución:** Universidad Politécnica de Querétaro (UPQ)  
**Proyecto:** Ingeniería Química y Petrolera - LAN Infrastructure

