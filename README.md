# TP Lab 11
Team:
- Chandler Guzman
- Summer Smith
<br><br>

# Video
https://github.com/user-attachments/assets/85c02770-bfbe-4a50-ac44-f2e06c6c0057

<br>

# Reflection
> <i>How does each pathfinding algorithm calculate and prioritize paths?</i><br>
<p>
  BFS dives headfirst into a path even if it's not the most optimal. As long as it progresses toward the goal, it will continue until it can't anymore, then backtrack and find another route to continue down. <br>
  A* calculates a "cost" for each node based on the current and ending positions. It calculates the approximate remaining distance to the goal and chooses a path based on which is the least costly. <br>
  Dijkstra's explores every possible route one could take and scores each route, then ultimately returns the shortest path. 
</p>
<br>

> <i>What challenges arise when dynamically updating obstacles in real-time?</i><br>
<p>
  Constant path recalculation can lead to performance issues depending on the algorithm being used (Dijkstra's being the worst offender). If you choose to only calculate during the initial trigger state, however, you risk a higher chance of pathfinding failure.
</p>
<br>

> <i>Which algorithm should you choose and how should you adapt it for larger grids or open-world settings?</i><br>
<p>
  The algorithm used depends on the use case. If you wanted to pick one based on simplicity and performance alone, you'd want to use BFS because it's usually the most performant. However, BFS won't work if certain areas have weights, it can be unpredictable because it doesn't stop until it has to backtrack, and it doesn't always pick the best path. The second-best option would be A*, but you have to ensure that it's calculating a smaller portion of the large grid and would want to make sure that there aren't too many agents pathfinding simultaneously. If you wanted to use a more advanced pathfinding algorithm, you would either use Jump Point Search or Hierarchical Pathfinding depending on the uniformity and complexity of the map.
</p>
<br>

><i>What would your approach be if you were to add weighted cells (e.g., "difficult terrain" areas)?</i><br>
<p>
  For cells with "weights" or scores, you would want to use a pathfinding algorithm that complements that system. You would not want to use BFS, for example, because this algorithm is best used for traversing unweighted graphs. The best approach would be to use A* only because it's a more performant version of Dijkstra's.
</p>
