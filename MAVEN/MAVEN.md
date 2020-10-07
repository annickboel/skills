# MAVEN
## Objectives:

1. Understand the interest of using MAVEN in a java project.
2. Write JUnit test cases.
3. Use third party librairies in a Java project



## Step 1: Create a minimal app

Create a java package named com.mycompany.app.

Inside this package create a class called App.java

Inside the main method, output the string "Hello World!" to the console

Compile the code

Package the code as a jar named my-app.jar

Run the program

## Step 2: Test the minimal app
Using JUnit, write a test to verify the app is working as expected

## Step 3: Install Maven 3.6.3
Ensure Maven is successfully installed running the command mvn --version.

## Step 4: Create a MAVEN project  
Create a directory called my-app

Inside this directory create a MAVEN project using mvn archetype:generate

Expliquez ce qui a été créé par MAVEN :	

- Arborescence pour le code	

- Arborescence pour les tests	

- pom.xml

> ### Step 5: Utiliser Maven 
>
> 1. Reporter le code de l'application au sein de l'arborscence MAVEN 
> 2. Reporter le code du test au sein de l'arborescence MAVEN
> 3. Lancer la commande MAVEN qui permet de compiler le code Java
> 4. Lancer la commande MAVEN qui permet de créer un livrable sous forme de jar
> 5. Une fois le livrable constitué, lancer le programme
> 6. Quel est l'intérêt d'utiliser MAVEN?


> ### Step 6: Write JUnit tests
> 
> 1. Create a new package **com.mycompany.maths**.
> 2. Inside this package  create a class called **Operations**.
> 3. The **Operations** class must Implement the following methods:
> 	- *public int add(int a, int b);*
> 	- *public int sub(int a, int b);*
> 	- *public int mul(int a, int b);*
> 	- *public int div(int a, int b);*
> 	- *public int mod(int a, int b);*
> 4. Write Junit tests for the Operations class 









## Resources
### https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html




