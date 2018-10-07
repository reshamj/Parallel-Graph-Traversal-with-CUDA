# Parallel-Graph-Traversal-with-CUDA
Parallel Graph Traversal with CUDA


 Performing bidirectional BFS using CUDA 
 
Pseudocode for BFS algorithm on CUDA:
Function Kernel (graph_nodes, graph_edges, graph_frontier, updating graph frontier, graph_visited, cost, no_of_nodes):
// Instantiate tid object to keep track of IDs for threads and blocks
If (tid is less than the total number of nodes) then 
 	visited[x] = true; // visit node x based on id 
	// forward 
	For ( loop from starting node to ending node) 
		// Instantiate id object to keep track of edges by id index
		If ( nodes in specified graph has not been visited based on id)
			Increment and update cost[id] based on cost[tid]
			Updating graph frontier based on id
		End
	End
	// backward 
	For ( loop from ending node to starting node ) 
		// Instantiate id object to keep track of edges by id index
		If ( nodes in specified graph has not been visited based on id)
			Increment and update cost[id] based on cost[tid]
			Updating graph frontier based on id
		End
	End
End


Commands to execute BFS (Breadth First Search) algorithm/program:


Compile the program to obtain executable:
nvcc bfsearch.cu


Run BFS for  data:
		./a.out file_name.txt
     


