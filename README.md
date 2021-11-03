# ComputationalIntelligence_TSPoptimization
TSP optimization using the Ant Colony optimization algorithm.

## Example
This example shows an initial random solution with its cost, and the final solution after we have applied the optimization.
```python
solution = np.array(range(NUM_CITIES))
np.random.shuffle(solution)
solution_cost = problem.evaluate_solution(solution)
problem.plot(solution)

dm = problem.distance_matrix(solution)
optimizer = AntColonyOptimizer(ants=100, evaporation_rate=.1, intensification=2, alpha=1, beta=1, choose_best=0.1)
 
solution = optimizer.fit(dm, iterations=1000)
problem.plot(np.array(solution))
```
### Before the Ant Colony optimization

### After the Ant Colony optimization

## References:
https://en.wikipedia.org/wiki/Ant_colony_optimization_algorithms
https://www.researchgate.net/publication/3418512_Gambardella_LM_Ant_Colony_System_A_cooperative_learning_approach_to_the_Traveling_Salesman_Problem_IEEE_Tr_Evol_Comp_1_53-66
https://www.researchgate.net/publication/5589170_Ant_System_Optimization_by_a_colony_of_cooperating_agents_IEEE_Trans_Syst_Man_Cybernetics_-_Part_B
