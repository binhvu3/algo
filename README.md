# Data Strutures and Algorithms
-  <a href="https://www.youtube.com/playlist?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX ">Video lectures from ROBERT SEDGWIG</a>

## Search
![search summary](resource/search_summary.png)

## Undiracted Graphs
- **DFS**: Go Deep down use recursion/stack to check adj node(s). 
- **BFS**: Queue each node and check the adj. Use df {edge (index), edgeTo[] (int), disTo[] (int)}
- **CC (connected components)**: Each cluster into 1 category. Each node in category is connected.

## Directed Graph
- **Strong Component**: digraph that have in and out. Similar to CC.
- **Kosaraju-Sharir**: (1) reverse graph and dfs -> return list of nodes list (2) Use node list to run dfs on og graph
![https://www.youtube.com/watch?v=zFgkK4g65ys&list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&index=40](resource/digraph.png)

## Minimum Spanning Tree (MST)
- Graph with weights -> find the lowest
- Kruskal's: sort weight lowest to highest, go down and add unless it create a cycle
- Prim's: Start at node #0, check node 1 step away, take the lowest usinng Priority Queue (PQ). 
  - Two version (1) Lazy and (2) Eager
- 
### Priority Queue
- Use binary heap as data structure  <a href="https://www.youtube.com/watch?v=AE5I0xACpZs">What is a Binary Heap?</a>

## Shortest Path
- Generic Shortest-path: check from 0-inf and relax any edge.
- <a href="https://youtu.be/_lHSawdgXpI?t=31">What is edge relaxation?</a> Initalize first node w/ 0 and everything else inf. Update/relax edge based on weights.
- <a href="https://youtu.be/_lHSawdgXpI">Dijkstra's algo (non-negative weights)</a>: similar start to Generic, keep track of total distance from root, update path if better weight found. <a href="https://youtu.be/uzHJXbToiIU?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=127">demo</a>
- <a href="test">Topological Sort (no directed cycles)</a>: Find the lowest weight from the choosen node.<a href="https://youtu.be/Qp9zy9qMJzE?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=42">demo</a>
- <a href="https://www.youtube.com/watch?v=obWXjtg0L64">Bellman-Ford (no negative cycle)</a>: Double relaxation w/ v-1 iteration <a href="https://youtu.be/A54rUI6CPSs?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=406">demo</a>

### Application
- <a href="https://youtu.be/_lHSawdgXpI?t=31">Seam Carving</a>: non-linear scaling algorithm that determine the shortest path given the energy
- Parallel job scheduling problem

### Definition
- <a href="https://youtu.be/A54rUI6CPSs?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=182">Negative Cycle</a>: Negative loop that traps shortest path algo
- <a href="https://www.youtube.com/watch?v=9PHkk0UavIM">Differences b/w Dijkstra vs Bellman-Ford</a>

![Shortest path summary](resource/shortest_path.png)