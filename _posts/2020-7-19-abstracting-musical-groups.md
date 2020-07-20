---
type: post
title: Musical Groups Further Abstracted
date: 2020-7-19
category: jekyll-update
---

So we've done some elementary algebra, elementary number theory,
and we've come up with ~~complete garbage~~ 
a jumping off point for diving deeper into rediscovering a nice framework for composing music.

I think the most important observation made is that context matters.
Individual notes by themselves aren't what we want to capture.
We want to capture how they play, why they play the way they do,
and if there is something that makes sequences of notes *tick* in a manner unlike any other familiar system.

So let's think even more abstractly.
What we are searching for is a way to capture, not just notes. 
but chords, 
triads, 
and all the fancy lingo there is in the music vocabulary.
Call these things musical objects. 
We don't know what we're really staring at here, but it helps to give it a label.
For each $$n$$ consecutive musical objects, we want to encapsulate some sort of distance to them.
This isn't just distance that you can just count though.
This should be an encapsulation of *all* the distances. 
Mathematicians aren't terribly concerned with the $$n=2$$ case. 
Mathematicians want all $$n\in\mathbb{N}$$.
This distance should encapsulate going from musical object I to musical object II.
Maybe a description of transposition? Maybe a description of modal transformations?
Let's go wild: a description that maps one object onto frequency space,
maps it to an integer, which goes through a process of algebraic manipulation, spits it back onto frequency space,
and yield a whole new musical object altogether.

# I Looked Up the Recipe in a Book

Let's stop dreaming and actually put some structure to whatever this unholy thing will eventually be--which will actually look a bit familiar.
Here's what we want:

Generalize distances should be composed. Call $$\mathcal{M}$$ a musical object. Consider three (distinct) of them,
$$\mathcal{M}_1, \mathcal{M}_2, \mathcal{M}_3$$. The distance from $$\mathcal{M}_1$$ and $$\mathcal{M}_2$$,
can be encapsulated by just the regular distance operator, so $$d(\mathcal{M}_1, \mathcal{M}_2)=\mathcal{D}_1$$.
Likewise $$\mathcal{D}_2=d(\mathcal{M}_2,\mathcal{M}_3)$$.
Then we want to be able to yield $$d(\mathcal{M}_1,\mathcal{M}_3)=\mathcal{D}_3$$ 
to just be $$\mathcal{D}_1\circ\mathcal{D}_2$$. 
We may even want $$\mathcal{D}_2\circ\mathcal{D}_1=\mathcal{D}_3$$ if we're feeling brave.

As we've seen before, identity transformations are useful.
They help us denote when things *don't* change. 
Hence, we would like $$d(\mathcal{M}_n, \mathcal{M}_n)=\mathcal{D}_{id}$$, for $$n$$ in some indexing set,

It is also helpful to note that for any two arbitrary objects,
if $$d(\mathcal{M}_2,\mathcal{M}_1)= \mathcal{D}_i$$ and $$d(\mathcal{M}_1, \mathcal{M}_2)=\mathcal{D}_j$$,
then $$\mathcal{D}_i\circ\mathcal{D}_j=\mathcal{D}_{id}$$.
This just simply means, if we can calculate the distance between two objects, going forward and going backward,
then if we calculate the distance going forward and then backward, we *should* get the identity transformation back.
This is analagous to our Muse Group $$(\mathcal{T},\circ)$$.
If we went up $$n$$ tones and then down the same number of tones,
we would effectively be not moving up or down at all in tuning space.

Fortunately, the heavy lifting has already been done by [Lewin][1]--yes that Lewin, 
the theorist who wrote multiple papers and essays and contributed originally to his respective field with first-hand discoveries, and could've been found in the recent past at an Ivy League University.
There is no need to cook up another group, structure, framework, whatever. 
Let's just take Lewin's word for it.

# The GIS
**Definition**: A generalized Interval System (GIS) is an ordered triple ($$S$$, $$IVLS$$, $$int$$) 
where $$S$$, the space of the GIS. is a a family of elements of $$IVLS$$,
the group of intervals for the GIS, is a mathematical group, and $$int$$,
is a function $$int: S\times S\to IVLS$$ subject to the following conditions.
 - A) $$\forall r,s,t\in S,\ int(r,s)\circ int(s,t)=int(r,t)$$
 - B) $$\forall s\in S, i\in IVLS, \exists! t\in S\$$ such that $$t$$ lies in the interval $$i$$ from $$s$$ satisfying $$int(s,t)=i$$

Okay let's break it down. What is $$S$$? The set $$S$$ is a the space of the generalized interval system.
What is $$IVLS$$? It is a group of intervals for the GIS.
What is $$int$$? It is simply a function. Take elements from $$S\times S$$ to $$IVLS$$, 
and it satisfies the conditions A) and B). 
What is condition A)? It states that for all $$r,s,t$$ in $$S$$,
it is the case that $$int(r,s)\circ int(s,t)=int(r,t)$$.
This is extremely similar to our distance formulation. 
You might be wondering how we allow composition to take in another variable when $$int$$ is already binary.
I claim this is old news, and you've done it already.

