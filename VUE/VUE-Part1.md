# VUE - Part 1
> ## Objectives:
> 
> 1. Understand the concept of SPA
> 2. Bootstrap a SPA application with Vue
> 3. Understand the properties of a Vue instance (el, data, computed, methods)
> 4. Use Vue directives (v-if, v-else, v-for, v-bind, v-on, v-show, v-model)

> ## Step 1: Bootstrap a SPA application
> 
> 1. Create a html page called **index.htm**
> 2. Insert a **div** with id **app**
> 3. Insert the script to include the Vue.js framework
> 4. Insert a script to create a **Vue instance** called app, to **handle the app div**

> ## Step 2: Define and use a datastore in your app.
> 
> 1. Inside this script that defines the **Vue instance**, define a **datastore**
> 2. Answer the question: What is a datastore in Vue.js?
> 3. Inside the datastore, define the following properties:
>  -  **stringData** of type String
>  -  **numberData** of type number
>  -  **booleanData** of type boolean
>  -  **arrayData** of type array
>  -  **objectData** of type Object 
> 4. Display the data in the app div using the **mustache syntax**

> ## Step 2: Define and use computed properties

> 1. To handle a ecommerce cart, define the price of 3 products in your datastore. 
> 2. Define a **computed property** called **totalAmount**. The function will compute total price for items in the cart
> 3. Answer the question: What is a computed property in Vue.js?
> 4. Display the cart 

> ## Step 3: Use Vue.js directives (v-for)
>
> 1. In the datastore, define a items property as and array of objects.
>   - The object structure will define the name and the price of a  item 
>   - The array will define 6 items.
> 2. Use the v-for directive to display the lines of the cart
> 3. Adapt the **totalAmount** function to use the items array
> 4. Diplay the cart


> ## Step 4: Use Vue.js directives (v-if, v-else)
>
> 1. Use the v-if, v-else directives to display two different backgrounds for the cart items (either the index line is odd or even)
> 2. Create styles for your app to define the odd and even backgrounds
> 4. Diplay the cart


> ## Step 5: Use Vue.js directive (v-bind)
>
> 1. Add a url property to each item in the datastore.
> 2. Add a anchor to allow navigation to each item page.
> 3. Use the v-bind directive to bind the href attribute to the url property of the item. 
> 4. Diplay the cart. Check the anchors are working as expected
> 5. Answer the question: What's the use of v-bind?

> ## Step 6: Use Vue.js directive (v-on) and react to an event
>
> 1. Define a button. This button will be used to toggle display of the cart
> 2. Add a boolean property in the datastore called **visible**
> 3. Add a method in the Vue instance called **toggleDisplay**
>    - The method will change the value of the visible poperty
>    - Log the value of the visible property to the console
> 4. Use the v-on directive to react to a click event on the button by calling the **toggleDisplay method**
> 5. Check that the value of the visbible property is changed on button click

> ## Step 7: Use Vue.js directive (v-show) and react to an event
>
> 1. Add a div around the cart
> 2. Use the v-show directive in this div. The v-show diretive will be associated to the visible property.
> 3. Check that the Cart is toogled by the Toggle display button.

> ## Step 8: Use the Vue.js directive (v-model and v-bind:class) 
>
> 1. In the data section of the vue intance, define the following properties (**profiles, profile, user, logged, messgae**)
>   - The **profiles** property is defined as an array of user objects
>   - The **profile** property is defined as an object with the following properties (firstName, lastName, email and password)
>   - The **user** property is defined as an object with the following properties (email and password)
>   - The **logged** property is a boolean
>   - The **message** property is a string
> 2. Define three links (**Login, Register and Logout**) and a **'Logged as:'** that displays user firstName and lastName
> 3. Define a Register form 
>    - The form will have for input fields (firstName, lastName, email and password) and a Register button.
>    - Use the **v-model directive** inside the form to enable to fill the **profile** property
>    - On click on the Register button, the **profiles** property and **logged** properties will be updated. 
The Register form will disappear. The 'Logged as:' and the Logout link will appear
>    - Display a error message if you try to register an already existing user. 
> 4. Define a Login form 
>    - The form will have for input fields (email and password) and a Login button.
>    - Use the **v-model directive** inside the form to enable to fill the **user** property
>    - The Login form must be displayed, if the user is not logged.
>    - On click on the Login button and **on login successfull** : The **logged** property will be updated. The Login form will disappear. The 'Logged as:' and the Logout link will appear
>    - On click on the Login button and **on login failure** : A error message will be displayed.
> 5. Implement the logout process 

> ## Step 9: Tests

> In this part, no Unit tests will be implemented. Your tests will be done through the UI.

>    - List the tests you have made, and give each Test a name (Ex: DisplayLoginLinkTest)

> ## Resources
> *https://openclassrooms.com/fr/courses/6390311-creez-une-interface-web-progressive-avec-vue-js*
> *https://fr.vuejs.org/v2/*




