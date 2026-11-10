# Cómo leer las métricas de Meta Ads para mejorar los videos (nov 2026)

Propósito: saber si el CONTENIDO funciona y qué parte del video mejorar. No es para manejar campañas.
Nombres de campos verificados en la herramienta de Meta Ads (ads_get_field_context, 10 nov 2026).

## 1. Las métricas que importan para un guion
| Pregunta | Métrica | Campo en la herramienta | Nivel disponible |
|---|---|---|---|
| ¿Cuántas veces se mostró? | Impresiones | `impressions` | anuncio |
| ¿El gancho detiene el scroll? | Reproducciones de 3 s ÷ impresiones (tasa de gancho) | `3_second_video_plays` | SOLO campaña / conjunto, NO anuncio |
| (alternativa a nivel anuncio) | Reproducciones continuas de 2 s ÷ impresiones | `video_continuous_2_sec_watched_actions` | anuncio |
| ¿El contenido sostiene la atención? | ThruPlays (15 s o completo) ÷ reproducciones de 3 s (tasa de retención) | `video_thruplay_watched_actions` | anuncio |
| ¿Dónde se va la gente? | Reproducciones al 25 / 50 / 75 / 95 / 100 % | `video_p25_watched_actions` … `video_p100_watched_actions` | anuncio |
| ¿Cuánto lo ven en promedio? | Tiempo promedio de reproducción | `video_avg_time_watched_actions` | anuncio |
| ¿Cuántos empezaron a verlo? | Reproducciones iniciadas | `video_play_actions` | anuncio |
| ¿Dan clic? | CTR de enlace | `website_ctr` (alias link_ctr) | anuncio |
| ¿Escriben por WhatsApp? | Resultados y costo por resultado (si el objetivo de la campaña es mensajes, el resultado = conversación) | `results`, `cost_per_result` | anuncio |
| ¿Se cansó el público? | Frecuencia | `frequency` | anuncio |
| Gasto | Importe gastado | `amount_spent` | anuncio |
Notas: las reproducciones al 25–100 % incluyen a quien adelantó el video. Los 3 s no están a nivel de anuncio: si cada conjunto tiene un solo anuncio, se puede leer a nivel de conjunto; si no, se usa la de 2 s como aproximación (y se dice).

## 2. Cómo calcular (cálculos propios, decirlo así en el informe)
- Tasa de gancho = 3 s (o 2 s) ÷ impresiones.
- Tasa de retención = ThruPlays ÷ reproducciones de 3 s (o 2 s).
- Curva de abandono = cada % (25, 50, 75, 95) ÷ reproducciones iniciadas → el salto más grande marca el momento del guion donde se van.
- Tiempo promedio ÷ duración del video = qué fracción ven.

## 3. Referencias externas (ORIENTACIÓN, no metas)
Las fuentes no coinciden y Meta no publica un "buen" valor oficial.
- Tasa de gancho: un análisis de 479 anuncios de Meta encontró mediana de 20,9 % y la mitad central entre 14 % y 30 % (Biddyco). Otras fuentes piden 25 % o más.
- Retención (ThruPlays ÷ 3 s): unas fuentes dan 20–25 % como sano en público frío; otras, 40–50 % como promedio. Videos de menos de 15 s marcan más alto: comparar solo videos de duración parecida.
Regla del agente: la comparación más útil es ENTRE NUESTROS PROPIOS ANUNCIOS (mismo producto, público y duración). Las referencias externas solo dan contexto.

## 4. Diagnóstico: qué parte del guion mejorar
| Lo que se ve | Diagnóstico | Qué cambia el próximo guion |
|---|---|---|
| Gancho bajo frente a los otros anuncios | Los primeros 3 s no detienen | Probar los ganchos alternativos con el mismo cuerpo |
| Gancho bueno, retención baja | El inicio promete y el desarrollo no sostiene | Ritmo, cortes, cumplir la promesa del gancho, acortar |
| Caída fuerte en un punto de la curva | Esa escena aburre o confunde | Reescribir o quitar esa escena |
| Lo ven, pero CTR o conversaciones bajas | Falta razón para actuar | Llamado a la acción, oferta, prueba, precio "desde" |
| Muchas conversaciones, pocas empresas | El anuncio no filtra | Decir "para empresas", mostrar precio y mínimo |
| Conversaciones de empresas, pocas ventas | Proceso comercial o precio | Se reporta; no es culpa del guion |
| Frecuencia alta y métricas cayendo | Cansancio | Rotar a un guion nuevo |

## 5. Cuándo se puede concluir algo
- Sin datos suficientes no hay conclusión: menos de ~1.000 impresiones por anuncio o menos de 7 días = solo pista (confianza baja).
- Con $900.000/mes los volúmenes son pequeños: no convertir un resultado aislado en regla.
- Separar siempre: dato de Meta · cálculo propio · interpretación.

Fuentes: Biddyco (hook rate benchmarks Meta), Adsights (video creative benchmarks 2026; cómo leer métricas de video), Motion vía Peachblue/agencyai, Jon Loomer (métricas de video), definiciones de la herramienta de Meta Ads.
