# Material 1 · Conferencia "IA y publicidad" (Juan, Feria EFI) — transcripción

Tipos: [P] práctica recomendada · [V] afirmación por verificar o dudosa · [D] descartado para este agente.
Aplicación: cómo se usa en Chef & Bakery (C&B).

## 1. Principios útiles

| # | Principio | Tipo | Categoría | Aplicación a C&B |
|---|---|---|---|---|
| 1 | Implementar vale más que acumular información; consumir contenido da falsa sensación de aprendizaje. | P | IA y arquitectura | Cada material se convierte en reglas o pasos que el agente usa, no en resúmenes. Ya es nuestro método del 20 %. |
| 2 | La publicidad no se hace para el gusto del dueño: el creativo más bonito no es el que más vende, sino el que más conecta. | P | Creatividad | Paula y el equipo no descartan un guion porque "no les gusta cómo se ven"; se decide con datos. Sí se descarta si rompe una regla (honestidad, sanidad, cobertura). |
| 3 | Ser más atrevido que la competencia: la pieza típica (producto + "oferta especial") no se diferencia. | P | Creatividad / Hooks | El agente debe evitar la "imagen de catálogo navideño" y proponer ganchos que nadie del sector usa en Medellín. |
| 4 | Lo natural supera a la superproducción en redes: grabar como se es, sin "Hollywood". | P | Creatividad / Plataforma | Encaja con lo que tienen: Paula a cámara y celular. Los guiones se escriben para grabarse con celular en la cocina real. |
| 5 | La gente entra a redes a entretenerse, no a comprar; el contenido entretenido "camufla" la venta. | P | Psicología del consumidor | El primer segundo debe entretener o identificar; la oferta llega después. |
| 6 | Hablarle a gente normal, no volverse "clase alta" en el tono. | P (con matiz) | Persuasión | CONTRADICCIÓN con el posicionamiento premium de C&B. Propuesta: producto y marca premium, tono cercano y humano (humor de oficina, situaciones reales). Pendiente de validar. |
| 7 | Cada campaña debe aprender de la anterior, no empezar de cero. | P | Pruebas y aprendizaje | Bitácora de aprendizajes por anuncio; el agente la consulta antes de escribir guiones nuevos. Responde a tu requisito "aprender de anuncios anteriores". |
| 8 | Los aprendizajes se guardan con nivel de confianza (baja/media/alta) y no se borran. | P | Pruebas y aprendizaje | Con $900.000/mes los datos serán pocos: casi todo empezará en confianza "baja". El agente no debe convertir un resultado aislado en regla. |

## 2. Metodología propuesta por el conferencista

Niveles de uso de IA para publicidad:
1. Chat con Claude conectado a Meta (conector) para crear campañas.
2. Skill: enseñarle a la IA el método de un experto (cursos, videos) para que lo aplique siempre.
3. Agente propio en Claude Code.
4. Ciclo infinito que se automejora con poca intervención humana.

Ciclo de 7 subagentes: lanzar → vigilar → leer datos → concluir → optimizar → aprender (guardar en base de conocimiento) → crear (consultando lo aprendido).
- El lanzamiento y la optimización piden confirmación humana al inicio ("seguro en el gatillo").
- El que lee solo recopila; otro concluye; otro decide. Separar funciones.
- Memoria externa: un repositorio de GitHub como "disco duro"; el orquestador consulta el repositorio, no el chat.

Dónde estamos: entre el nivel 2 y el 3. El repositorio de este proyecto ya es la memoria externa del agente.
Alcance de nuestro agente: guiones y aprendizaje creativo. NO lanza ni modifica campañas ni gasta dinero.

## 3. Errores a evitar al construir el agente
1. Pedirle todo de un solo tiro (investigar, crear, guionizar, evaluar) → dividir en pasos o roles.
2. Usar la conversación como memoria → todo lo importante se guarda en el repositorio.
3. Creer todo lo que responde la IA: inventa con seguridad antes que admitir que no sabe → reglas de fuentes y marcas [C]/[H].
4. Acumular skills o conocimiento sin filtro → solo lo que mejora guiones.
5. Crear cada anuncio desde cero → consultar la bitácora antes de crear.
6. Corregir la propuesta creativa por gusto personal → corregir por regla o por dato.
7. Darle autonomía con dinero demasiado pronto → nuestro agente no toca dinero.

## 4. Afirmaciones a verificar o descartar
| Afirmación | Evaluación |
|---|---|
| "Una vuelta del ciclo gasta 35 % de la memoria y con subagentes 5 %" | [V] Cifras ilustrativas (él mismo dudó del número). La idea de fondo sí es válida: la memoria de trabajo es limitada y dividir tareas ayuda. |
| "Claude tiene 1 millón de tokens de contexto" | [V] Depende del modelo y del plan; no es un dato fijo. |
| "Muchas skills llenan la memoria" | [V] Parcialmente: en Claude Code las skills cargan su contenido completo solo cuando se usan. El riesgo real es cargar documentos largos innecesarios. |
| "Optimizar el día 7 y escalar el día 10" | [V] Regla práctica del conferencista, no de Meta. Con $30.000/día es poco probable salir rápido de la fase de aprendizaje: el ritmo debe adaptarse al presupuesto. |
| Usar un token de Meta con todos los permisos | [D] Riesgo innecesario; nuestro agente no maneja la cuenta. |
| Generar video/imagen del producto con IA (HeyGen, Gemini) sin intervención | [D] para el producto: la comida mostrada debe ser real (honestidad). La IA sí puede apoyar ideas, guiones y textos. |
| Insultar a Claude bloquea la cuenta; agentes crean idiomas propios; 1.000 millones de robots en 2030; ingresos de Anthropic atribuidos a una persona | [D] No verificado y sin relación con los guiones. |
| "Más de 30 millones de dólares invertidos en anuncios" | [V] Afirmación de autoridad del conferencista, no verificable. |

## 5. Propuestas para incorporar (a decidir en etapas siguientes)
- Bitácora de aprendizajes: por anuncio, qué se probó (gancho, ángulo, formato, público), resultado, conclusión y confianza.
- Roles separados dentro del agente (no 18; 3 a 5 bastan para un negocio de este tamaño): investigador, creativo de ideas, guionista, evaluador crítico, analista de resultados.
- Regla de autonomía: el agente propone; la persona aprueba lo que implica dinero o publicación.
