# Data Strutures and Algorithms
- Video lectures from ROBERT SEDGWIG
- https://www.youtube.com/playlist?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX 

## Search
![img.png](resource/search_summary.png)


## Data Types
### Undiracted Graphs
- **DFS**: Go Deep down use recursion/stack to check adj node(s). 
- **BFS**: Queue each node and check the adj. Use df {edge (index), edgeTo[] (int), disTo[] (int)}
- **CC (connected components)**: Each cluster into 1 category. Each node in category is connected.

### Directed Graph
- **Strong Component**: digraph that have in and out. Similar to CC.
- **Kosaraju-Sharir**: (1) reverse graph and dfs -> return list of nodes list (2) Use node list to run dfs on og graph
![https://www.youtube.com/watch?v=zFgkK4g65ys&list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&index=40](resource/digraph.png)