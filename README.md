# hilaga-pathfinder
An agent-based AI program for the fulfillment of CSCI 111 requirements under sir Francis Bautista and Dr. Andrei Coronel by Gabriel Mercado, Franz Tarbolupa, and Joshua Son	

# User Manual

## How to Install the Game
Download the source code ```hilaga_pathfinder.py``` from this repo and open it on Jupyter Notebook, VS Code, Google Colab or any Python interface.

## How to Run the Game
### Local Environment
1. Using the command prompt, navigate to the folder the file is located then run ```python hilaga_pathfinder.py```

### Google Colab
1. Run all the cells in the notebook to set up all the variables and functions of the game
2. To start, run the last cell ```start_screen ( )```

### Game Flow

1. The game will first enumerate all the locations in the game, as these would be choices for the first prompt.
2. The first prompt **“What building are you in right now?”** will ask for input for your starting location. Type your location on the box next to the prompt.
*Note that if you choose CTC in the first prompt, the game will end as it is the set end-state*
3. The next prompt **“How would you like to traverse to CTC? (D for DFS, B for BFS, M for Minimum)”** will allow the user to choose the traversal method.
4. The game will then proceed to find and show the best path it has taken to reach CTC as well as tell you how many steps it took to get there. A step here is defined as movement from building to building.
5. Once it has reached CTC, it would prompt: **“Thank you for using Hilaga! Would you like to start again? (Y/N):”** Should you wish to play again, press ```Y```, should you wish to end the program, press ```N```.

# Technical Documentation

* **[Stack]** The programming language used was Python, with Google Colab and Github as the team’s Version Control Systems.
* **[Strategies]** The program employs the use of FOR loops which nested IF and ELSE statements to determine the optimal route to get to CTC from the location given. The program has two options of traversal: Breadth-First Search and Depth First Search. Depending on what the user chooses, the program will search for the best route using that search. 
* **[Heuristics Implemented]** We have implemented the weights of the edges corresponding to the “distance” and “stamina”; however, due to time constraints we have decided to drop the agent’s stamina limit. We have implemented at best the agent’s ability to find the best path possible that takes into account the weight of the edges i.e., the distance between one place to another. This was implemented with the use of loops and dictionaries to find the minimum weight and save it as the best path then move on from there until it reaches CTC. 

