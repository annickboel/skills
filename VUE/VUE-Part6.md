# VUE - Part 6
> ## Objectives:
> 
> 1. Improve your coding skills by implementing the Login/Register/Logout mechanism
 
> ## Step 1: [User Story] Register UI setup
>     [User story] Register UI setup
>       ID:  ES-4 
>       Type: Functional     
>       Description:      
>         As a Designer of the site 
>         I want to have a Register page
>         So that the users of the site can create an account
>       Business rules:
>         A Register link will be added in the navigation bar
>         On click on the Register Link, the user will be redirected to the Register page
>         The Register page will be implemented as a component called Register
>         The Register page will follow the base layout of the site
>         The BaseLayout of the site displays 3 sections: header, content and footer
>         The header section will cover 100% of the screen with 
>         The content section will cover 100% of the screen width
>         The footer section will cover 100% of the screen with and 20% of the screen height
>         The three sections will be implemented as components (BaseLayoutHeader, BaseLayoutContent and BaseLayoutFooter). 
>         The Register page will display:
>         - The title of the page in the header section. This title must not be displayed
>         - A Register form where the user can enter the following informations: firstName, lastName, email, password, password confirmation, function, company
>         - A button called Register
>         The firstName, lastName, email, password and password confirmation fields are mandatory
>         An error message will be displayed on form submit if: 
>         - Mandatory fields are not filled (empty mandatory fields should appear in red) 
>         - Passwords are not identical  
>         The error message disappears on focus in a mandatory field  
>         Fields in error will appear in black on focus on any mandatory field 
>         On form submit the user profile will contain form data  
>       Acceptance tests:  
>         A Register Link is added in the navigation bar
>         On click on the Register Link, the user is redirected to the Register page  
>         The Register page follows the base layout of the site
>         The Register form displays the relevant information
>         An error message is displayed when mandatory fields are not filled on form submit  
>         Empty mandatory fields appear in red on form submit
>         The error message disappears on focus in any mandatory field
>         Fields in error appear in black on focus in any mandatory field
>         On form submit the user profile contains form data


 > ## Step 2: [User Story] Login UI setup
>     [User story] Login UI setup
>       ID:  ES-4 
>       Type: Functional     
>       Description:      
>         As a Designer of the site 
>         I want to have a Login page
>         So that the users of the site can authenticate
>       Business rules:
>         A Login link will be added in the navigation bar
>         On click on the Login Link, the user will be redirected to the Login page
>         The Login page will be implemented as a component called Login
>         The Login page will follow the base layout of the site
>         The Login page will displays
>         - The title of the page in the header section. This title must not be displayed
>         - A Login form where the user an enter the following informations: email and password.
>         - A button called Login
>         The email and password fields are mandatory
>         A error message will be displayed if:
>         - Mandatory fields are not filled (empty mandatory fields should appear in red) 
>         The error message disappears on focus in any mandatory field  
>         Fields in error will appear in black on focus in any mandatory field 
>         On form submit the usercontains form data  
>       Acceptance tests:  
>         A Login Link is added in the navigation bar
>         On click on the Login Link, the user is redirected to the Login page
>         The Login page follows the base layout of the site
>         The Login form displays the relevant information
>         An error message is displayed if the mandatory fields are not filled on form submit
>         Empty mandatory fields appear in red on form submit
>         The error message disappears on focus in any mandatory field
>         Fields in error appear in black on focus in any mandatory field
>         On click on the Login button the user is logged to the console.

> ## Step 3: Setup the User API
>     [User story] User API
>       ID:  ES-X 
>       Type: Non functional     
>       Description:      
>         As a Designer of the site 
>         I want to consume an API
>         So that easily users can register, login and logout
>       Business rules:
>         The API entrypoint will be api/v0 with the follow endpoints:
>           - api/users/ (POST): Create a user profile
>           - api/users (GET) : List the user profiles
>           - api/users/:id (GET) : Read a user profile
>           - api/users/id/:id (PUT): Update a user profile
>           - api/users/:id (DELETE): Delete a user profile
>       Acceptance tests:  
>         The User API is available when the application starts
>       Notes:
>           For the sake of simplicity, the API will be a fake REST API:
>           - The API will be embedded in the Vue application
>           - The API will be implemented with JSON Server.
>           - The API will be installed in the api directory as a db.json file

## Step 4: [User Story] Register
>     [User story] Register
>       ID:  US-X 
>       Type: Functional     
>       Description:      
>         As a User of the site 
>         I want to create an account 
>         So that I can access to features protected by authentication
>       Business rules:
>         The Register mechanism will rely on the User API
>         The state will be maintained in the centralized store
>         Registration with an already existing email will be forbidden. An error message will be displayed
>         On successfull registration: 
>         - 'Logged as' and Logout sections will be added in the navigation bar
>         - Login and Register links will disappear
>         - A new user profile will be added in the fake database 
>         - The user will be considered as authenticated.
>         - The user will be redirected to the Home page
>       Acceptance tests:  
>         After successfull registration a new profile has been added in the fake database
>         A error message is displayed if the email is already existing
>         The registered user is considered as authenticated
>         'Logged as' and Logout section have been added in the navigation bar
>         Login and Register are no more present
>         The registered user is redirected to the Home page

## Step 5: [User Story] Login
>     [User story] Login
>       ID:  US-X 
>       Type: Functional     
>       Description:      
>         As a User of the site 
>         I want to login 
>         So that I can access to features protected by authentication
>       Business rules:
>         The Login mechanism will rely on the User API
>         The state will be maintained in the centralized store
>         On login success: 
>         - 'Logged as' and Logout sections will be added in the navigation bar
>         - Login and Register links will disappear
>         - The user will be considered as authenticated.
>         - The user will be redirected to the Home page
>         On login failure:
>         - An error message will be displayed
>       Acceptance tests:  
>         A error message is displayed if the credentials are not valid
>         A 'Logged as' section has been added in the navigation bar
>         The authenticated user is redirected to the Home page

## Step 6: [User Story] Logout
>     [User story] Logout 
>       ID:  US-X 
>       Type: Functional     
>       Description:      
>         As a User of the site 
>         I want to logout 
>         So that I can quit my session
>       Business rules:
>         A logout link will be added in the navigation bar
>         The state will be maintained in the centralized store
>         On logout: 
>         - 'Logged as' and Logout sections will disappear
>         - Login and Register links will be displayed
>         - The user will be redirected to the Home page
>       Acceptance tests:  
>         A error message is displayed if the credentials are not valid
>         A 'Logged as' section has been added in the navigation bar
>         The authenticated user is redirected to the Home page


> ## Resources
> https://fr.vuejs.org/v2/cookbook/using-axios-to-consume-apis.html
>

