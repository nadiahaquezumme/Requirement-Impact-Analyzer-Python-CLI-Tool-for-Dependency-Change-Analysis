📌 Requirement Impact Analyzer

A lightweight Python CLI tool designed to analyze requirement dependencies and quickly determine how a change in one requirement affects others. It helps software engineers, business analysts, and QA teams understand dependency chains and evaluate the ripple effect of requirement updates.

🚀 Features

✔ Define requirement dependencies using a graph structure

✔ Forward (downstream) and backward (upstream) impact analysis

✔ ASCII-based dependency tree visualization

✔ Simple, interactive CLI interface

✔ Easy to extend with new requirements or relationships

🧠 How It Works

The tool:

Loads a collection of sample requirements

Treats dependencies as a directed graph

Uses DFS (Depth-First Search) to calculate impacted requirements

Displays the results in text format

Optionally prints a visual dependency tree

📂 Project Structure
Requirement_Analyzer.ipynb
      Python script inside notebook containing:
      - Requirement data model
      - Graph building functions
      - DFS impact analysis
      - ASCII tree generator
      - CLI for user interaction

📝 Usage
Run the script
python Requirement_Analyzer.py

Interactive flow

The tool lists all available requirements

You input:

Requirement ID (e.g., R1)

Direction of impact

F → Forward (downstream)

B → Backward (upstream)

The analyzer prints:

Type of impact

All affected requirements

Optional ASCII dependency tree

🧩 Example Output
Available requirements:
- R1: User login
- R2: Password reset
- R3: Multi-factor authentication
- R4: Security log monitoring
- R5: Admin dashboard

Enter changed requirement ID: R1
Impact direction [F/B]: F

Change type: Downstream impact
Impacted requirements:
- R2
- R3
- R4
- R5

Dependency view:
R1 (User login)
   └─ R2 (Password reset)
       └─ R3 (MFA)
           └─ R4 (Security logs)
               └─ R5 (Admin dashboard)

🛠 Technologies Used

Python 3

Dataclasses

DFS graph traversal

CLI interaction
📈 Future Enhancements

Import requirements from CSV/JSON

Export impact reports

Visual graphs using networkx

GUI version
