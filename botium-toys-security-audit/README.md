# 🛡️ Auditoría Interna de Ciberseguridad: Botium Toys

**Autor:** Stefania Redondo  
**Marco de Referencia:** NIST Cybersecurity Framework (NIST CSF)  
**Normativas Evaluadas:** PCI DSS, GDPR, SOC 1 / SOC 2, HIPAA, FERC-NERC  
**Nivel de Riesgo Inicial:** 8 / 10 (Alto)  
**Fecha:** Noviembre de 2026  

## 📁 Estructura del Repositorio

Este repositorio documenta una auditoría interna integral de seguridad de la información realizada para **Botium Toys**, incluyendo tanto el análisis técnico de riesgos y controles como la comunicación ejecutiva dirigida a las partes interesadas.

```text
botium-toys-security-audit/
├── README.md                             # Informe ejecutivo y resumen integral de la auditoría
├── docs/
│   ├── scope-and-objectives.md           # Contexto, alcance y objetivos definidos por la Gerencia de TI
│   ├── risk-assessment.md                # Inventario de activos críticos y matriz de riesgos (R-01 a R-06)
│   ├── compliance-checklist.md           # Análisis detallado de normativas nacionales e internacionales
│   └── stakeholder-memorandum.md         # Memorando ejecutivo con hallazgos y recomendaciones para gerencia
    └── controls-assessment.csv           # Matriz completa de evaluación de controles (Administrativos, Técnicos y Físicos)
```

### Enlaces Rápidos a la Documentación

* 📄 [Alcance y Objetivos de la Auditoría (`docs/scope-and-objectives.md`)](docs/scope-and-objectives.md)
* 📊 [Evaluación de Riesgos e Inventario de Activos (`docs/risk-assessment.md`)](docs/risk-assessment.md)
* ⚖️ [Lista de Verificación de Cumplimiento Normativo (`docs/compliance-checklist.md`)](docs/compliance-checklist.md)
* ✉️ [Memorando para las Partes Interesadas (`docs/stakeholder-memorandum.md`)](docs/stakeholder-memorandum.md)
* 📋 [Matriz de Evaluación de Controles en CSV (`templates/controls-assessment.csv`)](templates/controls-assessment.csv)

---

## 1. Resumen Ejecutivo

**Botium Toys** es una pequeña empresa estadounidense dedicada al desarrollo y venta de juguetes. Aunque cuenta con una única sede física, su plataforma de comercio electrónico ha crecido rápidamente, atrayendo clientes tanto en Estados Unidos como en la Unión Europea (UE).

A solicitud de la Gerencia de TI, se realizó una auditoría interna integral del programa de ciberseguridad para evaluar la postura de seguridad actual, identificar riesgos críticos sobre los activos tecnológicos (`R-01` a `R-06`), definir controles de mitigación priorizados, establecer las obligaciones de cumplimiento normativo y comunicar los resultados de forma clara a las partes interesadas. Los resultados de esta auditoría sirven como base técnica para fortalecer la infraestructura, garantizar la continuidad del negocio y justificar la ampliación del equipo de seguridad.

---

## 2. Alcance y Objetivos de la Auditoría

> *Ver detalle completo en [`docs/scope-and-objectives.md`](docs/scope-and-objectives.md).*

### Alcance (Scope)

La auditoría abarca la totalidad del programa de seguridad de Botium Toys, evaluando todos los activos gestionados por el departamento de TI, así como los procesos y procedimientos internos en los siguientes sistemas:

* Contabilidad y gestión financiera (*Accounting*).
* Detección y respuesta en endpoints (*EDR / Antivirus*).
* Cortafuegos (*Firewalls*) y red interna.
* Sistemas de Detección de Intrusiones (*IDS*).
* Gestión de Información y Eventos de Seguridad (*SIEM*).
* Inventario de hardware, acceso de proveedores y sistemas heredados (*legacy*).

### Objetivos (Goals)

