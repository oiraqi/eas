# Part I. Requirement Areas, Priniples and Architectural Models of EAs
## Table of Contents
- [Introduction](#introduction)
- [Common (Non-functional) Requirement Areas](#common-non-functional-requirement-areas)
- [Principles](#principles)
- [Architectural Models](#architectural-models)

## Introduction
In the context of this course, we will use the term Enterprise Applications (EAs) to mean Enterprise-class Applications, i.e., applications that exhibit enterprise-level features and characteristics. These features and characteristics can be captured/expressed as _complex non-functional requirements_ in terms of:
- How secure they are
- How fast they are
- How they can handle growing loads and numbers of users
- How they can evolve and offer a richer functionality through time
- How they can be accessible anytime, anywhere
- How they can integrate with other systems
- How they can be maintained
### Examples
- Enterprise Resource Planning (ERP) software, such as Odoo (https://www.odoo.com)
- Hotel & Travel Management software, such as Booking (https://www.booking.com)
- Communication software, such as WhatsApp (https://www.whatsapp.com)
- Social Networking software, such as Facebook (http://www.facebook.com)
- E-commerce software, such as Amazon (https://www.amazon.com)

Notice that _NOT_ all these software apps and/or platforms are necessarily used by enterprises/professionals, e.g., WhatsApp, Facebook, Amazon, etc. However, all these examples have complex *enterprise-grade* requirements under the bullets mentioned above. These can be formally mapped to requirement areas detailed below.

## Common (Non-functional) Requirement Areas
### Security
Protecting the _Confidentiality_, _Integrity_ and _Availability_ (CIA triad) of data:
- at the level of _processing_
- In _motion_ (between processes within the same host or through the network)
- At _rest_

So, we need to:
- Identify and categorize the data that will be managed by the app, e.g., student personal records, academic records, financial records
- Identify the processes (the functions) that will act on each data category
- Identify the actors (user roles) allowed to perform each process: The basis for IAAA (Identification, Authentication, Authorization and Accounting)
- Identify motion paths, related risks and what it is required to mitigate those risks
- Identify storage systems, entities and attributes, related risks and what it is required to mitigate those risks

### Performance
Ensuring response time under a predefined limit. Response time includes:
- I/O time
- Processing time (at the level of the application, DBMS, middleware)
- Transfer time (between client side and server side, within the server side)

So, you need to determine a _reasonable_ and _acceptable_ response time, taking into account:
- UX
- What competitors offer
- Cost
- Constraints (e.g. poor client-side network connectivity)

To specify requirements in terms of:
- Caching (client side and server side)
- Compression
- Processing power
- Multithreading
- Asynchronicity
- Parallelism

### Scalability
### Extensibility
### Ubiquitous Access
### Interoperability
### Maintainability

## Principles
- Principle 1: EAs should be aligned with the business – It’s not about technology; it’s about business
- Principle 2: EAs should be cost-effective
- Principle 3: EA requirements should be addressed through the whole <a href="./lifecycle.png">software development lifecycle</a>
- Principle 4: Don’t reinvent the wheel – Common business requirements mean common business solutions
- Principle 5: There is no best technology

## Architectural Models
### Client / Server (Two-Tier) Model
### Multi-tier SOA Model
### MVC
### Microservices
