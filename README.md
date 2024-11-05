# Travelling_Salesman_Problem
Travelling Salesman Problem (TSP) is a classic problem in optimization and computer science. Imagine a salesman who needs to visit a list of cities, starting and ending at the same city. The challenge is to find the shortest possible route that allows the salesman to visit each city exactly once and return to the starting point.

# Overview
The Travelling Salesman Problem (TSP) is a well-known problem in the field of computer science and mathematics. In essence, it involves finding the shortest possible route for a salesman to take in order to visit a given set of cities, each exactly once, and then return to the starting city. The goal is to minimize the total distance traveled or the cost incurred

# Components
The Travelling Salesman Problem (TSP) has several key components that make it an interesting and challenging problem in optimization and computer science:

1.Cities (Nodes): These represent the locations that the salesman needs to visit.

2.Distances (Weights): The cost or distance associated with traveling from one city to another. This can be represented in a distance matrix or graph with weighted edges.

3.Tour (Path): The route that the salesman takes to visit each city exactly once and returns to the starting city. This is a permutation of the cities.

4.Objective Function: The function that needs to be minimized. In TSP, this is typically the total travel distance or cost of the tour.

5.Constraints:
The salesman must visit each city exactly once.
The tour must start and end at the same city.

6.Optimization Methods: Techniques used to find the shortest possible tour. These can include exact algorithms like brute force and dynamic programming, as well as heuristic and metaheuristic algorithms like Genetic Algorithms, Simulated Annealing, and Ant Colony Optimization.

# How to Run

Make sure you have Python installed on your machine.

Install the required libraries using 
                    
    pip install numpy 
    
    pip install matplotlib

Run the script using python **filename.py**, replacing **filename.py** with the actual name of your Python script.

# Example parameters
    num_cities = 10
    num_routes = 50
    num_generations = 500

    # Randomly generate city coordinates and calculate the distance matrix
    cities = np.random.rand(num_cities, 2)
    distance_matrix = np.linalg.norm(cities[:, np.newaxis, :] - cities, axis=2)

    # Generate an initial population of routes
    population = generate_population(num_routes, num_cities)

    # Evolve the population to find the best route
    best_route = evolve(population, distance_matrix, num_generations)

    # Print results
    print("Best route:", best_route)
    print("Total distance:", calculate_total_distance(best_route, distance_matrix))

# Acknowledgments

Inspired by the **Genetic Algorithm** and its application to combinatorial optimization problems.

The NumPy and Matplotlib libraries were instrumental in the implementation.
