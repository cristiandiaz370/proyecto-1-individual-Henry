<p align=center><img src=https://github.com/cristiandiaz370/proyecto-1-individual-Henry/assets/167250663/4fafcd79-690e-4324-9bc3-cf7fbbd238ad><p>

# <h1 align=center> **Proyecto Final individual #1** </h1>

# <h1 align=center> **Machine Learning Operations (MLOps)** </h1>
<p align=center><img src=https://github.com/cristiandiaz370/proyecto-1-individual-Henry/assets/167250663/1c52bdcc-ab0f-45cd-82c6-63d330e0c7b7><P>

## INTRODUCCION

Este proyecto es el primer proyecto individual en el área de Machine Learning, realizado durante un bootcamp de Henry. Su objetivo es emular el trabajo de un MLOps Engineer, un profesional que combina habilidades de un Ingeniero de Datos y un Científico de Datos. En este escenario, el MLOps Engineer trabaja para Steam, la popular plataforma de videojuegos. El enfoque del proyecto es resolver un problema comercial importante: desarrollar un Producto Mínimo Viable (MVP) que incluya tanto una API para su implementación como un modelo de Machine Learning.

## DESCRIPCION DEL PROYECTO

El proyecto tiene como objetivo superar dos retos clave con éxito:


**El primer desafío:** del proyecto es examinar y categorizar las opiniones de los usuarios. Se utiliza TextBlob, una biblioteca de Procesamiento del Lenguaje Natural (NLP), para evaluar la polaridad de los sentimientos expresados en cada comentario, clasificándolos como negativos, neutrales o positivos.

**El segundo desafío:** del proyecto es desarrollar un sistema de recomendación de videojuegos. Este sistema sugiere juegos a los usuarios según sus gustos y actividades pasadas.

## DATASETS

Para desarrollar el proyecto se utilizaron tres archivos en formato JSON:

`**output_steam_games.json**`: Contiene información sobre los juegos; el nombre, el editor, el desarrollador, los precios y las etiquetas.

`**australian_users_items.json**`: Contiene información sobre los juegos utilizados por los usuarios y el tiempo que cada usuario pasa en cada juego.

`**australian_users_reviews.json**`: Contiene los comentarios que los usuarios realizaron sobre los juegos que usan, así como recomendaciones o críticas sobre esos juegos, ID del usuario y su URL.

## TAREAS RESUELTAS

### ETL (Extract, Transform and Load)

En esta etapa, se realizó la ingestión de datos. Los conjuntos de datos se transformaron en DataFrames para facilitar su manejo. También se llevaron a cabo procesos como desanidar columnas, transformar y limpiar datos. Específicamente, se analizaron y limpiaron valores nulos, se completaron datos que faltaban, se eliminaron algunas columnas innecesarias y se renombraron otras, además de cambiar los tipos de datos de ciertos campos, entre otras tareas.