# Condition A
Recall, we had three musical objects: $$\mathcal{M}_1,\mathcal{M}_2,\mathcal{M}_3$$.
If we calculate the distance from $$\mathcal{M}_1$$ and $$\mathcal{M}_2$$, this would just be
$$\mathcal{D}_1=d(\mathcal{M}_1,\mathcal{M}_2)$$.  Likewise,
$$\mathcal{D}_2=d(\mathcal{M}_2,\mathcal{M}_3)$$. 
Once again, we want to be able to compose these two in order to yield $$d(\mathcal{M}_1,\mathcal{M}_3)=\mathcal{D}_3$$.
Rephrased once more, we want to compose $$\mathcal{D}_1$$ and $$\mathcal{D}_2$$ to yield $$\mathcal{D}_3$$.
Rephrased once more again, we want $$\mathcal{D}_1\circ\mathcal{D}_2=\mathcal{D}_3$$.
Now we substitute and reveal      

$$d(\mathcal{M}_1,\mathcal{M}_2)\circ d(\mathcal{M}_2,\mathcal{M}_3)=d(\mathcal{M}_1,\mathcal{M}_3)$$

This is what we wanted. Lewin just put it a little more neatly.
But this still leaves up in the air what unholy magic we've done.
Because once again, we still don't know.
What deal have we made that allows us to compose $$int(r,s)$$ and $$int(s,t)$$.
Lewin has made that deal for us already.
In his book [Generalized Music Intervals and Transformations][2],
he goes on to prove that this composition is an equivalence class.
As a result, we're able to immediately jump to the conclusion of condition A).

As a bit of a side note, this is why I love algebra so much.
It is the mathematician's deal with the devil.
In exchange for your vision (although Atiyah would call this your soul), 
he will grant you a powerful tool to compute anything you'd like,
without regard for your precious graphs and visualizations.
Even when I was in elementary or middle or high school I would despise the thought of laboriously drawing a graph.
Why would I waste my time thinking about shapes when a simple calculation can tell me the root of a polynomial.
This was all up until I took Complex Analysis.
In which case I would be very happy to visualize transformations in $$\mathbb{C}$$.
However, I am also hypocritical. Because even back then I would draw graphs without realizing it.
Visual intuition is a marvelous thing.
[There's a very nice essay written on this exact topic.][3]

# Condition B
Lewin claims this is to guarantee $$S$$ is large enough to contain all the elements we need.
This is just a really slick way of saying the function is closed.
In the same way addition is closed under the integers, $$int$$ is closed under $$S$$.
As Lewin puts it, "if we can conceive of an elements $$s\in S$$,
and we can conceive of a characteristic measurement, distance, or motion $$i$$,
then we can conceive of an element $$t$$ which lies the interval $$i$$ from $$s$$."
Let's dial it back a bit.

We have musical object $$\mathcal{M}_i$$, and some notion of distances of other musical objects with respect to $$\mathcal{M}_i$$.
For instance, we indeed have $$d(\mathcal{M}_i,\mathcal{M}_2)=\mathcal{D}$$.
We know this. We can quantify this somehow. Now while we're doing this, condition B) just says
there is indeed another musical object $$\mathcal{M}_j$$,
such that we can use our already god-given notion of measurement, to find $$d(\mathcal{M}_i,\mathcal{M}_j)$$,
without any regard to $$\mathcal{M}_2$$.

Back to Lewin's formalities.
In other words, we know $$s\in S$$. Just pick any $$s\in S$$. 
There must be a *unique* $$t\in S$$ which holds the property

$$int(s,t)=i$$

# Properties Falling Into Our Laps
Great. Alright Lewin, I've used your recipe now where are all the other properties I wanted?
Well he argues those are given to us for free, and he is absolutely correct.
We get identity for free. Just take $$int(s,s)$$. We know what that is by the first condition $$int$$ must meet.
Left composition by inversion yields $$int(s,s)=int_{id}$$. Most algebraists call this special number $$e$$.
[Yes that $$e$$][4]--the $$e$$ that may come up 
when you want to take a derivative over and over again and still get the same thing.

Inversion follows very quickly. We get $$int(s,t)=int(t,s)^{-1}$$. We know how to get $$in(s,s)$$ from property A).
We just apply that and it falls into our laps.

He also goes off on the specifics of weakened condition B) which just partitions $$S$$ into cosets.
However, we don't really have anything interesting there.
What we do have though, is a bunch of exotic algebra here.
This will be unwrapped in a later post.


[1]: https://en.wikipedia.org/wiki/David_Lewin
[2]: https://www.oxfordscholarship.com/view/10.1093/acprof:oso/9780195317138.001.0001/acprof-9780195317138
[3]: https://people.math.umass.edu/~hacking/461F19/handouts/atiyah.pdf
[4]: https://en.wikipedia.org/wiki/Identity_element
