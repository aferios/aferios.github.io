---
layout: post
title: Proof for Maximum Number of Solutions
date: 2019-12-22
categories: jekyll update
---

Around the end of September or beginning of October, I played through a trilogy called Zero Escape.
They revolve around a series of "escape room"-like games.
The characters pitted have to escape some unknown area by solving puzzles, and they're really nice puzzles to solve.
If they don't they might die. In the second game of the trilogy, there's a system that dictates how the players
can navigate the area.

There are three doors, each assigned a unique color: yellow, cyan, and magenta. Three people must present at this door to open it;
however, there is a catch. Each person has assigned to them a color--red, green, or blue--and some are assigned a pair.
Those who are assigned a pair, share the same color. Pairs must never be seperated when traveling through a door.
Those who are not in pairs are free to travel wherever they please as long as they are able to go through the door.
To open the door, the players's or pair's colors when mixed must either match the same color,
or be the color's compliment.
How many ways are there for this group of people to travel?*

Let's decompose what is given.
Three pairs makes a total of six people in pairs. Let's conjure our players by the following label system:
$$p_1, p_2,\cdots, p_9$$

Now we must first assign pairs. There is a number of ways to do this but let's go with something simple.
$$(p_1,p_2), (p_3,p_4), (p_5, p_6), p_7, p_8, p_9$$.

As of right now, it is clear what a solution is not. Pairs cannot travel with pairs. 
This is just as true as the statement singles cannot travel with singles.
Now, without assigning colors just yet, we know the form for a possible solution. It looks something like this:
$(u,v)$ such that $u$ is an pair and $v$ is a single. From this alone, we can find the possible solutions.
If you've taken a counting class (more commonly known as a combinatorics class in colleges), then you know the form.
But let's build this from the ground up. We have the ordered pairs and the singletons.
and an ordered pair must go with a singleton. Cycle through the solutions one by one, and we will yield a form.
The following is a possible solution: $$\{\ ((p_1,p_2),p_7),\ ((p_3,p_4),p_8),\ ((p_5,p_6),p_9)\ \}$$
This works as well: $$\{\ ((p_1,p_2),p_8),\ ((p_3,p_4),p_9),\ ((p_5,p_6),p_7) \}$$
There are a few more. But we know the general pattern.
It looks something like this:
$${\ (u_1,v_1), (u_2, v_2), (u_3,v_3)\ }$$
But we can change where the $$u$$'s and $$v$$'s land throughout the solution given our constraints.
In other words, solutions can show up in three ways. 
For the first element in our solution set (in other words, the first stuff in parentheses inside the brackets {} ), 
we can choose any $$u$$ to pair up with any $$v$$. So out of three of the $$u$$'s pick one,
and out of three of the $$v$$'s pick one as well. This is a total of 3 free choices.
For the next element, we can choose all but one of the $$u$$'s or $$v$$'s (the one we picked last), This translates into 2 choices.
and for the last element, we only have one choice. This is just 1 choice.

Hence, we have $$3*2*1$$ or 6 solutions. Now we have a maximum number of solutions for the ways people can travel.
We still have to put on our color constraints. Let's make this meld with the given color constraint.
I once took an art class in secondary, but I'm not about to recall all the material from that class, so I just
searched up a color venn diagram online and yielded this: 
[venn diagram]
Fine and dandy. Just what we need. Red and green yield yellow, Blue and red yield magenta. Green and blue yield cyan.
This diagram also gives us the compliments.
Green and magenta are compliments; red and cyan are compliments; blue and yellow are compliments.

From here it becomes fairly clear how many solutions there are.
But let's double tap this problem into the ground before it decides to fight back.

Now we can assign pairs and singletons colors. There's a number of ways to do this but let's pick the simplest one.
A pair $u_i$ and singleton $$v_j$$ will share the same color if $$i=j$$. This yields a nice and immediate consequence.
Solutions of the form $$\{(u_i, v_i) \|\ i\in \{ 1,2,3\} \}$$ are valid.
This is the solution for the complimentary colors of the doors, or the complimentary (C) solution.

I wouldn't really call this much of a proof as much as a calculation. Not to mention, it's pretty ugly as it stands
since we used a pretty brute-force-y method. It's not pretty; it's not cute; it's not really much of anything.

I read a wonderful piece once by a Professor Bruce Reznick on what to do after you've proved something.
He says "... water it and make it grow... Return to your theorem. Try to *push* the conclusions... What if you play with the hypothesis?"
Let's do exactly that. Let's push the limits of our conclusion by tweaking our question.


[venn diagram][//assets/img/venn.png]