1. **Alineación con NIST CSF:** Estructurar la gestión de seguridad bajo las funciones del marco NIST (especialmente *Identify* y *Protect*).
2. **Control de acceso:** Implementar el principio de privilegios mínimos (*Least Privilege*) en la gestión de credenciales y permisos.
3. **Fortalecimiento de controles:** Mitigar las vulnerabilidades de alto riesgo mediante controles administrativos, técnicos y físicos.
4. **Cumplimiento normativo:** Asegurar la adhesión a leyes y estándares internacionales aplicables al comercio electrónico y la privacidad de datos.
5. **Gobernanza:** Formalizar políticas, procedimientos y planes de recuperación ante desastres.

---

## 3. Inventario de Activos y Evaluación de Riesgos

> *Ver matriz completa de riesgos e inventario detallado en [`docs/risk-assessment.md`](docs/risk-assessment.md).*

### Resumen de Activos Críticos (Función NIST CSF: *Identify*)

* **Infraestructura Local (*On-Premises*):** Equipos y servidores ubicados en la sede física para operaciones internas del negocio *(Criticidad: Alta)*.
* **Dispositivos de Usuario Final:** Computadoras de escritorio, laptops, teléfonos inteligentes, estaciones de trabajo remotas, periféricos y cámaras de vigilancia *(Criticidad: Media / Alta)*.
* **Sistemas, Software y Servicios:** Plataformas de contabilidad, telecomunicaciones, bases de datos, herramientas de seguridad, tienda de comercio electrónico (*e-commerce*) y gestión de inventario *(Criticidad: Crítica)*.
* **Conectividad y Red:** Acceso a Internet corporativo, red interna (LAN/Wi-Fi) y servicios de alojamiento en centros de datos (*data center hosting*) *(Criticidad: Crítica)*.
* **Gestión de Terceros y Datos:** Gestión de acceso de proveedores (*vendors*) y sistemas de retención y almacenamiento de datos de clientes y empleados *(Criticidad: Alta)*.
* **Seguridad Física y Sistemas *Legacy*:** Lectores de credenciales (*badge readers*) y sistemas heredados (*end-of-life*) sin soporte oficial que requieren monitoreo manual *(Criticidad: Alta)*.

### Resumen de Riesgos Identificados (Puntuación Global: 8 / 10 - Alto)

| ID | Riesgo Identificado | Nivel de Riesgo | Mitigación Principal |
| :--- | :--- | :---: | :--- |
| **R-01** | Gestión inadecuada del inventario de activos | **Alto** | Inventario centralizado alineado con *NIST CSF (Identify)*. |
| **R-02** | Ausencia de privilegios mínimos (*Least Privilege*) | **Crítico** | Control de acceso basado en roles (RBAC) y segregación de funciones. |
| **R-03** | Falta de cifrado en pagos en línea y datos personales | **Crítico** | Cifrado TLS en tránsito y en reposo (**PCI DSS** / **GDPR**). |
| **R-04** | Inexistencia de Plan de Recuperación ante Desastres (DRP) | **Alto** | Diseño de DRP formal y automatización de copias de seguridad. |
| **R-05** | Exposición por sistemas heredados (*Legacy / End-of-Life*) | **Alto** | Segmentación de red, monitoreo manual y plan de migración. |
| **R-06** | Incumplimiento normativo internacional | **Crítico** | Implementación de controles **GDPR**, **PCI DSS** y **SOC 1/2**. |

---

## 4. Evaluación de Controles (Controls Assessment)

> *Ver archivo descargable en formato tabla interactiva: [`templates/controls-assessment.csv`](templates/controls-assessment.csv).*

### 4.1 Controles Administrativos

