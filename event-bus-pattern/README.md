# TLDR; Software Architecture - Event-Bus Pattern

## Description

Basically it's behaves like a pipeline (Bus) of computers connected, that whenever one of them sends a message (Event),
it's dispatched to all the others, and they decide if they consume or ignore that message.

## Pattern Architecture

This architecture can be built in two different ways:

### Classic Event-Bus

We start by defining an `EventBus`, a `Subscribable` and an `Event` interface.

- Subscribable

  - Needs to have a method that can handle given types of Events.
    - Given a type that it recognizes, it must analyze and process the data, otherwise ignore it.

- EventBus

  - Holds the contract (process) information
  - Holds a list of registered Subscribers
  - Is the dispatch manager

- Event
  - Hold the data, and type of the message

### Consumer / Dispatcher Event-Bus

## Advantages and Disadvantages

- Advantages

- Disadvantages

## Usecases
