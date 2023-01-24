## Tags:
Here you can find a quick list of the tags used on this feature

### Test Type:
	- @login
	- @layout
	- @happy_path
	- @negative_path
### Pre-condition:
	- @pre_condition_default_user_with_admin_role_permission
	- @pre_condition_default_user_with_admin_role_permission_and_domain

## Strategy:
	- Create Login page Layout Validation
	- Create happy path Validation
		- Login with username/password
		- Login wiwth domain/password
	- Create negative path Validation
		- No credentials at all
		- Invalid credentials

## Login Tests:
	1. @As a UFE user, I want to validate Login page, is well displayed.
	2. As a UFE User, I want to validate it is possible to login with a valid Username.
	3. As a UFE User, I want to validate it is possible to login with a valid Domain.
	4. As a UFE User, I want to validate it is NOT possible to login with a Invalid Credentials.
	5. As a UFE User, I want to validate it is NOT possible to login with No Credentials.

## To Do
	- Create specific journey to validate federeated login its displayed only when have federated permissions 

## Mapping to Old Tests:
1. @1974 - Login Testing With Valid Credentials - @happy_path @tc001 #TaskReview
2. @1976 - Login Testing Without Credentials -> @negative_path @tc002 #TaskReview
3. @1976 - Login Testing With Wrong Credentials -> @negative_path @tc001 #TaskReview
4. @1982 - Login Testing With Valid Domain Credentials -> @happy_path @tc002 #TaskReview