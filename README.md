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
- Insight 1:
- Insight 2:
- Insight 3:“Conflicto” es el negativo dominante; el resto apunta a problemas operativos y tensión/emoción.
  |Palabras especificas|conflicto, problema, dificultades, falta, daño,  tensión, violencia, pelea, chisme, mal, rabia.|
- Insight 4: Es necesario hacer una segunda normalizacion dado que hay exceso de muletillas, dado que estas palabras pueden agregar ruido en el analisis.
  


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
