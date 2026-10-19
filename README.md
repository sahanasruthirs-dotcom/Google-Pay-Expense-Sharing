# Google-Pay-Expense-Sharing


A lightweight, matrix-based **Expense Sharing System** built in Python using Jupyter Notebook. This application allows groups of friends to log expenses, distribute costs equally or with custom amounts, and dynamically track net group balances.

## 🚀 Features

*   **Matrix-Based Tracking:** Uses a 2D matrix structure to track exact amounts owed between group members.
*   **Equal Splits:** Automatically divides an expense equally among a selected list of beneficiaries.
*   **Custom Splits:** Assign specific, custom monetary shares to individual group members.
*   **Beautiful Tables:** Renders transaction logs, matrices, and balance sheets inside clean ASCII tables.
*   **Net Balance Summaries:** Quickly computes who is owed money and who needs to pay to settle up.
*   **Interactive CLI Menu:** Features a terminal-based loop interface for managing expenses on the fly.

## 🛠️ Prerequisites & Installation

Make sure you have Python installed. You will need to install the following dependencies:

```bash
pip install numpy prettytable
```

## 💻 Core Functions

*   `add_expense(payer, beneficiaries, amount)`: Splits a total amount evenly across specified beneficiaries.
*   `add_custom_expense(payer, custom_shares)`: Logs a payment where group members owe specified individual amounts.
*   `display_matrix()`: Displays the raw spending matrix showing exactly how much every person has paid for everyone else.
*   `show_history()`: Lists all recorded transaction types, payers, and split breakdowns.
*   `show_balances()`: Generates a clear balance report showing the net amount each user should receive or owes (e.g., *Alice should receive ₹600.00*).

## 📊 Sample CLI Output

### Spending Matrix
```text
+-------+-------+-------+-------+-------+

|       | Alice |  Bob  | Carol | David |
+-------+-------+-------+-------+-------+

| Alice | 250.0 | 250.0 | 250.0 | 250.0 |
|  Bob  |  0.0  | 300.0 | 300.0 | 300.0 |
| Carol | 100.0 | 200.0 | 300.0 | 400.0 |
| David |  0.0  |  0.0  |  0.0  |  0.0  |
+-------+-------+-------+-------+-------+
```

### Balance Report
```text
Settlement Summary
+---------+---------+

| Friend  | Balance |
+---------+---------+

| Alice   |  650.0  |
| Bob     |  150.0  |
| Carol   |  150.0  |
| David   | -950.0  |
+---------+---------+

Balance Report

Alice should receive ₹650.00
Bob should receive ₹150.00
Carol should receive ₹150.00
David owes ₹950.00
```

## 🛠️ How to Run
1. Open the `.ipynb` file in **Jupyter Notebook** or **VS Code**.
2. Run all initialization cells to load the libraries, variables, and core functions.
3. Execute the interactive menu cell at the bottom to start logging your expenses!
