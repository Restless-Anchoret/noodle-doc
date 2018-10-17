# Noodle User Stories

## #1: Opening authentication page

**Preconditions**
- Web-application is closed.

**Actions**
- Web-application is opening first time.

**Results**
- Page has header with "Noodle" title.
- Two tabs are placed on the page: "Authentication" and "Registration".
- Tab "Authentication" is chosen by default.
- Two fields are placed on authentication page: "Login", "Password" - with button "Sign in".


## #2: Successful authentication

**Preconditions**
- Authentication page is opened ("Authentication" tab is chosen).
- At least one account should be registered before this User Story.

**Actions**
- "Login" and "Password" fields are filled with credentials of registered account.
- Button "Sign in" is clicked.

**Results**
- Signing in is successful.
- Search view is opened.


## #3: Authentication failure

**Preconditions**
- Authentication page is opened ("Authentication" tab is chosen).

**Actions**
- "Login" and "Password" fields are filled with credentials of nonexistent account.
- Button "Sign in" is clicked.

**Results**
- Warning notification is shown with message "Incorrect login or password".


## #4: Authentication with empty fields

**Preconditions**
- Authentication page is opened ("Authentication" tab is chosen).

**Actions**
- Some of "Login" and "Password" fields are empty.
- Button "Sign in" is clicked.

**Results**
- Warning notification is shown with message "Fill in required values".


## #5: Opening registration page

**Preconditions**
- Authentication page is opened ("Authentication" tab is chosen).

**Actions**
- "Registration" tab is chosen by clicking on it.

**Results**
- Registration tab is shown.
- Three fields are placed on authentication page: "Login", "Password", "Name" - with button "Sign up".


## #6: Successful registration

**Preconditions**
- Registration page is opened ("Registration" tab is chosen).

**Actions**
- "Login", "Password" and "Name" fields are filled with credentials of new account, login should not be matching with some existing account.
- Button "Sign up" is clicked.

**Results**
- Signing up is successful.
- Search view is opened.


## #7: Registration failure

**Preconditions**
- Registration page is opened ("Registration" tab is chosen).
- At least one account should be registered before this User Story.

**Actions**
- "Login", "Password" and "Name" fields are filled with credentials of new account, login should be matching with existing account.
- Button "Sign up" is clicked.

**Results**
- Warning notification is shown with message "Account with this login cannot be used".


## #8: Registration with empty fields

**Preconditions**
- Registration page is opened ("Registration" tab is chosen).

**Actions**
- Some of "Login", "Password" and "Name" fields are empty.
- Button "Sign up" is clicked.

**Results**
- Warning notification is shown with message "Fill in required values".


## #9: Registration with week password

**Preconditions**
- Registration page is opened ("Registration" tab is chosen).

**Actions**
- "Login", "Password" and "Name" fields are filled with credentials of new account, login should not be matching with some existing account, password should be week.
- Button "Sign up" is clicked.

**Results**
- Warning notification is shown with message "Minimum password length is 8 symbols, both digits and letters should be used".


## #10: Search view is opened

**Preconditions**
- Authentication or registration was successfully done.

**Actions**
- Wait until search view is opened.

**Results**
- Page has header with "Noodle" title and the link to Search view at the left and links "{Name}", "Sign out" at the right ({Name} is a name of currently authenticated user).
- Page has list of account lists at the left.
- Each list has two buttons near its title (for edition and deletion).
- Button "+" is present below all lists.
- Page has set of empty filter fields and button "Search" at the center.
- There are three filter fields: "Lists", "Tags" and "Status".
- Page has empty area at the right.


## #11: Signing out

**Preconditions**
- Search view is opened.

**Actions**
- "Sign out" button is clicked.

**Results**
- User is signing out.
- Authentication page is opened ("Authentication" tab is chosen).


## #12: Opening profile settings

**Preconditions**
- Search view is opened.

**Actions**
- "{Name}" button is clicked ({Name} is a name of currently authenticated user).

**Results**
- Profile settings page is opened.
- The same header is shown on this page.
- "Profile settings" header is below header component.
- Five fields are located on this page: "Login", "Name", "Old password", "New password", "Repeat new password".
- "Login" field is not editable.
- Button "Save" is located on this page below text fields.


## #13: Successful changing profile settings

**Preconditions**
- Profile settings page is opened.

**Actions**
- "Name" field is modified (optionally).
- "Old password", "New password" and "Repeat new password" fields are filled correctly (optionally).
- Button "Save" is clicked.

**Results**
- Profile is updated successfully.
- Password fields are empty.
- Informational notification is shown "Profile is updated".


## #14: Changing profile settings failure (incorrect old password)

**Preconditions**
- Profile settings page is opened.

**Actions**
- "Old password" is filled with incorrect value.
- "New password" and "Repeat new password" fields are filled with the same strong password value.
- Button "Save" is clicked.

**Results**
- Warning notification is shown "Incorrect old password".


## #15: Changing profile settings failure (new password mismatching)

**Preconditions**
- Profile settings page is opened.

**Actions**
- "Old password" is filled with correct value.
- "New password" and "Repeat new password" fields are filled with different values.
- Button "Save" is clicked.

**Results**
- Warning notification is shown "New password values mismatch".


## #16: Changing profile settings failure (week password)

**Preconditions**
- Profile settings page is opened.

**Actions**
- "Old password" is filled with correct value.
- "New password" and "Repeat new password" fields are filled with the same week password value.
- Button "Save" is clicked.

