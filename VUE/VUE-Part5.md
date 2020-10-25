# VUE - Part 5
> ## Objectives:
> 
> 1. Understand state management in a SPA. 
> 2. Use VueX to create and manage a centralized state.
> 3. Understand the notion of smart and dumb components.
> 4. Call an API with axios
> 5. Understand the VueX notions of mutations and actions
> 6. Subsribe to changes in the centralized store

## Step 1: Create a centralized state manager with VueX
>  VueX will be used to create a centralized store where the global state of the application will be managed
>  1. Install VueX in the application via the CLI, using the command **vue add vuex**
>  2. Inspect the artifacts created by the command and list those artifacts.
>  3. Answer the question: What's the name of the centralized state manager?
>  4. Answer the question: Why to we need a centralized state manager?

## Step 2: Describe the initial state of the Blog feature.
>  1. List the variables we need to describe the state of the Blog feature.
>     - For each variable, describe it's name, type and value
>  2. In the state property of the store, setup the Blog feature initial state.

## Step 3: Read data from the centralized store. Understand the notion of Smart and Dumb components
>  The **[User story] List of the most recently published posts** will be refactored to use a centralized store
>  1. In the **data** function of the Blog component return an empty object
>  2. In the **computed** section of the Blog component:
>     - Use the **mapState helper** to retrieve the blogposts array from **the centralized store**
>     - In the mounted method, log the the content of the blogposts array
>  Note: 
>     - The Blog component has access to the centralized store. 
>     - The children of the Blog component do not have access to the centralized store. 
>  3. Answer the question: What's the qualifier of a component which has access to the store?
>  4. Answer the question: What's the qualifier of a component which doesn'h have access to the store?

> ## Step 4: [User Story] Blog API
>     [User story] Blog API
>       ID:  ES-3 
>       Type: Non functional     
>       Description:      
>         As a Conceptor of the Blog post feature 
>         I want to consume an API
>         So that easily Create, Read, Update, Delete posts
>       Business rules:
>         The API entrypoint will be api/v0 with the follow endpoints:
>           - api/blogposts (POST): Create a post
>           - api/blogposts (GET) : List the posts
>           - api/blogposts/:id (GET) : Read a post
>           - api/blogposts/:id (PUT): Updata a post
>           - api/blogposts/:id (DELETE): Delete a post
>       Acceptance tests:  
>         The API is available when the application starts
>       Notes:
>           For the sake of simplicity, the API will be a fake REST API:
>           - The API will be embedded in the Vue application
>           - The API will be implemented with JSON Server.
>           - The API will be installed in the api directory as a db.json file

> ## Step 5: Modify the state using actions and mutations. Subscribe to changes in the state
> In this state we'll use the **Blog API** to retrieve the list of the most recently published posts
> 1. Install the axios library using **npm install --save axios**  
>   - An API call is asynchronous. 
>   - There are 3 possible states in an API call: loading, success and failure  
>  2. In the store add a property called **fetchBlogListStatus** initialized as null
>  The API call will be make by **dispatching an action** in the centralized store.
>  3. In the **beforeCreate** hook of the Blog component, dispatch an **action** called **fetchBlogList**
>  4. In the **actions** section of the store, create a **action** called **fetchBlogList**
>     - An **action** is a method with tow parameters : context and payload, the payload parameter is optional
>     - An **action** will coordinate several **mutations** in the state
>  5. Log a message to ensure the **fetchBlogList** action is called when the Blog page is displayed.
>  6. In the **mutations** section of the store, create a **mutation** called **SET_FETCH_BLOG_LIST_LOADING**
>     - A **mutation** updates one or more properties in the state in a **synchronous** way
>     - A **mutation** is a method with two parameters : state and payload
>     - The SET_FETCH_BLOG_LIST_LOADING will set the **fetchBlogListStatus** property from null to 'loading', the **errorMessage** property  to an empty string and the **blogposts** property to a empty array
>     - Commit this mutation in the **fetchBlogList** action
>  7. In the **fetchBlogList** action :
>     - Call the Blog API using the axios http client. 
>     - Log the response, in the **then** function of the API call
>     - Log the error, in the **catch** function of the API call
>  8. In the **mutations** section of the store, create a **mutation** called **SET_FETCH_BLOG_LIST_SUCCESS**
>     - This mutation will set **fetchBlogListStatus** property from '**loading**' to '**success**' and the **blogposts** property to the data retrieved from the API call
>     - **Commit** this **mutation** in the **then** function of the API call.
>  9. In the **mutations** section, create a **mutation** called **SET_FETCH_BLOG_LIST_FAILURE**
>     - This **mutation** will set **fetchBlogListLoading** property from '**loading**' to '**failure**' and the **errorMessage** to the data retrieved from the API call
>     - **Commit** this **mutation** in the **catch** function of the API call.
>  10. **Subscribe** to changes in the state, so that the Blog component **will react to changes in the state** and render again.  
>     - In the **data** section of the **Blog** component, add two properties: **status** and **message**  
>     - In the **created** hook of the **Blog** component, subscribe to **mutations** of the state to update the **status**, **errorMessage** and **list** properties in the **data** section. 
>     - In the **beforeDestroy** of the **Blog** component, **unsubscribe** to **mutations** on the state
>  11. Tests  
>     - Check that a 'Loading....' message is displayed during API call  
>     - Check that the list of most recently published post is successfully displayed  
>     - Check that a error message is displayed in case of API call failure  

> ## Step 6: [User Story] - Display the full content of a blog post (Refactoring)
> 1. Refactor this User Story to use the BlogAPI

> ## Resources
> *https://vuex.vuejs.org/guide/state.html*
> *https://dev.to/viniciuskneves/watch-for-vuex-state-changes-2mgj*


