# Shark-Fish-Algae Predator-Prey Ecosystem

## Ecosystem Chosen:  
- **Sharks (Predator)**  
- **Fish (Prey)**  
- **Algae (Food)**

## Model Overview

This model simulates a predator-prey ecosystem involving sharks, fish, and algae, where the dynamics are based on the interactions between these three components.

### Key Interactions:
- **Sharks** eat fish to survive and reproduce.  
- **Fish** eat algae to survive and reproduce.  
- **Algae** regrows over time in empty water patches.

### Model Rules:
- Sharks gain **20 energy** when eating fish.  
- Fish gain **10 energy** when eating algae.  
- Reproduction for sharks and fish is **probabilistic**:  
  - Sharks reproduce if a random number (4) is less than 3.  
  - Fish reproduce under similar probabilistic conditions.
- The **movement** of sharks and fish is **random**.
- Algae grows back over time on patches of empty water.

### Ecosystem Behavior:
- The simulation uses **50 patches** in a grid.  
- The environment checks for empty patches that are not covered by algae and attempts to place algae on them:  
  - `ask n-of 50 patches with [pcolor = blue and not any? algae-here]`.

## Initial Variables:

- **initial-fish:** (Adjustable slider for the initial number of fish)  
- **initial-sharks:** (Adjustable slider for the initial number of sharks)  
- **initial-algae:** 1000 units at the start

## Monitors Added:
- **Fish Count:** Displays the current number of fish in the ecosystem.  
- **Sharks Count:** Displays the current number of sharks in the ecosystem.  
- **Algae Count:** Displays the current number of algae patches.  

## Plot:
A plot is provided to visualize the **shark** and **fish** count over time, showing how the population of both predators and prey fluctuates as they interact with each other.
