🎉 Picnic Expense Distribution Tracker

📖 Purpose
The Picnic Expense Distribution Tracker is a lightweight, client-side web application designed to fairly and transparently split the costs of a group picnic among multiple families.

Instead of doing complex math manually, this tool calculates expenses based on a "Unit System" where:

1 Adult = 1 Unit
1 Child = 0.5 Units
This ensures that a family with 2 adults pays proportionally more than a family with 1 adult and 2 children. Furthermore, it tracks who paid for what upfront, automatically calculating the final balance to show exactly who owes money and who is owed money at the end of the trip.

🔑 Key Fields Description

Summary Dashboard (Top Section)
Total Families: The current number of families participating.
Total Adults / Children: The headcount across all families.
Total Units: The sum of all calculation units (Adults + 0.5 * Children).
Cost Per Unit: The base cost divided by the total units (i.e., how much 1 Adult's share costs).
Family Distribution Table (Main Table)
Family Name: Identifier for the family.
Adults / Children: Input fields for the number of people attending.
Total Members: Simple headcount (Adults + Children).
Units: The calculated weight of the family's share (Adults + [Children * 0.5]).
Share %: The percentage of the total expense this family is responsible for.
Amount (PKR): The exact monetary amount the family owes based on their Share %.
Amount Paid (PKR): An input field to enter how much money this family has already spent/paid upfront.
Balance (PKR): The final settlement amount (Amount Paid - Amount Owed).

🟢 Green (Positive): The family is owed money.
🔴 Red (Negative): The family still needs to pay.

Expense Breakdown Table (Bottom Section)
Item / Category: What was bought (e.g., Food, Transport, Drinks).
Quantity / Unit Price: Used to calculate the item's total cost.
Total (PKR): Auto-calculated total for that specific item.
Paid By: Which family paid for this specific item out of pocket.

🛠️ How to Use It

Open the Application:
Simply double-click the HTML file to open it in any modern web browser. No internet connection or server setup is required.
Add or Modify Families:
The app starts with 3 default families. Click ➕ Add Family to add more, or ➖ Remove Last to delete one.
Click on the "Family Name" cells to rename them (e.g., "Ahmed's Family").
Adjust the number of Adults and Children for each family. The distribution table will update instantly.
Log the Expenses:
Scroll down to the "Expense Breakdown" section.
Click ➕ Add Expense Item.
Enter the item name (e.g., "Biryani"), category, quantity, and unit price. The table will automatically calculate the total.
In the "Paid By" column, type the name of the family who paid for that item (e.g., "Family 1").
Track the Balance:
As you add expense items, the "Total Picnic Expense" at the top automatically increases.
Go back to the main table and enter the amounts each family has paid in the Amount Paid (PKR) column (if you used the "Paid By" column in step 3, just match those amounts here).
Look at the Balance (PKR) column to settle up at the end of the picnic!
Note: You can also manually override the "Total Picnic Expense" at the top if you just want to split a fixed lump sum without logging individual items.

🔄 Reset

If you want to start over for a new picnic, simply click the 🔄 Reset button, and all data will revert to the default template.
