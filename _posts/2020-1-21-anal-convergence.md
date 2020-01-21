---
layout: post
title: Analysis Proof
date: 2020-1-21
categories: jekyll update
---

Looking over my scratch work for mathematics, I never realized how much I struggled with my proofing.
One in particular caught my eye which I am willing to share with you. I took the problem out Terence Tao's Analysis I.

*Let $X\subset\mathbb{R}. f: X\to\mathbb{R}, E\subset\mathbb{R}, x_0$ an adherent point of $E$, $L\in\mathbb{R}$*
*Then the following are equivalent:*
*a) $f$ converges to $L$ at $x_0\in E$*
*b) For every sequence $(a_n)_n^\infty$ composed entirely of elements of $E$, converging to $x_0$, the sequence $f((a_n)_n^\infty)$ converges to $f(x_0)$.*

Now this is a handful to digest if you've not taken analysis so I will give a quick run down of the definitions.
Firstly, what is an adherent point? Well if we pick a subset $X$ of the real numbers, and a point $x$ in the real numbers
(not necessarily part of $X$), then we say 
$x$ is an adherent point of $X$ iff the distance between some particular number of $X$ and $x$ is at most $\epsilon$
for all $\epsilon$.
Illustrated, this is just $x$ is an adherent point if and only if for all $\epsilon>0$, $d(y,x)\leq\epsilon$ for some $y$ in $X$.
The operator $d(-,-)$ is just the distance form. On a real line it's just $|x - y|$.
This matter of $\epsilon>0$ may be confusing. It just means that we can pick an $\epsilon$ that satisfies this condition. We can also pick another one and find $y$ to satisfy the condition. We can also pick another... and another... and another... we can be doing this for eons and it wouldn't matter. We can always pick a positive number and find a $y$ to satisfy this equation.
Great! We know what an adherance point is. But what's a sequence? What's it mean to converge? 
Is there a difference between a function converging and a sequence converging?

