# GENETIC ALGORITHMS
Genetic Algorithms are based on simple core idea taken from Nature's process of evolution,"The Survival of the Fittest".
## MAZE_SOLVER_GENETIC_ALGORITHM
This project implements a genetic algorithm to solve a maze represented as a 2D grid.
## Project Implementation and Code Explanation

### Customizable Parameters
- Length of an individual
- Length of Population
- Selector Function
- Mutation function & mutation probability of each gene
- Number of generations
#### Defining the maze 
- Defining the maze as a 2-D matrix of 0's and 1's where 0's represent empty spaces and 1's are the walls
- The start point is (0,0) which is at top left corner and end point is (len(maze)-1,len(maze[0])-1)
#### Genetic Algorithm setup
- We basically creates 2 classes "FitnessMin" (inherited from base.Fitness) and "Individual" whcih is of type 'list'.
- We basically put all functions : attr_direction,individual and population, whcih will be used in the toolbox.
- We define evaluate function which will be used to compute fitness score of each individual.
- For the solutions that successfully reach the endpoint, simply return the number of steps taken as the score.
- For solutions that fail to reach the endpoint, consider returning a score that is 100 plus the Manhattan distance from the point where they hit the wall or got stuck to the endpoint.
- Since, the number of moves in an individual i.e. the length of an individual is 100 so worst number of moves to reach the endpoint=100 so we can use 100 as a baseline.
- We define custom-mutate function which will mutate some of the genes/ moves of the given individual by 20%.
- We use 'TOURNAMNET SELECTION' as a selection strategy where each chancee of each individual getting picked is 50%.
- We define plot_path function to visulaize the maze, start point and the end point and path taken by the best-individual of a particular Generation.
#### Running of Genetic Algorithm 
- We run the GA for 2000 generations and population size=50. We define best_individuals which will store the list of the best individual of a particular generation and run_ga function will also plot the path taken by the best individual of a particular generation represented by blue dots.

  

