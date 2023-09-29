[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/hibernator11/notebooks-chatbot-v2/master)

[![DOI](https://zenodo.org/badge/298878713.svg)](https://zenodo.org/badge/latestdoi/298878713)


# notebooks-chatbot
Este proyecto incluye ejemplos de chatbot basado en Jupyter notebooks que utilizan diferentes librerías para entrenar en varios idiomas, procesar las consltas y proporcionar la respuesta a los usuarios.

A continuación se describen varios ejemplos realizados con diferentes tecnologías como spaCy y ChatterBot.

## spaCy
Este ejemplo hace uso del API sobre el tiempo a través del API https://openweathermap.org/api. Además, utiliza la librería spaCy para identificar en la consulta la localización sobre la que se desea conocer el tiempo. Se ha creado un ejemplo en inglés y su traducción al español. Para ello, se han utilizado los modelos del lenguaje proporcionados por spaCy disponibles en https://spacy.io/usage/models.


## Chatterbot
Los siguientes se basan en la librería [ChatterBot](https://pypi.org/project/ChatterBot/). Proporciona diferentes ejemplos para crear un chatbot y enternarlo de forma sencilla para los desarrolladores.

Los ejemplos no funcionan en Binder por problemas de la distribución de la librería.

### Introducción a ChatterBot
Este ejemplo introduce las bases para crear un chatbot utilizando la librería ChatterBot. Consultar [Notebook](https://nbviewer.org/github/hibernator11/notebooks-chatbot/blob/master/Ejemplo-chatterbot.ipynb)

### Entrenamiento de ChatterBot en inglés
Este ejemplo introduce cómo entrenar un chatbot en inglés con la librería ChatterBot. Consultar [Notebook](https://nbviewer.org/github/hibernator11/notebooks-chatbot/blob/master/Ejemplo-chatterbot-entrenamiento-ingles.ipynb)

### Entrenamiento de ChatterBot en español
Este ejemplo introduce cómo entrenar un chatbot en español con la librería ChatterBot. Consultar [Notebook](https://nbviewer.org/github/hibernator11/notebooks-chatbot/blob/master/Ejemplo-chatterbot-entrenamiento-espanol.ipynb)

### Entrenamiento de ChatterBot con fichero personalizado
Este ejemplo introduce cómo entrenar un chatbot a partir de un corpus personalizado con la librería ChatterBot. Consultar [Notebook](https://nbviewer.org/github/hibernator11/notebooks-chatbot/blob/master/Ejemplo-chatterbot-entrenamiento-corpus.ipynb)

## Referencias

- https://mybinder.readthedocs.io/
- https://mybinder.readthedocs.io/en/latest/examples/sample_repos.html#conda-environment-with-environment-yml
