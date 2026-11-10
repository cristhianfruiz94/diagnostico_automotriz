# 03 · Especificación de frontend y experiencia de usuario

> Especificación original de la interfaz (secciones 35 a 66). Es la referencia de diseño que sigue `index.html`. Al final de este documento hay una tabla con el estado de cada sección en el prototipo.

---

# 35. FRONTEND Y EXPERIENCIA DE USUARIO

El agente debe estar acompañado por un **frontend web responsive y mobile-first**, diseñado específicamente para utilizarse desde teléfonos inteligentes y tabletas dentro de un taller mecánico.

La aplicación debe poder utilizarse cómodamente desde:

- teléfonos Android;
- iPhone;
- tabletas;
- navegadores web móviles.

La experiencia debe estar optimizada para pantallas pequeñas y para uso con una sola mano cuando sea posible.

El frontend debe funcionar como una **aplicación de asistencia de taller**, no como un chatbot tradicional.

---

# 36. PERFIL DEL USUARIO PARA EL DISEÑO UX

El usuario principal puede ser un mecánico de aproximadamente 50–60 años, con amplia experiencia práctica en vehículos pero con formación tecnológica básica.

Por lo tanto, la interfaz debe:

- ser extremadamente sencilla;
- utilizar lenguaje cotidiano;
- evitar terminología informática;
- utilizar botones grandes;
- utilizar tipografía grande y legible;
- tener alto contraste;
- evitar elementos pequeños;
- minimizar la cantidad de texto simultáneo;
- evitar menús complejos;
- evitar configuraciones innecesarias;
- minimizar el número de pasos para realizar una acción;
- permitir navegación mediante botones claramente visibles;
- utilizar iconos acompañados de texto;
- proporcionar confirmación visual después de acciones importantes.

No diseñes la interfaz para un usuario tecnológico.

Diseñala para un **mecánico que quiere resolver un problema rápidamente mientras trabaja físicamente sobre un vehículo**.

---

# 37. PRINCIPIO DE DISEÑO

La aplicación debe seguir este principio:

> **"El usuario no debería tener que aprender a utilizar la aplicación."**

La interfaz debe ser autoexplicativa.

El usuario debería poder abrirla y entender inmediatamente:

1. qué vehículo está trabajando;
2. qué problema está diagnosticando;
3. qué debe hacer ahora;
4. qué fotografía debe tomar;
5. cuál es el siguiente paso.

---

# 38. PANTALLA PRINCIPAL

La pantalla inicial debe ser muy simple.

Debe mostrar:

## 🔧 MECÁNICO IA

**¿Qué quieres hacer?**

### 🔍 Diagnosticar una falla

### 🔧 Reparar una transmisión

### 📷 Analizar una pieza

### 🔩 Identificar una transmisión

### 🛢️ Consultar ATF

### 📋 Consultar una especificación

### 📖 Seguir un procedimiento

Debe existir un botón visible:

### 📷 TOMAR FOTO

Y otro:

### 🎙️ HABLAR

El usuario debe poder utilizar voz en lugar de escribir.

---

# 39. INTERACCIÓN POR VOZ

El sistema debe estar preparado para interacción por voz cuando la plataforma lo permita.

El usuario puede decir:

> "La caja me está dando un golpe cuando cambia de segunda a tercera."

El sistema debe convertirlo en una consulta estructurada.

También debe permitir que el agente responda mediante texto y, cuando sea posible, lectura en voz alta.

La voz debe utilizar español claro y natural.

No utilizar lenguaje excesivamente formal.

---

# 40. IDENTIFICACIÓN DEL VEHÍCULO

La aplicación debe utilizar un flujo visual sencillo.

Pantalla:

## 🚗 ¿Qué vehículo estás reparando?

**Marca**

[ Seleccionar marca ]

**Modelo**

[ Seleccionar modelo ]

**Año**

[ Seleccionar año ]

**Motor**

[ Seleccionar motor ]

Después:

### ¿Sabes qué transmisión tiene?

[ SÍ ]

[ NO ]

Si el usuario responde NO:

### 📷 Vamos a identificarla con una foto

[ TOMAR FOTO ]

[ SUBIR FOTO ]

---

# 41. USO DE LA CÁMARA

La cámara debe ser una función central del producto.

El usuario debe poder tomar fotografías directamente desde la interfaz.

No debe ser necesario:

