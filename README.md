# DMV Service System Simulation

This Python program simulates a Department of Motor Vehicles (DMV) customer service system using probabilistic service assignment and server utilization calculations.

Customers arrive and are randomly assigned one of three DMV services based on historical probabilities. The program then assigns each customer to the DMV server with the lowest current workload and calculates server utilization.

This simulation demonstrates how randomness and probability affect real-world service systems.

---

## DMV Services

The DMV offers three services:

| Service ID | Service | Time (minutes) | Probability |
|-------------|---------|---------------|-------------|
| 0 | Get a title | 18.63 | 30% |
| 1 | Take a test | 36.21 | 20% |
| 2 | Get a license | 5.97 | 50% |

Each customer receives exactly one service.

---

## Program Inputs

The program asks the user for:

- Number of customers
- Number of DMV servers
- Length of the work shift (minutes)

Input validation ensures that:

- all inputs are numeric
- number of customers is an integer greater than 0
- number of servers is an integer greater than 0
- shift length is greater than 0

---

## Simulation Logic

1. Each customer is assigned a service randomly based on probabilities:
   - 30% title
   - 20% test
   - 50% license

2. Each customer is assigned to the DMV server with the **lowest total service time**.

3. Server workloads update after each assignment.

4. After all customers are processed, the program calculates:

- total service time for each server
- server utilization

Utilization is calculated as:
