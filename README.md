# Edmund_Karp_Algorithm
*****************************************************************************************************************************
The Edmonds-Karp algorithm is a modified form of the Ford-Fulkerson algorithm. 
The difference Is that Ford-Fulkerson uses the DFS approach and Edmonds-Karp uses the BFS approach.
The time complexity of this algorithm Is O(E^2) for irrational capacities and maximum longest path from source to sink.
*****************************************************************************************************************************
Algorithm:
def bfs(arr, dp, source, sink):
  q = [source]
paths = {
  source: []
}
if source == sink:
  return paths[source]
while queue:
  u = queue.pop(0)
for neigh in range(len(arr)):
  if arr[u][neigh] - dp[u][neigh] > 0 and neigh not in paths:
  paths[neigh] = paths[u] + [(u, neigh)]
print(paths)
if neigh == sink:
  return paths[neigh]
q.append(neigh)
return
def max_flow(arr, source, sink):
  n = len(arr)
dp = [[0] * n
  for i in range(n)]
path = bfs(arr, dp, source, sink)
while path != None:
  flow = min(arr[u][v] - dp[u][v]
    for u, v in path)
for u, v in path:
  dp[u][v] += flow
dp[u][v] -= flow
path = bfs(arr, dp, source sink)
return sum(dp[source][i]
  for i in range(n))
**************************************************************************************************************************************
The time complexity of the Edmonds-Karp algorithm is O(VE^2) and space complexity is O(E+V), where E and V are the edges and vertices.
**************************************************************************************************************************************
  
  
