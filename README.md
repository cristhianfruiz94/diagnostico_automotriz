# 🔧 Mecánico IA — Asistente de taller para transmisiones automáticas

Prototipo funcional de una **aplicación web en español, pensada para el teléfono**, que acompaña a un mecánico mientras diagnostica y repara transmisiones automáticas. El mecánico describe la falla con palabras de taller ("la caja da un golpe", "no entra reversa"), toma fotos y recibe instrucciones cortas, paso a paso, con advertencias de seguridad y puntos de control con foto.

> **Estado:** prototipo (v0.1). Sirve para validar la idea con mecánicos reales. No es un producto listo para uso comercial.

---

## ¿Qué problema resuelve?

Un mecánico con mucha experiencia práctica muchas veces no tiene a mano el manual de servicio de cada caja, no lee documentación técnica en inglés y no tiene a quién preguntar mientras tiene las manos dentro del carro. Un dato equivocado en una transmisión (un torque, un tipo de ATF, una pieza de otra variante) cuesta dinero, tiempo y a veces seguridad.

Mecánico IA busca ser **un especialista en transmisiones que acompaña al mecánico en el taller**: le pregunta lo justo, le pide la foto correcta, le dice qué hacer ahora y lo detiene cuando algo no cuadra.

## Objetivo del prototipo

Validar tres hipótesis antes de invertir en un producto completo:

1. **Usabilidad:** un mecánico de 50–60 años, con formación tecnológica básica, puede usar la app sin que nadie le explique cómo.
2. **Utilidad:** el flujo *identificar → diagnosticar → guiar → comprobar con foto* le ahorra tiempo o errores en un trabajo real.
3. **Confianza:** las reglas del asistente (no inventar datos, marcar el nivel de confianza, detenerse ante dudas) generan confianza en vez de frustración.

El detalle está en [docs/01-objetivo-y-alcance.md](docs/01-objetivo-y-alcance.md).

## Qué incluye

| Función | Qué ve el mecánico |
|---|---|
| Pantalla de inicio | 7 acciones en botones grandes: diagnosticar, reparar, analizar pieza, identificar caja, ATF, especificación, procedimiento |
| Preguntas una a la vez | Marca, modelo, año, motor y si conoce la caja; luego qué falla y cuándo ocurre |
| Asistente con IA | Respuestas cortas en español, con nivel de confianza 🟢🟡🟠🔴 |
| Fotos guiadas | El asistente dice qué fotografiar, desde dónde, a qué distancia y qué debe verse |
| Análisis de fotos | Identifica cajas, piezas y conectores; separa lo que ve de lo que deduce |
| Procedimiento por pasos | Una tarjeta grande por paso ("PASO 3 DE 12"), con torque destacado |
| Fotos de control | En pasos críticos no deja avanzar sin foto; responde ✅ *Parece correcto* o ⚠️ *DETENTE* |
| Botones de ayuda | 👉 ¿Qué hago ahora? · ❓ No entiendo · ⚠️ No coincide |
| Progreso | Estado del trabajo siempre visible (ficha del vehículo y etapas) |
| Memoria del trabajo | Se guarda en la cuenta del usuario; "¿Dónde íbamos?" retoma el trabajo |
| Lectura en voz alta | Lee la última respuesta |

## Cómo probarlo

### Opción A — Con IA (recomendada)
La app usa las capacidades de las páginas publicadas en Claude (preguntar a Claude, enviar fotos, guardar datos). Por eso **la IA solo funciona cuando la app se abre desde claude.ai** como artefacto publicado:

1. Abre el artefacto publicado desde tu cuenta de Claude (pide el enlace al dueño del proyecto).
2. La primera vez, acepta el permiso para que la página use Claude y envíe fotos.
3. Elige **🔍 Diagnosticar una falla** y sigue las preguntas.

Cada persona usa su propia cuenta de Claude; el uso se descuenta de esa cuenta.

### Opción B — Solo la interfaz
Abre `index.html` en cualquier navegador (o publícalo con GitHub Pages). Puedes recorrer las pantallas y las preguntas, pero aparecerá el aviso **"Asistente sin conexión"**: fuera de Claude la página no tiene acceso a la IA ni al guardado en la nube (sí guarda el trabajo en el navegador).

## Estructura del repositorio

```
├── index.html                      La app completa (HTML, CSS y JavaScript en un solo archivo)
├── docs/
│   ├── 01-objetivo-y-alcance.md    Objetivo, usuarios, alcance, qué queda fuera y criterios de éxito
│   ├── 02-especificacion-agente.md Qué debe hacer el asistente y cuándo se activa
│   ├── 03-especificacion-ux.md     Especificación de frontend y experiencia de usuario (secciones 35–66)
│   ├── 04-arquitectura.md          Cómo está construido, flujo de datos y modelo de datos
│   ├── 05-reglas-del-asistente.md  Instrucciones que recibe la IA y formato de sus respuestas
│   ├── 06-limitaciones-y-roadmap.md Limitaciones conocidas y siguientes pasos
│   └── 07-guia-de-pruebas.md       Cómo probar el prototipo con mecánicos
├── agente/
│   ├── README.md                   Qué es la skill y cómo se relaciona con la app
│   └── skill/mecanico-transmisiones/
│       ├── SKILL.md                Comportamiento completo del especialista (skill de Claude)
│       └── references/             Protocolos: fotos e identificación, investigación, seguridad
└── CHANGELOG.md
```

## Principios del producto

- **PRECISIÓN > VELOCIDAD**
- **EVIDENCIA > SUPOSICIONES**
- **SEGURIDAD > COMPLETAR LA RESPUESTA**
- **CLARIDAD > TECNICISMO**
- **VERIFICACIÓN > CONFIANZA EXCESIVA**
- **Todo en español**, aunque la documentación técnica de origen esté en otro idioma.
- **Menos es más:** la inteligencia va detrás de la interfaz; el mecánico solo necesita saber dónde está, qué hacer ahora y qué hacer si algo no coincide.

## ⚠️ Aviso importante

Este prototipo **no reemplaza el manual de servicio del fabricante** ni el criterio de un técnico calificado. En esta versión el asistente **no consulta manuales ni internet**, así que no entrega torques, capacidades, tipos de ATF ni números de pieza: los marca como 🔴 *No confirmado* y explica dónde confirmarlos. Solo los da como confirmados si el mecánico envía una foto del manual o de la etiqueta donde se lee el dato. Ver [limitaciones](docs/06-limitaciones-y-roadmap.md).

## Licencia

Aún no se ha definido una licencia. Mientras no exista un archivo `LICENSE`, todos los derechos quedan reservados por el autor.

---

Autor: Cristhian Ruiz · Prototipo construido con Claude.
