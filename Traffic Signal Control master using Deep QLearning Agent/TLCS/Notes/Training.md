# **Traffic Signal Control master using Deep QLearning Agent**

This script is the main entry point for training the reinforcement learning agent for traffic signal control. Here's a step-by-step explanation of its components:

**Import Statements:** The script imports necessary modules and packages for running the training simulation.

**Configuration and Paths:** The import_train_configuration function reads configuration settings from the training_settings.ini file. The set_sumo function configures the SUMO simulation settings, and the set_train_path function sets the path to save trained models and visualizations.

**Creating Objects:**
TrainModel: Creates an instance of the TrainModel class, which is responsible for building and training the neural network model.
Memory: Creates an instance of the Memory class, which stores the agent's experiences for replay during training.
TrafficGenerator: Creates an instance of the TrafficGenerator class, which generates traffic scenarios for each episode.
Visualization: Creates an instance of the Visualization class, which handles visualization-related tasks.
Simulation: Creates an instance of the Simulation class, which orchestrates the entire training process.

**Training Loop:**
A while loop runs for the specified number of episodes in the configuration (total_episodes).
For each episode:
The epsilon value for epsilon-greedy policy is calculated based on the episode number.
The run method of the Simulation class is called to perform the simulation and training for the current episode. The episode number and epsilon are passed as arguments.
The simulation time, training time, and total time for each episode are printed.

**Saving Data and Models:**
After all episodes are completed:
The start and end times of the training session are printed.
The trained model is saved to the specified path using the save_model method of the TrainModel instance.
The training_settings.ini file is copied to the training path for reference.
The cumulative negative reward, delay, and queue length data are saved and plotted using the save_data_and_plot method of the Visualization instance.
This script essentially sets up the training environment, runs training episodes, and saves relevant data and models for analysis and further use.

  Here's a brief description of each of the files:

1) generator.py: This file likely contains the implementation of the TrafficGenerator class, responsible for generating the route file for simulating traffic in SUMO.

2) memory.py: This file likely contains the implementation of the Memory class, used for storing and managing the experiences (samples) of the agent during training.

3) model.py: This file likely contains the implementation of the TrainModel and TestModel classes, which define the neural network models used for training and testing the reinforcement learning agent.

4) testing_main.py: This file likely contains the main code for testing the trained agent's performance in the simulated environment.

5) testing_settings.ini: This is a configuration file that likely contains settings and parameters for testing the agent.

6) testing_simulation.py: This file likely contains the implementation of the Simulation class used for testing the agent's performance in the simulated environment.

7) training_main.py: This file likely contains the main code for training the reinforcement learning agent.

8) training_settings.ini: This is a configuration file that likely contains settings and parameters for training the agent.

9) training_simulation.py: This file likely contains the implementation of the Simulation class used for training the agent in the simulated environment.

10) utils.py: This file likely contains utility functions or helper functions used throughout the project.

11) visualization.py: This file likely contains the implementation of the Visualization class used for visualizing and saving data and plots related to the training and testing process.