| Control | Tipo y Propósito | Implementar | Prioridad |
| :--- | :--- | :---: | :---: |
| **Principio de privilegios mínimos** (*Least Privilege*) | **Preventivo:** Reduce el riesgo asegurando que proveedores y personal no autorizado solo accedan a los sistemas y datos estrictamente necesarios para su rol. | **X** | **Alta** |
| **Planes de recuperación ante desastres** (*Disaster Recovery Plans*) | **Correctivo:** Garantiza la continuidad del negocio y minimiza el tiempo de inactividad ante incidentes en hardware, red, aplicaciones y datos. | **X** | **Alta** |
| **Políticas de contraseñas** (*Password Policies*) | **Preventivo:** Establece requisitos de complejidad para reducir el compromiso de cuentas mediante fuerza bruta o ataques de diccionario. | **X** | **Alta** |
| **Políticas de control de acceso** (*Access Control Policies*) | **Preventivo:** Protege la confidencialidad e integridad de los datos mediante reglas formales de autorización. | **X** | **Alta** |
| **Políticas de gestión de cuentas** (*Account Management Policies*) | **Preventivo:** Reduce la superficie de ataque y mitiga riesgos asociados a cuentas inactivas o de ex empleados. | **X** | **Alta** |
| **Segregación de funciones** (*Separation of Duties*) | **Preventivo:** Evita que una sola persona concentre privilegios excesivos que permitan fraudes o abusos internos. | **X** | **Media** |

### 4.2 Controles Técnicos

| Control | Tipo y Propósito | Implementar | Prioridad |
| :--- | :--- | :---: | :---: |
| **Firewall** | **Preventivo:** Filtra tráfico malicioso o no deseado hacia la red interna *(ya implementado en la infraestructura actual; requiere revisión de reglas)*. | — | **NA** |
| **Sistema de Detección de Intrusiones (IDS)** | **Detectivo:** Permite al equipo de TI identificar rápidamente tráfico anómalo o intentos de intrusión. | **X** | **Alta** |
| **Cifrado** (*Encryption*) | **Disuasivo / Preventivo:** Protege información confidencial en tránsito y en reposo (ej. transacciones de pago en el sitio web). | **X** | **Alta** |
| **Copias de seguridad** (*Backups*) | **Correctivo:** Respalda la continuidad operativa y permite la restauración de datos tras un incidente, alineado al plan de recuperación. | **X** | **Alta** |
| **Sistema de gestión de contraseñas** (*Password Management System*) | **Correctivo:** Facilita el restablecimiento seguro de credenciales, recuperación y alertas de bloqueo de cuentas. | **X** | **Alta** |
| **Software Antivirus (AV)** | **Correctivo:** Detecta, bloquea y pone en cuarentena amenazas conocidas en estaciones de trabajo y servidores. | **X** | **Alta** |
| **Monitoreo y mantenimiento manual** | **Preventivo / Correctivo:** Necesario para supervisar sistemas heredados (*legacy*) sin soporte oficial y mitigar vulnerabilidades activas. | **X** | **Media** |

### 4.3 Controles Físicos

| Control | Tipo y Propósito | Implementar | Prioridad |
| :--- | :--- | :---: | :---: |
| **Gabinetes con cerradura** (*Locking cabinets*) | **Preventivo:** Impide el acceso o manipulación física no autorizada de equipos de red e infraestructura crítica. | **X** | **Media** |
| **Cerraduras físicas** (*Locks*) | **Preventivo:** Asegura el acceso perimetral e interno a oficinas, salas de servidores e inventario. | **X** | **Media** |
| **Detección y prevención de incendios** | **Detectivo / Preventivo:** Alarmas y rociadores para proteger al personal, servidores e inventario físico contra daños por fuego. | **X** | **Media** |
| **Caja fuerte con control de tiempo** (*Time-controlled safe*) | **Disuasivo:** Reduce el impacto de robos o amenazas físicas sobre activos de alto valor. | **X** | **Baja** |
| **Iluminación adecuada** (*Adequate lighting*) | **Disuasivo:** Elimina puntos ciegos en el perímetro de la sede física para disuadir intrusiones. | **X** | **Baja** |
| **Señalización de servicio de alarma** | **Disuasivo:** Advierte sobre monitoreo activo para reducir la probabilidad de ataques físicos. | **X** | **Baja** |
| **Videovigilancia (CCTV)** | **Preventivo / Detectivo:** Disuade incidentes y aporta evidencia forense *(cámaras ya presentes en el inventario de activos)*. | — | **NA** |

