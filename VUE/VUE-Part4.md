# VUE - Part 4
> ## Objectives:
> 
> 1. Enhance your coding skills with Vue.js

> ## Step 1: Implement the [User Story] Add a Blog link in the navigation bar
> 
>     [User story] Add a Blog link in the navigation bar
>       ID:  US-1 
>       Type: Functional     
>       Description:      
>         As a user of the Blog feature    
>         I want to click on a Blog link  
>         So that I can access to the Blog feature
>       Business rules:  
>         The Blog page will be implemented as a component called Blog
>         The Blog feature will be accessible as the /blog URL
>         The Blog component will be placed in the views directory
>       Acceptance tests:  
>         Blog link added in the navigation bar. 
>         Access to Blog feature successful when the link is clicked
>         The Blog component is in the views directory

> ## Step 2: Implement the [User Story] Setup the layout of the Blog feature
> 
>     [User story] Setup the layout of the Blog feature
>       ID:  ES-2 
>       Type: Non functional     
>       Description:      
>         As a user of the Blog feature    
>         I want the Blog to have the usual layout 
>         So that I can use the Blog feature easily
>       Business rules: 
>         The layout will be made of 3 sections (Header, Left, Right) 
>         The Header section will cover 100% of the screen with
>         The Left section will cover 75% of the screen width
>         The Right section will cover 25% of the screen with.
>         The Blog layout will be implemened as a component name BlogLayout
>         The three sections will be implemented as components (BlogLayoutHeader, BlogLayoutLeft and BlogLayoutRight). 
>         All the components needed for the layout will be placed in the components directory
>       Acceptance tests:  
>         The Blog feature has the usual layout
>         The Blog page relies on the BlogLayout component
>         All the components used for the layout are in the components directory

## Step 3: Implement the [User Story] List of the most recently published posts 
> 
>     [User story] List of the most recently published posts 
>       ID:  US-2 
>       Type: Functional     
>       Description:      
>         As a user of the Blog feature    
>         I want to have of list of the most recently published posts
>         So that I can read them as soon as there are published
>       Business rules: 
>         The Blog page will display a list of the most recently published posts 
>         A maximum of four posts will be displayed on this list
>         The list will be implemented as a component called BlogPostList
>         Each item in the list will be implemented as a component called BlogPost
>         The BlogPost component will display the following informations: publication date, title, summary and a 'Read more link'
>         The list will be ordered (the most recent post the first)
>       Acceptance tests:  
>         The Blog page displays the list of most recently published posts
>         The list displays a maximum of four posts
>         The list is well ordered
>         An item will be implemented as in a BlogPost component
>         The BlogPost component will be placed in the components directory
>         The BlogPost component will display the following informations: publication date, title, summary and a 'Read more link'

## Step 4: Implement the [User Story] Navigate from the list page to the detail page 
> 
>     [User story] Navigate from the list page to the detail page
>       ID:  US-3 
>       Type: Functional     
>       Description:      
>         As a user of the Blog feature    
>         I want to navigate from the list page to a given post when I click on the 'Read more' link
>         So that I can read the full content of the post
>       Business rules: 
>         The post page will be implemented as a component called BlogPost
>         The BlogPost component will be placed in the views directory (because it is routable)
>         The BlogPost page will follow the usual layout of the blog
>         The BlogPost page will be accessible through the /blog/post/:id url
>         A click on a 'Read more' link will display the BlogPost page
>       Acceptance tests:  
>         Navigation is possible from list to detail 
>         The Blog page follows the layout of the Blog feature
>         A Blog post is accessible through the /blog/post/:id url



