# Revisión de calidad y puertas de control — Actividad 9

## Cobertura de la rúbrica
- 25 pts escalabilidad: reporte §§1–3 y dos diagramas.
- 25 pts FinOps: reporte §4, hoja de costos, fórmulas y SLA propuesto.
- 25 pts auditoría integral: reporte §§5–7, matriz de riesgos y fairness sintético.
- 25 pts escalamiento responsable: reporte §8, fases 0–4 con responsables y criterios de aprobación.

## Hallazgos que deben mantenerse explícitos
1. La arquitectura base no es un despliegue inspeccionado, sino un escenario hipotético.
2. Los ahorros (~69–73 %) dependen de supuestos de tarifas; no incluyen todos los costos de adquisición, operación y amortización de Edge. No son ahorro neto garantizado.
3. La latencia calculada es un modelo analítico, no p95 medido. No permite declarar cumplimiento de SLA.
4. El FPR sintético por condición es 3–5 %, superior al objetivo tentativo de 0.5 %. **No aprobar un despliegue automático con esta evidencia.** Se requiere calibración, evaluación con dataset representativo y revisión humana/fail-safe.
5. La brecha TPR entre día (97 %) y ángulo oblicuo (85 %) es de **12 puntos porcentuales**, superior al umbral propuesto de 5 pp. Es un hallazgo, no un cumplimiento.
6. Los grupos por condiciones de captura no sustituyen una auditoría de equidad sobre personas ni constituyen por sí mismos categorías protegidas.
7. ISO/IEC 42001 y NIST AI RMF se usan como marcos de referencia, no como certificaciones; análisis jurídico sujeto a validación.

## Estado
Documentación y datos simulados: preparados. Pruebas reales, validación legal, aprobación de seguridad física y despliegue: **no realizados**. La calificación de 100 puntos es un objetivo académico, no una nota garantizada.
