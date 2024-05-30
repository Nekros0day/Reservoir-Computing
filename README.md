# Reservoir Computing for the Lorenz System

This repository contains an implementation of a Reservoir Computing (RC) system to predict the Lorenz system's dynamics. The Lorenz system is a set of ordinary differential equations that model atmospheric convection and is known for its chaotic solutions.

## Overview

Reservoir Computing is a type of recurrent neural network (RNN) where only the output weights are trained, making it computationally efficient. This project uses RC to predict the Lorenz system's behavior given initial conditions.

## Files

- `RC.ipynb`: Jupyter notebook containing the implementation of Reservoir Computing for the Lorenz system. It includes data generation, model training, prediction, and error analysis.

## Key Components

### Data Generation

The Lorenz system's equations are defined as:

- dx/dt = sigma * (y - x)
- dy/dt = x * (rho - z) - y
- dz/dt = x * y - beta * z

Where:
- sigma is the Prandtl number.
- rho is the Rayleigh number.
- beta is a geometric factor.

### Reservoir Computer

The reservoir computer consists of:
- **Input Layer**: Maps the input signal to a high-dimensional space.
- **Reservoir Layer**: A fixed, recurrent network of neurons.
- **Output Layer**: Trained to produce the desired output.

### Implementation Details

- **Data Preparation**: Generate training and testing data from the Lorenz system.
- **Training**: Train the reservoir computer using the training data.
- **Prediction**: Use the trained model to predict the Lorenz system's future states.
- **Error Analysis**: Compare the predicted states with the actual states and compute the prediction errors.

## Usage

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/lorenz-reservoir-computing.git
    cd lorenz-reservoir-computing
    ```

2. **Install the necessary dependencies**:
    ```bash
    pip install numpy matplotlib torch
    ```

3. **Run the Jupyter notebook**:
    Open `HW D.ipynb` in Jupyter Notebook or Jupyter Lab and execute the cells to generate data, train the model, and visualize the results.

## Example Output

The notebook will generate plots showing:
- The predicted vs. actual trajectories of the Lorenz system.
- The cumulative prediction error over time.

## Dependencies

- numpy
- matplotlib
- torch

Install the dependencies using:
```bash
pip install numpy matplotlib torch
