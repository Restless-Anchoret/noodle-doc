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
- Page has header with "Noodle" title at the center and links "{Name}", "Sign out" at the right ({Name} is a name of currently authenticated user).
- Page has list of account lists at the left.
- Each list has two buttons near its title (for edition and deletion).
- Button "New" is present below all lists.
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
- "{Name}" button is clicked ({Name} is a name currently authenticated user).

**Results**
- Profile settings page is opened.
- The same header is shown on this page.
- "Profile settings" header is below header component.
- Five fields are located on this page: "Login", "Name", "Old password", "New password", "Repeat new password".
- "Login" field is disabled (cannot be edited).
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
- Informal notification is shown "Profile is updated".


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

**Actions**

**Results**


## #19: Editing a list

**Preconditions**

**Actions**

**Results**


## #20: Deleting a list

**Preconditions**

**Actions**

**Results**


## #21: Choosing filter values in search view

**Preconditions**

**Actions**

**Results**


## #22: Changing task status in search view

**Preconditions**

**Actions**

**Results**


## #23: Choosing found task in search view

**Preconditions**

**Actions**

**Results**


## #24: Editing task in task component

**Preconditions**

**Actions**

**Results**


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
