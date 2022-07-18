# TLDR; Software Architecture - Pipe-Filter Pattern

## Description

- In today's standards, a pipe-filter pattern is an architecture where an complex operation is broken down into smaller, simpler operations.
- Pipes would become the process stages between each filter stage.
- Parts of a Pipe-Filter Architecture: Pump, Pipe, Filter, Sink.

### Pump

- The pup is the producer of the data, or the data source

### Pipe

- Is the connector that passes data from one filter to the next. Is a directional stream of data that buffers the transmission until the next filter queue can accept it.

### Filters

- The filter(s) transform the data it receives via the pipes.
- A filter can have any number of input pipes and any number of ouput pipes.

### Sink

- The sink is the consumer of the data, or the data storage.

## Pros

- Separation of concerns
- Step-by-step development

## Cons

- If a filter needs to wait until it has received all the data, its data buffer may overflow or deadlock
- If the pipes only allow for a single data type, the filters will need to do parsing. This is a performance issue.

## Applications

- Often used in compilers. (Lexical Analysis, Parsing, Semantic Analysis, Code Generation)
- Filters are commonly implemented by separate threads. These may be either hardware or software threads/coroutines.

## Rating

- Agility
  - Rate:
  -
- Deployment
  - Rate:
  -
- Testability
  - Rate:
  -
- Performance
  - Rate:
  -
- Scalability
  - Rate:
  -
- Ease of development
  - Rate:
  -
