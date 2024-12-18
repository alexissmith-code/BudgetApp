# Budget View

A budget app that displays your "budget" based on the paychecks and expenses given, as well as a list of all your expenses.

## Description

When the app is launched for the first time, the "Budget" and "Expense" TextViews are initialized to $0.00, and the Recycler View will be empty. Users can add expenses by clicking the add expense item in the toolbar. When a new expense is added, it is saved in the database and displayed in the RecyclerView through a the expenses adapter. The Expense class manages the list of expenses as a mutable list. Users can click on any item in the RecyclerView to update or delete it. Expense names and amounts can be updated, and changes are reflected both in the database and the Recycler View. Deleting an expense removes it from the database and updates the Recycler View in real time as well. Clicking the other toolbar item allows the user to enter their paycheck amount and select a date using the Date Picker Fragment. After entering the information, users can click the "Add Paycheck" button to update the "Budget" TextView. A Toast message displays the paycheck date as confirmation and the media player is used to make a cha ching sound. The app calculates the remaining budget by subtracting the total expenses from the paycheck amount. This calculation is performed in the background using the Work Manager, ensuring smooth performance and real-time updates via LiveData.



### Dependencies

Runs on Android Studio.
need to add the following line to your build.gradle.kts (:app)
```
implementation("androidx.work:work-runtime:2.10.0")
```
### Executing program

## Help
May need to update compileSdk from 34 to 35 in build.gradle.kts if doesn't sync.
```
compileSdk = 35
```
## Authors

Alexis Smith
linkedin//alexissmithe
