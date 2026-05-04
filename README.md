# fare-allocation-overbooking-model
MILP-based revenue optimization model for Norwegian Cruise Line, optimizing fare-class allocation and overbooking decisions to maximize profit under demand uncertainty.
 

Project Overview
This project develops a Mixed Integer Linear Programming (MILP) model to optimize revenue management decisions for Norwegian Cruise Line (NCL).

NCL serves around 2.9 million guests annually with approximately 9.5 billion dollars in revenue. However, revenue is often lost due to manual decisions in fare pricing and overbooking.

This model replaces intuition with data-driven optimization.

Objective
Maximize net profit by optimizing:

1. Fare-class allocation
   Early-Bird
   Standard
   Premium

2. Controlled overbooking
   Accept bookings beyond capacity
   Account for no-show probability
   Minimize compensation cost

Model Scope
20 sailings
7 cabin types
3 fare classes
420 decision variables

Model Structure
Decision variable:
x(s,c,f) = number of bookings for each sailing, cabin type, and fare class

Objective:
Maximize total profit = revenue minus compensation cost

How to Use

Step 1
Open the Excel file named NCL_profit_maximization.xlsx

Step 2
Set the no-show rate in cell Q2:
0.01 for conservative
0.03 for base case
0.05 for optimistic

Step 3
Run Solver:
Go to Data → Solver
Set objective to maximize cell P4
Select decision variable cells
Add constraints for demand and capacity
Choose Simplex LP or GRG

Step 4
Interpret results:
P4 gives total profit
Column K gives revenue
Column L gives compensation cost
Column M gives net profit

Key Result
Approximately 31.23 million dollars optimized profit in base case
Around 2.5 million improvement compared to no-overbooking

Limitations
Demand treated as fixed
Single no-show rate
Static model
No substitution between fare classes
Estimated compensation cost
No seasonality
Solver limitations

Future Improvements
Stochastic demand
Cabin-specific no-show rates
Dynamic re-optimization
Demand substitution
Machine learning forecasting
Fleet-level optimization
Customer lifetime value

Applications
Airlines
Hotels
Car rentals
Event ticketing
Healthcare scheduling
Freight logistics
Advertising

Author
Sampada Donahalli Dinesh
