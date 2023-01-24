## Test Type:
	- @user_settings
	- @user_settings_top_bar
	- @user_settings_page
	- @layout
	- @happy_path
	- @negative_path
### Pre-condition:
	- @pre_condition_default_user_with_admin_role_permission

## Strategy
- Create User Settings overlay and page Layout Validation
	- [User Settings Top Bar]
	- [General Settings]
	- [Change Password]
	- [Active Sessions]
	- [Reset Profile]
- Create happy path Validations
	- Validate ovarlay features:
		- **Refresh Session**
		- **Private Mode**
		- **Logout**
	- Validate it is possible to edit **User Details**
	- Validate it is possible to edit **User Language**
	- Validate it is possible to edit **User Reading Options**
	- Validate it is possible to edit **Inteface Theme**
	- Validate it is possible to update **User Password**
	- [Active Sessions]
- Create negative path Validations
	- Validate it is **NOT** possible to edit **User Details**, with invalid email
	- [Session Timeout]
	- [Password Validation]
	- [Active Sessions]

## Test Scenarios:
### [User Settings Top Bar]:
	1. As a UFE user, I want to validate User Settings Overlay, is well displayed.
	2. As a UFE user, on User Settings Overlay, I want to validate it is possible to refresh User Session.
	3. As a UFE user, on User Settings Overlay, I want to validate it is possible to enable Private Mode.
	4. As a UFE user, on User Settings Overlay, I want to validate it is possible to logout.

### [General Settings]:
	1. As a UFE user, I want to validate Genral Settings Tab at User Settings page, is well displayed.
	2. As a UFE user, on Genral Settings Tab at User Settings page, I want to validate it is possible to edit User Details.
	3. As a UFE user, on Genral Settings Tab at User Settings page, I want to validate it is NOT possible to edit invalid email.
	4. As a UFE user, on Genral Settings Tab at User Settings page, I want to validate it is possible to edit User Language.
	5. As a UFE user, on Genral Settings Tab at User Settings page, I want to validate it is possible to edit User Reading Options.
	6. As a UFE user, on Genral Settings Tab at User Settings page, I want to validate it is possible to edit User Inteface Theme.

### [Change Password]:
	1. As a UFE user, I want to validate Change Password Tab at User Settings page, is well displayed.
	2. As a UFE user, on Genral Settings Tab at User Settings page, I want to validate it is possible to update User Password.

### [Active Sessions]:
	1. As a UFE user, I want to validate Active Sessions Tab at User Settings page, is well displayed.

### [Reset Profile]:
	1. As a UFE user, I want to validate Reset Profile Tab at User Settings page, is well displayed.

## To do
- In order to validate [Session Timeout], we will add timeout session (2mn or less), as configuration on a specific test journey as pre-condition and then validate on the portal. 
- In order to validate [Password Validation] Module, we will create a test that validates the Password Validation feature behaviour, with this configuration set to ON or OFF on the [[Test Journey]]
- In order to validate [Active Sessions] "Other sessions" feature,, it is necessary to run several tests in parallel using the same user, and validate that this sessions can see each other.
- In order to validate [Reset Profile] we need to before add some favourites or dashboards and then validate they are no longer configured
## Current Tests:
1. As a UFE user, I want to validate Profile Options Menu is well displayed. #Review #Execute
2. As a UFE user, I want to validate Settings page is well displayed. #Review 
	1. Join tests that validate **validate_user_settings_fields** and **validate_general_settings** **(@5877 @5878)**
3. As a UFE user, I want to validate Private Mode on Profile Options Menu. #Review  
	1. Duplicate validation on the next scenario
4. As a UFE user, I want to validate Private Mode on Profile Options Menu, persists through sessions.
5. As a UFE user, I want to validate Dark theme on Settings. #Review 
	1. Pre-condition: pre_condition_user_admin_change_theme_role_permission
	2. Add validation "through sessions"
6. As a UFE user, I want to validate Reading Direction on Settings, persists through sessions.
	1. Pre-condition: pre_condition_user_admin_reading
	4. _direction_role_permission
7. As a UFE user, I want to validate Change Language on Profile Options Menu, persists through sessions.
	1. Pre-condition: pre_condition_user_admin_change_language_role_permission
8. As a UFE user, I want to validate it is possible to edit first name, last name and email adress on user info. #Review 
	1. Add validation process
9. As a UFE user, I want to validate it is not possible to edit invalid email adress on user info.
10. As a UFE user, I want to validate it is possible to reset profile