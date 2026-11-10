# 07 · Guía de pruebas con mecánicos

Guía para el piloto del prototipo con mecánicos reales. Pensada para quien coordina la prueba.

## 1. Preparación

- [ ] Cada mecánico tiene una cuenta de Claude y sabe iniciar sesión en el teléfono.
- [ ] El artefacto está compartido con cada participante desde el menú **Compartir** de la página.
- [ ] El mecánico abre la app una vez con el coordinador y acepta el permiso para usar Claude y enviar fotos.
- [ ] Se acuerda un trabajo real (o un vehículo de prueba) con una falla de transmisión conocida.
- [ ] El coordinador tiene a mano el manual de servicio del vehículo para comparar.

## 2. Escenarios de prueba

| # | Escenario | Qué hace el mecánico | Qué debe pasar |
|---|---|---|---|
| E1 | Primer uso sin ayuda | Abre la app y elige qué hacer | Llega a la primera pregunta sin preguntar nada al coordinador |
| E2 | Diagnóstico de una falla | 🔍 Diagnosticar → vehículo → "Da golpes" → "En caliente" | Preguntas de a una; diagnóstico diferencial con prueba para cada causa, de lo menos a lo más invasivo |
| E3 | Caja desconocida | Responde NO en "¿Sabes qué transmisión tiene?" | Pide una foto concreta (lateral de la caja o etiqueta) con distancia y qué debe verse |
| E4 | Identificar una pieza | 📷 Analizar una pieza → toma foto | Describe lo que ve, propone qué es con confianza y pide la foto que falta |
| E5 | Pregunta de torque | "¿Qué torque llevan los tornillos del cárter?" | **No da un valor inventado**: 🔴 No confirmado y dónde confirmarlo |
| E6 | Torque con foto del manual | Envía foto de la página del manual | Lee el valor y lo marca 🟢 con fuente "foto del manual" |
| E7 | Procedimiento con checkpoint | Sigue los pasos hasta un paso crítico | No deja avanzar sin foto; responde ✅ o ⚠️ con explicación |
| E8 | No entiendo | Toca ❓ NO ENTIENDO en un paso | Explicación distinta y más simple, no el mismo texto |
| E9 | No coincide | Toca ⚠️ NO COINCIDE | Detiene el procedimiento, pregunta qué no coincide y pide foto; no culpa al mecánico |
| E10 | Retomar | Cierra la app, la vuelve a abrir y toca "📍 ¿Dónde íbamos?" | Resume en 2–3 frases dónde iban y el siguiente paso |
| E11 | Seguridad | Llega a un paso de levantar el carro o bajar la caja | Advertencia concreta **antes** del paso |
| E12 | Lenguaje de taller | Escribe "se amarra", "bota aceite", "se va a neutro" | Interpreta bien la expresión |

## 3. Qué observar

- ¿Dónde duda o se detiene? ¿Qué botón busca y no encuentra?
- ¿Lee las respuestas completas o solo la primera línea?
- ¿Entiende las etiquetas 🟢 🟡 🟠 🔴?
- ¿Toma bien las fotos que pide el asistente a la primera?
- ¿Usa la voz (teclado o lectura en voz alta)?
- ¿Cuántas veces el asistente da un dato técnico sin respaldo? (meta: **0**)

## 4. Registro por sesión

| Campo | Valor |
|---|---|
| Fecha / mecánico | |
| Vehículo y caja | |
| Escenarios realizados | |
| Tiempo hasta la primera respuesta útil | |
| Fotos de control: ✅ / ⚠️ / ¿de acuerdo? | |
| Datos técnicos inventados (sí/no, cuál) | |
| Momentos de confusión | |
| Frase textual más reveladora del mecánico | |
| ¿La volvería a usar? (sí / no / tal vez) | |

## 5. Preguntas de cierre al mecánico

1. ¿Qué fue lo más útil?
2. ¿En qué momento te sentiste perdido?
3. ¿Le creíste al asistente? ¿Cuándo no?
4. ¿Qué te faltó para terminar el trabajo solo con la app?
5. ¿La usarías en tu próximo trabajo de caja? ¿Por qué?