![Pandas](https://img.shields.io/badge/-Pandas-333333?style=flat&logo=pandas)
![Numpy](https://img.shields.io/badge/-Numpy-333333?style=flat&logo=numpy)
![VSCode](https://img.shields.io/badge/-VSCode-333333?style=flat&logo=visual-studio-code)
![Jupyter](https://img.shields.io/badge/-Jupyter-333333?style=flat&logo=jupyter)
![Python](https://img.shields.io/badge/-Python-333333?style=flat&logo=python)

> Para ver en detalle las tareas realizadas en esta etapa, ingrese al siguiente link: [ETL](/ETL)

### Feature Engineering

En esta fase, se concentró en analizar los sentimientos expresados en los comentarios de los usuarios utilizando la biblioteca TextBlob. Se añadió una nueva columna llamada 'sentiment' al conjunto de datos 'user_reviews', donde las reseñas de los usuarios se clasifican como positiva, neutral o negativa, utilizando los valores 0 para negativa, 1 para neutra y 2 para positiva.
También se llevaron a cabo tareas para preparar y optimizar los conjuntos de datos, asegurando así que las consultas y las funcionalidades del servicio en la nube sean más eficientes.

![Pandas](https://img.shields.io/badge/-Pandas-333333?style=flat&logo=pandas)
![Numpy](https://img.shields.io/badge/-Numpy-333333?style=flat&logo=numpy)
![VSCode](https://img.shields.io/badge/-VSCode-333333?style=flat&logo=visual-studio-code)
![Jupyter](https://img.shields.io/badge/-Jupyter-333333?style=flat&logo=jupyter)
![Python](https://img.shields.io/badge/-Python-333333?style=flat&logo=python)
![Beautiful Soup](https://img.shields.io/badge/Beautiful%20Soup-333333?style=flat&logo=beautiful)
![TextBlob](https://img.shields.io/badge/TextBlob-333333?style=flat&logo=textblob)

> Para ver en detalle las tareas realizadas en esta etapa, ingrese al siguiente link: [FeatureEngineering](/Funcion_analisis_sentimiento.ipynb)

### EDA (Exploratory Data Analysis)

Después del proceso de ETL, se realizó un análisis exploratorio detallado de los tres conjuntos de datos principales. Este análisis incluyó la evaluación del porcentaje de valores nulos, la distribución y la presencia de valores atípicos en los precios de los ítems, el análisis de los usuarios que más horas han jugado, y la identificación del TOP 5 de los mejores desarrolladores, entre otros aspectos. Este examen ayudó a comprender mejor las características tanto categóricas como numéricas de los datos, destacando aquellas que son cruciales para el modelo de recomendación.
Además, se organizaron y prepararon los conjuntos de datos específicos necesarios para facilitar cada una de las funciones del sistema.

![WordCloud](https://img.shields.io/badge/WordCloud-333333?style=flat&logo=WordCloud)
![SciPy](https://img.shields.io/badge/SciPy-333333?style=flat&logo=WordCloud)
![Matplotlib](https://img.shields.io/badge/Matplotlib-333333?style=flat&logo=WordCloud)
![Seaborn](https://img.shields.io/badge/Seaborn-333333?style=flat&logo=Seaborn)

> Para ver en detalle las tareas realizadas en esta etapa, ingrese al siguiente link: [EDA](/EDA)

### Modelamiento (Desarrollo de modelos de aprendizaje automático)

En esta fase, desarrollamos nuestro sistema de recomendación basado en la relación entre ítems. Esto significa que seleccionamos un ítem y, comparándolo con otros en función de su similitud, recomendamos aquellos que son más parecidos utilizando la técnica de similitud de coseno.
Relación Item-Item: Se elige un ítem y, a través de los tags que poseemos como información, identificamos y recomendamos cinco ítems similares.
Para construir este sistema de recomendación, utilizamos el conjunto de datos que obtuvimos de las etapas previas y creamos un nuevo dataset específicamente diseñado para apoyar este proceso.

![VSCode](https://img.shields.io/badge/-VSCode-333333?style=flat&logo=visual-studio-code)
![Jupyter](https://img.shields.io/badge/-Jupyter-333333?style=flat&logo=jupyter)
![Pandas](https://img.shields.io/badge/-Pandas-333333?style=flat&logo=pandas)
![Numpy](https://img.shields.io/badge/-Numpy-333333?style=flat&logo=numpy)
![Scikitlearn](https://img.shields.io/badge/-Scikitlearn-333333?style=flat&logo=scikitlearn)

> Para ver en detalle las tareas realizadas en esta etapa, ingrese al siguiente link: [Modelo_recomendacion](/modelo_recomendacion.ipynb)

### Desarrollo de la API

Se construyó una API mediante el uso del framework FastAPI. Esta API ofrece varias funciones, estas son: 

- **Developer:** Función que recibe como parametro el nombre de una empresa desarrolladora y retorna la cantidad de items y porcentaje de contenido gratuito por año según la empresa dada. 

- **UserData:** Función que recibe como parametro un identificador uncio de usuario y retorna la cantidad de dinero gastado por el mismo, el porcentaje de recomendación y cantidad de items. 

- **UserForGenre:** Función que recibe como parametro un genero de juego y retorna el usuario con más horas jugadas para dicho genero y una acumulación de horas jugadas por año de lanzamiento.

- **BestDeveloperYear:** Función que recibe como parametro un año y retorna el TOP 3 de desarrolladores con más recomendaciones para el año dado.

- **DeveloperReviewsAnalysis:** Función que recibe como parametro el nombre de una empresa desarrolladora y retorna la cantidad de reseñas positivas y negativas, descartando las neutras.

- **GameRecommendation:** Esta función recibe como parametro el id de un juego y retorna una lista de los 5 juegos recomendados similares al ingreso.

![FastAPI](https://img.shields.io/badge/-FastAPI-333333?style=flat&logo=fastapi)
![Render](https://img.shields.io/badge/-Render-333333?style=flat&logo=render)

> Para poder interactuar con las funciones, ingrese al siguiente link: [Deploy en Render](https://proyecto-1-individual-henry-1bsg.onrender.com/)