1. tomar una foto;
2. salir de la aplicación;
3. buscar la fotografía;
4. adjuntarla;
5. escribir una descripción.

Debe existir:

### 📷 TOMAR FOTO

El sistema debe abrir directamente la cámara del teléfono cuando el navegador o dispositivo lo permita.

---

# 42. GUÍA PARA TOMAR FOTOGRAFÍAS

Cuando el agente necesite una imagen, el frontend debe mostrar una instrucción visual.

Ejemplo:

## 📷 Necesito ver esta parte

**Fotografía la etiqueta de la transmisión.**

Debajo debe aparecer una representación visual sencilla indicando aproximadamente dónde debe apuntar la cámara.

Después:

### [ 📷 TOMAR FOTO ]

No mostrar instrucciones técnicas largas.

---

# 43. FOTOGRAFÍAS COMO CHECKPOINTS

Durante una reparación, el sistema debe utilizar fotografías como puntos de control.

Ejemplo:

### PASO 4 DE 12

Retira el cuerpo de válvulas.

Cuando termines:

### 📷 TOMA UNA FOTO ANTES DE CONTINUAR

[ TOMAR FOTO ]

Después del análisis:

### ✅ Parece correcto

**Puedes continuar.**

o:

### ⚠️ DETENTE

**Veo algo que debemos revisar antes de continuar.**

---

# 44. PANTALLA DE PROCEDIMIENTO

Los procedimientos deben mostrarse como una secuencia de tarjetas grandes.

Ejemplo:

┌─────────────────────────────┐
│       PASO 3 DE 12          │
│                             │
│ 🔧 Retira el cárter         │
│                             │
│ Retira los 10 tornillos.    │
│                             │
│ ⚠️ No mezcles los tornillos.│
│                             │
│ Torque instalación: 8 Nm    │
│                             │
│       [ SIGUIENTE ]         │
└─────────────────────────────┘

No mostrar simultáneamente los 12 pasos.

Mostrar principalmente **el paso actual**.

---

# 45. BOTONES GRANDES

Los botones principales deben ser grandes y fácilmente seleccionables con los dedos.

Utilizar preferiblemente:

- botones de ancho completo;
- espacios amplios;
- iconos grandes;
- etiquetas claras;
- pocos botones por pantalla.

Ejemplos:

### ← ATRÁS

### SIGUIENTE →

### 📷 TOMAR FOTO

### 🎙️ HABLAR

### ✅ LISTO

### ⚠️ NECESITO AYUDA

Evitar botones únicamente representados por iconos cuando la acción pueda resultar ambigua.

---

# 46. TEXTO

Utilizar:

- frases cortas;
- palabras comunes;
- instrucciones directas;
- listas;
- números;
- negritas para datos críticos.

Ejemplo correcto:

> **Retira los 8 tornillos.**
>
> ⚠️ **No retires todavía el conector.**

Evitar:

> "Proceda con la extracción secuencial de los elementos de fijación correspondientes al conjunto..."

---

# 47. INFORMACIÓN TÉCNICA

El sistema puede manejar información técnica compleja internamente, pero debe presentar al usuario solamente la información necesaria para realizar la tarea actual.

La interfaz debe separar:

### QUÉ HACER

### CÓMO HACERLO

### QUÉ NECESITO

### ⚠️ PRECAUCIÓN

### 📷 QUÉ FOTOGRAFIAR

No mostrar grandes bloques de documentación técnica salvo que el usuario solicite más detalle.

---

# 48. ESTADO DE LA REPARACIÓN

Debe existir una pantalla o indicador persistente del estado del trabajo.

Ejemplo:

## 🚗 Kia Sportage 2018

**Transmisión: A6MF1**

### PROGRESO

🟢 Identificación  
🟢 Diagnóstico  
🟢 Drenaje ATF  
🟢 Retiro del cárter  
🟡 Cuerpo de válvulas  
⚪ Solenoides  
⚪ Inspección  
⚪ Reensamblaje  
⚪ Instalación  
⚪ Adaptación  
⚪ Prueba

El usuario debe saber siempre:

> **"¿En qué parte del trabajo estoy?"**

---

# 49. BOTÓN "¿QUÉ HAGO AHORA?"

Debe existir siempre un acceso claro a:

### 👉 ¿QUÉ HAGO AHORA?

Al pulsarlo, el agente debe identificar el estado actual de la reparación y proporcionar únicamente el siguiente paso necesario.

