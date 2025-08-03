# 📦 Production-Planning-Optimization

Production planning and optimization project using both exact (solver-based) and heuristic methods.

The case study is based on Pro Deco, a company launching two new furniture products with a short production cycle over a 6-month planning horizon.

🪑 Project Context
Company: Pro Deco
New Products:

P1: Modular coffee tables

P2: Reconfigurable chairs

Planning Horizon: April to September 2024
Objective: Meet product demand while minimizing overall production and workforce-related costs.

📊 Project Components
1. Problem Modeling
Initial stock: 0 units

Workforce: 65 operators

No overtime allowed

Demand forecasted over 6 months

2. Cost Structure
Cost Element	Value
Raw materials	45 DT/unit
Inventory holding	8 DT/unit/month
Stockout penalty	40 DT/unit/month
Hiring & training	800 DT/operator
Firing cost	1600 DT/operator
Labor cost	18 DT/hour
Subcontracting (P1/P2)	80 / 60 DT per unit
Time required (P1/P2)	3.5 / 2.5 hours per unit

3. Solver-Based Optimization
Implemented a mathematical model using a linear solver to determine the optimal production plan, including:

Decision variable declarations

Objective function

Constraints (workforce, production capacity, inventory, etc.)

Optimal solution cost: 1,709,492 DT

4. Heuristic Method
A rule-based algorithm was implemented to:

Satisfy monthly demand using available workforce

Apply hiring/firing decisions dynamically based on monthly needs

Heuristic solution cost: 1,744,500 DT

Gap vs optimal: +2.04%

Benefits: Much faster execution and adaptable logic

5. Heuristic Implementation
Written in Python

Includes a graphical interface (Tkinter) for visual interaction (Note: may not work in headless environments like servers or Jupyter)

🖥️ GUI (Tkinter)
To launch the GUI (locally):

bash
Copier
Modifier
python main.py


📈 Outputs
Demand curves for P1 & P2

Workforce evolution across months

Cost comparison (solver vs heuristic)

✅ Key Takeaways
Solver provides optimal results but is computationally expensive.

Heuristics offer speed and adaptability with minor cost trade-offs.

Real-world production planning often benefits from combining both.

🧠 Future Work
Add support for GUI-less environments

Explore hybrid metaheuristics (e.g., Genetic Algorithm + LP)

Extend to multi-product, multi-plant scenarios
