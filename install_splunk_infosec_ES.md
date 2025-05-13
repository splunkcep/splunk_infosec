# Guía de Instalación de Splunk InfoSec

Este documento proporciona una guía completa, paso a paso, para instalar **Splunk InfoSec**, basada en las mejores prácticas y recomendaciones oficiales de Splunk. Su objetivo es ayudar a los analistas de seguridad y arquitectos a implementar una solución InfoSec potente y escalable de manera eficiente.

---

## Tabla de Contenidos

- [Visión General de Splunk InfoSec](#overview-of-splunk-infosec)
   - [Características Clave](#key-features)
   - [Beneficios](#benefits)
   - [Quién Debería Implementar Splunk InfoSec](#who-should-deploy-splunk-infosec)
   - [Sobre el Conjunto de Datos Boss of the SOC (BOTS) Versión 3](#about-boss-of-the-soc-bots-dataset-version-3)
   - [Aplicaciones Prerrequisito](#prerequisite-apps)
- [Requisitos del Sistema y Prerrequisitos](#system-requirements-and-prerequisites)
- [Instalación de la Aplicación Splunk InfoSec y el Conjunto de Datos BOTS v3](#installing-the-splunk-infosec-app--bots-v3-dataset)
- [Fin de la Guía](#end-of-guide)

---

## Visión General de Splunk InfoSec

Splunk InfoSec es una solución de seguridad de vanguardia que aprovecha las capacidades de análisis de datos de Splunk para proporcionar información de seguridad integral y detección de amenazas en tiempo real. Es esencial para las organizaciones que buscan fortalecer su postura de ciberseguridad en el dinámico panorama de amenazas actual.

### Características Clave

- **Monitoreo y Análisis en Tiempo Real**: Monitoreo continuo de flujos de datos para detección y respuesta a amenazas en tiempo real.
- **Detección Avanzada de Amenazas**: Integración con Splunk Machine Learning Toolkit (MLTK) para correlación de amenazas basada en ML y alertas.
- **Investigación de Incidentes y Forense**: Herramientas para investigación detallada y forense.
- **Cumplimiento y Reportes**: Ayuda en el cumplimiento normativo con herramientas de reporte extensas.

### Beneficios

- **Postura de Seguridad Mejorada**: Identificación proactiva de amenazas utilizando análisis avanzados.
- **Operaciones Simplificadas**: Gestión centralizada de operaciones de seguridad.
- **Escalabilidad y Flexibilidad**: Adecuado para organizaciones de todos los tamaños.
- **Detección y Respuesta Rápida a Amenazas**: Minimizar daños mediante acción rápida.
- **Inteligencia Operacional**: Obtener información estratégica y optimizar procesos de seguridad.

---

### Quién Debería Implementar Splunk InfoSec

Splunk InfoSec está diseñado para alinear **personas, procesos y herramientas**, ofreciendo:

- **Eficiencia para Recursos Limitados**: Ideal para equipos de seguridad pequeños.
- **Mejora de Habilidades**: Simplifica tareas complejas a través de interfaces intuitivas.
- **Plataforma de Seguridad Integral**: Centraliza la detección de amenazas, respuesta y reporte.
- **Integración y Personalización**: Se integra perfectamente con la infraestructura existente.
- **Playbooks de Respuesta a Incidentes**: Ayuda en la creación y refinamiento de playbooks de IR.
- **Flujos de Trabajo Automatizados**: Asegura manejo de incidentes repetible y documentado.

---

### Sobre el Conjunto de Datos Boss of the SOC (BOTS) Versión 3

Un conjunto de datos de seguridad de muestra y plataforma CTF para profesionales de seguridad de la información, investigadores, estudiantes y entusiastas.

#### Sobre las Aplicaciones Prerrequisito de BOTS v3

El conjunto de datos requiere las siguientes aplicaciones que se distribuyen y licencian por separado y **deben instalarse antes de usar el conjunto de datos**. Estamos utilizando diferentes versiones de aplicaciones del uso originalmente previsto del conjunto de datos y algunas cosas pueden no funcionar correctamente, pero funcionará bien para propósitos de laboratorio. Más información sobre BOTS v3 se puede encontrar [aquí](https://github.com/splunk/botsv3).

---

### Aplicaciones Prerrequisito

Antes de implementar Splunk InfoSec, instale las siguientes aplicaciones prerrequisito:

| Aplicación | Propósito | Beneficio | Enlace |
|:----|:--------|:--------|:-----|
| **Splunk Common Information Model (CIM)** | Normaliza y categoriza datos | Datos accionables y consistentes a través de fuentes | [Splunkbase](https://splunkbase.splunk.com/app/1621) |
| **Punchcard - Custom Visualization** | Visualización de patrones temporales | Identificar tendencias/anomalías fácilmente | [Splunkbase](https://splunkbase.splunk.com/app/3129) |
| **Force Directed App for Splunk** | Visualización de gráficos de relaciones | Descubrir patrones ocultos en redes | [Splunkbase](https://splunkbase.splunk.com/app/3767) |
| **Splunk App for Lookup File Editing** | Editar archivos de búsqueda | Mejorar precisión y eficiencia en manejo de datos | [Splunkbase](https://splunkbase.splunk.com/app/1724) |
| **Splunk Sankey Diagram - Custom Visualization** | Visualización de flujo e interacción | Comprender movimiento de datos y relaciones | [Splunkbase](https://splunkbase.splunk.com/app/3112) |
| **Splunk Security Essentials (SSE)** | Ejemplos de casos de uso y perspectivas | Acelerar implementación de seguridad | [Splunkbase](https://splunkbase.splunk.com/app/3435) |
| **Alert Manager Add-on** | Mejorar gestión de alertas | Mejorar clasificación de alertas y respuesta a incidentes | [Splunkbase](https://splunkbase.splunk.com/app/3365) |
| **Alert Manager** | Extender marco de alertas | Gestión integral del ciclo de vida de alertas | [Splunkbase](https://splunkbase.splunk.com/app/2665) |

Antes de implementar el conjunto de datos BOTS v3, instale las siguientes aplicaciones prerrequisito:

| Aplicación / Complemento | Propósito | Beneficio | Enlace |
|:----|:--------|:--------|:-----|
| **Amazon GuardDuty Add-on for Splunk** | Proporciona objetos de conocimiento para datos de GuardDuty a través de Amazon CloudWatch Events. | Mejora la detección de amenazas integrando conocimientos de GuardDuty en Splunk. | [Splunkbase](https://splunkbase.splunk.com/app/3790/) |
| **Cisco Endpoint Security Analytics (CESA)** | Analiza y correlaciona el comportamiento de usuarios y endpoints en Splunk Enterprise. | Proporciona mayor visibilidad en comportamientos de endpoints con contexto como usuario, dispositivo y ubicación. | [Splunkbase](https://splunkbase.splunk.com/app/2992/) |
| **Code42 App For Splunk** | Integra Splunk y Code42 para correlación de datos de endpoints y respaldo. | Mejora la protección de datos y perspectivas de recuperación. | [Splunkbase](https://splunkbase.splunk.com/app/3736/) |
| **Code42ForSplunk Technology Add-On** | Proporciona complemento técnico para la aplicación Code42 para Splunk. | Facilita la ingestión e indexación de datos de Code42. | [Splunkbase](https://splunkbase.splunk.com/app/3746/) |
| **DecryptCommands** | Proporciona comandos para rutinas Base32, Base64, XOR, ROTX, RC4 y ROL/ROR. | Útil para descifrar comunicaciones de malware ofuscadas. | [Splunkbase](https://splunkbase.splunk.com/app/2655/) |
| **ES Content Updates** | Ofrece contenido de seguridad preempaquetado para Splunk Enterprise Security. | Mantiene el contenido de seguridad actualizado con los últimos métodos de detección de amenazas. | [Splunkbase](https://splunkbase.splunk.com/app/3449/) |
| **Microsoft Azure Active Directory Reporting Add-on for Splunk** | Recopila datos de Microsoft Azure incluyendo datos de usuario, inicios de sesión y auditorías. | Mejora el monitoreo y reporte de cumplimiento para entornos de Azure. | [Splunkbase](https://splunkbase.splunk.com/app/3757/) |
| **Microsoft Cloud App for Splunk** | Proporciona paneles para datos de Microsoft 365. | Mejora la visibilidad y gestión de servicios de Microsoft 365. | [Splunkbase](https://splunkbase.splunk.com/app/3786/) |
| **Microsoft Office 365 Reporting Add-on for Splunk** | Recopila datos de rastreo de mensajes de Microsoft Office 365. | Mejora la seguridad de correo electrónico y el monitoreo de cumplimiento. | [Splunkbase](https://splunkbase.splunk.com/app/3720/) |
| **Microsoft Sysmon Add-on** | Proporciona entrada de datos y extracciones de campo compatibles con CIM para Microsoft Sysmon. | Mejora el monitoreo de creación de procesos y conexiones de red. | [Splunkbase](https://splunkbase.splunk.com/app/1914/) |
| **OSquery App for Splunk** | Permite la recopilación remota de datos de clientes osquery. | Actúa como un servidor de gestión de osquery para mejorar la visibilidad de endpoints. | [Splunkbase](https://splunkbase.splunk.com/app/3902/) |
| **Splunk Add-on for Cisco ASA** | Mapea eventos de dispositivos Cisco ASA al CIM de Splunk. | Facilita la integración con otras aplicaciones de Splunk para monitoreo de seguridad integral. | [Splunkbase](https://splunkbase.splunk.com/app/1620/) |
| **Splunk Add-on for Microsoft Cloud Services** | Extrae datos de varios servicios en la nube de Microsoft. | Mejora el monitoreo de servicios en la nube y el cumplimiento. | [Splunkbase](https://splunkbase.splunk.com/app/3110/) |
| **Splunk Add-on for Microsoft Office 365** | Recopila registros de actividad de gestión y estado de servicio de Office 365. | Mejora el monitoreo y cumplimiento para entornos de Office 365. | [Splunkbase](https://splunkbase.splunk.com/app/4055/) |
| **Splunk Add-on for Microsoft Windows** | Recopila datos de sistemas Windows y los normaliza al CIM. | Mejora la visibilidad y el monitoreo de entornos Windows. | [Splunkbase](https://splunkbase.splunk.com/app/742/) |
| **Splunk Add-on for Symantec Endpoint Protection** | Recopila registros de actividad del servidor y cliente SEP. | Mejora el monitoreo de seguridad de endpoints y la detección de amenazas. | [Splunkbase](https://splunkbase.splunk.com/app/2772/) |
| **Splunk Add-on for Tenable** | Recopila datos de escaneo de vulnerabilidades de Tenable. | Mejora la gestión de vulnerabilidades y el reporte de cumplimiento. | [Splunkbase](https://splunkbase.splunk.com/app/1710/) |
| **Splunk Add-on for Unix and Linux** | Proporciona información sobre entornos Unix y Linux. | Mejora la visibilidad operacional y el monitoreo de rendimiento. | [Splunkbase](https://splunkbase.splunk.com/app/833/) |
| **Splunk Stream Add-on** | Captura y analiza datos de tráfico de red. | Mejora la visibilidad de la red y el análisis forense. | [Splunkbase](https://splunkbase.splunk.com/app/1809/) |
| **Splunk Add-on for AWS** | Recopila datos de servicios AWS para integración en Splunk. | Mejora el monitoreo de servicios en la nube y el cumplimiento. | [Splunkbase](https://splunkbase.splunk.com/app/1876/) |
| **SA-cim_vladiator** | Valida el cumplimiento del CIM de complementos tecnológicos. | Simplifica el proceso de validación y asegura el cumplimiento del modelo de datos. | [Splunkbase](https://splunkbase.splunk.com/app/2968/) |
| **URL Toolbox** | Proporciona herramientas para manipulación y análisis de URLs. | Mejora el análisis de seguridad con capacidades avanzadas de análisis de URLs. | [Splunkbase](https://splunkbase.splunk.com/app/2734/) |
| **TA-VirusTotalActions** | Proporciona acciones de flujo de trabajo para VirusTotal. | Mejora la inteligencia de amenazas integrando conocimientos de VirusTotal. | [Splunkbase](https://splunkbase.splunk.com/app/3446/) |
| ---- | -------- | -------- | ----- |
| **Splunk Common Information Model** | Normaliza y categoriza datos | --**ya instalado con InfoSec**-- | [Splunkbase](https://splunkbase.splunk.com/app/1621/) |
| **Splunk Security Essentials**  | Ejemplos de casos de uso y perspectivas | --**ya instalado con InfoSec**-- | [Splunkbase](https://splunkbase.splunk.com/app/3435/) |

---

## Requisitos del Sistema y Prerrequisitos

### Compatibilidad del Kernel de Linux

- **General**: La mayoría de las distribuciones modernas de Linux son compatibles.
- **Recomendado**: Siga los [Requisitos del SO de Splunk](https://docs.splunk.com/Documentation/Splunk/latest/Installation/Systemrequirements#Supported_Operating_Systems).
- **Kernel Personalizado**: Puede requerir configuración adicional.

### Requisitos Mínimos de Hardware

| Recurso | Requisitos Mínimos |
|:---------|:----------------------|
| Procesador | CPU de cuatro núcleos (x64) |
| Memoria | 16 GB de RAM |
| Almacenamiento | 500 GB de espacio en disco (SSD recomendado) |
| Red | Red interna de 1 Gbps |

### Dependencias de Software Requeridas

- **Sistema Operativo**: Linux actualizado (Ubuntu, CentOS, RHEL).
- **Java Runtime Environment**: JRE 8 o posterior (para funcionalidades específicas).
- **Splunk Enterprise**: Última versión compatible con Splunk InfoSec.

> **Nota**: Abra los puertos necesarios siguiendo las pautas y mejores prácticas de Splunk.

### Recomendaciones Adicionales

- Escale el hardware para despliegues más grandes.
- Implemente firewall e IDS.
- Mantenga copias de seguridad regulares de los datos de Splunk.

---

## Instalación de la Aplicación Splunk InfoSec y el Conjunto de Datos BOTS v3

### Prerrequisitos

Asegúrese de que Splunk Enterprise esté instalado y en funcionamiento. Verifique el estado de la instalación:

```
su splunkuser
```
```
/opt/splunk/bin/splunk status
```

Si Splunk no está en funcionamiento, inícielo usando:

```
/opt/splunk/bin/splunk start
```

### Instalación Paso a Paso
   - [Instalar vía Splunk Web](#method-1-install-via-splunk-web)
   - [Instalar vía CLI](#method-2-install-via-command-line)
> Salte a este [paso](#4-extract-files) si está utilizando el entorno TD SYNNEX para este laboratorio 

#### **Método 1: Instalar vía Splunk Web**

Aunque es posible instalar las aplicaciones vía Splunk Web, todavía es necesario descomprimir/desempaquetar el conjunto de datos BOTS utilizando la interfaz de línea de comandos.
Aquí están los pasos para instalar las aplicaciones y luego descomprimir el conjunto de datos.

##### 1. **Acceder a Splunkbase:**
   - Visite [Splunkbase](https://splunkbase.splunk.com).
   - Busque "Splunk InfoSec App" y descárguelo junto con todas las aplicaciones prerrequisito.

##### 2. **Subir la Aplicación a Splunk:**
   - Inicie sesión en su interfaz web de Splunk.
   - Navegue a **Apps** > **Manage Apps**.
   - Haga clic en **Install app from file**.
   - Seleccione el paquete de la aplicación descargada y haga clic en **Upload**.

##### 3. **Verificar Instalación:**
   - Asegúrese de que las aplicaciones estén listadas bajo **Apps**.

##### 4. **Instalación de BOTS v3:**
   Descargue el conjunto de datos BOTS v3:
   ```bash
   wget https://botsdataset.s3.amazonaws.com/botsv3/botsv3_data_set.tgz
   ```
##### 5. **Extraer Archivos:**
   Descomprima/desempaquete el archivo descargado en `$SPLUNK_HOME/etc/apps`:
   ```bash
   sudo tar -xvf botsv3_data_set.tgz -C /opt/splunk/etc/apps/
   ```
##### 6. **Asignar Propiedad:**
   Asegúrese de que el usuario correcto tenga la propiedad de los directorios y archivos utilizados por Splunk:
   ```bash
   sudo chown -R splunkuser:splunkuser /opt/splunk
   ```
##### 7. **Iniciar Splunk:**
   ```bash
   /opt/splunk/bin/splunk start
   ```

#### **Método 2: Instalar vía Línea de Comandos**

##### 1. **Detener Splunk:**
   ```bash
   /opt/splunk/bin/splunk stop
   ```

##### 2. **Descargar y Extraer Aplicaciones:**
   Cree un directorio de descargas:
   ```bash
   sudo mkdir /opt/downloads
   ```
   ```bash
   cd /opt/downloads/
   ```
   Clone el repositorio o descargue manualmente:
   ```bash
   git clone https://github.com/artioli/splunk.git
   ```
   ```bash
   cd /opt/downloads/botsv3_&_infosec_apps/
   ```

##### 3. **Descargar Conjunto de Datos BOTS v3:**
   ```bash
   wget https://botsdataset.s3.amazonaws.com/botsv3/botsv3_data_set.tgz
   ```

##### 4. **Extraer Archivos:**
   ```bash
   for file in *.tgz; do
       tar -xf "$file" -C /opt/splunk/etc/apps/
   done
   ```

##### 5. **Asignar Propiedad:**
   ```bash
   sudo chown -R splunkuser:splunkuser /opt/splunk
   ```

##### 6. **Iniciar Splunk:**
   ```bash
   /opt/splunk/bin/splunk start
   ```

#### Uso del conjunto de datos y configuración de InfoSec

##### 1. **Verificar Importación de Datos:**
   Abra Splunk Web y busque el conjunto de datos usando:
     ```
     index=botsv3 earliest=0
     ```
   - Asegúrese de que los datos sean accesibles.
   - > **Nota** que este conjunto de datos no cuenta contra los límites de licencia de Splunk debido a su naturaleza pre-indexada.

##### 2. **Configuración de InfoSec:**

   - Todos los datos utilizados por la aplicación InfoSec deben ser compatibles con el Common Information Model (CIM). 
   - Los siguientes Modelos de Datos deben ser acelerados:
      - Authentication
      - Change
      - Intrusion_Detection
      - Malware
      - Network_Sessions
      - Network_Traffic
      - Endpoint
      - Web

   - Pasos
      - En su despliegue de la plataforma Splunk, en Splunk Web, vaya a **Settings > Data Models**.
      - Seleccione **Edit > Edit Acceleration** para un modelo de datos acelerado que desee editar.
      - Seleccione **Summary Range > All Time** y haga clic en **Save**.
      - > **Nota** Al acelerar modelos de datos a *All Time*, asegúrese de que esto solo se haga en un entorno de laboratorio controlado. En producción, considere el impacto en el rendimiento y almacenamiento.

   - La aceleración puede tardar un tiempo.
   - Después de que la aceleración haya terminado, acceda a la aplicación InfoSec y filtre los eventos utilizando el rango de tiempo "All Time"

   - Consulte la [Documentación de Splunk® InfoSec App](https://docs.splunk.com/Documentation/InfoSec) para instrucciones detalladas.

---

## Fin de la Guía
