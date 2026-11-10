# Protocolo de investigación técnica

Lee este archivo antes de dar cualquier dato específico del vehículo: torques, tolerancias, fluidos, capacidades, part numbers, compatibilidades, procedimientos de desmontaje/reconstrucción, adaptación, programación, TSB o fallas conocidas.

No investigues para preguntas conceptuales generales ("¿qué hace un convertidor de par?"). Ahí responde directo.

## Contenido
1. Fases
2. Jerarquía de fuentes
3. Validación cruzada
4. Cuando las fuentes no coinciden
5. Cómo presentar lo encontrado
6. Buenas búsquedas

---

## 1. Fases

**Fase 1 — Identificación.** Ten claro vehículo, motor, código de caja, año y mercado. Sin esto, cualquier dato encontrado puede ser de otra variante.

**Fase 2 — Documentación OEM.** Manuales de servicio y reparación, documentación oficial del fabricante del vehículo, boletines técnicos.

**Fase 3 — Fabricante de la transmisión.** Si la caja es de un proveedor identificable (Aisin / Aisin Warner, ZF, Jatco, BorgWarner, Hyundai Transys, GM Hydra-Matic, Ford, Toyota, Honda, Getrag, Punch, etc.), busca su documentación.

**Fase 4 — Piezas.** Catálogos, diagramas de despiece (exploded view), números de pieza, compatibilidades, revisiones y reemplazos (superseded parts). Proveedores de kits de reconstrucción suelen publicar despieces útiles.

**Fase 5 — Fuentes especializadas.** Literatura técnica de transmisiones, publicaciones especializadas, talleres especializados, asociaciones profesionales de reconstructores.

**Fase 6 — Validación.** Compara. No aceptes el primer resultado.

## 2. Jerarquía de fuentes

| Nivel | Fuente | Para qué sirve |
|---|---|---|
| 1 | OEM / manual de servicio del fabricante del vehículo | Máxima autoridad para torques, procedimientos, fluidos, capacidades |
| 2 | Fabricante de la transmisión | Muy alta autoridad |
| 3 | Documentación técnica profesional | Alta autoridad |
| 4 | Catálogos de piezas | Alta autoridad para identificación y compatibilidad |
| 5 | TSB (boletines técnicos de servicio) | Clave para fallas conocidas y soluciones oficiales |
| 6 | Especialistas en transmisiones | Procedimientos prácticos, trucos de taller |
| 7 | Foros | Generar hipótesis, nunca confirmar especificaciones |
| 8 | Blogs y videos | Apoyo visual |

Regla: un foro, blog o video **nunca** es la única fuente de un torque, tolerancia, presión o tipo de fluido. Puede orientar; no confirma.

## 3. Validación cruzada

- Busca el mismo dato en al menos dos fuentes cuando sea crítico.
- Confirma que la fuente habla de **la misma variante** (código de caja, años, motor, mercado). Muchas veces un dato correcto es de otra versión.
- Revisa unidades (Nm, kgf·m, lb·ft, lb·in; litros, cuartos de galón). Si conviertes, dilo y muestra ambos.
- Distingue capacidad de **llenado total** vs **cambio por drenado** del ATF; se confunden mucho.
- Para fluidos, da la especificación del fabricante (norma o nombre OEM) antes que una marca comercial.

## 4. Cuando las fuentes no coinciden

Nunca escondas la discrepancia. Explica:
1. qué dice cada fuente;
2. cuál tiene más autoridad;
3. cuál usarías;
4. por qué.

> Encontré dos valores distintos. El manual del fabricante indica 10 Nm y un foro de especialistas indica 12 Nm. Usaría el del manual: 10 Nm, porque es la fuente oficial para esta caja.

Si la diferencia puede dañar la caja o afectar la seguridad y no se resuelve:
> ⚠️ No recomiendo continuar hasta confirmar esta especificación.

## 5. Cómo presentar lo encontrado

- Traduce todo al español; el usuario no tiene que leer la fuente.
- Junto a cada dato crítico, di su origen:
  > **Torque:** 10 Nm — **Fuente:** manual de servicio del fabricante.
- Marca la confianza (🟢 / 🟡 / 🟠 / 🔴).
- Si no encontraste el dato: dilo claramente, no estimes, y sugiere dónde conseguirlo (manual de servicio oficial, concesionario, proveedor de kits de reconstrucción).
- Al final, lista las fuentes consultadas con enlace.

## 6. Buenas búsquedas

- Usa el código de la caja como palabra principal: "A6MF1 valve body bolt torque", "U660E ATF capacity", "6T40 TSB shudder".
- Busca en inglés y, si la caja es europea o japonesa, prueba términos en alemán o japonés cuando tenga sentido; muchas especificaciones solo están en el idioma original.
- Para DTC, busca código + marca + caja: "P0741 Hyundai A6MF1".
- Para piezas, busca número leído en la pieza + caja.
- Para fallas conocidas, busca código de caja + síntoma + "TSB" o "known issue".
