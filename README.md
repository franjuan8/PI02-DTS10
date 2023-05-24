# PI02-DTS10-DataAnalyst-Henry
Proyecto Individual Numero 2 del bootcamp soy Henry
# Contexto
La Organización de Aviación Civil Internacional (OACI), organismo de la Organización de las Naciones Unidas, quiere investigar en profundidad los accidentes producidos desde inicios del siglo XX. Para ello, les solicita la elaboración de un informe y un dashboard interactivo que recopile tal información.

La OACI únicamente cuenta con un dataset sobre datos de accidentes de aviones, pero insta a la consultora de datos -de la que forman parte- que intente cruzar esta información con otras fuentes de su interés. Esto con el objetivo de obtener mayor claridad y consistencia en los fundamentos del estudio.

# Propuesta de trabajo
A raíz de esta solicitud, nuestro Project Manager nos encarga una serie de tareas a cumplir:

Realizar un EDA con el dataset provisto, junto con un reporte de calidad y diccionario de datos
Buscar y relacionar información relevante con los eventos
Crear una base de datos en un motor SQL e ingestar el csv procesado
Elaborar un dashboard e idear un storytelling con el objetivo de presentarlo ante la OACI
Adjuntar todo el trabajo en un repositorio de GitHub
Stack tecnológico:

* Python: EDA + transformaciones + KPI
* Power BI -preferentemente- o Streamlit: dashboard
* GitHub: con un README.md donde se elabore el informe
* A modo de resumen, se espera que puedan realizar un primer acercamiento al dataset con Python. Allí, crearán un notebook que contendrá un análisis exploratorio y realizarán las transformaciones y el preprocesamiento que consideren pertinentes. Esta etapa debe estar oportunamente documentada y con los comentarios necesarios. Recuerden que Python brinda un recurso muy valioso para este fin -celdas markdown-.

En una instancia posterior, tendrán que ingestar el dataset en un motor SQL de su preferencia. Finalmente, la herramienta de visualización empleada debe conectarse y tomar los datos desde ese motor.
# Pasos que Utilice para Realizar el Proyecto
1)Importamos las tablas en python.  
2)Realizamos un proceso de ETL a las tablas para arreglar ciertas columnas como las de Date y Time las cuales estaban en un formato un tanto extraño. 
Para normalizar los datos de estas dos columnas creamos dos funciones distintas para que en la columna date queden con el formato dia/mes/año y en la columna Timequeden con un formato Hora/Minutos/Segundos.    
   
3)Despues de eso creamos un dashboard con los datos mas relevantes de la tabla de accidentes de aviones. Para esto considere necesario crear una columna nueva desde power query llamada "Porcentaje Muertes" y "Porcentaje Muertes Crew". Estas dos columnas calculan del total de pasajeros y tripulantes que tenia cada uno de los aviones al partir, cual fue el porcentaje de estos que salieron vivos y cuantos murieron. Considere que esto era mejor para analizar los valores de las tablas a que simplemente calcular la cantidad de muertes con la columna Fatalities ya que no es lo mismo calcular las muertes de un vuelo que tiene 300 pasajeros a un vuelo en el que solo hay 2 pasajeros. Por esta razon me parecio que una buena forma de normalizar los valores para calcularlos de una manera optima era esta, la de incorporar la columna de Porcentaje de muerte.   
La diferencia entre la columna "Porcentaje Muerte" y "Porcentaje Muerte Crew" es que la columna "Porcentaje Muertes" muestra el porcentaje de muertes generales del avion, en cambio la de "Porcentaje Muertes Crew" incluye solamente el porcentaje de muerte de la tripulacion del avion, es decir los trabajadores, incluyendo pilotos/copilotos y asafatas.   
6) Luego realizamos todos los pasos anteriores con otra tabla la cual es una tabla de terrorismo de los ultimos años y creamos un dashboard con esta.   
