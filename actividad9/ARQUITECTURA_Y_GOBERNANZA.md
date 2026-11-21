# Arquitectura y gobernanza — Actividad 9

## Arquitectura actual (hipotética)
Cámara → API + inferencia en VM cloud única → base de datos/logs → controlador de barrera. Riesgos: dependencia de internet, punto único de falla, escalamiento vertical y costo por inferencia.

## Arquitectura objetivo (propuesta)
Cámara → Edge AI + caché local firmada de permisos → controlador físico con interlocks de seguridad. Sincronización de eventos mínimos mediante cola cifrada → API y almacenamiento cloud con escalado horizontal, observabilidad y FinOps.

La clasificación por visión computacional **no es por sí sola una autorización de apertura**. Se exige una política de permisos, umbral conservador, registro de decisiones y alternativa de revisión humana. Definir procedimientos de emergencia y fallo seguro con personal responsable.

## Gobernanza
- Riesgos: falsos positivos/negativos, spoofing, corte de internet, exposición de placas, sesgo por iluminación y sobrecostos.
- Controles: cifrado, RBAC, retención mínima, auditoría, validación estratificada, revisión humana, rollback y presupuestos.
- Marcos: NIST AI RMF y referencia de gestión ISO/IEC 42001:2023 (sin afirmar certificación).
- Legal: análisis de obligaciones mexicanas de datos personales, aviso de privacidad, tratamiento de imágenes/placas y revisión jurídica antes de producción.

## SLA de referencia, no verificados
Disponibilidad local ≥ 99.9% mensual; latencia p95 ≤ 500 ms; tasa de falsos positivos ≤ 0.5%; diferencia TPR entre condiciones ≤ 5 puntos porcentuales. Requieren validación experimental.
