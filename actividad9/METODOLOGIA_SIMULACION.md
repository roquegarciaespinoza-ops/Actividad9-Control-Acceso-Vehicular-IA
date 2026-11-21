# Metodología de simulación y limitaciones

## Escenarios
Piloto: 1 cámara, 120 eventos/día, 2 RPS pico. Condominio: 2 cámaras, 450 eventos/día, 5 RPS. Multisitio: 8 cámaras, 1,800 eventos/día, 18 RPS.

## Costos (USD/mes hipotéticos)
Mes de 30 días, 720 horas. Base = 1.5 × 720 + 0.0007 × eventos/día × 30 + 35 + 0.02 × eventos/día × 30. Objetivo = 0.45 × 720 + 0.0007 × eventos/día × 30 + 18 + 0.003 × eventos/día × 30 + 9 × cámaras. No son precios reales ni cotizaciones.

## Rendimiento modelado, no medido
Para r solicitudes/segundo: latencia base (ms) = 210 + 18r + 1.6r²; latencia objetivo = 105 + 5r + 0.16r². CPU base (%) = min(100, 65 + 1.6r); CPU objetivo = min(95, 30 + 0.9r). Estas funciones ilustran tendencias; no representan p95 real.

## Fairness sintético
200 ejemplos por condición (100 autorizados, 100 no autorizados), semillas 42 a 45. TPR/FPR hipotéticos: día .98/.02; noche .90/.04; lluvia .88/.05; ángulo oblicuo .84/.06. Comparar TPR y FPR por condición y calcular brecha. Son estratos operativos, no grupos demográficos protegidos.

## Evidencia pendiente
Benchmarks reales, cotizaciones, pruebas de fallas, evaluación jurídica, revisión de seguridad física y dataset autorizado. No afirmar que un sistema real cumple SLA.
