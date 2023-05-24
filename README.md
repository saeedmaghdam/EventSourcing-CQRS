# Event Sourcing Terminologies

| Terminology    | Description                                                                                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Event          | An immutable record that represents a specific state-changing occurrence in the system. It encapsulates information about the event, such as its type, timestamp, and relevant data.  |
| Event Stream   | A sequential log of events that have occurred in the system. It provides a historical record of state changes and can be used to reconstruct the current state of an entity.              |
| Aggregate      | A domain object or entity that is responsible for processing and applying events. It encapsulates the current state of an entity and handles the logic to mutate its state based on events. |
| Event Store    | A persistent storage mechanism that stores and retrieves events. It typically supports appending new events to an event stream and querying events based on criteria such as time or entity.  |
| Snapshot       | A snapshot is an optimization technique used to capture the current state of an aggregate at a specific point in time. It helps reduce the time and resources required to rebuild an aggregate.  |
| Event Handler  | A component responsible for reacting to specific types of events. It listens for events from the event store and takes appropriate actions, such as updating read models or triggering side effects. |
| CQRS           | Command Query Responsibility Segregation is a pattern that separates the read and write operations into distinct models. Event sourcing is often used in conjunction with CQRS to handle writes.  |
| Projection     | A projection is a denormalized view of the event stream or a subset of events. It represents a specific perspective or state derived from the events and is optimized for efficient querying or display. |
| Replay         | The process of rebuilding an aggregate's state by replaying events from the event store. It involves applying events in the order they were recorded to recreate the current state of an entity.  |
| Event Version  | A unique identifier assigned to each event. It helps with ordering and detecting conflicts during event replay or when multiple processes are concurrently generating events.             |