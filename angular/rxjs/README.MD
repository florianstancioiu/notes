# RxJS

RxJS is a library for observing and reacting to data and events by using observable sequences.

## Reactive development

Code is reactive when an input change leads to an automatic change in output.

## Observer

A collection of callbacks that knows how to listen to values delivered by the Observable.

An Observer is a consumer of values delivered by an Observable.

In RxJS, an Observer is also defined as an interface with next, error and complete methods.

## Observable

A collection of events or values emitted over time.

## Operators

An operator is a function, used to transform and manipulate emitted items.

Apply operators in sequence using the Observable's `pipe` method.
