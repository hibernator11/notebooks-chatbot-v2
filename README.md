[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/hibernator11/notebooks-chatbot-v2/master)

[![DOI](https://zenodo.org/badge/298878713.svg)](https://zenodo.org/badge/latestdoi/298878713)


# notebooks-chatbot
Este proyecto incluye ejemplos de chatbot basado en Jupyter notebooks que utilizan diferentes librerías para entrenar en varios idiomas, procesar las consltas y proporcionar la respuesta a los usuarios.

A continuación se describen varios ejemplos realizados con diferentes tecnologías como [spaCy](https://spacy.io/) y [ChatterBot](https://chatterbot.readthedocs.io/en/stable/).

## spaCy
Este ejemplo hace uso del API sobre el tiempo a través del API https://openweathermap.org/api. Además, utiliza la librería spaCy para identificar en la consulta la localización sobre la que se desea conocer el tiempo. Se ha creado un ejemplo en inglés y su traducción al español. Para ello, se han utilizado los modelos del lenguaje proporcionados por spaCy disponibles en https://spacy.io/usage/models.

- [Jupyter Notebook de Windy en inglés](https://nbviewer.org/github/hibernator11/notebooks-chatbot-v2/blob/master/Windy-Chat.ipynb)
- [Jupyter Notebook de Windy en español](https://nbviewer.org/github/hibernator11/notebooks-chatbot-v2/blob/master/Windy-Chat-es.ipynb)
- [Jupyter Notebook de Escritores en español](https://nbviewer.org/github/hibernator11/notebooks-chatbot-v2/blob/master/Escritores-Chat-es.ipynb)

Se incluye un ejemplo basado en los Wikidata y los datos abiertos de la Biblioteca Virtual Miguel de Cervantes para recuperar las obras de un autor en concreto. En el siguiente [enlace](https://w.wiki/7bWQ) se puede ejecutar la consulta SPARQL utilizada en el ejemplo.

```
select ?workLabel
where { ?s wdt:P2799 ?id . 
       ?s wdt:P1559 ?name . 
       filter regex(?name, "lope de vega", "i")
       BIND(uri(concat("https://data.cervantesvirtual.com/person/", ?id)) as ?bvmcID) 
       SERVICE <http://data.cervantesvirtual.com/openrdf-sesame/repositories/data> {
          ?bvmcID <http://rdaregistry.info/Elements/a/authorOf> ?work .
          ?work rdfs:label ?workLabel        
       }
} limit 10
```



## Chatterbot
Los siguientes se basan en la librería [ChatterBot](https://pypi.org/project/ChatterBot/). Proporciona diferentes ejemplos para crear un chatbot y enternarlo de forma sencilla para los desarrolladores.

Los ejemplos no funcionan en Binder por problemas de la distribución de la librería.

### Introducción a ChatterBot
Este ejemplo introduce las bases para crear un chatbot utilizando la librería ChatterBot. Consultar [Notebook](https://nbviewer.org/github/hibernator11/notebooks-chatbot/blob/master/chatterbot/Ejemplo-chatterbot.ipynb)

### Entrenamiento de ChatterBot en inglés
Este ejemplo introduce cómo entrenar un chatbot en inglés con la librería ChatterBot. Consultar [Notebook](https://nbviewer.org/github/hibernator11/notebooks-chatbot/blob/master/chatterbot/Ejemplo-chatterbot-entrenamiento-ingles.ipynb)

### Entrenamiento de ChatterBot en español
Este ejemplo introduce cómo entrenar un chatbot en español con la librería ChatterBot. Consultar [Notebook](https://nbviewer.org/github/hibernator11/notebooks-chatbot/blob/master/chatterbot/Ejemplo-chatterbot-entrenamiento-espanol.ipynb)

### Entrenamiento de ChatterBot con fichero personalizado
Este ejemplo introduce cómo entrenar un chatbot a partir de un corpus personalizado con la librería ChatterBot. Consultar [Notebook](https://nbviewer.org/github/hibernator11/notebooks-chatbot/blob/master/chatterbot/Ejemplo-chatterbot-entrenamiento-corpus.ipynb)

## Licencia y términos de uso
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Licencia Creative Commons" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/80x15.png" /></a><br />Esta obra está bajo una <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licencia Creative Commons Atribución 4.0 Internacional</a>.

## Referencias

- https://mybinder.readthedocs.io/
- https://mybinder.readthedocs.io/en/latest/examples/sample_repos.html#conda-environment-with-environment-yml
- https://www.askpython.com/python/examples/chatbot-in-python-using-spacy
- https://github.com/hibernator11/hdh-cafe-con-2023
- https://data.cervantesvirtual.com/noticia/dariah-annual-event-2023-y-la-bvmc
