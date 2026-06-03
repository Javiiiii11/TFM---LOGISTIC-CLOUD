# 🚛 LogisticCloud — TFM Grupo C1

> Laboratorio de ciberseguridad sobre infraestructura logística empresarial con monitorización SIEM mediante Wazuh, simulación de ataques reales y detección de amenazas.

---

## 🎬 Demo del laboratorio

https://github.com/user-attachments/assets/fc72cc87-9501-4e40-ae83-79814aafea27

---

## 📋 Descripción del proyecto

**LogisticCloud** es un laboratorio de ciberseguridad desplegado en entorno virtualizado que simula una empresa logística real. El proyecto combina **administración de sistemas**, **pentesting** y **monitorización SIEM** con Wazuh para detectar y analizar ataques en tiempo real.

El escenario plantea dos vectores de ataque simultáneos:
- Un **atacante externo** (Kali Linux) que compromete la infraestructura de la empresa
- Un **insider threat** (usuario interno con privilegios) que abusa de su acceso

Todo monitorizado y detectado por **Wazuh** mediante Threat Hunting, MITRE ATT&CK y Vulnerability Detection.

---

## 🏗️ Arquitectura del laboratorio

El entorno se compone de **tres máquinas virtuales** interconectadas:

| Máquina | Rol | Descripción |
|---|---|---|
| `TFM Wazuh 2` | SIEM | Wazuh Manager con dashboard centralizado |
| `TFM empresa` | Servidor corporativo | Web, BD, SSH — objetivo del atacante externo |
| `TFM usuario 2` | Cliente interno | Estación de trabajo con usuarios Pepe y Juan |

> ⚠️ Las `.ova` no están incluidas en este repositorio por su tamaño (~19 GB). Enlace de descarga al final del README.

---

## 🔴 Flujo de ataque — Kali Linux (externo)

```
1. Escaneo de puertos con Nmap
2. Acceso a la web → búsqueda de pistas + diccionario personalizado
3. Acceso a la base de datos con credenciales obtenidas
4. Obtención de credenciales de Elba → acceso por SSH
5. Escalada de privilegios a root
6. Lectura de archivos con credenciales de otro usuario
7. Pivoting a la máquina usuario via SSH con diccionario rockyou
```

## 🟡 Flujo de ataque — Insider Threat (interno)

```
Estructura de usuarios:
├── Pepe  →  usuario despedido que conserva privilegios
└── Juan  →  usuario nuevo sin privilegios (acceso restringido)

1. Acceso inicial como Juan (sin privilegios, todo restringido)
2. Cambio a usuario Pepe usando pistas encontradas en la empresa
3. Acceso a Documentos con notas académicas → modificación de calificaciones
4. Detección completa por monitorización Wazuh
5. EXTRA: explotación de la máquina usuario mediante script malware (Wazuh)
```

---

## 🛡️ Configuración de Wazuh

```
1. Instalación de Wazuh Manager
2. Instalación y configuración de agentes en máquinas empresa y usuario
3. Visibilidad de agentes en el dashboard del manager
4. Testing mediante:
   - Threat Hunting
   - MITRE ATT&CK
   - Vulnerability Detection
```

---

## 🛠️ Herramientas utilizadas

**Ataque externo:**
| Herramienta | Uso |
|---|---|
| Nmap | Escaneo de puertos y reconocimiento |
| Gobuster | Enumeración de directorios web |
| Ferroxbuster | Fuzzing web |
| John the Ripper (office2john) | Cracking de contraseñas |
| msoffcrypto | Descifrado de archivos Office |
| Python | Scripting |
| SSH | Acceso remoto |
| MinIO | Almacenamiento de objetos |

**Movimiento lateral:**
| Herramienta | Uso |
|---|---|
| Nmap | Reconocimiento interno |
| SSH / Reverse Shell | Acceso y persistencia |
| Samba / FTP | Transferencia de archivos |

**Monitorización y defensa:**
| Herramienta | Uso |
|---|---|
| Wazuh | SIEM, detección de intrusiones |
| Suricata | IDS/IPS de red |
| Fim & Yara | Integridad de ficheros y detección de malware |

---

## 📁 Estructura del repositorio

```
TFM---LOGISTIC-CLOUD/
├── Memoria/
│   ├── Memoria del proyecto Grupo C1 LogisticCloud.pdf
│   └── TFM_LogisticCloud_Final_Profesional.docx
├── Presentación/
│   └── Presentación tfm_grupo C1.pptx
├── ¡Tenemos una idea!/
│   ├── ¡Tenemos una idea! Grupo C1.docx
│   └── ¡Tenemos una idea! Grupo C1.pdf
└── Video proyecto/
    ├── TFM - Grupo C1.mp4
    └── Video LogisticCloud_TFM-Grupo C1.txt
```

---


## 👥 Equipo — Grupo C1

Trabajo de Fin de Máster desarrollado por el **Grupo C1**.

> 📌 *Añade aquí los usuarios de GitHub de tus compañeros cuando los tengas*

---

## 📄 Licencia

Este proyecto ha sido desarrollado con fines académicos.
