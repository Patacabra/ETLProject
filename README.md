
# ETL PROJECT

Este es un proyecto de ETL donde se van a utilizar datos de los incendios forestales ocurridos en España desde 2001 a 2015.
Junto con información meteorológica obtenida a través de AEMET.



## Apéndice

1. Fuentes de información.

2. Proceso de extracción de los datos.

3. Limpieza.

4. Conclusiones.

5. Exportación a SQL.


## Fuentes de información.

[Archivo '.csv' sobre incendios forestales de España](https://datos.civio.es/dataset/todos-los-incendios-forestales/)

[API AEMET](https://opendata.aemet.es/dist/index.html?#/valores-climatologicos/Climatolog%C3%ADas%20diarias._1)

[Código de identificación de provincias](https://www.ine.es/daco/daco42/codmun/cod_provincia.htm)

[Archivo '.csv' sobre calentamiento global por países](https://www.kaggle.com/datasets/berkeleyearth/climate-change-earth-surface-temperature-data?resource=download&select=GlobalLandTemperaturesByCountry.csv)


## Proceso de extracción de datos.

Dejando a un lado los archivos '.csv' obtenidos a partir de una base de datos.

La información meteorológica fue extraída a través de Selenium, utilizando el Web Scraping en la API de AEMET.

Se creó un bot que podía obtener los links de los archivos 
'.json' que aportaba la API, la complicación y el uso de Selenium tienen que ver con este proceso ya que la API sólo proporcionaba la información en lapsos de 31 días como máximo y te exigía validar el link (el cual tenía una caducidad de unos minutos) para poder obtener los .json , que posteriormente se exportaron a diferentes archivos '.csv' los cuales se unieron en uno sólo a través de pandas.
## Conclusiones

![](/img/2.jpeg)

![](/img/1.jpeg)

![](/img/3.jpeg)