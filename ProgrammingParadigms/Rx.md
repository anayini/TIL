# Reactive Programming

## RxSwift

Swift library implementing the Rx standard for reactive programming.  At a fundamental level this provides an abstraction called `Observable`, which can be thought of as the dual of `Iterator`:

|         | Iterator<T>            | Observable<T>  |
| ------------- |:-------------:| -----:      |
| Data Flow     | Pull          |   Push (subscribe) |
| Next value    | next() -> T   |   OnNext: (T) -> Void |
| Is Done?      | hasNext() -> Bool | completed: () -> Void|

Provides an abstraction useful for the composition of asynchronous APIs.
