---
layout: post
title: 'Big O Notation!'
date: 2020-04-24 23:46:42 -0400
categories: jekyll update
---

{% include breadcrumbs.html %}

In this post, we will discuss slightly boring yet very important concept in Computer Science called `Big O Notation!`

I chose this topic as my very first personal blog because I was never satisfied with the way I understood `Big O` at least in a way that I could explain to a child in a digestible manner.

Before we discuss what is Big O, let's talk about why do we care to learn it? And what makes me feel that there is a need to understand it well to be able to explain it to a child?

If you are in the field of Computer Science, we know we need to write programs that our computer will process to get a job done. Each of our programs consist of a set of step by step instructions also known as algorithms that we want our computer to execute. But how do we know the algorithm we wrote is really efficient to get the job done in a meaningful way. This efficiency could be measured in terms of the amount of time it takes to run and the amount of space or memory it requires to process. This is also known as `Time and Space complexity` of an algorithm.

You might think, why do we care how our program performs as long as it works? Well, there are several reasons why it becomes important but here are some important reasons

- When your program slows down or crashes, identifying parts of the program that are inefficient can help us find the pain points thereby making it more efficient.

- It's useful to discuss the trade-offs between different approaches to solve a specific problem.

- It's useful knowledge to have to impress your future employers in an technical interview.

`Big O Notation` helps us provide a general vocabulary to talk about how our program performs. It's a way of describing how the runtime of a program grows as the input to the program grows.

So, say we have a function f(n), where n is the input to the function, the runtime of this function could be constant time, linear, quadratic etc,.

- f(n) is constant => f(n) = O(1)
- f(n) is linear => f(n) = O(n)
- f(n) is quadratic => f(n) = O(n²)

Let's discuss couple of these time complexity through an example.

1. Constant Time Complexity

```javascript
function sumAll(n) {
	return (n * (n + 1)) / 2;
}
```

As you can see in the above function, this has a total of three operations: `1 multiplication n *`, `1 addition (n + 1)`, and `1 division / 2`. So, as the value of n grows, there is no impact on the runtime of this function, it will always execute exactly three operations. In other words, there are always three simple operations regardless of the size of n.

2. Linear Time Complexity

```javascript
function sumAll(n) {
  int result = 0;
  for(int i = 0; i < n; i++) {
    result = result + i;
  }
  return result;
}
```

In this algorithm, we can see that there are at least n additions and assignments inside the for loop where we add first `result + 1` and then assign `result =`result + 1. And there are other operations like `int i = 0; i < n; i++`, plus one more outside the for loop like `result = 0`. Even if we ignore operations outside the for loop, we can see that the number of operations inside the loop directly depends on the size of n. In other words, there are at least n operations for the input of size n. Hence this is a linear time complexity as the number of operations linearly increases with the value of n.
