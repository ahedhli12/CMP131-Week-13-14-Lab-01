# CMP 131 – Python Programming


> **Required file location:** Keep every Python file directly in the repository root. Do not create a `src` folder.

## Weeks 13 and 14 – Lab 1: Grocery List Manager

**Total Points: 100**

## Learning Objectives

After completing this lab, students should be able to:

* Create and use a Python list.
* Add items to a list using `append()`.
* Display list items using a loop.
* Number displayed items beginning with `1`.
* Remove an item from a list.
* Accept and validate menu selections.
* Validate that an item number is within the correct range.
* Use a loop to display a menu repeatedly.
* Use conditional statements to process menu choices.
* Organize a Python program using a `main()` function.
* Test an interactive menu-driven program.

## Assignment Overview

Create a Python program that manages a simple grocery list.

The program must repeatedly display the following menu:

```text
GROCERY LIST MANAGER

1. Add an item
2. View the list
3. Remove an item
4. Exit
```

The user must be able to:

1. Add grocery items to the list.
2. View all items with their corresponding numbers.
3. Remove an item by entering its number.
4. Exit the program.

The menu must continue to appear until the user selects Option 4.

The instructor is not providing completed Python code or an exact output design. Students must design, write, and test their own programs.

## Required Python File

Create a Python file named:

`grocery_list.py`

Include a comment header containing:

* Student name
* Course number
* Week numbers
* Lab number
* Assignment title
* Date

Example header structure:

```python
# Student Name:
# Course: CMP 131
# Weeks: 13 and 14
# Lab: 1
# Assignment: Grocery List Manager
# Date:
```

# Program Requirements

## Part 1: Create the Grocery List

Create an empty list that will store the grocery items entered by the user.

Use a meaningful variable name for the list.

The list should initially contain no items. Items must be added while the program is running.

## Part 2: Display the Menu

Display a clearly formatted menu containing these four choices:

```text
1. Add an item
2. View the list
3. Remove an item
4. Exit
```

Ask the user to select an option by entering a number from `1` through `4`.

The menu must be placed inside a loop so that it appears again after each completed operation.

## Part 3: Validate the Menu Choice

The program must accept only the following menu choices:

* `1`
* `2`
* `3`
* `4`

If the user enters a number outside this range, display an error message and show the menu again.

Example:

```text
Invalid menu selection. Please enter a number from 1 through 4.
```

The program should also handle an entry that cannot be converted to an integer, such as:

* A letter
* A word
* An empty entry

An invalid entry must not stop the program.

## Part 4: Add an Item

When the user selects Option 1:

1. Ask the user to enter the name of a grocery item.
2. Remove unnecessary spaces from the beginning and end.
3. Validate that the item name is not empty.
4. Add the item to the grocery list.
5. Display a confirmation message.

Example interaction:

```text
Enter the grocery item: Apples
Apples was added to the grocery list.
```

If the user enters only spaces or presses Enter without entering an item:

* Do not add the empty item to the list.
* Display an appropriate error message.
* Return to the menu or ask for another item.

Duplicate items may be added unless the student chooses to prevent duplicates as an optional improvement.

## Part 5: View the Grocery List

When the user selects Option 2, display every item currently stored in the grocery list.

Each item must be displayed with a corresponding number beginning with `1`.

Example:

```text
GROCERY LIST

1. Apples
2. Milk
3. Bread
```

Use a loop to display the items. Do not create a separate output statement for every possible item.

The displayed numbers must begin with `1`, even though Python list indexes begin with `0`.

If the list is empty, display an appropriate message:

```text
The grocery list is currently empty.
```

The program must not produce an error when the user attempts to view an empty list.

## Part 6: Remove an Item

When the user selects Option 3:

1. Check whether the grocery list is empty.
2. If the list is not empty, display the numbered grocery list.
3. Ask the user to enter the number of the item to remove.
4. Validate the entered number.
5. Remove the corresponding item.
6. Display a confirmation message.

Example:

```text
GROCERY LIST

1. Apples
2. Milk
3. Bread

Enter the number of the item to remove: 2
Milk was removed from the grocery list.
```

Because displayed item numbers begin with `1` and Python indexes begin with `0`, the program must correctly convert the user’s item number into the corresponding list index.

For example:

| Displayed number | Python list index |
| ---------------: | ----------------: |
|                1 |                 0 |
|                2 |                 1 |
|                3 |                 2 |

### Removal Validation

The item number must be within the valid range.

For example, if the list contains three items, valid choices are:

```text
1, 2, or 3
```

The following entries must be rejected:

* `0`
* A negative number
* A number greater than the number of items
* A letter or word
* An empty entry

Display an appropriate error message when the entered number is invalid.

Example:

```text
Invalid item number. Please enter a number from 1 through 3.
```

An invalid item number must not remove anything from the list or stop the program.

