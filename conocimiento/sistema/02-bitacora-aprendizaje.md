# Etapa 4 · Bloque 2: bitácora de resultados y aprendizaje (APROBADO 4 nov 2026)

Objetivo: que cada anuncio enseñe algo al siguiente. El agente consulta esta bitácora ANTES de escribir guiones nuevos.

## 1. Qué se registra por anuncio
Identificación: código del anuncio · fecha de inicio y fin · producto · público (frío/tibio/caliente) · etapa del ciclo de ventas · estructura (# de la biblioteca) · gancho exacto · formato y duración · presupuesto gastado.

Métricas de Meta (el agente puede leerlas de la cuenta con el conector de Meta Ads):
| Métrica | Qué dice |
|---|---|
| Tasa de gancho = reproducciones de 3 s ÷ impresiones | ¿El gancho detiene el scroll? |
| Retención (reproducciones completas / ThruPlay) | ¿El contenido sostiene la atención? |
| CTR | ¿Dan ganas de dar clic? |
| Conversaciones iniciadas y costo por conversación | ¿Escriben por WhatsApp? |
| Frecuencia | ¿Se está cansando el público? |

Resultados del negocio (los registra la empresa en el Centro de Control):
conversaciones con empresas reales · cotizaciones enviadas · ventas cerradas · valor vendido.

## 2. Cómo se lee (diagnóstico por etapa)
| Si pasa esto… | El problema probable está en… | El siguiente guion cambia… |
|---|---|---|
| Tasa de gancho baja | Gancho | Solo el inicio (misma pieza, 3 ganchos) |
| Ganchan pero se van rápido | Contenido | El desarrollo / la estructura |
| Lo ven pero no escriben | Llamado a la acción u oferta | CTA, oferta, prueba |
| Escriben pero no son empresas o no cotizan | Público o mensaje que no filtra | Filtro (precio "desde", "para empresas") |
| Cotizan pero no compran | Proceso comercial o precio (no el anuncio) | Se informa; no se culpa al guion |

## 3. Nivel de confianza de cada aprendizaje (propuesta, ajustable)
- Baja: menos de 7 días o pocas conversaciones (menos de 10). Es una pista, no una regla.
- Media: 7+ días y 10+ conversaciones con resultado consistente.
- Alta: el mismo resultado se repite en 2 o más rondas.
Con $900.000/mes, casi todo empezará en confianza baja: no convertir un resultado aislado en regla.

## 4. Formato de cada aprendizaje
Qué probamos → qué pasó (con números) → qué creemos que significa → confianza → qué hacemos distinto.
Nunca se borra un aprendizaje: si se contradice, se marca y se explica.

## 5. Plantilla de registro
| Código | Fechas | Producto | Público | Etapa | Estructura | Gancho | Gasto | Tasa gancho | Retención | CTR | Conversaciones | Costo/conv. | Cotizaciones | Ventas | Valor | Aprendizaje | Confianza |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|

## 6. Decisiones de la empresa
- Sí se registrará en el Centro de Control cuando un cliente llega por un anuncio: opción "Meta Ads" en "¿Cómo se enteró?" + columna con el código/nombre del anuncio.
- El WhatsApp lo responde la mamá de Sofía: ella pregunta o anota de dónde viene cada contacto.
- Revisión de resultados con el agente: una vez por semana.
- Pendiente a futuro: la empresa quiere crear un CRM. Cuando exista, la bitácora se conecta a él (no se construye en esta etapa).

## 7. Revisión semanal automática
- Tarea programada "Revisión semanal de anuncios C&B": lunes 7:57 a. m. (hora de Bogotá), primera ejecución 16 nov 2026.
- Si no hay anuncios con gasto en los últimos 7 días, no hace informe.
- Informe en informes/AAAA-MM-DD_revision-semanal.md + actualización de la bitácora.
- PENDIENTE: la tarea quedó creada SIN los conectores de Meta Ads y Google Drive (la sesión no pudo pasarlos). Hay que agregarlos desde la configuración de tareas programadas en claude.ai; sin ellos, la tarea avisará que no puede leer las métricas.
