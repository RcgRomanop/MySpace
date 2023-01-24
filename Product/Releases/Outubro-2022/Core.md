## Automation Results
### Reference Data
- **15432 -** [Add entries to a Reference Data Entry] - Adapt test validation so it expects a 400 with a specific error message.
	- Current validation: Expecting 500
	- Current Response: 400, error message
		{
			  "statusCode": 400,
			  "errorCode": "P009",
			  "message": "Parameter validation failure",
			  "details": [
				{
				  "reference": "data",
				  "message": "may not be empty"
				},
				{
				  "reference": "group",
				  "message": "may not be empty"
				}
			]
		}
	- Comment: Review with **Miguel Gomes** the error message
- **15439 -** [Get all representations of an entity grouped by group name] - Service returns error once it doesn t recognize the requested entity 
	- Current validation: Expecting 200, (entity exists)
	- Current Response: 404, error message didn't translate ''{0}''
		{
			  "statusCode": 404,
			  "errorCode": "REFERENCEDATA404",
			  "message": "Reference Data - not found: The entity doesnt exists: {0}",
			  "details": []
		}
	- Comment: Review with **Miguel Gomes** the error message and validate the entity that we are currently using
- 20006 - [Get reference data by identifier] - Service returns error once it doesn t recognize the requested identifier
	- Current validation: Expecting 200, (identifier exists)
	- Current Response: 404, error message didn't translate ''{0}''
		{
			  "statusCode": 404,
			  "errorCode": "REFERENCEDATA404",
			  "message": "Reference Data - not found: Entity not found with given identifier: d157d0ea-9ca7-427b-b2a2-7723a73d6951",
			  "details": []
		}
	- Comment: Validate the identifier that we are currently using

### User Access Management
- 2220 - [CreateUser - firstName, lastName, email and authenticatorName] - Service returns authentication error 
	- Current validation: Expecting 200, user created
	- Current Response: 404, 
		{
			  "statusCode": 404,
			  "errorCode": "UAM018",
			  "message": "Authenticator not found: authenticatorNameTest",
			  "details": []
		}
	- Comment: Validate the authenticatorName that we are currently using
- 2228 - [GetAllUsers - with valid sort] - Refactor validation process
	- Current validation: Expecting to validate that it is possible to sort by "firstName"
	- Current Response: Service correctly  sort the  list by numbers then letters
	- Comment: Adapt validate action or validate if it is possible to validate using unit tests
- 2231 - [DeleteUser and GetUserById with success] - Validate if the requested user is correct #Review 
- 2233 - [UpdateUserById - invalid cases] - Service returns authentication error 
	- Current validation: Expecting 200, user created
	- Current Response: 404, 
		{
			  "statusCode": 404,
			  "errorCode": "UAM018",
			  "message": "Authenticator not found: authenticatorNameTest",
			  "details": []
		}
	- Comment: Validate the authenticatorName that we are currently using
- 2247 - [GetUserProperties - with limit and sort] - Test data unresolved #Review 
- 2267 - [GetUserPropertiesByExpression - with limit and sort] - Test data unresolved #Review 
- 2269 - [UpdateUserPropertyById - invalid cases] - Adapt test validation so it expects a 400 with a specific error message.
	- Current validation: Expecting 500
	- Current Response: 400, error message
		{
			  "statusCode": 400,
			  "errorCode": "P009",
			  "message": "Parameter validation failure",
			  "details": [
			    {
			      "reference": "name",
			      "message": "may not be empty"
			    }
			  ]
		}
	- Comment: Review with **Miguel Gomes** the error message
- 2278 - [CreateRole - invalid cases] - Adapt test validation so it expects a 409 with a specific error message. #Review 
	- Current validation: Expecting 500
	- Current Response: 409, error message
		{
			"statusCode": 409,
			"errorCode": "UAM008",
			"message": "Role already exists: invalidtest",
			"details": []
		}
	- Comment: Review with **Miguel Gomes** the error message
- 2286 - [UpdateRoleById - invalid cases] - Adapt test validation so it expects a 400 with a specific error message.
	- Current validation: Expecting 500
	- Current Response: 400, error message
		{
			  "statusCode": 400,
			  "errorCode": "P009",
			  "message": "Parameter validation failure",
			  "details": [
			    {
			      "reference": "name",
			      "message": "may not be empty"
			    }
		  ]
		}
	- Comment: Review with **Miguel Gomes** the error message
- 2287 - [UpdateRoleById and DeleteRoleById with success] - Update test and re-execute
- 2288 - [UpdateRoleById - update partially with success] - Update test and re-execute
- 2323 - [CreatePermission - invalid cases] - Adapt test validation so it expects a 400 with a specific error message.
	- Current validation: Expecting 500
	- Current Response: 400, error message
		{
			  "statusCode": 400,
			  "errorCode": "P009",
			  "message": "Parameter validation failure",
			  "details": [
			    {
			      "reference": "name",
			      "message": "may not be empty"
			    }
		  ]
		}
	- Comment: Review with **Miguel Gomes** the error message
- 2332 - [UpdatePermissionById - invalid cases] - Adapt test validation so it expects a 400 with a specific error message.
	- Current validation: Expecting 500
	- Current Response: 400, error message
		{
			  "statusCode": 400,
			  "errorCode": "P009",
			  "message": "Parameter validation failure",
			  "details": [
			    {
			      "reference": "name",
			      "message": "may not be empty"
			    }
		  ]
		}
	- Comment: Review with **Miguel Gomes** the error message