If the user selects Option 3 while the list is empty, display:

```text
The grocery list is empty. There are no items to remove.
```

## Part 7: Exit the Program

When the user selects Option 4:

* Stop the menu loop.
* Display an appropriate closing message.

Example:

```text
Thank you for using the Grocery List Manager.
```

The program must continue running until Option 4 is selected.

## Part 8: Organize the Program

Create a `main()` function that controls the program.

The program should follow this general sequence:

1. Display the program title.
2. Create the empty grocery list.
3. Display the menu.
4. Ask for and validate the menu choice.
5. Perform the selected operation.
6. Return to the menu.
7. Exit only when the user selects Option 4.

Call `main()` to begin the program.

Students may create additional functions to organize the program, but additional functions are optional.

# Required Python Features

The program must demonstrate the following:

| Task                      | Required Python feature  |
| ------------------------- | ------------------------ |
| Store the grocery items   | List                     |
| Add an item               | `append()`               |
| Display all items         | Loop                     |
| Number the items          | Counter or `enumerate()` |
| Choose an operation       | Conditional statements   |
| Repeat the menu           | Loop                     |
| Remove an item            | List-removal operation   |
| Validate item numbers     | Range checking           |
| Handle nonnumeric entries | Input validation         |

# Example Program Interaction

The exact formatting may vary, but the program should behave similarly to the following:

```text
GROCERY LIST MANAGER

1. Add an item
2. View the list
3. Remove an item
4. Exit

Enter your choice: 1
Enter the grocery item: Apples
Apples was added to the grocery list.

1. Add an item
2. View the list
3. Remove an item
4. Exit

Enter your choice: 1
Enter the grocery item: Milk
Milk was added to the grocery list.

1. Add an item
2. View the list
3. Remove an item
4. Exit

Enter your choice: 1
Enter the grocery item: Bread
Bread was added to the grocery list.

1. Add an item
2. View the list
3. Remove an item
4. Exit

Enter your choice: 2

GROCERY LIST

1. Apples
2. Milk
3. Bread

1. Add an item
2. View the list
3. Remove an item
4. Exit

Enter your choice: 3

GROCERY LIST

1. Apples
2. Milk
3. Bread

Enter the number of the item to remove: 2
Milk was removed from the grocery list.

1. Add an item
2. View the list
3. Remove an item
4. Exit

Enter your choice: 2

GROCERY LIST

1. Apples
2. Bread

1. Add an item
2. View the list
3. Remove an item
4. Exit

Enter your choice: 4
Thank you for using the Grocery List Manager.
```

Students should create their own prompts, headings, messages, and output formatting.

# Required Testing

## Test 1: Add Items

Add the following items:

```text
Apples
Milk
Bread
```

Confirm that:

* Each item is added successfully.
* A confirmation message appears after each item is added.
* The menu appears again after every addition.
* The program does not exit unexpectedly.

## Test 2: View the List

After adding the three required items, select Option 2.

The list should display:

```text
1. Apples
2. Milk
3. Bread
```

Confirm that:

* All items appear.
* The items appear in the order they were added.
* The displayed numbers begin with `1`.
* A loop is used to display the items.

## Test 3: Remove an Item

Remove Item 2.

Confirm that:

* `Milk` is removed.
* A removal confirmation is displayed.
* The remaining list contains:

```text
1. Apples
2. Bread
```

* The remaining items are renumbered correctly.

## Test 4: Invalid Removal Numbers

Test the following removal entries:

```text
0
-1
10
```

Confirm that:

* Each invalid number is rejected.
* An error message is displayed.
* No item is removed.
* The program continues running.

## Test 5: Nonnumeric Removal Entry

Enter:

```text
two
```

Confirm that:

* The program does not stop with an error.
* An appropriate validation message is displayed.
* The user can continue using the program.

## Test 6: Empty List

Start the program without adding an item.

Select:

* Option 2 to view the list.
* Option 3 to remove an item.

Confirm that:

* An empty-list message is displayed.
* The program does not produce an error.
* The menu continues to operate.

## Test 7: Invalid Menu Selections

Test the following menu entries:

```text
0
5
hello
```

Confirm that:

* Each invalid choice is rejected.
* An appropriate message is displayed.
* The menu appears again.
* The program does not stop unexpectedly.

## Test 8: Exit

Select Option 4.

Confirm that:

* The menu loop ends.
* A closing message is displayed.
* The program exits without errors.

# Required Screenshots

Submit screenshots showing the program running.

Your screenshots must clearly demonstrate:

1. Adding at least three grocery items.
2. Viewing the numbered grocery list.
3. Removing an item by its number.
4. Viewing the updated list after the item is removed.
5. At least one invalid item-number entry and its validation message.
6. Exiting the program normally.

The screenshots must clearly show both the user input and the program output.

