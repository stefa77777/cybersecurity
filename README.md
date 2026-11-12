# Auditoría Interna de Ciberseguridad: Botium Toys

**Autor:** Stefania Redondo  
**Marco de Referencia:** NIST Cybersecurity Framework (CSF)  
**Estándares Evaluados:** PCI DSS, GDPR, SOC 1 / SOC 2  
**Fecha:** Noviembre de 2026  

---

## 1. Resumen Ejecutivo

Esta auditoría de seguridad interna evalúa la postura de seguridad de **Botium Toys**, una empresa estadounidense dedicada al desarrollo y venta de juguetes con una creciente operación de comercio electrónico en Estados Unidos y la Unión Europea (UE). Actualmente, la organización presenta una **puntuación de riesgo de 8/10 (alta)** debido a la gestión inadecuada de activos, la ausencia de controles formales y el riesgo de incumplimiento frente a normativas internacionales de protección de datos y seguridad de pagos.

El objetivo de este informe es documentar los hallazgos de la auditoría, establecer prioridades de mitigación basadas en el riesgo y proporcionar una hoja de ruta alineada con el marco **NIST CSF** para fortalecer la infraestructura y justificar la ampliación del equipo de seguridad.

---

## 2. Alcance y Objetivos de la Auditoría

### Alcance
La evaluación cubre el programa integral de seguridad de la información de Botium Toys:
* **Permisos de usuario actuales** en sistemas críticos: Contabilidad, Detección de Endpoints (EDR), Firewalls, Sistemas de Detección de Intrusiones (IDS) y gestión de SIEM.
* **Controles implementados y procedimientos operativos** asociados a la infraestructura tecnológica.
* **Cumplimiento normativo** aplicable a transacciones en línea y operaciones internacionales.
* **Inventario tecnológico**, incluyendo hardware físico, sistemas heredados (*legacy*) y accesos lógicos.

### Objetivos
* Alinear la postura de seguridad con las mejores prácticas de la industria mediante el **NIST CSF**.
* Implementar el principio de **privilegios mínimos** (*Least Privilege*) en la gestión de credenciales y accesos.
* Establecer políticas, procedimientos y *playbooks* de respuesta y continuidad.
* Fortificar los controles técnicos, administrativos y físicos para reducir la superficie de ataque.

---

## 3. Inventario de Activos y Evaluación de Riesgos

### Activos Gestionados por TI
* **Equipos locales:** Infraestructura física en la oficina principal y centro de datos.
* **Equipos de empleados:** Dispositivos de usuario final (escritorios, laptops, smartphones), estaciones remotas, periféricos y cámaras de vigilancia.
* **Sistemas, software y servicios:** Contabilidad, telecomunicaciones, bases de datos, seguridad, comercio electrónico (*e-commerce*) y gestión de inventarios.
* **Red y conectividad:** Acceso a Internet, red interna, alojamiento de centro de datos y gestión de acceso de proveedores.
* **Seguridad física y sistemas heredados:** Lectores de tarjetas de acceso (*badge readers*) y sistemas *legacy* que requieren monitoreo humano continuo.

### Hallazgos de Riesgo (Puntuación: 8/10 - Alta)
* **Gestión inadecuada de activos:** Falta de visibilidad completa sobre el impacto operativo ante la pérdida de activos críticos.
* **Deficiencia en controles de acceso:** Ausencia de restricciones basadas en roles y privilegios mínimos, exponiendo datos financieros y personales (PII/SPII).
* **Exposición regulatoria:** Alta probabilidad de sanciones por falta de adherencia a normativas de privacidad de clientes y procesamiento de pagos.

---

## 4. Evaluación de los Controles (Controls Assessment)

### 4.1. Controles Administrativos

| Control | Tipo y Propósito | ¿Implementar? | Prioridad |
| :--- | :--- | :---: | :--- |
| **Least Privilege** | Preventivo; restringe el acceso de empleados y proveedores únicamente a los activos/datos necesarios para su función. | **X** | **Alta** |
| **Disaster Recovery Plans** | Correctivo; garantiza la continuidad del negocio y la restauración de sistemas, red y datos tras un incidente. | **X** | **Alta** |
| **Password Policies** | Preventivo; establece reglas de complejidad de contraseñas para mitigar ataques de fuerza bruta o diccionario. | **X** | **Alta** |
| **Access Control Policies** | Preventivo; protege la confidencialidad e integridad de los datos mediante reglas formales de autorización. | **X** | **Alta** |
| **Account Management Policies** | Preventivo; reduce la superficie de ataque y el riesgo asociado a ex-empleados o cuentas inactivas. | **X** | **Alta** |
| **Separation of Duties** | Preventivo; divide tareas críticas para evitar abusos de privilegios o fraude interno. | **X** | **Media** |

### 4.2. Controles Técnicos

