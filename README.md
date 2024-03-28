# Node.js Backend Architectures

Exploring popular backend architectures with Node.js & TypeScript. 

All of these architectures & patterns focus on same thing. **Separation of Concerns**, **Testability**, **Maintainability**. Following a set of rules from one or more of these architectures can help to create softwares that are easier to evolve and test over time.

All popular architecture have a few things in common. Most have layers like **Domain Layer**, **Application Layer**, **Infrastructure Layer** and **Presentation Layer**. The Domain Layer is the core of the application, it contains the business logic. The Application Layer contains the usecases, the business rules. The Infrastructure Layer contains the database, the web server, the external services. The Presentation Layer contains the UI, the API, the CLI.

In all architecture, **dependencies flow inward**, with inner layers having no knowledge of outer layers.

### Inversion of Control (Dependency Injection)

When a piece of code `A` depends on another piece of code `B`, instead of creating the depependency inside `A`, we inject (fancy word for pass) `B` from outside. This way `A` is not responsible for creating `B` and can be easily tested with a mock `B`.

- [Dependency Injection & Inversion Explained | Node.js w/ TypeScript](https://khalilstemmler.com/articles/tutorials/dependency-injection-inversion-explained/)

### Domain Driven Design

- [Value Objects - DDD w/ TypeScript](https://khalilstemmler.com/articles/typescript-value-object/)

### Clean Architecture

![clean-architecture](https://blog.cleancoder.com/uncle-bob/images/2012-08-13-the-clean-architecture/CleanArchitecture.jpg)

***Usecases are also referred as interactors sometimes***

- [Clean Node.js Architecture | Enterprise Node.js + TypeScript](https://khalilstemmler.com/articles/enterprise-typescript-nodejs/clean-nodejs-architecture/)

### Hexagonal Architecture / Ports & Adapters

### Onion Architecture

### DCI (Data, Context and Interaction)

### Vertical Slice Architecture

Separating the application around features or “vertical slices”. A good addition to the Clean Architecture. First just slice the application vertically, then apply the Clean Architecture principles to each slice.

![vertical-slice](https://blog.ndepend.com/wp-content/uploads/net-vertical-slice-architecture.png)

### Screaming Architecture

- [Screaming Architecture](https://blog.cleancoder.com/uncle-bob/2011/09/30/Screaming-Architecture.html)

### CQRS (Command Query Responsibility Segregation)

### Repository Pattern

### Modular Monoliths

- [Introducing Bounded Contexts in a monolithic application (24 min)](https://www.youtube.com/watch?v=DhMrqX_qrJE)

### Conway's Law

- [Conway's Law](https://martinfowler.com/bliki/ConwaysLaw.html)
- [Conway's Law](https://khalilstemmler.com/wiki/conways-law/) - when we build software, we need to know the different groups/teams/roles it serves, and divide the app up into separate parts, similar to how those groups normally communicate in real life

## Resources

- [VirtualDDD](https://virtualddd.com/)

### Articles

- [The Clean Architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html) - OG Clean Architecture blog post.

### YT Channels

- [About Clean Code](https://www.youtube.com/@AboutCleanCode) - Makes videos on software architecture, explains beutifully. Uses .Net but the concepts are easily mappable to Node.js.
- [Drawing Boxes](https://www.youtube.com/@drawingboxes/featured) - Easy visual explanations.
- [Domain-Driven Design Europe](https://www.youtube.com/@ddd_eu/videos) - Excellent talks on DDD.

### Videos

- [Hexagonal, Onion & Clean Architecture (4min)](https://www.youtube.com/watch?v=JubdZIdLQ4M) - Sums up the architecture evolutions easily.
- [Repository Pattern Explained: Can You Afford to Skip It? (2min)](https://www.youtube.com/watch?v=Twu21yltjvo) - Repository pattern is used to mediate between the domain layer and data mapping layer (database) using repository and abstract repository interfaces. A good question to ask is, with ORM libraries that supports all requirement of a repository pattern, do we still need to implement repository pattern? That depends :D
- [Why I like to use Clean Architecture for my software projects (17min)](https://www.youtube.com/watch?v=rBxJwhXWZM0) - General overview of Clean Architecture with Express.js. Good for someone really struggling to piecing it together.
- [Dependency Injection, The Best Pattern (13min)](https://www.youtube.com/watch?v=J1f5b4vcxCQ) - Beutiful explanation of IoC with a practical usecase of file uploading.
- [Clean Architecture IS about Vertical Slicing, actually! (15min)](https://www.youtube.com/watch?v=7ZXW_oWdTk4) - Is clean architecture and vertical slicing different? Does vertical slicing solve any problem that clean architecture introduces? Let's find out.