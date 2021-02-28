### Which of the following projects is not a good fit for Java and Spring Boot?
 
- A graphics processing application
- An e-commerce website
- A note-taking app
- An online video game

SOLUTION: A graphics processing application


### What are some services that Spring helps manage for us?

WRONG:
- Running Multiple Java Programs in Parallel
- Responding to Browser Requests
- 
RIGHT:
- Login Security
- HTML Generation
- Database Access


### What's the relationship between the Application Server and a Servlet?
Application Servers receive HTTP requests, parse the information, and send it to all the Servlets at once.

### Application Server Vs Servlet
An Application Server can load Servlets from a WAR file at any time.

### Relationship between Spring and a Java Application Server
Spring dispatches Servlet requests from the Application Server to specific Java code to handle the requests.

### Edge Case: When You Can't Use Spring Boot Intuition Quiz
Consider the following scenarios and decide if you can use Spring Boot in each of them. Mark each scenario where Spring Boot is a viable choice.
- <b>WRONG</b>: A project that already uses Spring
- <b>WRONG</b>: A project that uses Java EE Enterprise Java Beans and JNDI
- <b>RIGHT</b>: A project that uses Oracle WebLogic as an Application Server
- <b>RIGHT</b>: A project that uses plain Servlets to handle requests

### Edge Case: When You Can't Use Spring Boot Knowledge Quiz
Spring Boot is great, but sometimes you’ll have to configure Spring manually or work in an environment where Spring is not available. Which of the following scenarios might result in a configuration that doesn’t use Spring Boot?
 
- <b>RIGHT</b>: This project uses Java EE instead of Spring
- <b>WRONG</b>: This project that needs to work with a legacy database
- <b>RIGHT</b>: This project utilizes many features specific to one application server in particular

Sometimes, it's not an option to use Spring Boot in a project. Usually, this is because some form of IoC has already been implemented, or it would take a lot of time to rewrite the code to use Spring Boot. Sometimes, though, it's worth adding Spring or Spring Boot to a project by refactoring the code and adding the Spring Servlet manually. More information on this can be found in the Further Research section, but this won't be a focus for the course - just remember that it takes a decision and some setup to use Spring in an application, and not all applications do!