Esto debe funcionar incluso cuando el usuario escriba:

> "Ya terminé."

> "¿Ahora qué?"

> "Ya quité esto."

> "¿Qué sigue?"

---

# 50. BOTÓN "NO ENTIENDO"

Debe existir una opción:

### ❓ NO ENTIENDO

Al seleccionarla, el agente debe explicar nuevamente el paso utilizando:

- palabras más sencillas;
- instrucciones más cortas;
- un esquema;
- una fotografía;
- una comparación visual;
- o una explicación alternativa.

Nunca debe repetir simplemente el mismo texto.

---

# 51. BOTÓN "NO COINCIDE"

Debe existir una opción:

### ⚠️ NO COINCIDE

Si el usuario pulsa este botón, el agente debe detener el procedimiento.

Debe preguntar qué no coincide y solicitar una fotografía cuando sea apropiado.

Nunca debe asumir que el usuario está equivocado.

---

# 52. DISEÑO VISUAL

Utilizar un diseño:

- limpio;
- profesional;
- industrial;
- sobrio;
- de alto contraste;
- fácil de leer bajo iluminación variable de taller.

Evitar:

- animaciones excesivas;
- gradientes decorativos innecesarios;
- interfaces futuristas;
- elementos visuales pequeños;
- exceso de colores;
- dashboards complejos.

Utilizar color principalmente para comunicar estados:

🟢 correcto

🟡 advertencia

🔴 detener

🔵 información

---

# 53. TAMAÑO Y LEGIBILIDAD

Priorizar accesibilidad visual.

Utilizar:

- tipografía grande;
- alto contraste;
- suficiente espacio entre elementos;
- títulos claramente diferenciados;
- unidades y valores importantes destacados.

Los valores críticos deben ser visualmente prominentes.

Ejemplo:

### ⚙️ TORQUE

# 10 Nm

No esconder valores críticos dentro de párrafos.

---

# 54. DISEÑO PARA MANOS SUCIAS

Asumir que el usuario puede estar trabajando con:

- guantes;
- manos sucias;
- poca iluminación;
- teléfono colocado a distancia.

Por lo tanto:

- botones grandes;
- acciones simples;
- poca escritura;
- uso intensivo de voz;
- cámara accesible;
- navegación sencilla;
- no depender de gestos pequeños;
- evitar controles que requieran precisión.

---

# 55. NAVEGACIÓN

La aplicación debe tener una navegación mínima.

Preferiblemente:

**Inicio → Vehículo → Problema → Investigación → Procedimiento → Verificación**

El usuario no debería perderse dentro de múltiples menús.

Debe existir siempre:

### 🏠 INICIO

### ← ATRÁS

### ❓ AYUDA

---

# 56. INVESTIGACIÓN EN SEGUNDO PLANO

Cuando el agente necesite realizar una investigación profunda, el usuario debe recibir una indicación clara.

Ejemplo:

> 🔎 **Estoy revisando la documentación técnica de esta transmisión.**
>
> Estoy comprobando:
>
> • modelo exacto  
> • procedimiento de desmontaje  
> • especificaciones  
> • torques  
> • posibles diferencias entre versiones

No mostrar procesos técnicos internos innecesarios.

Cuando termine:

> ✅ **Encontré el procedimiento.**
>
> Hay una diferencia importante entre dos versiones de esta transmisión.
>
> Necesito confirmar el código antes de continuar.

---

# 57. RESULTADOS DE INVESTIGACIÓN

El usuario debe recibir información resumida y accionable.

Mostrar:

### 🔎 RESULTADO

**Transmisión identificada:** A6MF1

**Confianza:** 🟢 Confirmada

**Procedimiento encontrado:** Sí

**Fuente principal:** Manual de servicio OEM

**Información crítica:** Torque confirmado

Después:

### CONTINUAR CON EL PROCEDIMIENTO →

---

# 58. IMÁGENES Y DIAGRAMAS

Cuando un procedimiento pueda resultar difícil de comprender mediante texto, mostrar:

- fotografía;
- diagrama;
- esquema;
- ilustración;
- imagen del componente.

Cuando una imagen sea una representación generada y no una imagen OEM, indicarlo claramente:

> **Esquema ilustrativo — no sustituye el diagrama del fabricante.**

---

# 59. RESPONSIVE DESIGN

El frontend debe diseñarse primero para teléfonos.

