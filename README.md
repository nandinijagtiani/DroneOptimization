Drone Delivery Route Optimization - Project Specification
By: Sam Jenkins, Nandini Jagtiani

1. What is the issue being addressed?

The problem being addressed is the optimization of energy consumption for drones in a commercial delivery system. With the increasing use of drones for package delivery by companies such as Amazon, it is crucial to minimize the operational costs and flight time while maximizing delivery efficiency and meeting demand. The goal is to find the most efficient routes for drones to deliver packages, ensuring they cover the necessary locations while minimizing energy consumption and respecting constraints such as no-fly zones, and payload limits.

The main issue is designing delivery routes that are both computationally efficient and practically feasible, taking into account both the technical limitations of drones such as battery life and payload capacity and external constraints (s.t., airspace restrictions, weather conditions).

2. Where does the data come from and how will it be obtained?

Two primary data sources will be used:
Synthetic Data: we will generate a synthetic dataset including predefined delivery locations, charging locations, drone starting points, customer demand around Madison, and payload data (weight, and items).

Public Data: we will use publicly available datasets for real-world locations. This data will be sourced from the open Google Map API. We will also research battery life and payload capacity of Amazon Drones to use as our parameters for the main constraints.

Depending on the problem's complexity, we may focus on a small city or delivery region with a limited number of drones to start with, and later scale to larger regions. Our current objective is to focus on the city of Madison, with the Amazon drone delivering packages from our lovely campus to the other side of lake Mendota, and maybe stop at a “cargo” ship along the way.

3. What is the optimization problem underlying this project?
The optimization problem involves designing optimal routes for drones under various constraints. The main objectives are:
Minimize the total energy consumption: The goal is to minimize the total energy consumption for all drones to deliver packages to the designated locations.

Subject to the following constraints
Ensure demand is met by the end of the day: Since one of Amazon’s core values is customer service the drones MUST meet customer demand by the end of the business day. They will do this by finding the most efficient routes through the city of Madison.

Respecting no-fly zones and obstacles: The routes must avoid restricted airspace and obstacles (such as buildings, towers, or other flight hazards).

Payload constraints: Each drone has a payload limit, so the number of deliveries assigned to each drone must be carefully managed.
The problem can be formulated as a Vehicle Routing Problem with additional constraints related to drone-specific limitations.

In summary, the goal is to solve an optimization problem where we minimize energy consumption while ensuring the drones deliver the packages in compliance with the aforementioned constraints.

Potential Sub-problems:
Capacity constraints: Each drone can carry a limited number of packages or weight, but must meet demand.

Battery constraints: Drones have a finite range based on battery capacity and must return to charging sites periodically.

4. What are the deliverables?

Visualization: A final visualization (using Matplotlib or Geopandas) to display the drone routes on maps, illustrating the optimized flight paths and how drones meet delivery efficiently

Report: A final report detailing the model formulation, solution methods, results, and any challenges faced during the project. The report will also include a comparison of different optimization methods based on performance.

5. Other points to consider when evaluating.
Computational Complexity: The optimization problem could be expensive, especially when considering multiple drones and complex real-world constraints. A key consideration will be how to balance between solution quality and computation time.

