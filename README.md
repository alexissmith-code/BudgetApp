# Budget View

A budget app that displays your "budget" based on the paychecks and expenses given as a list of all your expenses.

## Description

This app utilizes a SQLite Database, recycler view, a toolbar with a clickable item for adding a paycheck and one for adding an expense, sound via MediaPlayer, a Date picker that utilizes a fragment, as well as a background thread via a Work Manager. When the app starts for the first time the budget and expense textview will both be equal to $0.00 and no expenses will be population the recycler view. The user can add all of their expenses through the clickable item in the toolbar. By adding these, it will populate the recycler view by using a database and expenseAdapter that updates the Expense class that contains a mutable list. One the recycler view is populated you are able to click on an item, and then you can either update the expense name or expense amouunt, or delete the item itself. Updating and deleting in this activity, update and delete the item from the database as well. Once you have all of your expenses, you can then click the other item in the toolbar to add your paycheck. You enter your paycheck amount and then choose the paycheck date. Then you can click the add paycheck button which will display a Toast message with the date and update the "budget" textview. This uses the Work Manager anf live data so the expenses are subtracted from the budget (or paycheck) to let you know how much more money you have after your expenses. 


### Dependencies

Runs on Android Studio.
need to add the following line to your build.gradle.kts (:app)
```
implementation("androidx.work:work-runtime:2.10.0")
```
### Executing program

## Help
May need to update compileSdk from 34 to 35 in build.gradle.kts if doesn't sync.
## Authors

Alexis Smith
linkedin//alexissmithe
