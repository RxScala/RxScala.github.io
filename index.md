---
layout: default
title: RxScala
---

## NOTE: Work on this page is in progress...

RxScala brings *Reactive Extensions* to Scala. Rx was first implemented for [.NET](https://rx.codeplex.com), and is now being implemented in [Java](https://github.com/Netflix/RxJava). The RxScala project is an adaptor for RxJava. Its code is in a [subdirectory](https://github.com/Netflix/RxJava/tree/master/language-adaptors/rxjava-scala) the RxJava repository, and it's also distributed from there on [Maven Central](http://search.maven.org/#search%7Cga%7C1%7Ca%3A%22rxjava-scala%22).

Get started by looking at [RxScalaDemo.scala](https://github.com/Netflix/RxJava/blob/master/language-adaptors/rxjava-scala/src/examples/scala/rx/lang/scala/examples/RxScalaDemo.scala), the [RxScalaExamples](https://github.com/RxScala/RxScalaExamples), or the [Scaladoc](http://rxscala.github.io/scaladoc/index.html#rx.lang.scala.Observable).

There's also a [comparison table](http://rxscala.github.io/comparison.html) between Java Observable and Scala Observable.


## Warning

This library is not yet finished. You have to expect breaking changes in future versions.


## Binaries

Binaries and dependency information can be found at [http://search.maven.org](http://search.maven.org/#search%7Cga%7C1%7Ca%3A%22rxjava-scala%22).

Example for sbt:

{% highlight scala %}
libraryDependencies ++= Seq(
  "com.netflix.rxjava" % "rxjava-scala" % "x.y.z"
)
{% endhighlight %}

Note that `rxjava-scala` depends on `rxjava-core`, so if you download the jars manually, don't forget `rxjava-core`.


## Communication

Just use the same communication channels as for RxJava:

-    Google Group: [RxJava](http://groups.google.com/d/forum/rxjava)
-    Twitter: [@RxJava](http://twitter.com/RxJava)
-    [GitHub Issues](https://github.com/Netflix/RxJava/issues)
