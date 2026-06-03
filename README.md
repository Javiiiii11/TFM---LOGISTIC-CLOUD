# 🚛 LogisticCloud — TFM Grupo C1

> Plataforma de gestión logística en la nube con monitorización de seguridad centralizada mediante Wazuh.

---

## 📋 Descripción del proyecto

**LogisticCloud** es una solución empresarial desplegada en entorno virtualizado que integra una infraestructura cloud segura para la gestión de operaciones logísticas. El proyecto implementa un sistema de monitorización y detección de amenazas en tiempo real mediante **Wazuh SIEM**, protegiendo tanto los activos de la empresa como los accesos de los usuarios.

El proyecto ha sido desarrollado como Trabajo de Fin de Máster por el **Grupo C1**, combinando administración de sistemas, ciberseguridad y gestión de infraestructura cloud.

---

## 🏗️ Arquitectura

El entorno se compone de **tres máquinas virtuales** interconectadas:

| Máquina | Rol | Descripción |
|---|---|---|
| `TFM empresa` | Servidor corporativo | Servicios internos de la empresa logística |
| `TFM usuario 2` | Cliente | Estación de trabajo de usuario final |
| `TFM Wazuh 2` | SIEM | Servidor de monitorización y seguridad (Wazuh) |

> ⚠️ Las máquinas virtuales (`.ova`) no están incluidas en este repositorio por su tamaño. Disponibles en el enlace de descarga al final de este README.

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

## 🛠️ Tecnologías utilizadas

- **Wazuh** — SIEM y plataforma de detección de intrusiones
- **Virtualización** — Entorno desplegado mediante máquinas virtuales (.ova)
- **Infraestructura cloud** — Gestión y administración de servicios en la nube
- **Linux / Windows Server** — Sistemas operativos del entorno

---

## 🎬 Vídeo del proyecto

El vídeo de demostración está incluido en la carpeta `Video proyecto/` de este repositorio.

---

## 📥 Descarga de máquinas virtuales

Las máquinas virtuales `.ova` están disponibles externamente debido a su tamaño:

🔗 **[Descargar máquinas virtuales](#)** ← *(sustituye este enlace por tu Drive/Mega)*

Instrucciones de importación:
1. Descarga los tres archivos `.ova`
2. Importa cada uno desde **VirtualBox** → `Archivo > Importar servicio virtualizado`
3. Arranca primero `TFM Wazuh 2`, después `TFM empresa` y por último `TFM usuario 2`

---

## 👥 Equipo — Grupo C1

Trabajo de Fin de Máster desarrollado por el **Grupo C1**.

---

## 📄 Licencia

Este proyecto ha sido desarrollado con fines académicos.
