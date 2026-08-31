# CMP 131 – Python Programming

> **Required file location:** Keep every Python file directly in the repository root. Do not create a `src` folder.

## Weeks 13 and 14 – Lab 1: Grocery List Manager

**Total Points: 100**

## Learning Objectives

After completing this lab, students should be able to:

- Create and use a Python list.
- Add items to a list using list operations.
- Display list items using a loop.
- Number displayed items beginning with 1.
- Remove an item from a list.
- Accept and validate menu selections.
- Validate that an item number is within the correct range.
- Use a loop to display a menu repeatedly.
- Use conditional statements to process menu choices.
- Organize a program using a `main()` function.
- Test an interactive menu-driven program.

## Assignment Overview

Create one Python program named `grocery_list.py` that manages a simple grocery list.

The user must be able to:

1. Add a grocery item.
2. View the grocery list.
3. Remove an item by its displayed number.
4. Exit the program.

The menu must continue to appear until the user chooses to exit.

The instructor is not providing completed Python code or an exact output design. Students must design, write, and test their own program.

# Program Requirements

Create `grocery_list.py`.

## Part 1: Create the Grocery List

- Create an empty list when the program begins.
- Use a meaningful variable name.
- Items must be added while the program is running.

## Part 2: Display the Menu

Repeatedly display these four choices:

1. Add an item
2. View the list
3. Remove an item
4. Exit

Ask the user to select an option from 1 through 4.

## Part 3: Validate the Menu Choice

- Reject menu choices outside the valid range.
- Display an appropriate message for an invalid choice.
- Continue displaying the menu until the user selects Exit.

## Part 4: Add an Item

When the user selects Add:

- Ask for the grocery item.
- Add the item to the end of the list.
- Confirm that the item was added.
- Return to the main menu.

## Part 5: View the List

When the user selects View:

- If the list is empty, display an appropriate message.
- Otherwise, display every grocery item.
- Number the displayed items beginning with 1.
- Use a loop to display the list.
- Return to the main menu afterward.

## Part 6: Remove an Item

When the user selects Remove:

- If the list is empty, explain that there is nothing to remove.
- Otherwise, display the current numbered list.
- Ask the user for the number of the item to remove.
- Validate that the number corresponds to an existing item.
- Remove only the selected item.
- Confirm the removal.
- Return to the main menu.

Remember that the number displayed to the user begins with 1, while Python list positions begin with 0. Your program must account for that difference correctly.

## Part 7: Exit

When the user selects Exit:

- Stop the menu loop.
- Display an appropriate closing message.
- End the program normally.

## Program Organization

Organize the program using a `main()` function. Use additional functions when helpful to keep the program readable and organized.

# Required Testing

Test the complete menu flow. Confirm that:

- The program starts with an empty list.
- Multiple items can be added.
- Viewing the list shows every item in the correct order.
- Displayed numbering starts with 1.
- An item can be removed using its displayed number.
- Invalid menu choices are rejected.
- Invalid removal numbers are rejected.
- Viewing or removing from an empty list is handled safely.
- The menu continues after Add, View, and Remove.
- Selecting Exit ends the program.
- The program runs without errors.

# Code Comments

Include a comment header containing:

- Student name
- Course number
- Weeks 13 and 14
- Lab number
- Assignment title
- Date

Use comments to explain major sections such as list creation, menu processing, input validation, adding, viewing, removing, and exiting.

# General Requirements

- Use meaningful variable names.
- Use a Python list to store the grocery items.
- Use loops and conditional statements where required.
- Keep `grocery_list.py` directly in the repository root.
- Test every menu option.
- Make sure the program runs without errors.
- Follow `AI-Use-Policy.md`.
- Complete `AI-Use-Report.md` honestly.

# Submission Requirements

Your repository must include:

- `CMP131-Week-13-14-Lab-01.md`
- `grocery_list.py`
- `AI-Use-Policy.md`
- `AI-Use-Report.md`

Before submitting:

1. Run and test every menu option.
2. Confirm the filename is correct and located in the repository root.
3. Complete the AI-use report.
4. Commit and push your latest work.
5. Verify the newest files on GitHub.
6. Submit through Blackboard Ultra as directed.

**Do not push your work to the instructor's starter repository.**
