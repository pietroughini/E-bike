# E-bike
Linear programming model that strategically place E-Bike charging stations to ensure full coverage of the entire cycle path, while minimizing installation costs and considering the bikes’ autonomy.

Although the linear optimization solution has been applied to a specific case study, characterized by an arbitrary selection of POI positions, number of POIs, energy consumption between consecutive nodes and deviations, maximum energy consumption between consecutive charging stations, and the cost of installing a charging station at each site, the framework can be easily adapted to any type of available data. Furthermore, additional interesting constraints can be incorporated into the problem. For instance, a hierarchical order of preference between the POIs could be introduced as a new practical constraint, in order to better meet the needs of travelers.

The concept behind the placement of the charging stations is that since the charging operations require a non negligible time, these should be positioned in places where alternative activities could be carried out, as restaurants, museums, swimming pool, or other amenities. These places, called Points of Interest (POI) are not on the main trajectory of the cyclepath, but the bikers must deviate to reach them.

To support the formulation we make use of a graph with  2n+2  nodes. Nodes  s  and  t  represent the extremes of the cyclepath.

![download](https://github.com/user-attachments/assets/930ca52b-61d9-44a3-8a19-fb949faff6c1)

Considering a biker that traverses the cyclepath from  s  to  t , the model determines in which nodes to install the charging stations so that the maximum energy consumption between two consecutive charging stations is no more than  "delta"  and minimizes the overall cost.
The code returns the total installation cost and plots a graph with the optimal solution Highlighted.

In the case of the image above: 

![download](https://github.com/user-attachments/assets/d4aa7609-4e5d-41ce-98f6-9ec06b02a558)



