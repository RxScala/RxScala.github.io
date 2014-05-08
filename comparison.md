---
layout: comparison
title: Comparison of Scala Observable and Java Observable
---

Note: 
*    This table contains both static methods and instance methods.
*    If a signature is too long, move your mouse over it to get the full signature.


| Java Method | Scala Method |
|-------------|--------------|
| `aggregate(R, Func2<R, ? super T, R>)` | `foldLeft(R)((R, T) => R)` |
| `aggregate(Func2<T, T, T>)` | `reduce((U, U) => U)` |
| `all(Func1<? super T, Boolean>)` | `forall(T => Boolean)` |
| `amb(Iterable<? extends Observable<? extends T>>)`<br/>`amb(Observable<? extends T>, Observable<? extends T>)`<br/><span title="amb(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>amb(...)</code></span><br/><span title="amb(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>amb(...)</code></span><br/><span title="amb(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>amb(...)</code></span><br/><span title="amb(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>amb(...)</code></span><br/><span title="amb(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>amb(...)</code></span><br/><span title="amb(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>amb(...)</code></span><br/><span title="amb(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>amb(...)</code></span> | **TODO: missing** |
| `asObservable()` | **TODO: missing** |
| `average(Observable<Integer>)`<br/>`averageDoubles(Observable<Double>)`<br/>`averageFloats(Observable<Float>)`<br/>`averageLongs(Observable<Long>)` | We can't have a general average method because Scala's `Numeric` does not have scalar multiplication (we would need to calculate `(1.0/numberOfElements)*sum`). You can use `fold` instead to accumulate `sum` and `numberOfElements` and divide at the end. |
| `buffer(Int, Int)` | `buffer(Int, Int)` |
| `buffer(Long, TimeUnit, Int)` | `buffer(Duration, Int)` |
| `buffer(Func0<? extends Observable<? extends TClosing>>)`<br/>`buffer(Observable<B>)`<br/>`buffer(Observable<B>, Int)`<br/><span title="buffer(Observable&lt;? extends TOpening&gt;, Func1&lt;? super TOpening, ? extends Observable&lt;? extends TClosing&gt;&gt;)"><code>buffer(...)</code></span> | **TODO: missing** |
| `buffer(Long, Long, TimeUnit, Scheduler)` | `buffer(Duration, Duration, Scheduler)` |
| `buffer(Long, Long, TimeUnit)` | `buffer(Duration, Duration)` |
| `buffer(Long, TimeUnit)` | `buffer(Duration)` |
| `buffer(Long, TimeUnit, Int, Scheduler)` | `buffer(Duration, Int, Scheduler)` |
| `buffer(Int)` | `buffer(Int)` |
| `buffer(Long, TimeUnit, Scheduler)` | `buffer(Duration, Scheduler)` |
| `cache()` | `cache` |
| `cast(Class<R>)` | **TODO: missing** |
| `collect(R, Action2<R, ? super T>)` | **TODO: missing** |
| <span title="combineLatest(List&lt;? extends Observable&lt;? extends T&gt;&gt;, FuncN&lt;? extends R&gt;)"><code>combineLatest(...)</code></span> | **TODO: missing** |
| <span title="combineLatest(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Func2&lt;? super T1, ? super T2, ? extends R&gt;)"><code>combineLatest(...)</code></span> | `combineLatest(Observable[U])` |
| <span title="combineLatest(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Observable&lt;? extends T3&gt;, Func3&lt;? super T1, ? super T2, ? super T3, ? extends R&gt;)"><code>combineLatest(...)</code></span><br/><span title="combineLatest(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Observable&lt;? extends T3&gt;, Observable&lt;? extends T4&gt;, Func4&lt;? super T1, ? super T2, ? super T3, ? super T4, ? extends R&gt;)"><code>combineLatest(...)</code></span><br/><span title="combineLatest(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Observable&lt;? extends T3&gt;, Observable&lt;? extends T4&gt;, Observable&lt;? extends T5&gt;, Func5&lt;? super T1, ? super T2, ? super T3, ? super T4, ? super T5, ? extends R&gt;)"><code>combineLatest(...)</code></span><br/><span title="combineLatest(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Observable&lt;? extends T3&gt;, Observable&lt;? extends T4&gt;, Observable&lt;? extends T5&gt;, Observable&lt;? extends T6&gt;, Func6&lt;? super T1, ? super T2, ? super T3, ? super T4, ? super T5, ? super T6, ? extends R&gt;)"><code>combineLatest(...)</code></span><br/><span title="combineLatest(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Observable&lt;? extends T3&gt;, Observable&lt;? extends T4&gt;, Observable&lt;? extends T5&gt;, Observable&lt;? extends T6&gt;, Observable&lt;? extends T7&gt;, Func7&lt;? super T1, ? super T2, ? super T3, ? super T4, ? super T5, ? super T6, ? super T7, ? extends R&gt;)"><code>combineLatest(...)</code></span><br/><span title="combineLatest(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Observable&lt;? extends T3&gt;, Observable&lt;? extends T4&gt;, Observable&lt;? extends T5&gt;, Observable&lt;? extends T6&gt;, Observable&lt;? extends T7&gt;, Observable&lt;? extends T8&gt;, Func8&lt;? super T1, ? super T2, ? super T3, ? super T4, ? super T5, ? super T6, ? super T7, ? super T8, ? extends R&gt;)"><code>combineLatest(...)</code></span><br/><span title="combineLatest(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Observable&lt;? extends T3&gt;, Observable&lt;? extends T4&gt;, Observable&lt;? extends T5&gt;, Observable&lt;? extends T6&gt;, Observable&lt;? extends T7&gt;, Observable&lt;? extends T8&gt;, Observable&lt;? extends T9&gt;, Func9&lt;? super T1, ? super T2, ? super T3, ? super T4, ? super T5, ? super T6, ? super T7, ? super T8, ? super T9, ? extends R&gt;)"><code>combineLatest(...)</code></span> | If C# doesn't need it, Scala doesn't need it either ;-) |
| `concat(Observable<? extends Observable<? extends T>>)` | `concat(<:<[Observable[T], Observable[Observable[U]]])` |
| `concat(Observable<? extends T>, Observable<? extends T>)`<br/><span title="concat(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>concat(...)</code></span><br/><span title="concat(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>concat(...)</code></span><br/><span title="concat(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>concat(...)</code></span><br/><span title="concat(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>concat(...)</code></span><br/><span title="concat(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>concat(...)</code></span><br/><span title="concat(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>concat(...)</code></span><br/><span title="concat(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>concat(...)</code></span> | unnecessary because we can use `++` instead or `Observable(o1, o2, ...).concat` |
| `concatMap(Func1<? super T, ? extends Observable<? extends R>>)` | **TODO: missing** |
| `contains(Any)` | `contains(U)` |
| `count()` | `length` |
| `create(OnSubscribeFunc<T>)`<br/>`create(OnSubscribe<T>)` | **TODO: missing** |
| `debounce(Long, TimeUnit)` | `debounce(Duration)` |
| `debounce(Func1<? super T, ? extends Observable<U>>)` | **TODO: missing** |
| `debounce(Long, TimeUnit, Scheduler)` | `debounce(Duration, Scheduler)` |
| `defaultIfEmpty(T)` | **TODO: missing** |
| `defer(Func0<? extends Observable<? extends T>>)` | `defer(=> Observable[T])` |
| `delay(Long, TimeUnit)` | `delay(Duration)` |
| <span title="delay(Func0&lt;? extends Observable&lt;U&gt;&gt;, Func1&lt;? super T, ? extends Observable&lt;V&gt;&gt;)"><code>delay(...)</code></span><br/>`delay(Func1<? super T, ? extends Observable<U>>)` | **TODO: missing** |
| `delay(Long, TimeUnit, Scheduler)` | `delay(Duration, Scheduler)` |
| `delaySubscription(Long, TimeUnit, Scheduler)` | `delaySubscription(Duration, Scheduler)` |
| `delaySubscription(Long, TimeUnit)` | `delaySubscription(Duration)` |
| `dematerialize()` | `dematerialize(<:<[Observable[T], Observable[Notification[U]]])` |
| `distinct(Func1<? super T, ? extends U>)` | `distinct(T => U)` |
| `distinct()` | `distinct` |
| `distinctUntilChanged()` | `distinctUntilChanged` |
| `distinctUntilChanged(Func1<? super T, ? extends U>)` | `distinctUntilChanged(T => U)` |
| `doOnCompleted(Action0)` | `doOnCompleted(() => Unit)` |
| `doOnEach(Observer<? super T>)` | `doOnEach(Observer[T])` |
| `doOnEach(Action1<Notification<? super T>>)` | **TODO: missing** |
| `doOnError(Action1<Throwable>)` | `doOnError(Throwable => Unit)` |
| `doOnNext(Action1<? super T>)` | `doOnNext(T => Unit)` |
| `doOnTerminate(Action0)` | `doOnTerminate(() => Unit)` |
| `elementAt(Int)` | `elementAt(Int)` |
| `elementAtOrDefault(Int, T)` | `elementAtOrDefault(Int, U)` |
| `empty()` | `empty` |
| `empty(Scheduler)` | `empty(Scheduler)` |
| `error(Throwable, Scheduler)` | **TODO: missing** |
| `error(Throwable)` | `error(Throwable)` |
| `exists(Func1<? super T, Boolean>)` | `exists(T => Boolean)` |
| `filter(Func1<? super T, Boolean>)` | `filter(T => Boolean)` |
| `finallyDo(Action0)` | `finallyDo(() => Unit)` |
| `first()` | `first` |
| `first(Func1<? super T, Boolean>)` | use `.filter(condition).first` |
| `firstOrDefault(T, Func1<? super T, Boolean>)` | use `.filter(condition).firstOrElse(default)` |
| `firstOrDefault(T)` | `firstOrElse(=> U)` |
| `flatMap(Func1<? super T, ? extends Observable<? extends R>>)` | `flatMap(T => Observable[R])` |
| `from(Iterable<? extends T>, Scheduler)` | `from(Iterable[T], Scheduler)` |
| `from(<repeated...><T>)`<br/>`from(T[], Scheduler)` | **TODO: missing** |
| `from(T[])`<br/>`from(T)`<br/>`from(T, T)`<br/>`from(T, T, T)`<br/>`from(T, T, T, T)`<br/>`from(T, T, T, T, T)`<br/>`from(T, T, T, T, T, T)`<br/>`from(T, T, T, T, T, T, T)`<br/>`from(T, T, T, T, T, T, T, T)`<br/>`from(T, T, T, T, T, T, T, T, T)`<br/>`from(T, T, T, T, T, T, T, T, T, T)` | use apply(T*) |
| `from(Future<? extends T>)`<br/>`from(Future<? extends T>, Long, TimeUnit)`<br/>`from(Future<? extends T>, Scheduler)` | TODO: Decide how Scala Futures should relate to Observables. Should there be a common base interface for Future and Observable? And should Futures also have an unsubscribe method? |
| `from(Iterable<? extends T>)` | `from(Iterable[T])` |
| `groupBy(Func1<? super T, ? extends K>)` | `groupBy(T => K)` |
| <span title="groupBy(Func1&lt;? super T, ? extends K&gt;, Func1&lt;? super T, ? extends R&gt;)"><code>groupBy(...)</code></span> | use `groupBy` and `map` |
| <span title="groupByUntil(Func1&lt;? super T, ? extends TKey&gt;, Func1&lt;? super GroupedObservable&lt;TKey, T&gt;, ? extends Observable&lt;? extends TDuration&gt;&gt;)"><code>groupByUntil(...)</code></span><br/><span title="groupByUntil(Func1&lt;? super T, ? extends TKey&gt;, Func1&lt;? super T, ? extends TValue&gt;, Func1&lt;? super GroupedObservable&lt;TKey, TValue&gt;, ? extends Observable&lt;? extends TDuration&gt;&gt;)"><code>groupByUntil(...)</code></span> | **TODO: missing** |
| <span title="groupJoin(Observable&lt;T2&gt;, Func1&lt;? super T, ? extends Observable&lt;D1&gt;&gt;, Func1&lt;? super T2, ? extends Observable&lt;D2&gt;&gt;, Func2&lt;? super T, ? super Observable&lt;T2&gt;, ? extends R&gt;)"><code>groupJoin(...)</code></span> | **TODO: missing** |
| `ignoreElements()` | **TODO: missing** |
| `interval(Long, TimeUnit)` | `interval(Duration)` |
| `interval(Long, TimeUnit, Scheduler)` | `interval(Duration, Scheduler)` |
| `isEmpty()` | `isEmpty` |
| <span title="join(Observable&lt;TRight&gt;, Func1&lt;T, Observable&lt;TLeftDuration&gt;&gt;, Func1&lt;TRight, Observable&lt;TRightDuration&gt;&gt;, Func2&lt;T, TRight, R&gt;)"><code>join(...)</code></span> | **TODO: missing** |
| `just(T, Scheduler)` | use apply(T*).subscribeOn(scheduler) |
| `just(T)` | use apply(T*) |
| `last()` | `last` |
| `last(Func1<? super T, Boolean>)` | **TODO: missing** |
| `lastOrDefault(T)`<br/>`lastOrDefault(T, Func1<? super T, Boolean>)` | **TODO: missing** |
| `lift(Operator<? extends R, ? super T>)` | `lift(Subscriber[R] => Subscriber[T])` |
| `longCount()` | **TODO: missing** |
| `map(Func1<? super T, ? extends R>)` | `map(T => R)` |
| `mapWithIndex(Func2<? super T, Integer, ? extends R>)` | combine `zipWithIndex` with `map` or with a for comprehension |
| `materialize()` | `materialize` |
| `merge(Array<Observable<? extends T>>)`<br/>`merge(Array<Observable<? extends T>>, Scheduler)`<br/>`merge(Iterable<? extends Observable<? extends T>>)`<br/>`merge(Iterable<? extends Observable<? extends T>>, Int)`<br/><span title="merge(Iterable&lt;? extends Observable&lt;? extends T&gt;&gt;, Int, Scheduler)"><code>merge(...)</code></span><br/>`merge(Iterable<? extends Observable<? extends T>>, Scheduler)`<br/>`merge(Observable<? extends Observable<? extends T>>, Int)` | **TODO: missing** |
| <span title="merge(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>merge(...)</code></span><br/><span title="merge(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>merge(...)</code></span><br/><span title="merge(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>merge(...)</code></span><br/><span title="merge(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>merge(...)</code></span><br/><span title="merge(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>merge(...)</code></span><br/><span title="merge(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>merge(...)</code></span><br/><span title="merge(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>merge(...)</code></span> | unnecessary because we can use `Observable(o1, o2, ...).flatten` instead |
| `merge(Observable<? extends Observable<? extends T>>)` | `flatten(<:<[Observable[T], Observable[Observable[U]]])` |
| `merge(Observable<? extends T>, Observable<? extends T>)` | `merge(Observable[U])` |
| `mergeDelayError(Observable<? extends Observable<? extends T>>)` | `flattenDelayError(<:<[Observable[T], Observable[Observable[U]]])` |
| <span title="mergeDelayError(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>mergeDelayError(...)</code></span><br/><span title="mergeDelayError(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>mergeDelayError(...)</code></span><br/><span title="mergeDelayError(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>mergeDelayError(...)</code></span><br/><span title="mergeDelayError(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>mergeDelayError(...)</code></span><br/><span title="mergeDelayError(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>mergeDelayError(...)</code></span><br/><span title="mergeDelayError(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>mergeDelayError(...)</code></span><br/><span title="mergeDelayError(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>mergeDelayError(...)</code></span> | unnecessary because we can use `Observable(o1, o2, ...).flattenDelayError` instead |
| <span title="mergeDelayError(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;)"><code>mergeDelayError(...)</code></span> | `mergeDelayError(Observable[U])` |
| `mergeMap(Func1<? super T, ? extends Observable<? extends R>>)`<br/><span title="mergeMap(Func1&lt;? super T, ? extends Observable&lt;? extends R&gt;&gt;, Func1&lt;? super Throwable, ? extends Observable&lt;? extends R&gt;&gt;, Func0&lt;? extends Observable&lt;? extends R&gt;&gt;)"><code>mergeMap(...)</code></span><br/><span title="mergeMap(Func1&lt;? super T, ? extends Observable&lt;? extends U&gt;&gt;, Func2&lt;? super T, ? super U, ? extends R&gt;)"><code>mergeMap(...)</code></span> | **TODO: missing** |
| <span title="mergeMapIterable(Func1&lt;? super T, ? extends Iterable&lt;? extends R&gt;&gt;)"><code>mergeMapIterable(...)</code></span><br/><span title="mergeMapIterable(Func1&lt;? super T, ? extends Iterable&lt;? extends U&gt;&gt;, Func2&lt;? super T, ? super U, ? extends R&gt;)"><code>mergeMapIterable(...)</code></span> | **TODO: missing** |
| <span title="multicast(Func0&lt;? extends Subject&lt;? super T, ? extends TIntermediate&gt;&gt;, Func1&lt;? super Observable&lt;TIntermediate&gt;, ? extends Observable&lt;TResult&gt;&gt;)"><code>multicast(...)</code></span><br/>`multicast(Subject<? super T, ? extends R>)` | **TODO: missing** |
| `nest()` | **TODO: missing** |
| `never()` | `never` |
| `observeOn(Scheduler)` | `observeOn(Scheduler)` |
| `ofType(Class<R>)` | **TODO: missing** |
| <span title="onErrorFlatMap(Func1&lt;OnErrorThrowable, ? extends Observable&lt;? extends T&gt;&gt;)"><code>onErrorFlatMap(...)</code></span> | **TODO: missing** |
| <span title="onErrorResumeNext(Func1&lt;Throwable, ? extends Observable&lt;? extends T&gt;&gt;)"><code>onErrorResumeNext(...)</code></span> | `onErrorResumeNext(Throwable => Observable[U])` |
| `onErrorResumeNext(Observable<? extends T>)` | `onErrorResumeNext(Observable[U])` |
| `onErrorReturn(Func1<Throwable, ? extends T>)` | `onErrorReturn(Throwable => U)` |
| `onExceptionResumeNext(Observable<? extends T>)` | `onExceptionResumeNext(Observable[U])` |
| `parallel(Func1<Observable<T>, Observable<R>>)` | `parallel(Observable[T] => Observable[R])` |
| `parallel(Func1<Observable<T>, Observable<R>>, Scheduler)` | `parallel(Observable[T] => Observable[R], Scheduler)` |
| `parallelMerge(Observable<Observable<T>>, Int)`<br/>`parallelMerge(Observable<Observable<T>>, Int, Scheduler)` | **TODO: missing** |
| <span title="pivot(Observable&lt;GroupedObservable&lt;K1, GroupedObservable&lt;K2, T&gt;&gt;&gt;)"><code>pivot(...)</code></span> | **TODO: missing** |
| `publish(Func1<? super Observable<T>, ? extends Observable<R>>)` | `publish(Observable[U] => Observable[R])` |
| <span title="publish(Func1&lt;? super Observable&lt;T&gt;, ? extends Observable&lt;R&gt;&gt;, T)"><code>publish(...)</code></span> | `publish(Observable[U] => Observable[R], U)` |
| `publish()` | `publish()` |
| `publish(T)` | `publish(U)` |
| `publishLast()`<br/><span title="publishLast(Func1&lt;? super Observable&lt;T&gt;, ? extends Observable&lt;R&gt;&gt;)"><code>publishLast(...)</code></span> | **TODO: missing** |
| `range(Int, Int)`<br/>`range(Int, Int, Scheduler)` | **TODO: missing** |
| `reduce(Func2<T, T, T>)` | `reduce((U, U) => U)` |
| `reduce(R, Func2<R, ? super T, R>)` | `foldLeft(R)((R, T) => R)` |
| `repeat(Long)` | `repeat(Long)` |
| `repeat(Long, Scheduler)` | `repeat(Long, Scheduler)` |
| `repeat(Scheduler)` | `repeat(Scheduler)` |
| `repeat()` | `repeat()` |
| `replay(Func1<? super Observable<T>, ? extends Observable<R>>)`<br/><span title="replay(Func1&lt;? super Observable&lt;T&gt;, ? extends Observable&lt;R&gt;&gt;, Int)"><code>replay(...)</code></span><br/><span title="replay(Func1&lt;? super Observable&lt;T&gt;, ? extends Observable&lt;R&gt;&gt;, Int, Long, TimeUnit)"><code>replay(...)</code></span><br/><span title="replay(Func1&lt;? super Observable&lt;T&gt;, ? extends Observable&lt;R&gt;&gt;, Int, Long, TimeUnit, Scheduler)"><code>replay(...)</code></span><br/><span title="replay(Func1&lt;? super Observable&lt;T&gt;, ? extends Observable&lt;R&gt;&gt;, Int, Scheduler)"><code>replay(...)</code></span><br/><span title="replay(Func1&lt;? super Observable&lt;T&gt;, ? extends Observable&lt;R&gt;&gt;, Long, TimeUnit)"><code>replay(...)</code></span><br/><span title="replay(Func1&lt;? super Observable&lt;T&gt;, ? extends Observable&lt;R&gt;&gt;, Long, TimeUnit, Scheduler)"><code>replay(...)</code></span><br/><span title="replay(Func1&lt;? super Observable&lt;T&gt;, ? extends Observable&lt;R&gt;&gt;, Scheduler)"><code>replay(...)</code></span><br/>`replay(Int)`<br/>`replay(Int, Long, TimeUnit)`<br/>`replay(Int, Long, TimeUnit, Scheduler)`<br/>`replay(Int, Scheduler)`<br/>`replay(Long, TimeUnit)`<br/>`replay(Long, TimeUnit, Scheduler)`<br/>`replay(Scheduler)` | **TODO: missing** |
| `replay()` | `replay` |
| `retry(Int)` | `retry(Int)` |
| `retry()` | `retry()` |
| `sample(Observable<U>)` | **TODO: missing** |
| `sample(Long, TimeUnit)` | `sample(Duration)` |
| `sample(Long, TimeUnit, Scheduler)` | `sample(Duration, Scheduler)` |
| `scan(Func2<T, T, T>)` | considered unnecessary in Scala land |
| `scan(R, Func2<R, ? super T, R>)` | `scan(R)((R, T) => R)` |
| `sequenceEqual(Observable<? extends T>, Observable<? extends T>)`<br/><span title="sequenceEqual(Observable&lt;? extends T&gt;, Observable&lt;? extends T&gt;, Func2&lt;? super T, ? super T, Boolean&gt;)"><code>sequenceEqual(...)</code></span> | **TODO: missing** |
| `serialize()` | `serialize` |
| `single(Func1<? super T, Boolean>)` | **TODO: missing** |
| `single()` | `single` |
| `singleOrDefault(T)`<br/>`singleOrDefault(T, Func1<? super T, Boolean>)` | **TODO: missing** |
| `skip(Long, TimeUnit, Scheduler)` | `drop(Duration, Scheduler)` |
| `skip(Int)` | `drop(Int)` |
| `skip(Long, TimeUnit)` | `drop(Duration)` |
| `skipLast(Long, TimeUnit, Scheduler)` | `dropRight(Duration, Scheduler)` |
| `skipLast(Long, TimeUnit)` | `dropRight(Duration)` |
| `skipLast(Int)` | `dropRight(Int)` |
| `skipUntil(Observable<U>)` | `dropUntil(Observable[E])` |
| `skipWhile(Func1<? super T, Boolean>)` | `dropWhile(T => Boolean)` |
| `skipWhileWithIndex(Func2<? super T, Integer, Boolean>)` | considered unnecessary in Scala land |
| `startWith(T[])` | use `Observable.items(items) ++ o` |
| `startWith(T[], Scheduler)` | use `Observable.items(items).subscribeOn(scheduler) ++ o` |
| `startWith(Iterable<T>, Scheduler)` | use `Observable.from(iterable).subscribeOn(scheduler) ++ o` |
| `startWith(Iterable<T>)` | use `Observable.from(iterable) ++ o` |
| `startWith(T)` | use `item +: o` |
| `startWith(T, T)`<br/>`startWith(T, T, T)`<br/>`startWith(T, T, T, T)`<br/>`startWith(T, T, T, T, T)`<br/>`startWith(T, T, T, T, T, T)`<br/>`startWith(T, T, T, T, T, T, T)`<br/>`startWith(T, T, T, T, T, T, T, T)`<br/>`startWith(T, T, T, T, T, T, T, T, T)` | use `Observable.items(...) ++ o` |
| `startWith(Observable<T>)` | use `++` |
| `subscribe(Observer<? super T>, Scheduler)` | `subscribe(Observer[T], Scheduler)` |
| `subscribe(Subscriber<? super T>, Scheduler)` | **TODO: missing** |
| `subscribe(Action1<? super T>, Action1<Throwable>)` | `subscribe(T => Unit, Throwable => Unit)` |
| `subscribe(Action1<? super T>, Action1<Throwable>, Action0)` | `subscribe(T => Unit, Throwable => Unit, () => Unit)` |
| `subscribe()` | `subscribe()` |
| <span title="subscribe(Action1&lt;? super T&gt;, Action1&lt;Throwable&gt;, Action0, Scheduler)"><code>subscribe(...)</code></span> | `subscribe(T => Unit, Throwable => Unit, () => Unit, Scheduler)` |
| `subscribe(Action1<? super T>)` | `subscribe(T => Unit)` |
| `subscribe(Action1<? super T>, Action1<Throwable>, Scheduler)` | `subscribe(T => Unit, Throwable => Unit, Scheduler)` |
| `subscribe(Action1<? super T>, Scheduler)` | `subscribe(T => Unit, Scheduler)` |
| `subscribe(Subscriber<? super T>)` | **TODO: missing** |
| `subscribe(Observer<? super T>)` | `subscribe(Observer[T])` |
| `subscribeOn(Scheduler)` | `subscribeOn(Scheduler)` |
| `sum(Observable<Integer>)` | `sum(Numeric[U])` |
| `sumDoubles(Observable<Double>)` | `sum(Numeric[U])` |
| `sumFloats(Observable<Float>)` | `sum(Numeric[U])` |
| `sumLongs(Observable<Long>)` | `sum(Numeric[U])` |
| `switchDo(Observable<? extends Observable<? extends T>>)` | deprecated in RxJava |
| `switchMap(Func1<? super T, ? extends Observable<? extends R>>)` | **TODO: missing** |
| `switchOnNext(Observable<? extends Observable<? extends T>>)` | `switch(<:<[Observable[T], Observable[Observable[U]]])` |
| `take(Long, TimeUnit)`<br/>`take(Long, TimeUnit, Scheduler)` | **TODO: missing** |
| `take(Int)` | `take(Int)` |
| `takeFirst(Func1<? super T, Boolean>)` | use `filter(condition).take(1)` |
| `takeLast(Int, Long, TimeUnit)`<br/>`takeLast(Int, Long, TimeUnit, Scheduler)`<br/>`takeLast(Long, TimeUnit)`<br/>`takeLast(Long, TimeUnit, Scheduler)` | **TODO: missing** |
| `takeLast(Int)` | `takeRight(Int)` |
| `takeLastBuffer(Int)`<br/>`takeLastBuffer(Int, Long, TimeUnit)`<br/>`takeLastBuffer(Int, Long, TimeUnit, Scheduler)`<br/>`takeLastBuffer(Long, TimeUnit)`<br/>`takeLastBuffer(Long, TimeUnit, Scheduler)` | **TODO: missing** |
| `takeUntil(Observable<? extends E>)` | `takeUntil(Observable[E])` |
| `takeWhile(Func1<? super T, Boolean>)` | `takeWhile(T => Boolean)` |
| `takeWhileWithIndex(Func2<? super T, ? super Integer, Boolean>)` | use `.zipWithIndex.takeWhile{case (elem, index) => condition}.map(_._1)` |
| `throttleFirst(Long, TimeUnit)` | `throttleFirst(Duration)` |
| `throttleFirst(Long, TimeUnit, Scheduler)` | `throttleFirst(Duration, Scheduler)` |
| `throttleLast(Long, TimeUnit)` | `throttleLast(Duration)` |
| `throttleLast(Long, TimeUnit, Scheduler)` | `throttleLast(Duration, Scheduler)` |
| `throttleWithTimeout(Long, TimeUnit, Scheduler)` | `throttleWithTimeout(Duration, Scheduler)` |
| `throttleWithTimeout(Long, TimeUnit)` | `throttleWithTimeout(Duration)` |
| `timeInterval()`<br/>`timeInterval(Scheduler)` | **TODO: missing** |
| `timeout(Func1<? super T, ? extends Observable<V>>)` | `timeout(T => Observable[V])` |
| <span title="timeout(Func0&lt;? extends Observable&lt;U&gt;&gt;, Func1&lt;? super T, ? extends Observable&lt;V&gt;&gt;)"><code>timeout(...)</code></span><br/><span title="timeout(Func1&lt;? super T, ? extends Observable&lt;V&gt;&gt;, Observable&lt;? extends T&gt;)"><code>timeout(...)</code></span> | `timeout(() => Observable[U], T => Observable[V])` |
| `timeout(Long, TimeUnit, Observable<? extends T>)` | `timeout(Duration, Observable[U])` |
| `timeout(Long, TimeUnit, Observable<? extends T>, Scheduler)` | `timeout(Duration, Observable[U], Scheduler)` |
| `timeout(Long, TimeUnit)` | `timeout(Duration)` |
| <span title="timeout(Func0&lt;? extends Observable&lt;U&gt;&gt;, Func1&lt;? super T, ? extends Observable&lt;V&gt;&gt;, Observable&lt;? extends T&gt;)"><code>timeout(...)</code></span> | `timeout(() => Observable[U], T => Observable[V], Observable[O])` |
| `timeout(Long, TimeUnit, Scheduler)` | `timeout(Duration, Scheduler)` |
| `timer(Long, Long, TimeUnit)` | `timer(Duration, Duration)` |
| `timer(Long, Long, TimeUnit, Scheduler)` | `timer(Duration, Duration, Scheduler)` |
| `timer(Long, TimeUnit)`<br/>`timer(Long, TimeUnit, Scheduler)` | **TODO: missing** |
| `timestamp(Scheduler)` | `timestamp(Scheduler)` |
| `timestamp()` | `timestamp` |
| `toBlockingObservable()` | `toBlockingObservable` |
| `toList()` | `toSeq` |
| <span title="toMap(Func1&lt;? super T, ? extends K&gt;, Func1&lt;? super T, ? extends V&gt;, Func0&lt;? extends Map&lt;K, V&gt;&gt;)"><code>toMap(...)</code></span> | `toMap(T => K, T => V, () => Map[K, V])` |
| <span title="toMap(Func1&lt;? super T, ? extends K&gt;, Func1&lt;? super T, ? extends V&gt;)"><code>toMap(...)</code></span> | `toMap(T => K, T => V)` |
| `toMap(Func1<? super T, ? extends K>)` | `toMap(T => K)` |
| `toMultimap(Func1<? super T, ? extends K>)`<br/><span title="toMultimap(Func1&lt;? super T, ? extends K&gt;, Func1&lt;? super T, ? extends V&gt;)"><code>toMultimap(...)</code></span><br/><span title="toMultimap(Func1&lt;? super T, ? extends K&gt;, Func1&lt;? super T, ? extends V&gt;, Func0&lt;? extends Map&lt;K, Collection&lt;V&gt;&gt;&gt;)"><code>toMultimap(...)</code></span><br/><span title="toMultimap(Func1&lt;? super T, ? extends K&gt;, Func1&lt;? super T, ? extends V&gt;, Func0&lt;? extends Map&lt;K, Collection&lt;V&gt;&gt;&gt;, Func1&lt;? super K, ? extends Collection&lt;V&gt;&gt;)"><code>toMultimap(...)</code></span> | **TODO: missing** |
| `toSortedList(Func2<? super T, ? super T, Integer>)` | Sorting is already done in Scala's collection library, use `.toSeq.map(_.sortWith(f))` |
| `toSortedList()` | Sorting is already done in Scala's collection library, use `.toSeq.map(_.sorted)` |
| `unsafeSubscribe(Subscriber<? super T>)` | **TODO: missing** |
| `unsubscribeOn(Scheduler)` | **TODO: missing** |
| <span title="using(Func0&lt;Resource&gt;, Func1&lt;Resource, ? extends Observable&lt;? extends T&gt;&gt;)"><code>using(...)</code></span> | **TODO: missing** |
| `window(Long, TimeUnit)` | `window(Duration)` |
| `window(Long, TimeUnit, Int)` | `window(Duration, Int)` |
| `window(Long, Long, TimeUnit, Scheduler)` | `window(Duration, Duration, Scheduler)` |
| `window(Int)` | `window(Int)` |
| `window(Int, Int)` | `window(Int, Int)` |
| `window(Long, Long, TimeUnit)` | `window(Duration, Duration)` |
| `window(Func0<? extends Observable<? extends TClosing>>)`<br/>`window(Observable<U>)`<br/><span title="window(Observable&lt;? extends TOpening&gt;, Func1&lt;? super TOpening, ? extends Observable&lt;? extends TClosing&gt;&gt;)"><code>window(...)</code></span> | **TODO: missing** |
| `window(Long, TimeUnit, Int, Scheduler)` | `window(Duration, Int, Scheduler)` |
| `window(Long, TimeUnit, Scheduler)` | `window(Duration, Scheduler)` |
| <span title="zip(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Func2&lt;? super T1, ? super T2, ? extends R&gt;)"><code>zip(...)</code></span> | use instance method `zip` and `map` |
| <span title="zip(Iterable&lt;? extends T2&gt;, Func2&lt;? super T, ? super T2, ? extends R&gt;)"><code>zip(...)</code></span><br/><span title="zip(Observable&lt;? extends T2&gt;, Func2&lt;? super T, ? super T2, ? extends R&gt;)"><code>zip(...)</code></span> | **TODO: missing** |
| `zip(Iterable<? extends Observable<_>>, FuncN<? extends R>)`<br/>`zip(Observable<? extends Observable<_>>, FuncN<? extends R>)` | use `zip` in companion object and `map` |
| <span title="zip(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Observable&lt;? extends T3&gt;, Func3&lt;? super T1, ? super T2, ? super T3, ? extends R&gt;)"><code>zip(...)</code></span><br/><span title="zip(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Observable&lt;? extends T3&gt;, Observable&lt;? extends T4&gt;, Func4&lt;? super T1, ? super T2, ? super T3, ? super T4, ? extends R&gt;)"><code>zip(...)</code></span><br/><span title="zip(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Observable&lt;? extends T3&gt;, Observable&lt;? extends T4&gt;, Observable&lt;? extends T5&gt;, Func5&lt;? super T1, ? super T2, ? super T3, ? super T4, ? super T5, ? extends R&gt;)"><code>zip(...)</code></span><br/><span title="zip(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Observable&lt;? extends T3&gt;, Observable&lt;? extends T4&gt;, Observable&lt;? extends T5&gt;, Observable&lt;? extends T6&gt;, Func6&lt;? super T1, ? super T2, ? super T3, ? super T4, ? super T5, ? super T6, ? extends R&gt;)"><code>zip(...)</code></span><br/><span title="zip(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Observable&lt;? extends T3&gt;, Observable&lt;? extends T4&gt;, Observable&lt;? extends T5&gt;, Observable&lt;? extends T6&gt;, Observable&lt;? extends T7&gt;, Func7&lt;? super T1, ? super T2, ? super T3, ? super T4, ? super T5, ? super T6, ? super T7, ? extends R&gt;)"><code>zip(...)</code></span><br/><span title="zip(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Observable&lt;? extends T3&gt;, Observable&lt;? extends T4&gt;, Observable&lt;? extends T5&gt;, Observable&lt;? extends T6&gt;, Observable&lt;? extends T7&gt;, Observable&lt;? extends T8&gt;, Func8&lt;? super T1, ? super T2, ? super T3, ? super T4, ? super T5, ? super T6, ? super T7, ? super T8, ? extends R&gt;)"><code>zip(...)</code></span><br/><span title="zip(Observable&lt;? extends T1&gt;, Observable&lt;? extends T2&gt;, Observable&lt;? extends T3&gt;, Observable&lt;? extends T4&gt;, Observable&lt;? extends T5&gt;, Observable&lt;? extends T6&gt;, Observable&lt;? extends T7&gt;, Observable&lt;? extends T8&gt;, Observable&lt;? extends T9&gt;, Func9&lt;? super T1, ? super T2, ? super T3, ? super T4, ? super T5, ? super T6, ? super T7, ? super T8, ? super T9, ? extends R&gt;)"><code>zip(...)</code></span> | considered unnecessary in Scala land |

This table was generated on Sun May 11 23:51:33 CST 2014.
**Do not edit**. Instead, edit `rx.lang.scala.CompletenessTest`.
