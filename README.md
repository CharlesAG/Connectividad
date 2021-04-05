# Connectividad
Creación de la base de datos y página de casos contenciosos usando grafos.

## Neo4j
Primero usamos el archivo contensiosos.json para crear las relaciones entre los casos, y exportar el grafo en la plataforma Neo4j, usando el notebook.
En cada nodo está guardada la siguiente información:
* **actions:** Acciones tomadas en el caso
* **case_id:** Número correspondiente al id del caso
* **country:** País involucrado 

Desplegando los primeros nodos en lainterfaz gráfica de Neo4j, se visualiza lo siguiente:

![Image of graph database](https://github.com/CharlesAG/Connectividad/blob/main/images/graph1.png)
