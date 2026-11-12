# Lista de Verificación de Cumplimiento Normativo — Botium Toys

**Documento:** `docs/compliance-checklist.md`  
**Criterios de evaluación:** Ubicación geográfica de clientes, métodos de pago y gobierno interno de datos.  

---

## Resumen de Aplicabilidad

| Normativa / Estándar | Estado | Obligatoriedad | Ámbito Principal |
| :--- | :---: | :--- | :--- |
| **GDPR** *(General Data Protection Regulation)* | **[X]** | **Obligatorio** | Privacidad de datos de ciudadanos de la Unión Europea. |
| **PCI DSS** *(Payment Card Industry Data Security Standard)* | **[X]** | **Obligatorio** | Protección de datos de tarjetas de crédito/débito en pagos en línea. |
| **SOC 1 / SOC 2** *(System and Organization Controls)* | **[X]** | **Aplicable / Recomendado** | Controles internos de acceso, integridad financiera y seguridad operativa. |
| **FERC-NERC** | **[ ]** | **No aplica** | Infraestructura crítica del sector eléctrico en Norteamérica. |
| **HIPAA** | **[ ]** | **No aplica** | Protección de información médica en el sector salud de EE. UU. |

---

## Detalle y Justificación por Normativa

### 1. General Data Protection Regulation (GDPR / RGPD) — `[X] Aplica`
* **Descripción:** Reglamento general de la Unión Europea que regula el tratamiento de datos personales de los ciudadanos de la UE dentro y fuera del territorio europeo, exigiendo notificación de brechas de seguridad en un plazo máximo de **72 horas**.
* **Justificación para Botium Toys:** Aunque Botium Toys tiene su sede física en Estados Unidos, su tienda en línea comercializa productos y recopila datos personales (nombres, direcciones, correos electrónicos, datos de pago) de clientes residentes en la Unión Europea. El cumplimiento del GDPR es obligatorio para operar legalmente en ese mercado y evitar multas administrativas significativas.

### 2. Payment Card Industry Data Security Standard (PCI DSS) — `[X] Aplica`
* **Descripción:** Estándar internacional de seguridad de la información diseñado para garantizar que todas las organizaciones que aceptan, procesan, almacenan o transmiten información de tarjetas de crédito lo hagan en un entorno seguro.
* **Justificación para Botium Toys:** Botium Toys acepta pagos en línea con tarjetas de crédito y débito a través de su plataforma de comercio electrónico. Debe cumplir con PCI DSS implementando cifrado fuerte, control de acceso estricto y monitoreo de red para proteger los datos de los titulares de tarjetas y conservar la autorización para procesar pagos electrónicos.

### 3. System and Organization Controls (SOC Type 1 & SOC Type 2) — `[X] Aplica`
* **Descripción:** Informes de auditoría enfocados en los controles internos de una organización sobre el acceso de usuarios, la integridad de los reportes financieros (SOC 1) y los principios de confianza: seguridad, disponibilidad, integridad del procesamiento, confidencialidad y privacidad (SOC 2).
* **Justificación para Botium Toys:** La auditoría reveló deficiencias en el control de acceso de usuarios y ausencia de segregación de funciones en sistemas de contabilidad y bases de datos. Adoptar los estándares SOC 1 y SOC 2 permite mitigar el riesgo de fraude interno, proteger la disponibilidad de los servicios en línea y demostrar madurez operativa ante socios comerciales.

### 4. FERC-NERC — `[ ] No Aplica`
* **Descripción:** Estándares de confiabilidad y protección de infraestructura crítica (CIP) para entidades que operan en la red eléctrica de América del Norte.
* **Justificación para Botium Toys:** Botium Toys es una empresa minorista y de desarrollo de juguetes; no participa en la generación, transmisión ni distribución de energía eléctrica.

### 5. Health Insurance Portability and Accountability Act (HIPAA) — `[ ] No Aplica`
* **Descripción:** Ley federal estadounidense de 1996 que protege la confidencialidad e integridad de la Información Médica Protegida (PHI) de los pacientes.
* **Justificación para Botium Toys:** La organización no pertenece al sector sanitario, no es aseguradora médica ni procesa registros clínicos o de salud.