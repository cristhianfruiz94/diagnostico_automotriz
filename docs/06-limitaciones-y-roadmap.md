# 06 · Limitaciones conocidas y siguientes pasos

## 1. Limitaciones del prototipo

| # | Limitación | Impacto para el mecánico | Por qué ocurre |
|---|---|---|---|
| 1 | **No consulta manuales, internet, catálogos ni TSB** | No recibe torques, capacidades, tipos de ATF ni números de pieza; todos salen 🔴 *No confirmado* | Desde la página publicada Claude no puede navegar. Se decidió no dar valores en vez de arriesgar datos inventados |
| 2 | **Voz parcial** | Para hablar usa el micrófono del teclado del teléfono, no un botón propio | La página no tiene permiso para usar el micrófono directamente |
| 3 | **Las fotos no quedan guardadas** | Al retomar un trabajo no se ven las fotos anteriores, solo lo que el asistente concluyó | El prototipo no guarda archivos |
| 4 | **IA solo dentro de claude.ai** | Fuera de Claude (GitHub Pages, archivo local) solo funciona la interfaz | La IA llega por las capacidades de los artefactos de Claude |
| 5 | **Cada mecánico necesita su cuenta de Claude** | Debe iniciar sesión y aceptar el permiso la primera vez; el uso se descuenta de su cuenta | Las consultas se hacen con la cuenta de quien usa la página |
| 6 | **Análisis de fotos sin garantía** | Una foto oscura o parcial puede llevar a una conclusión equivocada | Las fotos son evidencia, no certeza; el asistente debe pedir otra si duda |
| 7 | **Sin lectura de escáner** | Los DTC se escriben a mano | No hay conexión con OBD-II |
| 8 | **Un solo usuario por trabajo** | No se comparte un trabajo entre mecánicos del mismo taller | Los trabajos se guardan en el espacio privado de cada usuario |
| 9 | **Requiere internet** | En talleres con mala señal la app no responde | No hay modo sin conexión |

## 2. Riesgos a vigilar en el piloto

- **Confianza excesiva:** que el mecánico tome una 🟡 *Probable* como si fuera 🟢 *Confirmado*. Observar si las etiquetas se entienden.
- **Frustración por "No confirmado":** si casi todas las especificaciones salen sin valor, el mecánico puede abandonar la app. Es la señal más fuerte para priorizar la fase 2.
- **Fotos de control demasiado permisivas o demasiado estrictas.** Registrar cada ✅ y ⚠️ y preguntar al mecánico si estaba de acuerdo.
- **Seguridad:** confirmar que las advertencias aparecen antes de levantar el vehículo, bajar la caja o trabajar con ATF caliente.

## 3. Hoja de ruta sugerida

### Fase 1 — Piloto con el prototipo actual (2–4 semanas)
- Probar con 5 mecánicos en trabajos reales (ver [07-guia-de-pruebas.md](07-guia-de-pruebas.md)).
- Medir los criterios de éxito de [01-objetivo-y-alcance.md](01-objetivo-y-alcance.md).
- Ajustar las reglas del asistente y los textos con lo aprendido.

### Fase 2 — Especificaciones verificadas
- Backend propio que consulte fuentes técnicas autorizadas (manuales de servicio con licencia, catálogos de piezas, TSB) siguiendo la jerarquía de fuentes de la skill.
- Validación cruzada y cita de la fuente junto a cada dato crítico.
- Pantalla de resultado de investigación completa (sección 57 de la especificación UX).

### Fase 3 — Taller conectado
- Guardar fotos dentro del trabajo (antes / después de cada paso).
- Botón de micrófono propio y respuesta por voz más natural.
- Lectura de DTC desde un escáner OBD-II por Bluetooth.
- Trabajos compartidos entre mecánicos del mismo taller y resumen para el cliente.

### Fase 4 — Producto
- App instalable (PWA) con modo sin conexión parcial.
- Cuentas de taller, historial por vehículo (VIN) y métricas de uso.
- Ampliar a otros sistemas: CVT y doble embrague en profundidad, luego motor y frenos.

## 4. Decisiones abiertas

- Modelo de negocio: suscripción por taller, por mecánico o por consulta.
- Fuentes técnicas: licenciamiento de manuales OEM frente a bases de datos de terceros.
- Licencia del código de este repositorio.
