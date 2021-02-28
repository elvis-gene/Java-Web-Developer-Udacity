### Choosing Java for your project? 
You should not choose Java If speed is one of your priorities.

### Development:

| Stage of Development                    |  Next Step  |
| ----------------------------------------| ----------- |
| Debugging a feature that uses a library | Review the library's reference documentation and search the web for similar issues       |
| Starting a new feature                  | Research if and how Spring supports the feature        |
| Using a library for the first time      | Read the library's getting-started documentation and usage examples |

### Java Application Server
A Java Application Server is a pluggable architecture that can host many deployed applications at once. It provides utilities like multi-threading, request filtering, and resource sharing to each application. Those applications must expose endpoints that handle the requests routed to them by the server.

#### Key Terms:
- HTTP: Hypertext Transfer Protocol. A binary protocol that originally defined the mechanics of requesting and sending HTML over the internet. HTTP is a protocol for formatting web requests so that your Application Server can understand them
- Web Server: A program that listens responds to HTTP requests over the internet
- Application Server: A program that hosts other applications, forwarding incoming requests to the appropriate application according to a filter. Provides shared access to resources and multi-threading.
- Pluggable Architecture: A pluggable architecture refers to any piece of software that allows parts of it to be added, replaced, and removed. Usually, this is achieved through a common interface for every "pluggable" component. Sometimes the architecture can even replace components at runtime, as is the case with Servlets in an Application Server.
- Threads/Threading: These terms come from concurrent programming - a thread is essentially one track of computation, and multi-threading is running multiple threads in parallel. This gets a little complicated because your CPU has a limited number of physical cores that can process instructions in parallel, while the number of threads you can have can be many more than your computer has cores, but that's a topic for another time!


#### Benefits:
- It automatically handles multiple client connections simultaneously.
- It can be configured to forward requests with custom logic.
- It can share heavyweight or universal components with each of its applications.


### Java Servlets

The <b>Servlet</b> class is the main connection between the apps you develop and the application server they run on. By extending  <b>Servlet</b>, you can create endpoints that handle incoming requests in a way specific to your application needs, and you can map specific request URLs to specialized servlets by adding entries to a <b>web.xml</b> file. The app server uses this configuration to instantiate and manage your servlets. It interacts with each through three standard methods,  <b>init</b>, <b>service</b>, and  <b>destroy</b>:

-  <b>service</b> is where requests are handled, and the server will call this method when a request is routed to the servlet it's called on.
-  <b>init</b> is where initialization of the servlet is handled, and the server will call this method directly after instantiating the servlet.
-  <b>destroy</b> is where servlet resource cleanup is handled, and is called directly before the server terminates the servlet instance.

#### Key Terms
<b>IoC</b>: Inversion of Control, which is the practice of designing libraries as application runners. This allows developers to focus on application-specific logic and rely on IoC containers to connect application components with one another, eliminating a lot of boilerplate and encouraging a clean separation of development concerns.

### Java Application Files
When you compile a Java program and package it to be run, the Java compiler creates what is called a Java ARchive, or JAR file. This file contains a compressed file hierarchy, with folders that represent Java packages that contain Java .class files, which are the compiled versions of .java source code files. It can also contain arbitrary resource files, either at the root level or deeply nested in the package hierarchy. These files often contain metadata related to the app or library contained in the JAR file, which can be read by any program that interacts with the JAR.

When you want to deploy an app to an app server, you have to package it as a Web application ARchive, or WAR file. A WAR file is almost identical to a JAR file, but includes configuration files specific to web applications. When we copy a WAR file into the deployment directory of an app server, the server unpackages it, looks for a web.xml file, and uses that file to find the classes and resources required by the application. This uses advanced Java features like reflection and class loading to programmatically load Java class definitions and instantiate them which is quite a nifty trick! It allows us to dynamically load, start, stop, and replace any number of applications in a web server at any time.

### IoC
<b>Inversion of Control</b> is one of the main features of Spring. It allows Spring to manage instances of dependencies and provide them when needed.
We could say that Spring’s ability to inject dependencies is just like the Application Server’s ability to provide <b>Servlets</b>

A design pattern in which the developer creates independent application components and uses a framework to connect them, rather than writing the integration code themselves.

<b>Dependency Injection:</b> A mechanism by which IoC may be implemented. Components are configured with dependencies on other components, which are injected at runtime. Injection is quite literal - a component's dependencies are usually expressed as annotated fields on the component class, and Spring will populate those fields with the dependencies at runtime.


