---
layout: post
title: Musical Groups
date: 2020-6-13
category: jekyll-update
---

I might've mentioned it before, but one of my favorite classes in mathematics was introduction to algebra.
Yes, that algebra. The one where you learned how addition, multiplication, and exponentiation worked;
the one where you may have used matrices;
the one where you learned the properties of addition and multiplication (perhaps even in the first week if the class were so bold).

I also do play a good amount of instruments: string instruments that is.
That's a bit of a problem too, because knowing how to play doesn't translate into being able to compose.
Composition is really difficult.
Sure, it's possible to pick up an instrument and fiddle around with it until something that sounds legitimate is produced.
But accessibility is a problem when the instruments aren't within immediate reach.

In an effort to try and hack a framework to analyze music, and then use the same framework to compose music,
I repeated what had already been done.
Here is my attempt at explaining neo-Riemannian music theory.
Yes, that [Riemann][1], the theorist Riemann.

# Music and Mathematics
If you've taken Algebra, then you know we're not interested much in the atomic objects.
We like looking at the interactions between those atomic objects, and the general properties of those atomic objects.

In the same spirit, look at notes. 
We can play a note, and then play another note and call this some sort of collection.
We can play two notes, play another two notes, and it's the same as playing four notes.
We can yield identity, inversion, and some form of addition on these notes which is associative.

Let $$\mathcal{N}$$ be the set of all possible notes that can be played, with $$n,m\in\mathcal{N}$$.
Include $$0\in\mathcal{N}$$, and let that represent the lack of playing any note.
Let $$\mathcal{T}(n)$$ represent the function of playing a note (i.e. $$\mathcal{T}:\mathcal{N}\to\mathcal{N}$$)
Composition on our function we can define as:

$$\mathcal{T}(n)\circ\mathcal{T}(m)=\mathcal{T}(n+m)$$

Please note, $$\mathcal{T}(n+m)$$ does not mean we play notes $$n$$ and $$m$$ at the same time.
We'll solve that problem when we come to it.

These are the properties of our operation:

> i)	Under composition, we can play as many notes in succession as we want   
> ii)	The order in which we play the notes is arbitrary    
> iii)	We can choose to not play a note    
> iv)	We can yield the option of playing not a note from playing notes    

These are the properties of a group: closure, association, identity, and inversion.
Properties i and iii I think are a bit self explanatory, so I will explain ii and iv.

For ii, this is simply
    
$$\mathcal{T}(n)\circ[\mathcal{T}(m)\circ\mathcal{T}(l)]=[\mathcal{T}(n)\circ\mathcal{T}(m)]\circ\mathcal{T}(l)$$

The right hand yields $$\mathcal{T}([n+m]+l)=\mathcal{T}(n+m+l)$$,
while the sinister yields $$\mathcal{T}([n+[m+l]])=\mathcal{T}(n+m+l)$$; both are identical.
Thus, the order in which we compose is arbitrary.

Property iv is a simpler than stated.
The importance of bijection is that we automatically know inversion exists.
Say we look to play a note, but we hit the wrong one: i.e. we did $$\mathcal{T}(n)$$ but didn't mean to.
If we transpose it with the inverse, then that's just reversing whatever we did. 
Essentially, it is a declaration of not playing a note.

$$\mathcal{T}(n)\circ\mathcal{T}^{-1}(n)=\mathcal{T}(0)$$

# Messing with $$\mathcal{T}$$
Now here's where things get a bit interesting. We can change the set which $$\mathcal{T}$$ operates on.
We can say instead, start at middle C. Increasing by some tuning is $$\mathcal{T}(1)$$ which leads to C#.
In the same fashion, decreasing by same tuning one step is $$\mathcal{T}(-1)$$ leads to Cb or B. 
If we let $$\mathcal{T}$$ take $$\mathbb{Z}$$ instead, yield tonal steps; this is still a group.

We can simplify this even further to the point where it's $$\mathcal{T}$$ is trivial.
That is, it just increases by unit steps with respect to whatever tuning is used.
In which case $$\mathcal{T}^n$$ such that $$n\in\mathbb{Z}$$ is that same as going up $$n$$ steps in your tuning.
And this still holds as a group!

Note, this can be done with $$n\in\mathbb{N}$$. 
But it must be done with extra care when talking about inversions.
Surely, you can represent inversions as $$\mathcal{T}'$$ instead of $$\mathcal{T}^{-1}$$,
which would lead to an explanation as to why we don't accept $$-1$$ as an input for $$n$$.
But that's just a lot of confusion down the line.

# Trivial $$\mathcal{T}$$
Let $$\mathcal{T}$$ be trivial. It takes in two arguments only (a sequential argument and a "not" argument representative of not traveling anywhere),
and maps to a consequential tone.
If we compose over and over again $$n$$ times, $$\mathcal{T}\circ\mathcal{T}\circ\cdots \circ\mathcal{T}$$, yield
$$\mathcal{T}^n$$.
Closure follows easily. 
Associativity follows easily. 
Identity is just $$\mathcal{T}(0)$$ (the "not" argument which means don't travel up).
Inversion is just traveling back. i.e. $$\mathcal{T}^{-1}\circ\mathcal{T}$$ is the same as $$\mathcal{T}(0)$$! (no that is not factorial).

# Pointlessly analyzing Hanon
We have a tool to perfectly describe [Hanon][2]!
For those that don't know about it,
Hanon is canon when learning the piano.
Let's look at the first bar of the first exercise then!

![](https://image.jimcdn.com/app/cms/image/transf/none/path/s65bf75cc20d9b494/image/ibff5c6ff45f8a884/version/1533612361/piano-technique-exercise-n-1-in-c.jpg){:width="5cm" height="5cm"}

We begin at middle C, go up by two, and then by one until we hit A. Go back down via the same pattern.
This our sequence then.

$$\mathcal{T}(0),\mathcal{T}^4,\mathcal{T}^5,\mathcal{T}^7, \mathcal{T}^9,\mathcal{T}^7,\mathcal{T}^5,\mathcal{T}^4$$
# Realizing How Bad This Description Is
This is great. We have a framework to describe music. But it lacks in a lot of ways. 
We can't look at chords for one.
We can't look at different rhythms.
We can't look at key signatures.
We can't look at octaves.
We can just look at steps.

It would be very nice if this model were improved significantly.

[1]: https://en.wikipedia.org/wiki/Hugo_Riemann
[2]: https://www.hanon-online.com
