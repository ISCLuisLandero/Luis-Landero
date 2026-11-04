# Portafolio de Ciberseguridad & Análisis SOC

¡Hola! Soy un **Ingeniero en Sistemas Computacionales** con más de 12 años de experiencia en soporte técnico y diagnóstico de infraestructura IT, especializado en **Análisis SOC, Respuesta a Incidentes y Seguridad de Redes**.

Poseo la certificación **Google Cybersecurity** y me enfoco en el monitoreo de tráfico, análisis de eventos de seguridad y automatización de tareas con Python.

---

## 🛠️ Habilidades Técnicas

- **Análisis SOC & SIEM:** Monitoreo de eventos, detección de anomalías, investigación de alertas y análisis de registros (Linux `auth.log`, Windows Event Viewer).
- **Análisis de Redes & Tráfico:** Captura y procesamiento de paquetes con **Wireshark** y **tcpdump**, análisis de capas TCP/IP, diagnósticos DHCP y topologías.
- **Threat Intelligence & Phishing:** Extracción de IOCs (IPs, dominios, hashes), análisis de cabeceras de correo y evaluación de campañas maliciosas.
- **Sistemas Operativos & Herramientas:** Kali Linux, Windows Server/Client, Entornos Virtuales (VirtualBox).
- **Programación & Automatización:** Python (Scripting para procesamiento de logs, manipulación de texto e interfaces GUI con Tkinter).

---

## 📂 Proyectos Destacados

### 1. [Análisis de Tráfico de Red & Capturas PCAP](./proyectos/analisis-pcap)
- **Descripción:** Investigación de un flujo de red simulado utilizando **Wireshark** y **tcpdump**.
- **Resultados:** Identificación de handshakes TCP, análisis de peticiones DNS/HTTP y detección de patrones atípicos de tráfico.
- **Herramientas:** Wireshark, tcpdump, Kali Linux.

### 2. [Análisis de Campaña de Phishing e IOCs](./proyectos/analisis-phishing)
- **Descripción:** Inspección detallada de correos electrónicos maliciosos recibidos en un entorno controlado.
- **Resultados:** Extracción y documentación de cabeceras, identificación de IOCs y mitigación propuesta.
- **Herramientas:** MXToolbox, CyberChef, VirusTotal.

### 3. [Automatización con Python para Ciberseguridad](./proyectos/python-scripts)
- **Descripción:** Conjunto de scripts desarrollados para automatizar tareas de análisis y monitoreo.
- **Características:** Filtrado y validación de direcciones IP, parsing de archivos de logs y desarrollo de herramientas visuales en Tkinter.
- **Herramientas:** Python 3, Tkinter, PyInstaller.

---



# SOC/SOAR Automated Response Pipeline for Ransomware (MITRE ATT&CK T1490)

## 📌 Visión General del Proyecto
Este proyecto implementa un flujo automatizado de Detección y Respuesta (SOAR) de extremo a extremo para mitigar y documentar intentos de inhibición de recuperación del sistema (**MITRE ATT&CK T1490**). El laboratorio simula un ataque ejecutado desde un endpoint Windows mediante macros y comandos ofuscados, detectado a través de un SIEM Splunk, y gestionado de forma autónoma por un listener desarrollado en FastAPI que genera informes forenses en PDF.

---

## 🛠️ Arquitectura y Tecnologías del Laboratorio
* **Endpoint / Fuente de Telemetría:** Windows 10 con **Sysmon** (Monitoreo de procesos y EventCode 1).
* **SIEM:** **Splunk Enterprise** (Correlación de eventos, reglas de alerta en tiempo real y webhooks).
* **SOAR / Automatización:** **FastAPI** (Python) ejecutándose en Ubuntu Server.
* **Generación de Evidencia:** Librería Python **ReportLab** para la compilación dinámica de reportes ejecutivos en PDF.

---

## 🔄 Flujo de Trabajo (End-to-End Workflow)
1. **Simulación de Amenaza:** Se ejecuta una macro en Excel que invoca comandos para interactuar con utilidades del sistema (`vssadmin.exe`).
2. **Ingesta de Telemetría:** Sysmon captura la ejecución del proceso y el Universal Forwarder de Splunk ingiere el log en tiempo real.
3. **Detección (SIEM):** Una regla personalizada en Splunk evalúa la telemetría y dispara una alerta crítica basada en la técnica T1490.
4. **Respuesta Automatizada (SOAR):** Splunk envía un Webhook HTTP POST hacia el servidor FastAPI.
5. **Mitigación y Documentación:** El script deserializa la alerta, analiza el payload, ejecuta las rutinas de contención y genera un informe forense formal en formato PDF de manera instantánea.

---

## 🚀 Instalación y Ejecución del Servidor SOAR

1. Clonar el repositorio:
   ```bash
   git clone [https://github.com/tu-usuario/soc-soar-ransomware-lab.git](https://github.com/tu-usuario/soc-soar-ransomware-lab.git)
   cd soc-soar-ransomware-lab




## 📜 Certificaciones

- **Google Cybersecurity Professional Certificate**
- **Soporte de TI y Redes** (12+ años de experiencia práctica)

---

## 📬 Contacto

- **LinkedIn:** https://www.linkedin.com/in/luis-landero-705531a9/
- **Correo:** llandero@outlook.com
- **correo:** iscllandero@gmail.com
