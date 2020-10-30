# VUE - Part 7
> ## Objectives:
> 
> 1. Understand the interest of writing tests
> 2. Improve your testing skills
 
> ## Step 1: Understand the goal for testing. Understand the three levels of tests
>
>     Testing helps ensure that your app will work as expected for your end users. 
>     Tests improved code quality and code maintainability 
>     Tests can be considered at three levels:  
>     - Unit tests  
>     - Integration tests
>     - End-to-end tests

> ## Step 2: Understand the notion of Unit tests.
>
>     **Unit tests** test the functionality of an individual unit of code isolated from its dependencies. 
>     **Unit testing** should be combined with a **Continuous Integration (CI) process** 
>     **Unit tests shoud be run on each commit** in the repository

> ## Step 3: Using Vue Test Utils with Jest (recommended)

> 1. Install **Vue Test Utils with Jest**: npm install @vue/cli-plugin-unit-jest @vue/test-utils
> 2. At the root of the project create a file called **jest.config.js**  
>     module.exports = {
>       preset: '@vue/cli-plugin-unit-jest'
>     }
> 3. In package.json, in the scripts section add a line:
>      "test": "jest"
> 4. Run the command: **npm run test**
>     It should respond: No tests found, exiting with code 1

> ## Step 4: Write your first Unit Test
> 1. At the root of the project, create a directory  called **tests**
> 2. Under the **tests** directory create a directory called **unit**
> 3. In the **tests/unit** directory, create a file called **Login.spec.js**
>     - This file will contain all the **Unit tests** for the **Login** component
> 4. Test that the component name is **login**
> 5. Run **npm  run test**

> ## Step 5: Write the complete Test suite of the Login component

>     ✓ The Login component name should  be login  
>     ✓ The Login component should have two input fields  
>     ✓ The first input field should be named email   
>     ✓ The second input field should be named password   
>     ✓ The password field should be secured   
>     ✓ All fields fields should be empty when the component is created   
>     ✓ Mandatory fields shoud appear in black when component is created   
>     ✓ Message is empty and no message section is displayed when component is created   
>     ✓ The email field should appear in red when form is submitted with an empty email value   
>     ✓ The password field should appear in red when form is submitted with an empty password value   
>     ✓ Mandatory fields should appear in black on focus on the email field   
>     ✓ Mandatory fields in error should appear in black on focus on the password field   
>     ✓ The message 'Please fill the mandatory fields' is displayed when mandatory fields are not filled
>     ✓ The 'Please fill mandatory fields' message show disappear on focus on the email field   
>     ✓ The 'Please fill mandatory fields' message show disappear on focus on the password field   
>     ✓ A 'clean-api-message' event should be fired on form submit   
>     ✓ A 'login' event containing form data should be fired when mandatory fields are filled   
>     ✓ A message is displayed on api call failure


> ## Step 6: Write the complete Test suite for the Register component
1. List the Unit tests you will implement
2. Implement the **Register** component **Test suite** 


> ## Resources
> *https://testdriven.io/blog/vue-unit-testing/*
> *https://www.synbioz.com/blog/tech/testez-unitairement-application-vuejs-jest*
> *https://blog.octo.com/tests-unitaires-en-vue-js-avec-vue-test-utils-et-jest/*
> *https://frontstuff.io/unit-test-your-first-vuejs-component*


