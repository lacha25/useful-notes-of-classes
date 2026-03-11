# Software Architecture

## Core Qualities

- Modularity
- Encapsulation
- Security
- Documentation
- Performance

## Layered Architecture Pattern

- Layers:
  - Presentation layer: user interface where users see and enter data
  - Business layer: executes business logic
  - Application layer: communicates between presentation and data
  - Data layer: manages database access and storage
- Pros:
  - Scalability, because layers can be scaled independently
  - Maintainability
  - Flexibility, because modifications are more isolated
- Cons:
  - Complexity
  - Performance overhead and higher latency
  - Strict layer separation can be limiting
- Common use cases:
  - E-commerce
  - Banking apps
  - Finance software

## Client-Server Architecture Pattern

- One server serves several clients.
- Pros:
  - Centralized management
  - Scalable
  - More secure and easier to maintain centrally
- Cons:
  - Single point of failure
  - Server cost
  - Client-server communication adds complexity
- Examples:
  - Amazon
  - Gmail
  - Dropbox
  - Netflix

## Event-Driven Architecture Pattern

- Systems react when events occur.
- Pros:
  - Scalable
  - Real-time processing
  - Flexible
- Cons:
  - Hard to design
  - Hard to test because of asynchronous behavior
  - Can be less reliable
- Common use cases:
  - Stock market systems
  - Online games
  - Customer support systems

## Microkernel Architecture Pattern

- Built around a core system plus plug-ins.
- Pros:
  - Easy to add new features
- Cons:
  - Hard to scale if the core needs major changes

## Microservices Architecture Pattern

- Build many small independent services.
- Pros:
  - Easy to add new functionality
  - Services stay independent
- Cons:
  - Hard to monitor many services
  - Network latency
  - More security exposure

## Space-Based Architecture

- Shared memory or data grid across several nodes, often in cloud systems.
- Pros:
  - Scalable
  - Fast
  - Modular components
- Cons:
  - Requires several servers
  - Complex
  - Network latency
- Common use cases:
  - Online games
  - Telecom services

## Master-Slave Architecture

- A master assigns jobs to slaves.
- Pros:
  - Parallel processing
  - Easy to add more slaves
  - A slave failure does not necessarily stop the system
- Cons:
  - Single point of failure at the master
  - Complex communication
  - Latency

## Pipe-Filter Architecture

- Data flows through a series of filters connected by pipes.
- Pros:
  - Filters can be reused
  - Easy to add new filters
  - Filters can run in parallel
- Cons:
  - Difficult to debug long pipelines
  - Requires a consistent data format
  - Filter chains can add latency
- Common use cases:
  - Data processing pipelines
  - Signal processing

## Broker Architecture

- A broker acts as an intermediary between components.
- Pros:
  - Changing servers does not affect the whole system as much
  - The broker can help handle failures
- Cons:
  - Single point of failure
  - Complexity
  - Broker security risks

## Peer-to-Peer Architecture

- Decentralized system where each node acts as both client and server.
- Pros:
  - Scalable
  - Fault tolerant
  - Lower cost
  - Robust
- Cons:
  - Security risks from decentralization
  - Data consistency is difficult
  - Can be slower
- Examples:
  - BitTorrent
  - Blockchain

## Architecture Selection Criteria

- Scalability
- Performance
- Availability
- Security
- Budget
- Tool stack
