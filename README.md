# E-bike
Linear programming model that strategically place E-Bike charging stations to ensure full coverage of the entire cycle path, while minimizing installation costs and considering the bikes’ autonomy.

The concept behind the placement of the charging stations is that since the charging operations require a non negligible time, these should be positioned in places where alternative activities could be carried out, as restaurants, museums, swimming pool, or other amenities. These places, called Points of Interest (POI) are not on the main trajectory of the cyclepath, but the bikers must deviate to reach them.

To support the formulation we make use of a graph with  2n+2  nodes. Nodes  s  and  t  represent the extremes of the cyclepath.

![download](https://github.com/user-attachments/assets/930ca52b-61d9-44a3-8a19-fb949faff6c1)

Considering a biker that traverses the cyclepath from  s  to  t , the model determines in which nodes to install the charging stations so that the maximum energy consumption between two consecutive charging stations is no more than  "delta"  and minimizes the overall cost.
The code returns the total installation cost and plots a graph with the optimal solution Highlighted.

In the case of the image above: 

![download](https://github.com/user-attachments/assets/d4aa7609-4e5d-41ce-98f6-9ec06b02a558)

Although the linear optimization solution has been applied to a specific case study, characterized by an arbitrary selection of POI positions, number of POIs, energy consumption between consecutive nodes and deviations, maximum energy consumption between consecutive charging stations, and the cost of installing a charging station at each site, the framework can be easily adapted to any type of available data. Furthermore, additional interesting constraints can be incorporated into the problem. For instance, a hierarchical order of preference between the POIs could be introduced as a new practical constraint, in order to better meet the needs of travelers.

s and t, as said before, are the dynamic extremes of the path for which we want to find the optimal solution. These can be modified to test the model on different paths, and furthermore, nodes can be added/removed, consumption and installation costs can be adjusted directly from the data shown below, and the code will continue to return the optimal solution.

```python
#data PROBLEM 

n = 15  # number of nodes on the main course
n1 = 15 #number of touristic sites
delta = 50  # max distance before recharge
s = 0  # starting point
t = n + 1  # destination
consumption = [20, 32, 11, 37, 7, 14, 22, 5, 35, 17, 23, 3, 26, 24] # consumption (in Wh) between two consecutive location along the main course
consumption_deviation = [1.1, 0.7, 0.4, 0.9, 2.1, 1.8, 0.5, 0.4, 1.6, 2.5, 1.4, 0.8, 2.0, 1.3, 0.1] # consumption (in Wh) of the deviation
inst_cost = [1492, 1789, 1914, 1861, 1348, 1769, 1123, 1432, 1564, 1818, 1901, 1265, 1642, 1712, 1756] #cost (in €) of installation of a charging point related to the node
```



