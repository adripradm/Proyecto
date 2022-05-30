# Automatización del scrapeo de webs de segunda mano, comparación de precios y aviso por Telegram

## Scrapeo

Para el scrapeo de las paginas web se ha empleado Beautiful Soup version 4.11.0, que es una libreria de Python que traduce HTML y XML de la pagina web o de archivos para su posterior uso. En este caso para obtener 11 caracteristicas de los coches, como marca, modelo, potencia, combustible y kilometros. 

## ML

Para la comparación y predicción de precios se ha usado se ha empleado RandomForestRegressor, que es una herramienta de la libreria de Python sklearn.ensemble para predecir un valor mediante la introducción de muestras en arboles de decisión para obtener un valor basado en los promedios y así evitar la sobreestimación del modelo. 

Una vez se ha conseguido ajustar el modelo para que prediga un precio en función de 11 caracteristicas se guarda con la herramienta pickle y no tener que reentrenarlo, con el objetivo de ejecutarlo diariamente para obtener una lista de coches que tengan un precio por debajo de mercado.

## Telegram 

Con la libreria de Python Telegram-send 0.34 se manda a traves de un bot los resultados diarios.

## Datos 

De un proyecto de Kaggle que recopila precios de coches de diferentes webs de segunda mano, junto con los datos obtenidos en sucesivos scrapeos es el conjunto de datos empleado para el entremaniento del modelo. https://www.kaggle.com/datasets/datamarket/venta-de-coches

## Proceso

El proyecto consiste en la comparación diaria de precios de coches, de momento funciona con coches. com y con autoscout24. Ante los problemas que tuve para scrapear coches . net tuve que aplazarlo. Pero el proyecto consiste en ir apmpliando el numero de webs, wallapop podría ser una muy buena web para obtener buenas ofertas ya que hay mayor porcentaje de vendedores particulares. Pero al no requerir rellenar todos los campos el modelo actual de Machine Learning no funciona correctamente con menos caracteristicas y no se obtiene un resultado satisfactorio, por lo que habrá que trabajar con diferentes modelos para encontrar uno que se pueda ajustar a las condiciones.

