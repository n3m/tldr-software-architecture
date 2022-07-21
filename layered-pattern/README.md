# TLDR; Software Architecture - Layered Pattern / N-tier

## Description

- The **layered architecture** is one of the most common used patterns in Software Development.
  Also known as the _N-tier pattern_, refers to a type of organization that consists of
  horizontally-arranged _layers_ that work as a single module or unit.

### Layers

- A _layer_ is a logical separation of code or components that serve under the same purpose.
  One of the main characteristics of this pattern is that layers can only communicate in a
  downwards/left-to-right trend.

- An example of this conduct is seen in the following image:

![img](https://www.baeldung.com/wp-content/uploads/sites/4/2021/11/layered.drawio.svg)

- Layer 1 is connected to Layer 2 explicitly
- Layer 1 is connected to Layer 3 implicitly through Layer 2

- However we have to take into consideration another factor, a key concept of this pattern
  called _layer isolation_, which means that if, for example, changing or updating Layer 2
  from the image above will not have an effect on any other layer that is connected from or
  to.

## Pattern Architecture

- As previously stated, this pattern can have N types of layers, but a standard configuration
  might look like this.

  - **Presentation Layer** – responsible for user interactions with the software system
  - **Application/Business** Layer – handles aspects related to accomplishing functional requirements
  - **Domain Layer** – responsible for algorithms, and programming components
  - **Infrastructure/Persistence/Database Layer** – responsible for handling data, databases

![img](https://www.baeldung.com/wp-content/uploads/sites/4/2021/11/layered_common.drawio.svg)

## Advantages and Disadvantages

- Advantages

  - Easy to learn
  - Easy to implement
  - Testing is an easy task, mainly due to the layer separations

- Disadvantages
  - Scalability is an issue, due to the structure of the pattern. _However it can be mitigated if scaled-horizontally._
  - Parallel processing is not an option, since a layer could require another layer's output to proceed.
    _Often called interependence_.

## Usecases

- Often used in web development for simple applications that need to built quickly, as it is the easiest
  to implement, however, in the long run it may be difficult to maintain.
