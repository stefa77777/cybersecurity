# Evaluación de Riesgos e Inventario de Activos — Botium Toys

**Documento:** `docs/risk-assessment.md`  
**Función NIST CSF:** Identify (ID.AM - Gestión de Activos / ID.RA - Evaluación de Riesgos)  
**Puntuación Global de Riesgo:** 8 / 10 (Alto)  

---

## 1. Inventario de Activos en Alcance

El departamento de TI administra los siguientes grupos de activos críticos dentro de la sede física y el entorno digital:

| Categoría de Activo | Descripción Detallada | Criticidad |
| :--- | :--- | :---: |
| **Infraestructura Local (*On-Premises*)** | Equipos y servidores ubicados en la sede física para operaciones internas del negocio. | Alta |
| **Dispositivos de Usuario Final** | Computadoras de escritorio, laptops, teléfonos inteligentes, estaciones de trabajo remotas, periféricos (teclados, ratones, *docking stations*, auriculares) y cámaras de vigilancia. | Media / Alta |
| **Sistemas, Software y Servicios** | Plataformas de contabilidad, telecomunicaciones, bases de datos, herramientas de seguridad, tienda de comercio electrónico (*e-commerce*) y gestión de inventario. | Crítica |
| **Conectividad y Red** | Acceso a Internet corporativo, red interna (LAN/Wi-Fi) y servicios de alojamiento en centros de datos (*data center hosting*). | Crítica |
| **Gestión de Terceros y Datos** | Gestión de acceso de proveedores (*vendors*) y sistemas de retención y almacenamiento de datos de clientes y empleados. | Alta |
| **Seguridad Física y Sistemas *Legacy*** | Lectores de credenciales (*badge readers*) y sistemas heredados (*end-of-life*) sin soporte del fabricante que requieren monitoreo humano manual. | Alta |

---

## 2. Matriz de Riesgos Identificados

| ID | Riesgo Identificado | Activos Afectados | Probabilidad | Impacto | Nivel de Riesgo | Mitigación Recomendada |
| :--- | :--- | :--- | :---: | :---: | :---: | :--- |
| **R-01** | **Gestión inadecuada del inventario de activos:** Desconocimiento del impacto operativo exacto ante la pérdida o compromiso de equipos y sistemas. | Todo el inventario de TI | Alta | Medio / Alto | **Alto** | Implementar inventario centralizado bajo la función *Identify* del NIST CSF. |
| **R-02** | **Ausencia de privilegios mínimos:** Empleados y proveedores cuentan con acceso excesivo a sistemas contables, bases de datos y herramientas de seguridad. | Contabilidad, Bases de datos, SIEM, E-commerce | Alta | Alto | **Crítico** | Aplicar políticas de *Least Privilege*, control de acceso basado en roles (RBAC) y segregación de funciones. |
| **R-03** | **Falta de cifrado y controles en pagos en línea:** Exposición de datos de tarjetas de crédito y datos personales (PII) durante transacciones web. | Plataforma E-commerce, Bases de datos | Alta | Alto | **Crítico** | Habilitar cifrado TLS en tránsito y cifrado en reposo conforme a **PCI DSS** y **GDPR**. |
| **R-04** | **Inexistencia de Plan de Recuperación ante Desastres (DRP):** Falta de respaldos probados y procedimientos de continuidad ante fallos o ataques. | Servidores, E-commerce, Inventario | Media / Alta | Alto | **Alto** | Diseñar un DRP formal y automatizar copias de seguridad periódicas. |
| **R-05** | **Exposición por sistemas heredados (*Legacy*):** Sistemas fuera de ciclo de vida (*end-of-life*) vulnerables a exploits conocidos. | Sistemas *legacy* internos | Alta | Medio | **Alto** | Segmentar red, mantener monitoreo manual estricto y planificar migración. |
| **R-06** | **Incumplimiento normativo internacional:** Sanciones financieras y legales por operar en la UE y procesar tarjetas sin controles certificados. | Operaciones globales y legales | Alta | Alto | **Crítico** | Ejecutar lista de verificación de cumplimiento (**GDPR**, **PCI DSS**, **SOC 1/2**). |

---

## 3. Conclusión del Análisis de Riesgos

* **Probabilidad General:** **Alta** — Botium Toys carece actualmente de políticas formales de control de acceso, cifrado estandarizado y monitoreo automatizado de intrusiones.
* **Impacto Potencial:** **Medio / Alto** — La pérdida de disponibilidad de la tienda en línea o una brecha de datos de clientes afectaría directamente los ingresos, la reputación de la marca y expondría a la empresa a multas regulatorias severas.