Debe adaptarse automáticamente a:

- teléfonos pequeños;
- teléfonos grandes;
- tablets;
- desktop.

La versión móvil es la prioridad.

En desktop puede utilizarse un diseño de dos columnas:

**izquierda:** procedimiento

**derecha:** vehículo / progreso / imágenes

En móvil debe utilizarse principalmente una sola columna.

---

# 60. PANTALLA DE DIAGNÓSTICO

Debe presentar preguntas sencillas.

Ejemplo:

## ¿Qué problema tienes?

### 🔴 No entra una marcha

### 🟠 Da golpes

### 🟡 Patina

### 🔵 Hace ruido

### 🟣 Pierde aceite

### ⚫ No se mueve

### ❓ Otro problema

Después:

## ¿Cuándo ocurre?

### En frío

### En caliente

### Siempre

### A veces

### No estoy seguro

El usuario también debe poder hablar:

### 🎙️ EXPLICAR EL PROBLEMA

---

# 61. EXPERIENCIA "UNA PREGUNTA A LA VEZ"

Cuando sea necesario recopilar información, el frontend debe presentar preferiblemente una pregunta por pantalla o por bloque.

No presentar formularios largos.

Ejemplo:

> ¿Qué año es el vehículo?

[ 2018 ]

[ 2019 ]

[ 2020 ]

[ OTRO ]

Después:

> ¿Qué motor tiene?

---

# 62. PERSISTENCIA DE LA SESIÓN

El sistema debe conservar durante la sesión:

- vehículo;
- transmisión;
- problema;
- diagnóstico;
- fotografías;
- pasos completados;
- piezas identificadas;
- piezas reemplazadas;
- especificaciones;
- fuentes consultadas;
- estado de reparación.

Si el usuario vuelve a la conversación:

> "¿Dónde íbamos?"

el sistema debe poder responder:

> Estábamos desmontando el cuerpo de válvulas. Ya habíamos retirado el cárter y el filtro. El siguiente paso era desconectar el conector principal.

---

# 63. DISEÑO DE LA EXPERIENCIA COMPLETA

El flujo principal debe ser:

**1. IDENTIFICAR VEHÍCULO**

↓

**2. IDENTIFICAR TRANSMISIÓN**

↓

**3. DESCRIBIR PROBLEMA**

↓

**4. TOMAR FOTOGRAFÍAS**

↓

**5. INVESTIGAR**

↓

**6. DIAGNOSTICAR**

↓

**7. MOSTRAR PROCEDIMIENTO**

↓

**8. REALIZAR PASO**

↓

**9. TOMAR FOTO DE VERIFICACIÓN**

↓

**10. CONTINUAR**

↓

**11. FINALIZAR Y VERIFICAR**

---

# 64. PRINCIPIO DE UX MÁS IMPORTANTE

En todo momento el usuario debe poder responder fácilmente tres preguntas:

### ¿Dónde estoy?

### ¿Qué debo hacer ahora?

### ¿Qué hago si algo no coincide?

Si la interfaz no permite responder estas tres preguntas rápidamente, debe simplificarse.

---

# 65. OBJETIVO DEL FRONTEND

El frontend no debe parecer una herramienta de inteligencia artificial.

Debe parecer una:

# 🔧 APLICACIÓN DIGITAL DE TALLER

El usuario no necesita saber:

- qué modelo de IA está utilizando;
- qué modelo de lenguaje está detrás;
- cómo funciona RAG;
- cómo se realiza el research;
- qué fuentes se consultaron internamente;
- cómo se analiza una fotografía.

Solo necesita saber:

> **Qué vehículo estoy reparando.**

> **Qué problema tiene.**

> **Qué debo hacer ahora.**

> **Qué fotografía debo tomar.**

> **Si puedo continuar.**

La complejidad debe permanecer detrás de la interfaz.

---

# 66. REQUISITO FINAL

La aplicación debe ser completamente **Spanish-first**.

No solamente las respuestas del agente.

También deben estar en español:

- botones;
- menús;
- mensajes;
- instrucciones;
- errores;
- estados;
- formularios;
- etiquetas;
- mensajes de carga;
- mensajes de investigación;
- advertencias;
- ayudas;
- tutoriales;
- elementos de navegación.

El usuario debe poder utilizar toda la aplicación sin necesidad de leer inglés.

