# Microservices in Node.js

    * Microservices are an architectural approach based on building an application as a collection of small services.

## Let’s think of an application as a store.
     
     * Applications are traditionally “monolithic” which means they are built as a single, autonomous unit --think of your favorite big-box store, selling everything from bananas to lawn furniture.Everything is contained inside the unit.

     ** Let’s imagine the person - He is going inside the store to buy chewing gum and t-shirts. 

     ** He can get a shopping cart to carry his purchases, look at products in different aisles, and pay at the checkstand before leaving-essentially, everything he needs is inside the store. These could also just as easily be components of an online store application

     ** All of this is run within a single process, and if big-box store becomes very popular and we want to expand the business, we will have to add more blocks in the same unit and in the case of the online store, add more servers in order to scale it out.

     * So, every change (even minor changes) in our store (physical or online) can be slow or tedious as it affects the entire system. 

     * In the case of store, a modification can require the removal or addition of multiple  blocks, affecting the entire structure.

     * In the monolithic online store, a modification made to a small section of code might require building and deploying an entirely new version of software. 

     * So, scaling specific functions or components of the application, also means you have to scale the entire system.

# Other problems with a monolithic approach in an online application are:

    * Inflexibility:- it cannot be built using different technologies
    * Potentially unreliable:- if even one feature of the system does not work, then the entire system does not work
    * Unscalable:- applications cannot be scaled easily, since each time the application needs to be updated, the complete system has to be rebuilt
    * Not suitable for continuous development:- many features of an application cannot be built and deployed at the same time
    * Slow development:- As you can likely guess from the preceding points, development in monolithic applications takes a lot of time, since each feature has to be built individually, one after the other, rather than allowing multiple features to be worked on concurrently

# This is where microservices come to the rescue!

    * Instead of containing everything in a single unit, the microservices-based application is broken down into smaller, lightweight pieces based on a logical construct. 
    * The application consists of independent small (micro-) services, and when we deploy or scale the app, individual services get distributed within a set of machines which we call “a cluster” in the service fabric world.
    * So in online store example, perhaps one microservice contains a shopping cart, another one a product catalog, while another handles checkout, and so on. 
    * This approach allows developers to embrace compact and specialized tools that get each job done properly. 
    * Microservices are exactly that, scaled to enterprise level.

<img src = "https://images.ctfassets.net/hspc7zpa5cvq/6szXHVXaOaCxZD2ORnZ0FY/73f0df8b11694cc3274d9483a99e7f11/Microservices_Diagram.jpg">

    * Each service has its own unique and well-defined role, runs in its own process, and communicates via HTTP APIs or messaging.
    * Each microservice can be deployed, upgraded, scaled, and restarted independently of all the sibling services in the application.
    * They are typically managed by an automated system, making it possible to deploy frequent updates to live applications without affecting the end-users.
    * Following this pattern, online store will be very different: now he won’t have one big store where he can find everything he needs, but there would have multiple stores and each store will be independent and have specific functions. The first store may contain only vegetables and fruits, another one clothes, and another one, electronics.

    * All of the stores will be part of a “shopping mall” or “cluster,” and if I want to expand, scale, upgrade, or modify only the store selling clothes, the electronics store (and the rest) won’t be affected.
    * In other words, developers identify the separate service “pieces” that are logically closely related and necessary parts of a project.      
    * Then, they choose from the options available that meet their particular needs, from open source to enterprise solutions, and knit everything together into a functional application.


# Advantages of using microservices:

    * Allows us to build, operate and manage services independently, and we can easily scale them out based on the resources they need.

    * Microservices take a lot of infrastructure risk out of the project straight away. With the infrastructure made almost invisible, microservice teams can iterate quickly.

    * Each developer on a team can avoid getting tangled up in the underlying infrastructure, and focus on their piece of the project. Then, in production, if individual project modules don’t work exactly right together, it’s easy enough to isolate, disassemble and reconfigure them until they do. If shoppers aren’t big fans of the mall’s specialty ketchup store, a shoe store can be built in its place. It offers better resource utilization and cost optimization

    * Microservices have their own load balancer and execution environment to execute their functionalities, and at the same time, capture data in their own databases.

    * Finally, microservices offer language and platform freedom, so teams can choose the best language for the job at hand (even if that’s .NET for one team and Node.js for another team).


# Drawbacks of microservices:

    * Microservices are not automatically the right solution for every project. When you are running multiple instances of the same service or worker, you don’t necessarily need microservices. A well-built monolithic system can scale just as well for some classes of problems.

    * One of the big problems with microservices is “orchestration”, which means how to integrate the services with a guide to drive the process, much like a conductor in an orchestra. Integrating microservices can be quite complex.

    * Another complex process is “discovery” which is how applications and (micro)services locate each other on a network.

    * Moving away from a monolithic app architecture means the loss of an opinionated workflow that previously glued all the pieces together.

    * There is a risk in getting a very fragmented system where developers need to spend a lot of time and effort on gluing together services and tools, and where there’s a lack of common patterns and platforms that makes it difficult to work across different projects.

    * Microservices can also require increased testing complexity and possibly increased memory/computing resources.

    * It’s possible to create un-scalable microservices. It all comes down to how well you apply the fundamental principles. It’s all too easy to jump into shopping for all the microservices you want to apply without first truly considering the problem set you’re applying them to


# Creating Microservices with Node.js 

           * 1. Initial Steps
                  - Have Node.js installed
                  - Run npm init in the root folder for the project.
           * 2. Creating a Server to Accept Requests
           * 3. Defining the routes
           * 4. Adding Controller Logic
           * 5. Making the External Call
           * 6. Execution

   Code : https://blog.cloud66.com/beginners-guide-to-building-real-world-microservices-with-node-js/