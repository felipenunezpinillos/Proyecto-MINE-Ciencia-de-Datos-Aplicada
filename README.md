# Proyecto-MINE-Ciencia-de-Datos-Aplicada

# Integrantes del equipo:
- Felipe Nuñez
- Juan Manuel Pérez

# Objetivo
Estimar, con rigor y trazabilidad, la satisfacción de la comunidad educativa y el nivel de adopción/éxito del enfoque de Justicia Escolar Restaurativa (JER) a partir de entrevistas y documentos institucionales, mediante un pipeline de NLP (sentimientos + temas), y entregar un tablero interactivo por actor, localidad y periodo

# Alcance
- Fuentes: documentos institucionales (JER, manuales, orientaciones), Manuales de Convivencia de 13 colegios, entrevistas/anexos (estudiantes, docentes, directivos, familias, SED).
- Preprocesamiento: normalización en español, eliminación de ruido/duplicados, unigramas/bigramas y NER exploratorio para contexto léxico.
- Variables: localidad, estado del Manual, sentimiento (−1 a 1), tópicos recurrentes y alineación restaurativa.
- Entregables:
  - Notebook EDA (eda.ipynb) y cuadernos de modelado
  - Presentacion Ejecutiva
  - Documento ejecutivo

# Insights EDA
- **Insight 1: El NER revela foco en instituciones y funciones, no en personas.**  
  **Top entidades:** 1) *NOMBRE PERSONA* (anonimización), 2) *JER/Justicia Escolar Restaurativa*, 3) términos institucionales/roles: *Docente, SED, PEI, Manual de Convivencia, Consejo Directivo, Rector, Coordinador, Orientadora, Pedagogas*.

- **Insight 2: Los documentos se centran en 5 grandes temáticas**
  - **Convivencia y paz escolar / procesos restaurativos:** manejo/transformación del conflicto, acuerdos, justicia escolar restaurativa (JER).
  - **Normatividad y roles:** artículos/decretos/protocolos, derechos y deberes, PEI, Manual de Convivencia, Consejo/Comité; actores: docente, directivo, orientadora, familia.
  - **Participación y comunidad:** ciudadanía, comunidad educativa, memoria y reconocimiento.
  - **Cuidado y socioemocional:** reflexión, (auto)cuidado, apoyo/orientación, talleres/actividades.
  - **Escuela como eje operativo:** conversación operativa, tiempos de implementación, procesos y seguimiento.

- **Insight 3: Las palabras con connotación positiva** se centran en términos de paz/convivencia, acuerdo y cuidado, con énfasis en marcos restaurativos y participación.

| Palabras específicas | Paz, convivencia, restaurativo/restaurativa, reconciliación, acuerdo, diálogo, claro, importante, participación, ciudadanía, comunidad educativa, derecho(s), consejo/comité, promoción, responsable, atención, cuidado, autocuidado, ayudar/ayudado, apoyo, respeto, bien, bueno/buen, mejorar, desarrollo, fortalecimiento, experiencia/experiencial, enfoque, estrategia, promueve. |
|---|---|

- **Insight 4: “Conflicto” es el negativo dominante**; el resto apunta a problemas operativos y tensión/emoción.

| Palabras específicas | conflicto, problema, dificultades, falta, daño, tensión, violencia, pelea, chisme, mal, rabia. |
|---|---|

- **Insight 5:** Es necesario hacer una **segunda normalización** dado el **exceso de muletillas**, ya que estas palabras pueden **agregar ruido** en el análisis.

  


# Instrucciones de ejecución
## EDA:
   1. Clonar el repositorio
   2. Ejecutar el jupyter Notbook `eda.ipnyb`


# Dependencias
## EDA:
- stanza
- ftfy
- beautifulsoup4
- wordcloud
- nltk
- pandas
- openpyxl
- seaborn
