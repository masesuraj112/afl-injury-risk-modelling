# Modelling AFL Injury Risk Over a Full Season

**Python | Stochastic Modelling | Monte Carlo Simulation | Data Analysis**

A stochastic mathematical model developed to investigate how AFL player injury risk changes over a 24-round season.

The model explores whether players with a higher initial injury risk experience a greater reduction in injury risk over a season compared with players starting at a lower injury risk.

## Overview

The model represents an AFL season as a **dynamic, discrete and stochastic system**.

Injury risk is influenced by:

* Training load
* Match intensity
* Recovery time
* Previous injury risk
* Random injury events

The model also compares scenarios **with and without coaching intervention**, where coaches adjust a player's training load and match involvement based on their previous injury risk.

## Modelling Approach

The model uses a logistic function to represent injury risk as a probability between 0 and 1.

Previous-round values are used to calculate the conditions for the current round, allowing injury risk, training load, match intensity and recovery time to evolve throughout the season.

Random variables are incorporated to represent factors outside the player's control, such as unexpected injuries and variation in match and training conditions.

### Monte Carlo Simulation

Each scenario is simulated **1,000 times** to account for the stochastic nature of the model.

Different initial injury-risk values are tested and the resulting injury-risk trajectories are compared across a 24-round season.

## Key Results

The simulations suggested that players with higher initial injury risk generally experienced a greater reduction in injury risk over the simulated season than players with lower initial injury risk.

This pattern was observed both when coaching intervention was included and when it was removed.

The results also demonstrated the variability produced by the stochastic components of the model, with individual simulations producing different injury-risk trajectories despite identical starting parameters.

## Model Limitations

The model simplifies several aspects of AFL:

* Players are assumed to participate throughout the 24-round season.
* Match conditions are not explicitly varied between rounds.
* Player selection and reserve-grade matches are not modelled.
* Training and recovery inputs are simplified representations of real-world behaviour.
* The model is not intended to make real-world predictions about individual player injuries.

These limitations provide opportunities for future extensions of the model.

## Technologies

* Python
* NumPy
* Pandas
* Matplotlib
* Jupyter Notebook

## Repository Contents

`afl_injury_risk_model.ipynb` contains:

* Mathematical model implementation
* Season simulation functions
* Coaching intervention scenarios
* 1,000-run Monte Carlo simulations
* Data analysis
* Visualisations
* Discussion of model limitations and results

## Setup

### Requirements

* Python 3.9 or later
* Jupyter Notebook or JupyterLab

### Install Dependencies

Clone the repository and install the required Python libraries:

```bash
pip install numpy pandas matplotlib jupyter
```

The project uses the following libraries:

| Library    | Purpose                                         |
| ---------- | ----------------------------------------------- |
| NumPy      | Numerical calculations and array operations     |
| Pandas     | Data analysis and displaying simulation results |
| Matplotlib | Plotting simulation results                     |
| Jupyter    | Running the `.ipynb` notebook                   |

The `random` library is part of Python's standard library and does not need to be installed separately.

### Running the Project

1. Clone the repository.
2. Install the required dependencies using the command above.
3. Start Jupyter Notebook:

```bash
jupyter notebook
```

4. Open `afl_injury_risk_model.ipynb`.
5. Run the notebook cells from top to bottom.

The notebook will run the AFL injury-risk simulations and generate the corresponding tables and visualisations.


## Future Extensions

Potential extensions include modelling:

* Player selection and reserve-grade matches
* Varying match conditions throughout a season
* Different player fitness profiles
* More realistic training and recovery patterns
* Additional injury mechanisms

## Disclaimer

This is an academic modelling project and is not intended to predict real-world AFL injuries or provide medical advice.
