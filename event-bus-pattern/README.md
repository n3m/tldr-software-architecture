# TLDR; Software Architecture - Model View Controller Pattern

## Description

- Distributed system that can service async arriving messages with associated with high volume of events
- 4 main Components: Event Source, Event Listener, Channel, Event Bus

### Event Source

- Publish messages to particular channels on an event bus.

### Event Listener

- Subscribes to particular channels
- Are notified of messages that arrived to suscribed channels

## Pros

- New publishers, suscribers and connections can be added easily

## Cons

- Scalability is an issue, since all messages travel through the same event bus

## Applications

- Android development
- Ecommerce Apps
- Notification Services

## Rating

- Agility
  - Rate: High
  - The capacity to react swiftly to an environment that is continually changing is known as overall agility. Although this pattern's layers of isolation feature allows for the separation of modifications, the strong coupling of its components and the monolithic nature of most implementations make this architectural pattern difficult and time-consuming to update.
- Deployment
  - Rate: High
  - Because the event-processor components are isolated, this style is often simple to implement. Because the event mediator component is relatively strongly tied to the event processors, it may be necessary to alter the event mediator as well, necessitating the deployment of both for each given modification. This is why the broker topology is typically easier to install than the mediator topology.
- Testability
  - Rate: Low
  - Although it is not very challenging, each unit testing does need a dedicated testing client or testing tool to produce events. The asynchronous nature of this pattern makes testing harder.
- Performance
  - Rate: High
  - The ability to perform decoupled, parallel asynchronous operations outweighs the cost of queuing and dequeuing messages. While it is possible to implement an event-driven architecture that does not perform well due to all the messaging infrastructure involved, in general, the pattern achieves high performance through its asynchronous capabilities.
- Scalability
  - Rate: High
  - This pattern's extremely independent and separated event processors inherently enable scalability. Scalability on a finer scale is possible because each event processor may be scaled independently.
- Ease of development
  - Rate: Low
  - Due to the asynchronous nature of the pattern, contract formation, and the requirement for more sophisticated error handling conditions inside the code for unresponsive event processors and unsuccessful brokers, development may be fairly challenging.
