All of the algorithms and results are explained in the report, this README explains the content of the different files and how to use them.

## Code

All the functions are written in the jupyter notebook 'Graph Drawing Challenge.ipynb'.   
All the necessary libraries are imported in the first cell, especially tkinter for graph visualization, networkx to manipulate graphs, collections for queues, and more standard libraries such as numpy.   
  
The main functions are :  
- best_tutte_embedding (returns the planar drawing and outer face after applying tutte)
- find_planar_drawing (returns the networkx planar drawing)
- iterate (returns the graph after applying 500 random switches)
- apply_force_step (returns the graph after simulating a spring force on the nodes)
- split_min_edge (returns the graph with one more bend on the shortest edge which is allowed one more bend)
- find_best_ratio (tests all the configuration and returns the best instance with the best ratio)
  
Before these functions are written some auxiliary functions.  
After these functions are written a couple of cells aimed at visualizing graphs.  

## Inputs and outputs

The input graphs are located in 'datasets/json', the output solutions found with find_best_ratio are located in 'ouputs/json'. For each input file, there are 3 output files, one with the best version using tutte embedding (starting by 'tutte_'), one with the best version using the networkx embedding (starting by 'nx_'), and the final solution.   
There is also a file called 'image' in the 'outputs' were you can see the final result for each input graph.  

## Results

In the 'results' file, there is a document with all the time and ratio performances of each input. For both tutte embedding and networkx embedding, we saved the ratio and the time it took to compute 9 different configurations.   
  
init : initial embedding with nothing applied.  
1a : only add bends on shortest edges.  
1b : bends + simulate spring force.  
2a : only simulate spring force.  
2b : spring force + bends.  
Xbis : X + approximate integer coordinates and simulate 500 random switches.  
Some cases are empty, which means the ratio could not be computed because of unvalid instance. Some are not empty because the ratio could be computed, but they might still be unvalid solutions and not be kept as final solutions.   
  
Then the final ratio and corresponding configuration are written at the end.   
