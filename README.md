# E-bike
Linear programming model that strategically place E-Bike charging stations to ensure full coverage of the entire cycle path, while minimizing installation costs and considering the bikes’ autonomy.

The concept behind the placement of the charging stations is that since the charging operations require a non negligible time, these should be positioned in places where alternative activities could be carried out, as restaurants, museums, swimming pool, or other amenities. These places, called Points of Interest (POI) are not on the main trajectory of the cyclepath, but the bikers must deviate to reach them.

To support the formulation we make use of a graph with  2n+2  nodes. Nodes  s  and  t  represent the extremes of the cyclepath.

![download](https://github.com/user-attachments/assets/930ca52b-61d9-44a3-8a19-fb949faff6c1)
