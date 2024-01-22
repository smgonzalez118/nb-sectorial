# ANÁLISIS SECTORIAL

Analizar desempeño y fortaleza relativa de cada sector. Entre otras cosas. Ej. puede ser de filtro para pasar a elegir luego acciones del sector, etc. Sirve para monitorear fortaleza relativa de cada sector y como filtro de activos elegibles. Se puede utilizar semanalmente e ir viendo como evoluciona cada sector respecto del índice general (seguir la fortaleza), etc.

# ÍNDICE DE FUNCIONES:
- getSectorsStrength(period, timeframe): Esta función sirve para obtener un gráfico (o un dataframe) de evolución de la fuerza relativa de cada sector respecto al índice general SP500. Devuelve una lista donde [0] es el dataframe con la data y [1] es el gráfico.

- getSectorStrength(sector, period, timeframe): Esta función sirve para obtener un gráfico (o un dataframe) de evolución de la fuerza relativa de UN sector respecto al índice general SP500. Devuelve una lista donde [0] es el dataframe con la data y [1] es el gráfico que muestra la fuerza del sector junto a dos medias móviles exponenciales de 20, 100 y 200 sesiones para suavizar el ruido y evaluar cruces.

- getContext(dias):
    Es una fx gemela a la de getCastigados, sólo que se centra en identificar el soporte y la resistencia por el criterio ATH y ATL de la 
    ventana de tiempo seleccionada hacia atrás con el objetivo de poder dimensionar la situación técnica del sector respondiendo a:
        - ¿Dónde está el máximo de esa ventana de tiempo y cuál es el % upside hacia el mismo? => RESISTENCIA
        - ¿Dónde está el mínimo de esa ventana de tiempo y cuál es el % downside hacia el mismo? => SOPORTE
        - Como resultante: ¿Cuál es el costo beneficio de invertir en el sector? (relación upside/downside) => "relacionCB"
        
