# Test Cases
## Tags:
Here you can find a quick list of the tags used on this feature
### Test Type:
	- @back_office
	- @layout
	- @happy_path
	- @negative_path
### Pre-condition:
	- We need to create the qa-overlay, that will contain all the configurations to be tested and used on our scenarios.
	- Create [qa-app / qa-widget / qa-component] containing at least 2 configurations with at lest this subConfigurations:
		- 2 boolean configuration side by side, 
		- 2 snippet configuration side by side,
		- 1 image
#### Tags:
	- 
## Strategy:
	- Create Layout Validation for each sub feature
	- Create happy and negative path Validations for each sub feature
## Back Office Tests:
### Home Page:
	1. As a UFE user, I want to validate Backoffice Home page, is well displayed.
	2. As a UFE user, on Backoffice Home page, I want to validate search area is well displayed.
	3. As a UFE user, on Backoffice page, I want to validate that it is possible to search by a valid item.
	4. As a UFE user, on Backoffice page, I want to validate that it is NOT possible to search by an invalid item.
	5. As a UFE user, on Backoffice Home page, I want to validate import area is well displayed.
	6. As a UFE user, on Backoffice page, I want to validate that it is possible to import a valid item.
	7. As a UFE user, on Backoffice page, I want to validate that it is NOT possible to import an invalid item.
	8. As a UFE user, on Backoffice Home page, I want to validate export area is well displayed.
	9. As a UFE user, on Backoffice page, I want to validate that it is possible to export a specific configuration when multiple projects are selected.
	10. As a UFE user, on Backoffice page, I want to validate that it is possible to export a valid item.
	11. As a UFE user, on Backoffice page, I want to validate that it is NOT possible to export an invalid item.
	12. As a UFE user, on Backoffice Home page, I want to validate settings area is well displayed.
	13. As a UFE user, on Backoffice page, I want to validate that it is possible to enable/disable the Developer Mode.
	14. As a UFE user, I want to validate Backoffice Platform Index, is well displayed.

### Platform Page:
	1. As a UFE user, I want to validate Backoffice Platform page, is well displayed.
	2. 
	3. As a UFE user, on Platform page I want to validate UFE default configurations are applied when there is no custom configurations. #IntegrationTest
	4. As a UFE user, on Platform page I want to validate it is possible to change how multiple interactions are open - to complex should be done on E2E
	5. As a UFE user, on Platform page I want to validate it is possible to change the circular progress ui theming. #IntegrationTest include on overlay configurations
	6. As a UFE user, on Platform page I want to validate it is possible to change the default behavior of dispatching the filter journeys on menu on text update. validate what is the expected result
	7. As a UFE user, on Platform page I want to validate it is possible to change the default behavior of the menu ordering in UFE.
	8. As a UFE user, on Platform page I want to validate it is possible to change the session timeout expiration times.
	9. As a UFE user, on Platform page I want to validate it is possible to update the default save timeout of the journeys.
	10. As a UFE user, on Platform page I want to validate it is possible to update the notifications filter button type
	11. As a UFE user, on Platform page I want to validate it is possible to update the header extension manifest.
	12. As a UFE user, on Platform page I want to validate it is possible to update the categories manifest.
	13. As a UFE user, on Platform page I want to validate it is possible to update the journeys manifest.
	14. As a UFE user, on Platform page I want to validate it is possible to change the values of entitlements used in the Unified Front End.
	15. As a UFE user, on Platform page I want to validate it is possible to change the notifications configuration to use the snackbar aggregator or not
	16. As a UFE user, on Platform page I want to validate it is possible to update the date type of the notifications.
	17. As a UFE user, on Platform page I want to validate it is possible to update the configuration stating if only snackbar notifications should be used.
	18. As a UFE user, on Platform page I want to validate it is possible to update the manifest of the Floating Components.
	19. As a UFE user, on Platform page I want to validate it is possible to set the 360 expanded panel size.
	20. As a UFE user, on Platform page I want to validate it is possible to set the 360 to start as collapsed.
	21. As a UFE user, on Platform page I want to validate it is possible to change the search results fields of the 360 context search.
	22. As a UFE user, on Platform page I want to validate it is possible to change the maximum number of interactions open at the same time.
	23. As a UFE user, on Platform page I want to validate it is possible to change collapsed 360 panel size width.
	24. As a UFE user, on Platform page I want to validate it is possible to set if 360 opens with one result automatically or not.
	25. As a UFE user, on Platform page I want to validate it is possible to badly configured config are presented in text format in correct place.
	26. As a UFE user, on Platform page I want to validate it is possible to badly configured configs are presented in defined place.
	27. As a UFE user, on Platform page I want to validate it is possible to badly configured configs displays an error message after section/sub-section description.
	28. As a UFE user, on Platform page I want to validate it is possible to save changes in configs despite errors in other configs.
	29. As a UFE user, on Platform page I want to validate it is possible to change the authentication url.
	30. As a UFE user, on Platform page I want to validate it is possible to change the channel identifier of the authentication.
	31. As a UFE user, on Platform page I want to validate it is possible to change responsive configurations

### Apps Page:
	1. As a UFE user, I want to validate Backoffice Apps page, is well displayed.
	2. As a UFE user, I want to validate that my test app is installed and correctly displayed.
### Widgets Page:
	1. As a UFE user, I want to validate Backoffice Widgets page, is well displayed.
	2. As a UFE user, I want to validate that my test widgets are installed and correctly displayed.
### Components Page:
	1. As a UFE user, I want to validate Backoffice Components page, is well displayed.
	2. As a UFE user, I want to validate that my test components are installed and correctly displayed.

# Improvments
## UFE
### Home
#### Session Timeout Settings
![[Pasted image 20221229162434.png]]
Expiration objects should be grouped
#### Authentication
![[Pasted image 20221229164117.png]]
Objects Title is not idented

#### User Settings
![[Pasted image 20221229170323.png]]

## Task to be deleted

- 7983
- 7990
- 7991