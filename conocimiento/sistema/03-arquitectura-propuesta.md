# Etapa 5 · Bloque 1: arquitectura del agente (DECIDIDO 10 nov 2026)

## Dónde vive el agente (por decidir)
| Opción | Cómo funciona | A favor | En contra |
|---|---|---|---|
| A. Proyecto en claude.ai | Master Prompt como instrucciones + archivos de conocimiento subidos al proyecto | Muy fácil de usar, también desde el celular | No escribe solo la bitácora; hay que volver a subir archivos cuando cambian; un solo "rol" |
| B. Claude Code + este repositorio (recomendada) | El agente vive en el repositorio de GitHub: instrucciones principales + subagentes + conocimiento | Lee y actualiza su propia memoria (bitácora, referencias); puede leer Meta Ads; trabajo por roles; se usa desde claude.ai/code o la app | Un poco más técnico al inicio |
| C. Ambas | B como agente principal y una versión ligera en un Proyecto para borradores rápidos | Lo mejor de los dos | Dos lugares que mantener |

## Roles (5, no 18)
1. Director creativo (agente principal / orquestador): recibe el pedido, reparte el trabajo, entrega a Sofía.
2. Investigador: reseñas, comentarios, Biblioteca de anuncios, tendencias, referencias.
3. Creativo de ideas: propone conceptos y ángulos distintos (mecanismos diferentes).
4. Guionista: escribe el guion escena por escena + 3 ganchos alternativos.
5. Evaluador crítico: filtros, calificación, abogado del diablo; devuelve hasta que pase.
6. (Después del lanzamiento) Analista de resultados: lee Meta Ads + Centro de Control y actualiza la bitácora (revisión semanal).

## Flujo de un pedido
Pedido de Sofía → Investigador → Creativo (conceptos) → [¿Sofía elige concepto?] → Guionista → Evaluador (rehace hasta pasar) → Entrega a Sofía → Lanzamiento → Analista semanal → Bitácora → el siguiente pedido consulta la bitácora.

## Decisiones de Sofía (10 nov 2026)
- Opción B: Claude Code + este repositorio.
- Flujo en dos pasos: primero conceptos (Sofía elige), después guiones.
- Lectura de Meta Ads: SÍ, solo para aprender qué funciona y mejorar la calidad de los guiones.
- Las campañas (crear, segmentar, optimizar, presupuesto) las hará OTRO agente aparte, en el futuro. Este agente NO toca campañas.
