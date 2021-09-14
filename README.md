# Enterprise Cloud & Mobile Application Architecture, Design and Development
This course provides a solid background, both theoretical and practical, on the architecture, design and full stack development of cloud-based, web/mobile enterprise applications (EAs), based on well-defined security, performance, scalability, extensibility, ubiquitous access, interoperability and maintainability requirements. Such an architecture, design and development are performed according to best practices and patterns, and using state of the art technology in order to promote developer productivity and reduce application lifecycle management costs and risks. Covered topics are organized in four parts, where each builds on previous ones:
- **Part I. The Principles, Requirement Areas and Architectural Models of EAs**
- **Part II. The (Monolithic) Server Side of EAs**
- **Part III. The Progressive Web/Mobile Client Side of EAs**
- **Part IV. Microservices and Cloud Frameworks and Platforms for EAs**

This course adopts and/or opens up opportunities for students to use the most popular technologies on the server side (Spring, Yahoo! Elide, Node, Google Firebase, Netflix OSS), client side (Angular, React, Vue, Svelt), and in between (REST, GraphQL, JSON:API). The course uses several real-life case studies, mainly the ones under XCommerce meta-project: https://github.com/oiraqi/xcommerce and this guided project on Coursera: https://www.coursera.org/projects/microservices-spring-cloud-java

## Intended Learning Outcomes
This course enables students to achieve the ability to:
1. Master the principles, non-functional requirement areas, as well as the architectural models of enterprise applications
2. Master the architecture, design and development of the (monolithic) server side of enterprise applications, using a modern framework, such as Spring Boot
3. Master the design and development of progressive web/mobile client side of enterprise applications, using a modern technology, such as Angular, React and Vue
4. Apply microservices design patterns in a cloud environment to address the limitations of monoliths, using modern cloud frameworks and platforms, such as Spring Cloud, Netflix OSS  and Google Firebase

## Content
Part | Main Concepts | Language(s) | APIs / Libraries / Frameworks / Runtimes |
| --- | --- | --- | --- |
| [P1](https://github.com/oiraqi/eas/tree/main/P1-Big-Picture) | Principles, Common Requirement Areas (Security, Performance, Scalability, Extensibility, Interoperability, Portability, Maintainability), Architectural Models (Multi-tier, MVC, Microservices) | N/A | REST, GraphQL, JSON:API |
| [P2](https://github.com/oiraqi/eas/tree/main/P2-Server-Side) | Monolithic server-side architecture, design and development, IoC, DI, ORM, reverse proxying, load balancing, IAAA | UML, Java | Spring Boot, JPA, Hibernate, Elide, Nginx, Redis, Postgres |
| [P3](https://github.com/oiraqi/eas/tree/main/P3-Client-Side) | Progressive Web/Mobile Apps, FIRE attributes, UI components, proxy services, state management, navigation (routing), service workers, caching, offline access | Javascript, Typescript, HTML, CSS |Angular, Material Design |
| [P4](https://github.com/oiraqi/eas/tree/main/P4-Microservices-Cloud) | API gateway, circuit breaker, CQRS, asynchronous event-based architecture, cloud functions, messaging and storage, serverless | Java, Javascript | Spring Cloud, Netflix OSS, Firebase, Kafka |

## Tools
Develop | Build | Run | Collaborate |
| :---: | :---: | :---: | :---: |
| VS Code | Gradle | Docker | Git |
