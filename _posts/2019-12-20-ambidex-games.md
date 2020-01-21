---
layout: post
title: Ambidex Games
date: 2019-12-20
categories: jekyll update
---

# Ambidex Games
![Lagomorph Announcing the Ambidex Games: Image taken from Zero Escape: Virtue's Last Reward][lagomorph]

Around September of 2019, I dived into playing a visual novel/click-and-point puzzle trilogy called Zero Escape.
I played the first one *999* on my friend's DS (thank you Paul) and decided to play the rest of the games on my PC.

The plot revolves around a series of games called the Nonary Games, 
and a whole mess of events that make no sense without a tome of context, 
but one of the mechanics inside this game is a decision based game--called the Ambidex Games--
reminiscent of the Prisoner's Dilemma. Thus, this iteration of the nonary games is called Nonary Games: Ambidex Edition.
It should be noted that the objective of each player in every iteration of the game is to live;
however, this is just a side effect of events that may happen within the game. There is always a **main** objective.
In this particular iteration, the main objective is to escape through a door. 
How one escapes through this door will be clarified later.

Now of course, this wouldn't be interesting without a twist to it. Here's how the Ambidex Game,is played.
At the beginning you are assigned to a color. There are three in total and they change throughout the game.
Depending on this color, you are forced to group up with people of another particular color--and even before this,
you are predisposed to be a single player or a co-operative player. This will be explained later.
In addition to the color and player state (co-op or single), they are all pre-disposed with a digit of three.
These are the three main components of the game.
Tha mapping is fairly specific here, Later, I will introduce some functions here to help make sense of it.
For now, let's look at the first cycle of this Ambidex Game. 


## An example (or a cycle)
The game starts off with nine characters:
Sigma (a college student),
Phi (a girl with seemingly super muscle strength and unknown origins), 
Clover (a past participant of the nonary games), 
Alice (a woman working with a secret operatives group),
Quark (a young boy),
Luna (a very caring woman),
Dio (a mischievious hoodlum),
Tenmyouji (an old man with a seemingly familial relationship with Quark),
and K (who is only introduced as a person in a suit of armor and with amnesia).

They all have a bracelet that assigns them the three main components of the game.
Sigma, Phi, and Alice are assigned red. Sigma and Phi are co-op, so they must stay together. This leaves Alice as a single player.
Tenmyouji, Clover, and K are assigned green. Clover and K are co-op. Tenmyouji is a single player.
Dio, Quark, and Luna are assigned blue. Dio and Quark are co-op. Luna is a single player.
In order for them to survive this cycle of the game, it is imperative for them to form groups of three, and three only,
in a manner that when their assigned colors are mixed, they make a new color assigned to that of a door.
There is an alternate solution. They may also mix their colors 
such that they make the compliment of a color assigned to a door.
We will call the former solution a non-complimentary (NC) solution
and the latter a complimentary (C) solution.

In the beginning there are three doors assigned magenta, cyan, and yellow. 
Conjure the possible combinations of groups. This is where co-op and single players come in.
If one is a co-op player, they cannot separate from their co-op partner.
For example if we go with the non-complimentary solution,
Sigma cannot travel with anyone but Phi. If he chooses to go through the magenta door,
he is forced to go through the door with at least Phi and one other player (Luna).
The following are the possible combinations for an NC solution.

((Sigma, Phi), Luna) = Magenta
((Dio, Quark), Tenmyouji) = Cyan
((K, Clover), Alice) = Yellow

or

((Sigma, Phi), Tenmyouji) = Yellow
((K, Clover), Luna) = Cyan
((Dio, Quark), Alice) = Magenta

The following is the C solution.
((Sigma, Phi), Alice) = Red = Compliment(Cyan)
((Dio, Quark), Luna) = Blue = Compliment(Yellow)
((K, Clover), Tenmyouji) = Green = Compliment(Magenta)

Here's a fun one. Can we come up with an upper bound for NC solutions?

As of right now, this choice is arbitrary for survival. Nobody knows if there are any consequences for choosing
travel with a certain group over others. However, this will become more apparent in the second cycle.
(If you've played the game, then you know somebody knows the full set of rules at this point.
I argue that this doesn't really matter in the end for this cycle since the player is the one ultimately making the decisions.)

At this point, you jump through a few hoops, do as the game tells you, solve some puzzle,
and out you come to finally play the main event of this nonary game: the Ambidex Game.
Here is where things get interesting in terms of decision making.

Say you've chosen to travel with the complimentary solution.
After doing some puzzle solving, each of the players go into voting cells. If one is a co-op player,
you have no other choice but to go into the same cell as your partner. If one is a single player,
you have no other choice but to go into a cell by yourself.
For purposes of explanation, a co-op group will be referred to as a unit, 
and the single player they traveled with will be reffered to as their opponent.
Units will vote against their opponent, opponents will vote against their units. 
Every unit and opponent gets to either elect "Ally" or "Betray". 
This is where the point system comes in which is directly connected to the digit three everyone was assigned earlier.

The consequences of each outcome is displayed in the table below.

$
\begin{tabular}{ c | c | c }
  			& \textbf{Ally}		&  \textbf{Betray}	 \\
  \textbf{Ally}		& +2			&  -2    		 \\
  \textbf{Betray}	& +3 			&  0			 \\
\end{tabular}
$

Either column or row can be designated user or opponent. That doesn't really matter.
The pluses and minuses act on your points. Right now, everyone starts with three.
The minimum a unit or opponent will end up with is 1 and the maximum is 6. 
In a game, where it is imperative to travel in groups of three or face death, for some reason we all have this notion
that the lower a number is, the shorter your fate runs.
Once you vote, the outcome will show on a nice screen and players of the game can commence bickering.
Why bicker? Well, nobody really knows what will happen if you hit zero,
but it is in everyone's interest to stay away from that number for as long as possible.
If you remember the main objective of this game, it is directly tied with this Ambidex Game within the Nonary Game.
The goal is to reach 9 points so you can open the door; however, the door will open once, and only once. 
There's a lot to unpack when it comes to decision making.

## The Prisoner's Dilemma
Now, how do we know it's the Prisoner's Dilemma? Well let's recall what the story is.

Everyone I know says it's a thought experiment, but it's actually not. This really happened a long time ago in
the 18th century. You see, two French civilians, Adda Core and Jean Pierre Jean Jacques, 
had just been accused of witchcraft.
You see, Jean Pierre Jean Jacques was not exactly the best looking man.
<details about how ugly he was here>
Fortunately for him, he was married to Adda. Unfortunately for his wife, she was married to a trog,
and her shallowness drove her to come up with a way to get rid of him; however, she cannot just murder him
and call it a day. The royal guards nowadays will find any excuse to put you in prison, so she devised a plan.
A few months passed and she had gathered enough coin to execute her scheme.
At the end of a long day, working in the field, she invited her dear to the bar and said to him
"drink to your heart's content", and so he did. He pounded on the alcohol harder than the bartender had ever
seen.
Jean Pierre Jean Jacques was dazed as can be, and so Adda continued with her plan, motioning her
husband to a barmaid and claiming she was giver her eyes when he wasn't looking. Without miraculously passing out,
UI settled on two french prisoners from the revolution era named Adda Core and Jean Pierre Jean Jacques. But I caI settled on two french prisoners from the revolution era named Adda Core and Jean Pierre Jean Jacques. But I caI settled on two french prisoners from the revolution era named Adda Core and Jean Pierre Jean Jacques. But I cahe marched on out of his seat, motioned to the barmaid, and without a word coming out of 
Jean Pierre Jean Jacques, the barmaid shrieked. Adda Core ran out of the bar, searched for a royal guard and said
"quickly! Quickly! My husband is fancying another woman that is not me! He has violated the church, the crown,
and our bond! Arrest him at once and free me from these marital chains he has damned!"
The royal guard made haste towards the bar. The bartender was trying to get Jean Pierre Jean Jacques's wandering hands
away from his daughter, and all the other drunkards were oggling at the sight before them.
The royal guard bashed him over the head with a glass and started to drag him out.
As this was happening, the guard overheard talk of a rumor, saying the man was so heinous looking that the only
way he could have had that barmaid--or anyone human for that matter--is through demonic possession. Another of the
regulars speaks to his drinking buddy, asking if he saw the way the woman was not automatically repelled by his looks.
Another drunkard was commenting local folks at a table saying the barmaid surely didn't shriek out of disgust, but out
of flattery.
"Could it be witchcraft?" thought the guard. No. Impossible. The only ones capable of witchcraft are women. Unless...

He quickly found the wife, took her hand and forced her with him. They were both imprisoned for witchcraft.

Adda Core, baffled and worn from the travel, wondered why she was imprisoned. Months passed. 
Both Jean and Adda had lost track of time in their separate cells, far away from each other. 
Their cells had sigils drawn around them to stop any witchcraft from being conducted inside the cells.
No telepathy, no escape tricks. nothing for them to use to escape. Who knows what absurd magic these witches have up their sleeve?!
Finally, a guard came to both, one at a time.
His name was Alain Proviste, and he offered them both the same deal.
"Now I know at least one of you is a witch. One doesn not get that ugly and turn out with a barmaid seduced by the same
heinous look. So now, was it a team effor? Did both of you conduct witchcraft? Or is it the one you vowed your life
with? If you confess for the sins of the one you vowed your life with, your marital partner if you will,
I can guarantee a reduction of your sentence in the royal prison to one year,
and your marital partner will serve fifteen. But if I find out both of you have committed sin,
then I can reduce the sentence to ten years, for making me look like a hero. 
I have shared this information with your marital partner."
Alain Proviste leaves, with his armor clapping.
Of course the guard wasn't going to reduce their sentence at all. The accused will be executed,
but Jean Pierre Jean Jacques and Adda Core are none the wiser.

If jean Pierre Jean Jacques wanted to be selfish his best bet is to confess, assuming his dear is as faithful as can be.
That would reduce his sentence to a year. If she confesses however, They will both be in the royal slammer for 10 years.
How to get the best possible outcome then? The optimal solution is to stay silent.
Two years is considerably less than 10 years should you both confess; 
however, if one stays silent there's a risk the other will confess.
This just leads back to a solution that one should just confess.
Is it really the case that this "logical" decision leads to an unfavorable outcome for the individual and the party?

Now unfortunately, Jean Pierre Jeane Jacques and Adda Core are peasants.
They have no education and can only think back on the reasons why they are such bad marital partners.
Within a a split of a moment, they each confess and yell to the guard 
"I confess! Jean Pierre Jean Jacques/Adda Core has been practicing in secret! 
I witnessed him/her conjuring and making a deal with Aamon/Bilet. I swear by it, so help my soul!"

The very next day, both were dragged out in shackles and cast onto the razor of justice.
They uttered their famous last words to each other in unison: "this is all your fault".

## The Math
So what makes a prisoner's dilemma? There'a very easy way to check if you have two players.
Most prisoner's dilemmas are symmetric. We can draw it on a table

$
\begin{tabular}{ c | c | c }
			& \text{Decision A}	& \text{Decision B}	\\
\text{Decision A}	&	(u,u) 		& 	(x,y) 		\\
\text{Decision B}	&	(y,x) 		& 	(v,v) 
\end{tabular}
$

The entries of our tables are ordered pairs. The column and rows represent the decision they correspond to.
If we go with decision A, and pin that against decision A, that yields the same consequence for both parties.
Likewise for B.
However, if we pin decision B against A, one is likely to win over the other. 
For the Jean Pierre Jean Jacques and Adda Core, their table would look like this:

$
\begin{tabular}{ c | c | c }
			&\text{Silence}		& \text{Confess}	\\
\text{Silence}		& (2,2)			& (1,15)		\\
\text{Confess}		& (15,1)		& (10,10)
$

Now if Jean Pierre Jean Jacques were to pick confess. Then Adda Core should also pick confess.
We visualize this with arrows

$

$



## Decisions Decisions
Now that you know the scenario for the prisoner's dilemma, you play it out.
The outcomes show up on the board for everyone to bicker about. Now this is repeated a few more times in the game.
There's a lot to unpack here. 
There's the fact that two people make one decision and that affects them both;
there's conditional decisions based on what was in the previous cycle of Ambidex Game;
there's decisions between two parties (i.e. how do you decide who makes casts the final vote in a unit);

Well let's see. We can


We have three colors, hence three sets: $X,\ Y,\ Z$. The colors cycle throughout the game,
but hopefully I'm not stupid enough to actually mess up the math. Within each other, there are 3 people.
So three unique elements of each set and their union yielding a cardinality of 9. Call $U$ the union of all sets/colors.
Now we just need mappings,three to be exact. But it's not just as simple as mapping doing $f:X\to\X'$.
We require these 
[lagomorph]: ../assets/img/lagomorph.png
