# Connectividad
Creación de la base de datos y página de casos contenciosos usando grafos.

## Neo4j
Primero usamos el archivo [contensiosos.json](https://github.com/CharlesAG/Connectividad/blob/main/contensiosos.json) para crear las relaciones entre los casos, y exportar el grafo usando Neo4j, con el notebook [Creación de base de datos con Py2neo](https://github.com/CharlesAG/Connectividad/blob/main/Creaci%C3%B3n%20de%20base%20de%20datos%20con%20Py2neo%20(Neo4j%20for%20Python).ipynb).

`!pip install py2neo`

En cada nodo está guardada la siguiente información:
* **actions:** Acciones tomadas en el caso
* **case_id:** Número correspondiente al id del caso
* **country:** País involucrado 
* **court:** Corte que llevó el caso
* **date_creation**
* **date_modification**
* **date_sentence**
* **doc**
* **doc_type**
* **error**
* **id_**
* **involved_a**
* **involved_b**
* **name**
* **number**
* **pdf**
* **source_doc**
* **source_pdf**
* **title**
* **txt**
* **type_**
* **year**
* **pdf**

Las relaciones se dan de acuerdo a los casos que fueron citados en otros casos, y ésta relación se muestra en el grafo como **Incide**.

Desplegando los primeros nodos en la interfaz gráfica de Neo4j, se visualiza lo siguiente:

![Image of graph database](https://github.com/CharlesAG/Connectividad/blob/main/images/graph1.png)

## HTML

Una vez creada la base de datos, podemos pasar al archivo *Netwrok.html*, el cual hace uso de la librería [neovis.js](https://github.com/neo4j-contrib/neovis.js/) para poder conectar con Neo4j.
Es necesario tener inicializada la base de datos con Neo4j desde la consola, de lo contrario no podrá conectarse.

El archivo [Network.html](https://github.com/CharlesAG/Connectividad/blob/main/Network.html) crea una página que despliega una lista con los países que contiene el grafo, se selecciona el país deseado y se oprime el botón **Dibujar** paradesplegar el grafo correspondiente a los casos con ese país involucrado.

El siguiente es un ejemplo del resultado:

![Ejemplo Network.html](https://github.com/CharlesAG/Connectividad/blob/main/images/Ejemplo%20Per%C3%BA.png)

