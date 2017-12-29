# Reactive Programming

## RxSwift

Swift library implementing the Rx standard for reactive programming.  At a fundamental level this provides an abstraction called `Observable`, which can be thought of as the dual of `Iterator`:

|         | Iterator<T>            | Observable<T>  |
| ------------- |:-------------:| -----:      |
| Data Flow     | Pull          |   Push (subscribe) |
| Next value    | next() -> T   |   OnNext: (T) -> Void |
| Is Done?      | hasNext() -> Bool | completed: () -> Void|

Provides an abstraction useful for the composition of asynchronous APIs.

#### Subjects - Act as both observers and observables

- PublishSubject - Only publishes results to subscribers if they have already subscribed at the time of the event

- BehaviorSubject - Initalized with a value and replays original values or latest value to subscribers

- ReplaySubject - Replays a buffer of values to new subscribers

- Variable - Wrapper on BehaviorSubject that preserves latest value as state and replays latest value to subscribers.
