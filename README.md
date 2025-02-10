# COVID-19 Agent-Based Simulation Model

An agent-based simulation model implemented in Python to study and analyze the spread of COVID-19, incorporating various factors such as age distribution, asymptomatic transmission, social networks, super-spreaders, virus variants, and government interventions.

## Project Structure

The project is organized into four main parts:

### Part 1: Base Model Setup
- Implementation of 7 agent states:
  - Unexposed
  - Asymptomatic and contagious
  - Symptomatic and contagious
  - Asymptomatic and not contagious
  - Post-COVID immune
  - Naturally immune
  - Death
- Age-stratified mortality rates across 9 age groups
- State transition probabilities and durations
- Basic agent properties and behavior

### Part 2: Social Network Model
- Implementation of Barabási-Albert scale-free network
- Structured social interactions between agents
- Behavior modification based on symptom status
- Network-based transmission dynamics

### Part 3: COVID-19 Attributes Enhancement
- Super-spreader behavior modeling
  - Increased interaction frequency
  - Higher transmission probability
  - Population distribution control
- Variant strain implementation
  - Modified transmission rates
  - Adjusted mortality rates
  - Strain-specific properties

### Part 4: Policy Impact Simulation
- Dynamic interaction rate adjustments
- Quarantine period implementation (Days 10-25)
- Post-quarantine behavior modeling
- Policy effectiveness analysis

## Requirements

```python
import numpy as np
import random
import math
import matplotlib.pyplot as plt
import networkx as nx
import pandas as pd
from collections import Counter
```

## Key Features

### Age-Based Mortality
- 9 age groups with different mortality rates
- Age-specific risk factors
- Population distribution based on real-world data

### Social Network Structure
- Scale-free network implementation
- Neighbor-based interactions
- Community structure modeling

### Disease States
- Asymptomatic carrier modeling
- Variable infection periods
- Immunity status tracking
- State transition probabilities

### Policy Implementation
- Flexible interaction rate adjustment
- Time-based policy changes
- Quarantine period effects

## Usage

```python
# Initialize base parameters
numAgents = 1000
naturalImmunity = 0.01
numInteractions = 10
numDays = 50
contagion_prob = 0.05

# Create social network
social_network = create_social_network(numAgents, steps=2, power=1)

# Initialize agents
agents = initialize_agents(numAgents)
agents = infect_initial_agents(agents)

# Run simulation
disthistory_df = simulate_spread_with_network(social_network, agents, num_interactions, numDays)
```

## Model Parameters

- `numAgents`: Total number of agents in simulation (default: 1000)
- `naturalImmunity`: Proportion of naturally immune agents (default: 0.01)
- `numInteractions`: Daily interactions per agent (default: 10)
- `contagion_prob`: Base infection probability (default: 0.05)
- `super_spreader_prob`: Probability of being a super-spreader (default: 0.05)
- `variant_contagion_prob`: Variant strain infection probability (default: 0.2)
- `variant_mortality_multiplier`: Increased mortality for variants (default: 1.5)

## Visualization

The model provides two main types of visualizations:
1. State Distribution Over Time - Stacked bar chart showing population in each state
2. SIR Model Over Time - Line plot showing susceptible, infected, and recovered populations

## Authors

- Rui Qin (24121014)

## References

- Ritchie, H., & Roser, M. (2024, February). Age structure. Our World in Data.
- Centers for Disease Control and Prevention. (n.d.). Risk for COVID-19 infection, hospitalization, and death by age group.
- Byrne, A. W., et al. (2020). Inferred duration of infectious period of SARS-CoV-2: Rapid scoping review and analysis of available evidence for asymptomatic and symptomatic COVID-19 cases.
