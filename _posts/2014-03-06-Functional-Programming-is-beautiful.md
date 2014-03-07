---
layout: post
tagline: Scala
category: 
tags: [Hacker School, Scala, FP]
---
{% include JB/setup %}


For the past two weeks I was learning reactive programming using [Akka](http://akka.io/) - a toolkit fro building concurrent, distributed, and fault tolerant event-driven applications on the JVM. Because the things are best learnt by doing, I was building a chat application using it. But more about it in the future posts.

Today I decided to take a break from it and do some smaller tasks that do not keep me frustrated for too long. I was doing the [Ninety-Nine Scala Problems](http://aperiodic.net/phil/scala/s-99/). I learnt a small but beautiful thing - `flatMapSublists`. It is amazingly simple when you get it and super useful.

Everybody knows `flatMap` - a function that builds a collection by applying some function to all elements of a given list and using the elements of the resulting collections. It is an equivallent of `flatten` applied to the result of `map`. In Scala it's signature is:

```Scala
def flatMap[B](f: (A) ⇒ GenTraversableOnce[B]): List[B]
```

However, imagine a situation where you need to apply some function to all the sublists of a given list instead of all the elements of it. If `flatMapSublists` existed it would do exactly that. [Problem 26](http://aperiodic.net/phil/scala/s-99/#p26) of [Ninety-Nine Scala Problems](http://aperiodic.net/phil/scala/s-99/) asks to implement a function that generates the combinations of K distinct objects chosen from the N elements of a list. My solution is [here](https://github.com/laurita/NinetyNineScalaProblems/blob/master/src/main/scala/problems/P26.scala) and below:

```
def combinations[T](n: Int, list: List[T]): List[List[T]] = {
  def rec(list: List[T], acc: List[List[T]], comb: List[T]): List[List[T]] = {
    (comb, list) match {
      case (c, _) if c.length == n => List(c.reverse)
      case (c, Nil) if c.length < n => List()
      case (c, l) => rec(list.tail, acc, list.head::comb) ::: rec(list.tail, acc, comb)
    }
  }
  rec(list, Nil, Nil)
}
```

Not the most beautiful, not tail-recursive, though quite understandable I guess. However, what I found beutiful is the usage of `flatMapSublists` in their solution, which is also not tail-recursive but which very neatly introduces a layer of abstraction.

```Scala
def flatMapSublists[T, V](ls: List[T])(f: List[T] => List[V]): List[V] = {
  ls match {
    case Nil => Nil
    case list@(_ :: t) => f(list) ::: flatMapSublists(t)(f)
  }
}

def combinations[T](n: Int, list: List[T]): List[List[T]] = {
  if (n == 0) List(Nil)
  else flatMapSublists(list) { sl => combinations(n-1, sl.tail) map (sl.head :: _) }
}
```

Beautiful, huh? To easier understand it, imagine that for every element in a list you either take it or not until you reach a required number of elements in the current combination. If you take it, you map all the (n-1) element combinations from the list without this element cons'ed with it. If you do not take it, you find all the n elemet combinantions from the list without this element.

Totally beautiful!