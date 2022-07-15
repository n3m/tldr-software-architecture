# TLDR; Software Architecture - Layered Pattern / N-tier

## Description

- The layered architecture pattern organizes components into horizontal levels, with each layer playing a distinct function inside the program (e.g., presentation logic or business logic). The display, business, persistence, and database layers are the most common ones in layered architectures, however the layered architecture pattern does not define the number or types of layers that must exist in the design.

## Layers

- Presentation Layer

  - Handling the user interface

- Application / Business Layer

  - Responsible for executing specific business rules associated with the request

- Business Logic / Persistence Layer

  - It's used for handling functions like object-relational mapping

- Data Access / Database Layer
  - Data Storage interfaces

![image](https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/assets/sapr_0102.png)

### Pros

- A lower layer can be used by different higher layers

### Cons

- The layers are not well-defined.
- Performs poorly in high performance environments. Mainly due to the lack of separation of concerns.

## Applications

- Simple web applications
- Desktop applications
- Good for tight budgets and tight constrains

## Rating

- Agility
  - Rate: Low
  - The capacity to react swiftly to an environment that is continually changing is known as overall agility. Although this pattern's layers of isolation feature allows for the separation of modifications, the strong coupling of its components and the monolithic nature of most implementations make this architectural pattern difficult and time-consuming to update.
- Deployment
  - Rate: Low
  - Deployment may be problematic depending on how you use this technique, especially for more complex apps. The entire program (or a significant portion of the application) may need to be redeployed in response to a minor change in a component, necessitating the planning, scheduling, and execution of deployments at off-peak times or on weekends. As a result, this pattern is difficult to use in a continuous delivery pipeline, thus lowering the deployment grade.
- Testability
  - Rate: High
  - As components are associated with certain architectural levels, additional layers may be mimicked or stubbed, which makes this style very simple to test. To isolate testing within a business component, a developer can mock a presentation component or screen. They can also mock the business layer to test specific screen functionality.
- Performance
  - Rate: Low
  - Even while certain layered architectures can function effectively, the design does not work well for high-performance applications since it is inefficient to have to pass through several layers of the architecture in order to satisfy a business requirement.
- Scalability
  - Rate: Low
  - Applications built utilizing this architecture pattern are typically challenging to grow due to the inclination toward tightly connected and monolithic implementations of this style. A layered architecture may be scaled by dividing the layers into independent physical deployments or duplicating the entire application across many nodes, but generally the granularity is too broad, making scaling difficult and expensive.
- Ease of development
  - Rate: High
  - Considering how well-known and simple to execute this pattern is, ease of development receives a pretty good rating. Since the majority of businesses divide skill sets into layers (presentation, business, and database), this design becomes an obvious choice for the majority of business-application development. Conway's law describes the relationship between a company's organizational and communication structure and the way it creates software. To learn more about this remarkable correlation, search for "Conway's law" online.