---

## 5. Lista de Verificación de Cumplimiento Normativo

> *Ver justificación detallada en [`docs/compliance-checklist.md`](docs/compliance-checklist.md).*

| Normativa / Estándar | ¿Aplica? | Justificación de Cumplimiento |
| :--- | :---: | :--- |
| **GDPR** *(General Data Protection Regulation)* | **SÍ [X]** | **Aplica:** Botium Toys comercializa productos en línea a consumidores residentes en la Unión Europea y recopila sus datos personales. Debe garantizar la privacidad de los datos, gestionar el consentimiento y notificar brechas de seguridad en un plazo máximo de **72 horas** para evitar multas severas. |
| **PCI DSS** *(Payment Card Industry Data Security Standard)* | **SÍ [X]** | **Aplica:** La empresa acepta pagos en línea y procesa, transmite o almacena datos de tarjetas de crédito/débito en su *e-commerce*. Cumplir con PCI DSS es obligatorio para cifrar transacciones y proteger los datos financieros de los titulares de tarjetas. |
| **SOC 1 / SOC 2** *(System and Organization Controls)* | **SÍ [X]** | **Aplica:** Debido a la ausencia actual de segregación de funciones y políticas de acceso en sistemas contables y bases de datos, adoptar los controles SOC 1 y SOC 2 permite auditar el acceso de usuarios, garantizar la integridad financiera y proteger la confidencialidad y disponibilidad de los datos. |
| **HIPAA** *(Health Insurance Portability and Accountability Act)* | **NO [ ]** | **No aplica:** Botium Toys desarrolla y vende juguetes; no es una entidad de atención médica ni maneja información de salud protegida (PHI). |
| **FERC-NERC** *(Energy Reliability Standards)* | **NO [ ]** | **No aplica:** La organización no opera en el sector energético ni forma parte de la red eléctrica de América del Norte. |

---

## 6. Recomendaciones y Plan de Acción (Hoja de Ruta)

> *Ver memorando ejecutivo dirigido a gerencia en [`docs/stakeholder-memorandum.md`](docs/stakeholder-memorandum.md).*

1. **Fase 1 — Inmediata (0 a 30 días | Prioridad Alta):**
   * Implementar el **principio de privilegios mínimos** (`R-02`) y revocar permisos excesivos en sistemas de contabilidad, bases de datos y herramientas de seguridad.
   * Habilitar **cifrado** extremo a extremo (TLS/HTTPS y cifrado en reposo) (`R-03`) para cumplir con **PCI DSS** y **GDPR** (`R-06`).
   * Desplegar **copias de seguridad automatizadas**, políticas robustas de contraseñas y software antivirus en todos los *endpoints*.

2. **Fase 2 — Corto Plazo (30 a 90 días | Prioridad Alta / Media):**
   * Implementar un **Sistema de Detección de Intrusiones (IDS)** integrado con el SIEM para monitorear anomalías en la red.
   * Redactar y probar el **Plan de Recuperación ante Desastres (DRP)** (`R-04`) y establecer la segregación de funciones.
   * Asegurar físicamente los equipos de red mediante gabinetes con cerradura y verificar los sistemas contra incendios.

3. **Fase 3 — Mediano Plazo (90+ días | Gobernanza Continua):**
   * Planificar la migración o retiro de los sistemas heredados (*legacy*) que actualmente dependen de monitoreo manual (`R-05`).
   * Consolidar el inventario centralizado (`R-01`) y realizar auditorías periódicas alineadas con **NIST CSF** y **SOC 2**, justificando la contratación de personal especializado en seguridad y cumplimiento.
