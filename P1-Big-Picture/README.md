# Part I. Requirement Areas, Principles and Architectural Models of EAs
## Table of Contents
- [Introduction](#introduction)
- [Common (Non-functional) Requirement Areas](#common-non-functional-requirement-areas)
  - [Security](#security)
  - [Performance](#performance)
  - [Scalability](#scalability)
  - [Extensibility](#extensibility)
  - [Accessibility](#accessibility)
  - [Interoperability](#interoperability)
  - [Maintainability](#maintainability)
- [Principles](#principles)
- [Architectural Models](#architectural-models)
  - [Two-Tier Model](#two-tier-model)
  - [Multi-Tier Model](#multi-tier-model)
  - [MVC Model](#mvc-model)
  - [SOA Model](#soa-model)
  - [Microservices Model](#microservices-model)
- [References](#references)

## Introduction
In the context of this course, we will use the term Enterprise Applications (EAs) to mean Enterprise-class Applications, i.e., applications that exhibit enterprise-level features and characteristics. These features and characteristics can be captured/expressed as _complex non-functional requirements_ in terms of:
- How secure they are
- How fast they are
- How they can handle growing loads and numbers of users
- How they can evolve and offer a richer functionality through time
- How they can be accessible anytime, anywhere
- How they can integrate with other systems
- How they can be maintained
### Examples of EAs
- Enterprise Resource Planning (ERP) software, such as Odoo (https://www.odoo.com)
- Hotel & Travel Management software, such as Booking (https://www.booking.com)
- Communication software, such as WhatsApp (https://www.whatsapp.com)
- Social Networking software, such as Facebook (http://www.facebook.com)
- E-commerce software, such as Amazon (https://www.amazon.com)

Notice that _NOT_ all these software apps and/or platforms are necessarily or solely used by enterprises/professionals, e.g., WhatsApp, Facebook, Amazon, etc. However, all these examples have complex *enterprise-grade* requirements under the bullets mentioned above. These can be formally mapped to requirement areas detailed below.

## Common (Non-functional) Requirement Areas
### Security
Protecting the _Confidentiality_, _Integrity_ and _Availability_ (CIA triad) of data:
- at the level of _processing_
- In _motion_ (between processes within the same host or through the network)
- At _rest_

So, we need to:
- Identify and categorize the data that will be managed by the app, e.g., student personal records, academic records, financial records
- Identify the processes (which get down to the functions) that will act on each data category
- Identify the actors (user roles) allowed to perform each process: The basis for specifying IAAA (Identification, Authentication, Authorization and Accounting) requirements
- Identify motion paths, related risks and what it is required to mitigate those risks
- Identify storage systems, entities and attributes, related risks and what it is required to mitigate those risks
- Identify Single Points of Failure (SPoF) and corresponding resiliency requirements

### Performance
Ensuring response time under a predefined limit. Response time includes:
- I/O time
- Processing time (at the level of the application, DBMS, middleware)
- Transfer time (between client side and server side, within the server side)

So, you need to determine a _reasonable_ and _acceptable_ response time, taking into account:
- UX
- Competition
- Cost
- Constraints (e.g. poor client-side network connectivity)

To specify requirements in terms of:
- Algorithm optimization
- Caching (client side and server side)
- Compression
- Multithreading
- Asynchronicity
- Parallelism
- Processing power

A typical value for an interactive app, such as Facebook is 200 - 300 ms.

### Scalability
Preserving performance while the load grows, at an acceptable (linear) cost. The load grows because of an increasing:
- Customer base; and/or
- Number of transactions per customer.

In both cases, such a success should be handled correctly and efficiently. Otherwise, it will become the cause of a total failure.
There are two techniques to scale:
- Vertical scaling (Scale up): increasing processing power at the level of the same node -- Limited!
- Horizontal scaling (Scale out): increasing processing power by adding more nodes -- Used to extend vertical scaling

So, we need to model load growth through time, and determine corresponding requirements in terms of:
- Node characteristics
- Load balancing
- Distributed data management
- Distributed computing

### Extensibility
Extending the functionality of the application at an acceptable (development) cost, while controlling side effects on security, performance and scalability.
So, we need to identify potential extension scenarios and corresponding requirements in terms of:
- Modularity
- Loose coupling

### Accessibility
Ensuring ubiquitous access to data and functionality, i.e., access _anytime_, _anywhere_. So, we need to specify _client side_ requirements in terms of:
- Portability: ability to run on different devices (desktops, laptops, tablets, smartphones) and operating systems (Windows, Linux, Mac, Android, iOS)
- Responsiveness: UI adaptability to different screen sizes
- Offline access

### Interoperability
Ensuring the components of the application can work together, as well as with external (open) systems. So, we need to specify the requirements in terms of:
- (Standard) Protocols
- APIs

### Maintainability
Ensuring security flaws and logical bugs can be fixed at minimum cost (man-hour, downtime, service degradation), So, we need to specify requirements in terms of:
- Modularity
- Loose coupling
- Asynchronous brokered communication
- Redundancy

## Principles
- Principle 1: EAs should be aligned with the business – It’s not about technology; it’s about business
- Principle 2: EAs should be cost-effective
- Principle 3: EA requirements should be addressed through the whole <a href="./lifecycle.png">software development lifecycle</a>
- Principle 4: Don’t reinvent the wheel – Common business requirements mean common business solutions
- Principle 5: There is no best technology

## Architectural Models
_From Wikipedia_:
- Software architecture refers to the _fundamental structures_ of a software system and the discipline of creating such structures and systems. Each structure comprises:
  - _software elements_,
  - _relations_ among them, and 
  - _properties_ of both elements and relations.[1]
- The architecture of a software system is a metaphor, analogous to the architecture of a building.[2]
- It functions as a _blueprint_ for the system and the developing project, laying out the tasks necessary to be executed by the design teams.[3]

_End Wikipedia_

Now, what's the relationship between _Architecture_ and _Architectural Models_?
The architecture of a software shall:
- be derived from, and support the fulfillment of its requirements,
- take into consideration technological choices, which themselves depend on the software requirements among other things, such as developer skills and expertise.

However, instead of designing the software architecture from scratch, it's a good idea to use a _proven_, _generic_ architecture that solves _common problems_ as a _starting point_. This is what we call _Architectural Model_. Then, we _customize_ the architectural model based on specific _requirements_ and _technology_.

You can think of it as:
<p align="center">Architectural Model + Specific Requirements + Adopted Technology ==> Architecture</p>

### Two-Tier Model
<p align="center"><img src="Two-Tier.png"><br/><b>Figure 1. Tow-Tier Model</b></p>

#### Discussion: Advantages? Drawbacks?

### Multi-Tier Model
<p align="center"><img src="Multi-Tier.png"><br/><b>Figure 2. Multi-Tier Model</b></p>

#### Discussion: Advantages? Drawbacks?

### MVC Model
<p align="center"><img src="MVC.png"><br/><b>Figure 3. MVC Model</b></p>

#### Note
MVC is not specific to the server side or to the multi-tier model, but it enhances them. Any software (even a simple standalone app) must control input (C), process it (M) and output results (V). Separating the three as three independent but interacting modules is nothing but MVC.

#### Discussion: Advantages? Drawbacks?

### SOA Model
<p align="center"><img src="SOA.png"><br/><b>Figure 4. SOA Model</b></p>

#### Note
SOA is not specific to the multi-tier model, but enhances it.

#### Discussion: Advantages? Drawbacks?

### Microservices Model
<p align="center"><img src="Microservices.png"><br/><b>Figure 5. Microservices Model</b></p>

#### Discussion: Advantages? Drawbacks?

## References
[1] Clements, Paul; Felix Bachmann; Len Bass; David Garlan; James Ivers; Reed Little; Paulo Merson; Robert Nord; Judith Stafford (2010). Documenting Software Architectures: Views and Beyond, Second Edition. Boston: Addison-Wesley. ISBN 978-0-321-55268-6.

[2] Perry, D. E.; Wolf, A. L. (1992). "Foundations for the study of software architecture" (PDF). ACM SIGSOFT Software Engineering Notes. 17 (4): 40. CiteSeerX 10.1.1.40.5174. doi:10.1145/141874.141884. S2CID 628695.

[3] Software Architecture. https://www.sei.cmu.edu/our-work/software-architecture/
