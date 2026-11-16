# 🏥 Infraestructura de Red - Hospital Castellar

Diseño, segmentación y simulación completa de la infraestructura informática y de comunicaciones para el **Hospital Castellar**[cite: 3, 5].

**Autores:**
* Alejandro Salguero Marín[cite: 3]
* Aaron Leonel Márquez Arteta[cite: 3]
* **Ciclo:** CFGM Sistemas Microinformáticos y Redes (SMX2B)[cite: 3]

---

## 📋 Descripción del Proyecto
El objetivo del proyecto es proporcionar al hospital una red moderna, segura y escalable mediante segmentación por VLANs, políticas de control de acceso (ACL), servicios centralizados (DHCP, DNS, Web, Backup) y conectividad Wi-Fi diferenciada para personal interno e invitados[cite: 5, 6].

---

## 🌐 Plan de Direccionamiento IP y VLANs

| ID VLAN | Nombre | Departamento / Uso | Subred | Gateway | Rango de Hosts |
| :---: | :--- | :--- | :--- | :--- | :--- |
| **10** | Administración | Gestión interna[cite: 11] | `10.10.10.0/24`[cite: 12] | `10.10.10.1`[cite: 12] | `10.10.10.2 - 254`[cite: 12] |
| **20** | Médicos | Terminales médicos[cite: 11] | `10.10.20.0/24`[cite: 12] | `10.10.20.1`[cite: 12] | `10.10.20.2 - 254`[cite: 12] |
| **30** | Enfermería | Estaciones de control[cite: 11] | `10.10.30.0/24`[cite: 12] | `10.10.30.1`[cite: 12] | `10.10.30.2 - 254`[cite: 12] |
| **40** | Recepción | Atención al público[cite: 11] | `10.10.40.0/24`[cite: 12] | `10.10.40.1`[cite: 12] | `10.10.40.2 - 254`[cite: 12] |
| **50** | Equipos médicos | Aparatología conectada[cite: 11] | `10.10.50.0/24`[cite: 12] | `10.10.50.1`[cite: 12] | `10.10.50.2 - 254`[cite: 12] |
| **60** | Invitados | Wi-Fi visitantes (Solo Internet)[cite: 7, 11] | `10.10.60.0/24`[cite: 12] | `10.10.60.1`[cite: 12] | `10.10.60.2 - 254`[cite: 12] |
| **70** | Servidores | Servicios centralizados[cite: 11] | `10.10.70.0/24`[cite: 12] | `10.10.70.1`[cite: 12] | `10.10.70.2 - 254`[cite: 12] |

---

## ⚙️ Servicios y Seguridad Implementados
* **Segmentación y Enrutamiento:** Switches L2/L3, enlaces Trunk y Router con soporte Inter-VLAN[cite: 14].
* **Seguridad (ACL):** Listas de control de acceso para aislar la red de invitados (VLAN 60) y restringir el acceso a Servidores y Equipos Médicos[cite: 6, 13, 15].
* **Servicios Centralizados (VLAN 70):**
  * **DHCP:** Asignación dinámica de parámetros de red por subred[cite: 6].
  * **DNS:** Resolución de nombres interna[cite: 6].
  * **Web:** Interfaz web básica para consulta y monitorización del estado de la red[cite: 6, 16].
  * **Backup:** Copias de seguridad de servidores y configuraciones[cite: 6].

---

## 🛠️ Herramientas Utilizadas
* **Simulación de Red:** Cisco Packet Tracer[cite: 14, 16]
* **Diagramas y Diseño:** Draw.io / Figma[cite: 16]
* **Desarrollo Web:** HTML / CSS[cite: 6, 16]
