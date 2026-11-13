# Memorando para las Partes Interesadas (Stakeholder Memorandum)

**Para:** Gerente de TI y Partes Interesadas de Botium Toys  
**De:** Stefania Redondo — Analista de Ciberseguridad / Auditora Interna  
**Fecha:** 13 de noviembre de 2026  
**Asunto:** Resultados y recomendaciones de la auditoría interna de seguridad de TI  

---

## 1. Resumen de Alto Nivel del Alcance de la Auditoría

* La auditoría evaluó el programa integral de ciberseguridad de **Botium Toys**, abarcando todos los activos tecnológicos, procesos y procedimientos internos de la organización.
* Se revisaron los permisos de usuario actuales en sistemas críticos, incluyendo contabilidad, detección y respuesta en endpoints (*EDR*), cortafuegos (*firewalls*), sistemas de detección de intrusiones (*IDS*) y herramientas *SIEM*.
* Se analizaron los controles administrativos, técnicos y físicos implementados actualmente en la infraestructura de red y en la sede física.
* Se examinaron los procedimientos y protocolos operativos establecidos para la gestión de sistemas, acceso de proveedores y mantenimiento de equipos heredados (*legacy*).
* Se evaluó la alineación de los procesos actuales con las normativas y estándares de cumplimiento aplicables al comercio electrónico internacional.

---

## 2. Resumen de Alto Nivel de los Objetivos de la Auditoría

* Alinear la postura de seguridad actual de Botium Toys con las mejores prácticas de la industria mediante el **Marco de Ciberseguridad del NIST (NIST CSF)**.
* Implementar el principio de **privilegios mínimos (*Least Privilege*)** para fortalecer la gestión de credenciales y el control de accesos de empleados y proveedores.
* Establecer políticas, procedimientos y libros de jugadas (*playbooks*) estandarizados para garantizar la continuidad del negocio y la respuesta ante incidentes.
* Fortificar los controles internos de los sistemas críticos para reducir la puntuación de riesgo actual de **8 / 10 (Alto)**.
* Garantizar el cumplimiento normativo con estándares internacionales como **PCI DSS**, **GDPR** y **SOC 1 / SOC 2** para proteger los datos de clientes y evitar sanciones regulatorias.

---

## 3. Conclusiones Críticas (Implementación Inmediata — Prioridad Alta)

* **Falta de control de acceso y privilegios mínimos:** Actualmente, empleados y proveedores cuentan con acceso excesivo a sistemas sensibles, por lo que se requiere implementar de inmediato políticas formales de control de acceso, gestión de cuentas, políticas de contraseñas robustas y el principio de privilegios mínimos.
* **Ausencia de cifrado y protección en pagos en línea (PCI DSS y GDPR):** Los datos confidenciales y las transacciones de tarjetas de crédito/débito carecen de cifrado estandarizado, exponiendo a la empresa a brechas de seguridad y multas regulatorias tanto en Estados Unidos como en la Unión Europea.
* **Inexistencia de un Plan de Recuperación ante Desastres (DRP) y copias de seguridad:** Botium Toys no cuenta con respaldos automatizados ni con un plan formal de continuidad del negocio para restaurar sus operaciones de comercio electrónico tras un incidente cibernético o fallo técnico.
* **Falta de monitoreo activo y protección en endpoints:** Es urgente desplegar un Sistema de Detección de Intrusiones (*IDS*) y software antivirus/antimalware en todos los equipos para detectar amenazas y tráfico anómalo de manera oportuna.

---

## 4. Otras Conclusiones (Implementación a Mediano/Largo Plazo — Prioridad Media y Baja)

* **Segregación de funciones y monitoreo de sistemas heredados (*legacy*):** Se debe implementar la separación de funciones en áreas críticas como contabilidad para prevenir fraudes internos, además de formalizar el monitoreo y mantenimiento manual de los sistemas fuera de ciclo de vida (*end-of-life*).
* **Refuerzo de controles físicos en la sede:** Aunque existen cámaras de vigilancia (*CCTV*), se recomienda instalar gabinetes con cerradura para proteger los equipos de red, cerraduras físicas adicionales en áreas restringidas y sistemas de detección y prevención de incendios para resguardar servidores e inventario.
* **Medidas disuasivas complementarias:** A mediano plazo, se sugiere mejorar la iluminación perimetral, colocar señalización visible del proveedor de alarmas e incorporar una caja fuerte con control de tiempo.

---

## 5. Resumen Ejecutivo y Recomendaciones

La auditoría interna determinó que Botium Toys presenta un nivel de riesgo alto (8/10) debido a la gestión deficiente de activos, la falta de controles de acceso y el incumplimiento de normativas internacionales clave. Para cumplir con los objetivos alineados al marco NIST CSF, la empresa debe priorizar de inmediato la implementación de privilegios mínimos, cifrado de datos, copias de seguridad automatizadas y un plan formal de recuperación ante desastres. Asimismo, es indispensable adherirse de forma obligatoria a **PCI DSS** para asegurar los pagos en línea y al **GDPR** para proteger la privacidad de los clientes en la Unión Europea, apoyándose en los controles **SOC 1 y SOC 2** para fortalecer la gobernanza interna. En una segunda fase, se recomienda implementar la segregación de funciones, el monitoreo estructurado de sistemas heredados y las mejoras de seguridad física en la sede. Ejecutar estas recomendaciones reducirá drásticamente la superficie de ataque y garantizará la continuidad operativa del negocio en expansión. Finalmente, estos hallazgos respaldan la necesidad de ampliar el departamento de TI con personal especializado en ciberseguridad para gestionar y mantener estos controles a largo plazo.