| Control | Tipo y Propósito | ¿Implementar? | Prioridad |
| :--- | :--- | :---: | :--- |
| **Firewall** | Preventivo; filtra tráfico malicioso hacia la red interna *(Ya implementado en la infraestructura actual)*. | — | **NA** |
| **Intrusion Detection System (IDS)** | Detectivo; permite identificar tráfico anómalo y posibles intrusiones de forma temprana. | **X** | **Alta** |
| **Encryption** | Disuasivo/Preventivo; protege datos confidenciales y transacciones de pago en tránsito y en reposo. | **X** | **Alta** |
| **Backups** | Correctivo; respalda la recuperación operativa alineada al plan de recuperación ante desastres. | **X** | **Alta** |
| **Password Management System** | Correctivo; automatiza el restablecimiento seguro, recuperación y notificaciones de bloqueo de cuentas. | **X** | **Alta** |
| **Antivirus (AV) Software** | Correctivo; detecta y pone en cuarentena amenazas conocidas en los equipos de usuario y servidores. | **X** | **Alta** |
| **Manual Monitoring & Maintenance** | Preventivo/Correctivo; necesario para mitigar vulnerabilidades en sistemas heredados (*legacy*). | **X** | **Media** |

### 4.3. Controles Físicos

| Control | Tipo y Propósito | ¿Implementar? | Prioridad |
| :--- | :--- | :---: | :--- |
| **Time-Controlled Safe** | Disuasivo; reduce el impacto y exposición frente a amenazas físicas sobre activos críticos. | **X** | **Baja** |
| **Adequate Lighting** | Disuasivo; elimina puntos ciegos en el perímetro físico para disuadir intrusiones. | **X** | **Baja** |
| **CCTV Surveillance** | Preventivo/Detectivo; monitoreo e investigación de eventos *(Ya listado dentro del inventario de activos)*. | — | **NA** |
| **Locking Cabinets (Network Gear)** | Preventivo; protege la integridad física de switches, routers y equipos de red frente a accesos no autorizados. | **X** | **Media** |
| **Alarm Service Signage** | Disuasivo; reduce la probabilidad de intentos de intrusión física mediante señalización visible. | **X** | **Baja** |
| **Physical Locks** | Preventivo; asegura puertas de acceso a áreas restringidas y activos físicos/digitales. | **X** | **Media** |
| **Fire Detection & Prevention** | Detectivo/Preventivo; sistemas de alarma y rociadores para proteger servidores e inventario contra incendios. | **X** | **Media** |

---

## 5. Lista de Verificación de Cumplimiento Normativo

| Normativa / Estándar | ¿Aplica? | Justificación de Aplicabilidad |
| :--- | :---: | :--- |
| **GDPR / RGPD** *(General Data Protection Regulation)* | **[X]** | **Obligatorio:** Botium Toys vende productos en línea y recopila datos personales de ciudadanos de la Unión Europea. Debe garantizar la privacidad de los datos y notificar cualquier brecha de seguridad en un plazo máximo de **72 horas**. |
| **PCI DSS** *(Payment Card Industry Data Security Standard)* | **[X]** | **Obligatorio:** La empresa acepta pagos en línea y procesa/transmite datos de tarjetas de crédito y débito, por lo que debe mantener un entorno cifrado y seguro para proteger los datos financieros. |
| **SOC 1 y SOC 2** *(System and Organization Controls)* | **[X]** | **Aplicable:** Necesario para formalizar políticas de control de acceso, garantizar la integridad de los registros contables y asegurar la confidencialidad, disponibilidad y seguridad de los datos frente a fraudes internos. |
| **FERC-NERC** | **[ ]** | **No aplica:** Regulación exclusiva para proveedores de energía eléctrica e infraestructura crítica de la red eléctrica norteamericana. |
| **HIPAA** | **[ ]** | **No aplica:** Ley aplicable únicamente a entidades del sector salud que gestionan información médica protegida (PHI). |

---

## 6. Recomendaciones de Mitigación y Próximos Pasos

1. **Fase 1 — Remediación Inmediata (0 a 30 días):**
   * Implementar **cifrado** extremo a extremo en la pasarela de pagos y bases de datos de clientes.
   * Aplicar **privilegios mínimos**, políticas de contraseñas robustas y gestión centralizada de cuentas.
   * Desplegar **copias de seguridad automatizadas** y software **antivirus** en todos los endpoints.
2. **Fase 2 — Fortalecimiento y Monitoreo (30 a 90 días):**
   * Configurar alertas activas en el **IDS** y correlacionar eventos en el **SIEM**.
   * Formalizar el **Plan de Recuperación ante Desastres (DRP)** y aplicar segregación de funciones en contabilidad y sistemas críticos.
3. **Fase 3 — Cumplimiento y Seguridad Física (90+ días):**
   * Asegurar gabinetes de red, cerraduras y sistemas contra incendios en la sede física.
   * Realizar auditorías periódicas de cumplimiento **PCI DSS** y **GDPR**.
