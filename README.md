# Automatización del scrapeo de webs de segunda mano, comparación de precios y aviso por Telegram

##Scrapeo

Para el scrapeo de las paginas web se ha empleado Beautiful Soup version 4.11.0, que es una libreria de Python que traduce HTML y XML de la pagina web o de archivos para su posterior uso. En este caso para obtener 11 caracteristicas de los coches, como marca, modelo, potencia, combustible y kilometros. 

##ML

Para la comparación y predicción de precios se ha usado se ha empleado RandomForestRegressor, que es una herramienta para predecir un valor mediante la introducción de muestras de la en arboles de decisión para obtener un valor basado en los promedios y así evitar la sobreestimación del modelo. 

Una vez se ha conseguido ajustar el modelo para que prediga un precio en función de 11 caracteristicas se guarda con la herramienta pickle y no tener que reentrenarlo, con el objetivo de ejecutarlo diariamente para obtener una lista de coches que tengan un precio por debajo de mercado.

##Telegram 

Con la libreria de Python Telegram_send 0.34 se manda a traves de un bot los resultados diarios.

##Datos 

De un proyecto de Kaggle que recopila precios de coches de diferentes webs de segunda mano, junto con los datos obtenidos en sucesivos scrapeos es el conjunto de datos empleado para el entremaniento del modelo. https://www.kaggle.com/datasets/datamarket/venta-de-coches