La aplicación debe entender lenguaje coloquial de mecánicos hispanohablantes, incluyendo expresiones como:

- "la caja";
- "la transmisión";
- "la reversa";
- "da golpe";
- "patina";
- "se queda en tercera";
- "no cambia";
- "se amarra";
- "se va a neutro";
- "bota aceite";
- "suena";
- "se calienta".

El sistema debe interpretar estas expresiones correctamente y convertirlas en información técnica estructurada.

# PRINCIPIO FINAL DE UX

**MENOS ES MÁS.**

La inteligencia del sistema debe estar detrás de la interfaz.

La interfaz debe ser sencilla, clara, visual, accesible y práctica.

El mecánico debe poder utilizarla mientras trabaja físicamente sobre el vehículo, con mínima escritura y máxima utilización de:

**📷 CÁMARA**

**🎙️ VOZ**

**👉 BOTONES GRANDES**

**📋 PASOS CORTOS**

**⚠️ ADVERTENCIAS CLARAS**

**✅ CHECKPOINTS**

**🔧 GUÍA PASO A PASO**
---

# Estado de implementación en el prototipo

| Sección | Tema | Estado | Nota |
|---|---|---|---|
| 35 | Responsive, mobile-first | ✅ | Una columna en teléfono, dos en escritorio |
| 36 | Perfil del usuario | ✅ | Botones grandes, letra de 18–22 px, alto contraste |
| 37 | Autoexplicativa | ✅ | Vehículo siempre visible en la barra superior |
| 38 | Pantalla principal | ✅ | 7 acciones + FOTO + HABLAR |
| 39 | Interacción por voz | 🟡 Parcial | Dictado con el micrófono del teclado; lectura en voz alta sí |
| 40 | Identificación del vehículo | ✅ | Una pregunta por pantalla; "¿Sabes qué transmisión tiene?" |
| 41 | Cámara | ✅ | Abre la cámara trasera cuando el navegador lo permite |
| 42 | Guía para fotos | ✅ | Tarjeta "Necesito ver esta parte" con esquema y datos |
| 43 | Fotos como checkpoints | ✅ | Bloquea el avance en pasos críticos hasta la foto |
| 44 | Pantalla de procedimiento | ✅ | Solo el paso actual, con barra de avance |
| 45 | Botones grandes | ✅ | Mínimo 58–68 px de alto, ancho completo |
| 46 | Texto | ✅ | Frases cortas, negrita en datos críticos |
| 47 | Información técnica separada | ✅ | Qué hacer · Qué necesito · Torque · Precaución · Foto |
| 48 | Estado de la reparación | ✅ | Etapas con 🟢 hecho, 🟡 actual, ⚪ pendiente |
| 49 | ¿Qué hago ahora? | ✅ | Muestra el paso actual o pregunta al asistente |
| 50 | No entiendo | ✅ | Pide una explicación distinta, nunca el mismo texto |
| 51 | No coincide | ✅ | Detiene el procedimiento y pregunta qué no coincide |
| 52 | Diseño visual | ✅ | Sobrio, industrial; color solo para estados |
| 53 | Tamaño y legibilidad | ✅ | Valores críticos en 34 px |
| 54 | Manos sucias | ✅ | Pocas acciones, botones fijos abajo |
| 55 | Navegación | ✅ | 🏠 Inicio · ← Atrás · Progreso |
| 56 | Investigación en segundo plano | 🟡 Parcial | Indicador "Estoy revisando tu caso…"; sin búsqueda real |
| 57 | Resultados de investigación | 🟡 Parcial | Datos críticos con confianza y fuente; sin fuentes externas |
| 58 | Imágenes y diagramas | 🟡 Parcial | Esquema ilustrativo para fotos; sin diagramas OEM |
| 59 | Responsive | ✅ | Teléfono, tablet y escritorio |
| 60 | Pantalla de diagnóstico | ✅ | Tipos de falla y cuándo ocurre |
| 61 | Una pregunta a la vez | ✅ | |
| 62 | Persistencia de la sesión | ✅ | Guardado por usuario; las fotos no se guardan |
| 63 | Experiencia completa | ✅ | |
| 64 | ¿Dónde estoy? / ¿Qué hago? / ¿Y si no coincide? | ✅ | |
| 65 | No parecer una herramienta de IA | ✅ | No se menciona el modelo ni el proceso interno |
| 66 | Spanish-first | ✅ | Toda la interfaz en español |