**Results**
- Warning notification is shown with message "Minimum password length is 8 symbols, both digits and letters should be used".


## #17: Changing profile settings failure (empty name)

**Preconditions**
- Profile settings page is opened.

**Actions**
- "Name" field is modified and set empty.
- Button "Save" is clicked.

**Results**
- Warning notification is shown "Name cannot be empty".


## #18: Creating a new list

**Preconditions**
- Search view is opened.

**Actions**
- Button "+" below lists is clicked.
- Button "Create" is clicked for empty list title.
- New list title is entered and button "Create" is clicked.

**Results**
- Clicking button "+" causes showing dialog with title "Create list", one text field "Title" and button "Create".
- Clicking button "Create" with empty list title causes showing warning notification "List title cannot be empty".
- Clicking button "Create" causes new list creation and closing the dialog.


## #19: Editing a list

**Preconditions**
- Search view is opened.
- At least one list is presented in current account.

**Actions**
- Edit button is clicked near presented list.
- List title is removed from title field and "Save" button is tried to be clicked.
- New list title is entered in title field and "Save" button is clicked.

**Results**
- Clicking edit button causes showing dialog with title "Edit list", one text field "Title" and button "Save".
- Clicking "Save" button with empty title field causes showing warning notification "List title cannot be empty".
- Clicking "Save" button with corrected title field causes saving list title and closing the dialog.


## #20: Deleting a list

**Preconditions**
- Search view is opened.
- At least one list is presented in current account.

**Actions**
- Deleting button is clicked near presented list.
- Button "Delete" is clicked in the dialog.

**Results**
- Clicking deleting button causes showing dialog with title "Delete list", two buttons "Delete" and "Cancel", message "Are you sure you want to delete this list? All tasks from it will be deleted and can no longer be restored."
- Clicking "Delete" button causes deleting list and closing dialog.


## #21: Choosing filter values in search view

**Preconditions**
- Search view is opened.

**Actions**
- Some lists are chosen in "Lists" field.
- Some tags are chosen in "Tags" field.
- Some statuses are chosen in "Status" field.
- Button "Search" is clicked.

**Results**
- When "Lists" field is being filled, dropdown list of available lists is shown below, so that user could choose lists by clicking on them.
- When "Tags" field is being filled, dropdown list of available tags is shown below, so that user could choose tags by clicking on them.
- When "Status" field is being filled, dropdown list is shown below, which contains statuses "To do", "In progress", "Done".
- When "Search" button is clicked, filtered tasks are shown below filter fields.
- Lists and statuses, chosen for filtering, are used with "or" logic operator. Tags, chosen for filtering, are used with "and" logic operator.
- Tasks are shown without any indents from left side (nested tasks are shown like root tasks).
- Filtered tasks should be ordered following the next rule. Tasks from the same list should follow the order of DFS, choosing parent first.
- Each task is presented as a line with task title, tags and some buttons depending on task status.
- When task is in "To do" status, its line has white background and contains two buttons: starting button and ending button.
- When task is in "In progress" status, its line has blue background and contains two buttons: ending button and button with dropdown which contains single button "Back to "To do"".
- When task is in "Done" status, its line has white background, task title is crossed out, and line contains dropdown list with two buttons: "Back to "To do"" and "Back to "In progress"".


## #22: Changing task status in search view

**Preconditions**
- Search view is opened.
- Some filters were chosen and "Search" button was clicked.
- Some tasks were shown in the list.

**Actions**
- Status of some task is changed by clicking some button.

**Results**
- Task status is changed, task line view is changed correspondingly.
- If statuses of filtered tasks does not match to filtering options after status change, filtered tasks list should not be changed until "Search" button is clicked again.


## #23: Choosing found task in search view

**Preconditions**
- Search view is opened.
- Some filters were chosen and "Search" button was clicked.
- Some tasks were shown in the list.

**Actions**
- Some task is clicked.

**Results**
- Task content component is shown at the right of the page.
- At the top of this component tasks hierarchy is displayed (e.g. Task1 > Task2 > Task3).
- There are three text fields here: "Title", "Description" and "Tags".
- Button "Save" is placed near editable fields.
- There are also some informational fields here: "Status", "Creation date", "Start date" and "End date". 


## #24: Editing task in task component

**Preconditions**
- Task content component is opened.

**Actions**
- Field "Title" content is removed.
- Button "Save" is clicked.
- Content of fields "Title", "Description" and "Tags" is changed to correct values.
- Button "Save" is clicked again.

**Results**
- Clicking "Save" button with empty title field causes showing warning notification "Task title cannot be empty".
- Clicking "Save" button with nonempty title field saves new task fields.
- If task title was changed, it should be changed in task hierarchy at the top of component and in the component at the center of the page (search view or task tree view).
- If task tags were changed, they should be changed in the component at the center of the page (search view or task tree view).


## #25: Opening task tree view

**Preconditions**

**Actions**

**Results**


## #26: Creating task

**Preconditions**

**Actions**

**Results**


## #27: Deleting task

**Preconditions**

**Actions**

**Results**


## #28: Changing task status in task tree view

**Preconditions**

**Actions**

**Results**


## #29: Choosing task in task tree view

**Preconditions**

**Actions**

**Results**


## #30: Changing filtering option (task status) in task tree view

**Preconditions**

**Actions**

**Results**


## #31: Hiding/showing task children

**Preconditions**

**Actions**

**Results**
