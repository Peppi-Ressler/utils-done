# Done

This library contains just a single type called `Done`. It is beneficial to use this type instead of `Unit` mainly when combined
with `Future`. First of all it conveys more information than just `Future[Unit]`. But more importantly it prevents certain class
of bugs caused by automatic conversion of any value to `Unit` which can when combined with futures lead to quit/hidden throw away
of some value.

This library is inspired by the same type provided by Akka. We do not want to depend on Akka in each project so we separated this
into a single-purpose library.
