# COVID-19 Agent-Based Simulation Model

An agent-based simulation model implemented in Python to study and analyze the spread of COVID-19, incorporating various factors such as asymptomatic transmission, social networks, and government interventions.

## Overview

This project implements an Agent-Based Model (ABM) to simulate the spread of COVID-19 within a population. The simulation is designed to capture the complex dynamics of disease transmission while considering various real-world factors that influence the spread of the virus.

Key aspects of our simulation include:
- Modeling of individual behaviors and interactions
- Implementation of different health states (susceptible, infected, recovered)
- Integration of government intervention effects
- Analysis of transmission patterns and outbreak dynamics

## Background

COVID-19 presents unique challenges for disease modeling, including:
- Asymptomatic carriers
- Varying onset of symptoms
- Emergence of highly contagious variants
- Complex transmission dynamics

Our ABM approach is particularly suitable for COVID-19 simulation because it:
- Treats each individual as an agent with unique interactions
- Captures heterogeneous behavior patterns
- Models various transmission environments (homes, workplaces, public spaces)
- Adapts to changing intervention strategies

## Features

### Health States
- Unexposed
- Asymptomatic and contagious
- Symptomatic and contagious
- Asymptomatic and non-contagious
- Post-COVID immune
- Naturally immune
- Deceased

### Simulation Components
- Dynamic visualization of disease progression
- Real-time tracking of population states
- Analysis of intervention effectiveness
- Measurement of key epidemiological parameters

### Model Parameters
- Infection probability (default: 0.2)
- Social interaction rates
- Recovery and mortality rates
- Intervention timing and intensity
- Population characteristics

## Installation

```bash
# Clone the repository
git clone [repository-url]
cd covid-abm-simulation

# Install required packages
pip install -r requirements.txt
```

## Usage

```python
# Import the simulation module
from covid_simulation import CovidSimulation

# Initialize simulation with parameters
sim = CovidSimulation(
    population_size=1000,
    infection_probability=0.2,
    simulation_days=50
)

# Run the simulation
sim.run()

# Generate visualizations
sim.plot_results()
```

## Requirements
- Python 3.8+
- NumPy
- Pandas
- Matplotlib
- NetworkX (for social network modeling)
- Seaborn (for visualization)

## Results Analysis

The simulation provides insights into:
- Peak infection timing and magnitude
- Effects of various intervention strategies
- Development of population immunity
- Impact of social networks on transmission
- Mortality patterns and trends

## Authors
- Rui Qin (24121014)
- Qianqian Li (2377074)

## References

1. Kermack, W. O., & McKendrick, A. G. (1927). A contribution to the mathematical theory of epidemics.
2. He, S., Tang, S., & Rong, L. (2020). A discrete stochastic model of the COVID-19 outbreak: Forecast and control.
3. Epstein, J. M. (2009). Modelling to contain pandemics.
4. Ferguson, N. M., et al. (2020). Impact of non-pharmaceutical interventions (NPIs) to reduce COVID-19 mortality and healthcare demand.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