Use readable screenshots. Do not crop out information needed to demonstrate that the program works.

# Point Distribution

* Complete comment header and descriptive title: 5 points
* Correct creation and use of a Python list: 10 points
* Repeating menu with four required options: 15 points
* Correctly adding and validating grocery items: 15 points
* Correctly displaying and numbering list items: 15 points
* Correctly removing the selected item: 15 points
* Validating menu choices and removal numbers: 15 points
* Correct exit behavior, comments, formatting, screenshots, and testing: 10 points

**Total: 100 points**

# Code Comments

Include comments explaining the major sections of the program:

* Program information header
* `main()` function
* Grocery-list creation
* Menu loop
* Menu input and validation
* Adding an item
* Viewing and numbering items
* Removing an item
* Item-number validation
* Exit condition

Comments should explain the purpose of each major section. They should not repeat every Python statement word for word.

# General Requirements

* Use Python to complete the assignment.
* Create the required `grocery_list.py` file.
* Include and call a `main()` function.
* Store grocery items in a Python list.
* Begin with an empty grocery list.
* Display all four required menu options.
* Repeat the menu until the user selects Option 4.
* Add items using a list operation.
* Reject empty grocery-item entries.
* Display the grocery list using a loop.
* Number displayed items beginning with `1`.
* Allow the user to remove an item by entering its displayed number.
* Validate all menu and removal entries.
* Handle attempts to view or remove items from an empty list.
* Use meaningful and consistent variable names.
* Include a complete comment header.
* Include comments explaining the major program sections.
* Use clear prompts, headings, and result messages.
* Complete all required testing.
* Submit the required screenshots.
* Make sure the program runs without errors.
* Follow the course AI-use policy.
* Record any AI assistance in `AI-Use-Report.md`.

# Required Organization

Organize the assignment as follows:

* `Weeks-13-and-14`

  * `Lab-01`

    * `CMP131-Weeks-13-and-14-Lab-01.md`
    * `AI-Use-Report.md`
    * `screenshots`
    * `src`

      * `grocery_list.py`

# Submission Requirements

Submit or push the complete `Lab-01` folder.

The submission must include:

* `grocery_list.py`
* Screenshots showing the required program operations
* `AI-Use-Report.md`

Before submitting, verify that:

* The Python filename is exactly `grocery_list.py`.
* The program contains a complete comment header.
* The program includes and calls a `main()` function.
* An empty list is created when the program begins.
* The four required menu choices are displayed.
* The menu continues until Option 4 is selected.
* Users can add items to the list.
* Empty item names are rejected.
* Users can view the complete grocery list.
* Every item is displayed with a number beginning with `1`.
* Users can remove an item using its displayed number.
* The correct item is removed.
* Remaining items are renumbered correctly.
* Removal numbers are validated.
* Invalid menu choices do not stop the program.
* Nonnumeric entries are handled appropriately.
* Empty-list operations do not cause errors.
* The program displays an exit message.
* Required screenshots are included.
* All required tests were completed.
* The program runs without errors.
* The AI-use report is complete.
* The latest work has been committed and pushed to GitHub.

# Suggested Git Commit Messages

* Create Weeks 13 and 14 Lab 1 Python file
* Add grocery list menu
* Add grocery item input
* Display numbered grocery list
* Add item removal operation
* Validate menu and removal choices
* Handle empty grocery list
* Add program screenshots
* Improve comments and output formatting
* Complete Weeks 13 and 14 Python lab

---

## GitHub Starter Repository

Use the following public starter repository:

[CMP131-Week-13-14-Lab-01](https://github.com/ahedhli12/CMP131-Week-13-14-Lab-01)

### Getting Started

1. Open the starter repository using the link above.
2. Select **Use this template → Create a new repository** when the template option is available.
3. Choose your personal GitHub account as the owner.
4. Name your repository `LastName-FirstName-CMP131-Week-13-14-Lab-01`.
5. Set your repository to **Public**.
6. Clone your own newly created repository—not the instructor’s starter repository.
7. Open the entire cloned folder in Visual Studio Code.
8. Complete and test every required Python file.
9. Commit and push your work to GitHub.
10. Verify that your latest files appear on GitHub.
11. Complete `AI-Use-Report.md`.
12. Submit the required work through Blackboard Ultra and include your public repository link when requested.

### Required Repository Files

- `CMP131-Week-13-14-Lab-01.md`
- `AI-Use-Policy.md`
- `AI-Use-Report.md`
- `grocery_list.py`

### Before You Submit

- [ ] All required Python files are in the repository root.
- [ ] Every required filename is exact.
- [ ] Each program runs successfully.
- [ ] Required tests and screenshots are complete.
- [ ] `AI-Use-Report.md` is complete and accurate.
- [ ] The latest commit is visible on GitHub.
