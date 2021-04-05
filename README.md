# Connectividad
Creación de la base de datos y página de casos contenciosos usando grafos.

## Neo4j
Primero usamos el archivo contensiosos.json para crear las relaciones entre los casos, y exportar el grafo en la plataforma Neo4j, usando el [notebook](https://github.com/CharlesAG/Connectividad/blob/main/Creaci%C3%B3n%20de%20base%20de%20datos%20con%20Py2neo%20(Neo4j%20for%20Python).ipynb).

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

Las relaciones se dan de acuerdo a los casos que se citaron en otros, y ésta relación se muestra en el grafo como **Incide**.

Desplegando los primeros nodos en lainterfaz gráfica de Neo4j, se visualiza lo siguiente:

![Image of graph database](https://github.com/CharlesAG/Connectividad/blob/main/images/graph1.png)
