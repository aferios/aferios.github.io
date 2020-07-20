---
type: post
title: Applying the Muse
date: 2020-7-18
category: jekyll-update
---

I may have fibbed a bit. In the group we had conjured, it is indeed possible to analyze scales;
however, I think it's important to note the limitations of which scales we can analyze in the first place.
If we take the all-familiar C major scale most of us know,
then any song written in C major can be trascribed to this musical group (if we have no regard for rhythm).
Likewise, any song written in B minor can be trascribed.
One assumption we've made by conjuring this group $$(\mathcal{T},\circ)$$, is our subsciption to a certain tuning.
We recognize that there are indeed notes between C and C#, 
but for whatever reason sometime ago, we all decided to omit those notes when we agreed on this system.
Those reasons range from petty "oh, those notes just sound cacophonous with all the others",
to the more reasonable "well, we get sufficiently enough tones when we combine a few intervals".
Whatever that reason may be, it is important to be conscious of this.
We can go even deeper and subscribe to the thought that every step in our group increases by $$2^{\frac{1}{2}}$$.
We can even extend our group to be more inclusive of notes in between C and C#,
or restrict our group to be exclusive and only be mindful of a note sequence like the pentatonics.

Also, being able to look at octaves is debatable as you will see in a bit.
Simply put, it's possible to eject the same note even if they're not played at the same frequency.

# Appealing to our Muse Group
Anyways, we have this new thing, and I wanna try it out.
Let's see if anything meaningful can be produced from our Muse Group.

Some time ago, [I transcribed a song][2] from saxophone and vocals to fingerstyle guitar.
The vocals sing a little tune that is repeated throughout the song and sometimes on different notes.
There's one tune in particular that is sung a total five times. 
Altogether, there are six copies of that tune and one of them is a pseudo-copy.

<img src="../assets/img/music/measures-1.png" width="5" height="5" />

I call V the pseudo-copy since it's "missing" a bit of the tune. 
Although, others might say silence is just as good as a note.
This was transcribed for guitar, 
so it's a bit messy to actually read these chords and this goes double for our Muse Group.
A tool like Neo-Riemannian Analysis would be able to take in the chords and do some analysis.
Unfortunately, we're not there yet.
Filtering out to yield something like the melody isn't terribly difficult.
One method is just take the top notes of all the chords.

<img src="../assets/img/music/melody-1.png" width="5" height="5" />

Now we have something that can be read by our Muse Group.
It's in the key of Eb minor. 
The sequence for that would be      

$$\mathcal{T}^3, \mathcal{T}^5, \mathcal{T}^6, \mathcal{T}^8, \mathcal{T}^{10}, \mathcal{T}^{11}, \mathcal{T}^{13}. \mathcal{T}^{15}$$

Now here, we're at crossroads. It's true that $$\mathcal{T}^{15}=\mathcal{T}^{3}$$. That is just Eb but an octave above.
Must we sacrifice every note above $$\mathcal{T}^{14}$$ and rewrite them back into our scale?
Well for that matter, why not designate $$\mathcal{T}^0$$ as Eb and sacrifice every note above $$\mathcal{T}^{12}$$, 
unless we really want to flex our counting skills and just start counting at $$3$$.
I would very much like to designate $$\mathcal{T}^0$$ as Eb,
and since our melody operates within three octaves, we will not disregard the notes above $$\mathcal{T}^{12}$$.
Our sequence of notes to chosoe from is then    

$$\mathcal{T}^0, \mathcal{T}^2, \mathcal{T}^3, \mathcal{T}^5, \mathcal{T}^7, \mathcal{T}^8, \mathcal{T}^{10}, \mathcal{T}^{12}$$

and on the next octave we have

$$\mathcal{T}^{12}, \mathcal{T}^{14}, \mathcal{T}^{15}, \mathcal{T}^{17}, \mathcal{T}^{19}, \mathcal{T}^{20}, \mathcal{T}^{22} \mathcal{T}^{24}$$

and on the last octave,

$$\mathcal{T}^{24}, \mathcal{T}^{26},\mathcal{T}^{27},\mathcal{T}^{29},\mathcal{T}^{31},\mathcal{T}^{32},\mathcal{T}^{34},\mathcal{T}^{36}$$

The math checks out, and we have the set of notes to choose from.

# Crash Course on Reading Notes a Treble Clef Staff
It may be the case we don't know how to read notes from a staff.
Allow me to enlighten you.
The simplest way to read a treble clef is to note where the spiral at the bottom of the clef tends twoards.
That line (second from the bottom) is natural G, and revolving around G is a Gb and G#;
we don't really give Gb and G# their own space. 
The practice is to just append a simple mark of a sharp or a flat to denote that it is indeed flat or sharp.
So now that you know where G is, you just sing your ABCs as if you were a broken record player.
A-B-C-D-E-F-G...A-B-C-D-E-F-G...A-B-C-D-E-F-G.. and so forth.
If you go up, then you sing your alphabet forwards. If you go down, then sing your alphabet backwards.
There are pneumonics out there that help you memorize which note is which right off the bat.
but I never bothered to learn them because it was just one more thing to remember.
Playing an instrument, I believe, is the best manner to get intimate with the notation.
But this manner works as well.

The next thing to note is the key signature. 
That's the noise on the left side with just flat or sharp symbols with no notes attached.
It can come either in front of the clef, 
or in front of the time signature and behind the clef--at least from what I've seen.
For the rest of that line, those flats and sharps designate which notes are forever flat and sharp.
The key signature also gives you extra information on which scale we're using,
but for our purposes we'll just "observe" this fact from the point of view of our Muse Group.
(In fact we already have.)

The numbers just denote a time signature.
Our Muse Group doesn't account for anything in the time space, just the tonal space.
So we don't need to know anything about these numbers. 

[For those wanting a more in-depth exploration of the treble clef...][1]

# Feeding the Phrases
Now that we all know how to read treble clefs for those cursed with vision,
let's write down where our notes are.
For the sake of keeping track of which octave each note is in,
I will denote it by appending a number from 1 to 3,
with 1 signifying it is part of the lowest octave, and 3 signifying it is part of the highest octave.

**Melody I:**
$$\text{Db}_3, \text{Bb}_3, \text{Bb}_1, \text{Db}_1, \text{Bb}_3, \text{Db}_2, \text{Ab}_3, \text{Gb}_3$$

$$\mathcal{T}^{34},\mathcal{T}^{31},\mathcal{T}^{7},\mathcal{T}^{10},\mathcal{T}^{31},\mathcal{T}^{22},\mathcal{T}^{29},\mathcal{T}^{27}$$

$$\mathcal{T}^{10},\mathcal{T}^{7},\mathcal{T}^{7},\mathcal{T}^{10},\mathcal{T}^{7},\mathcal{T}^{10},\mathcal{T}^{5},\mathcal{T}^{3}$$

**Melody II:**      
$$\text{Db}_2, \text{Bb}_2. \text{Bb}_1, \text{Eb}_2, \text{Gb}_3. \text{Db}_2, \text{Db}_1, \text{Ab}_3, \text{Gb}_3, \text{Gb}_3$$

$$\mathcal{T}^{22},\mathcal{T}^{19},\mathcal{T}^{7},\mathcal{T}^{12},\mathcal{T}^{27},\mathcal{T}^{22},\mathcal{T}^{10},\mathcal{T}^{29},\mathcal{T}^{27},\mathcal{T}^{27}$$

$$\mathcal{T}^{10},\mathcal{T}^{7},\mathcal{T}^{7},\mathcal{T}^{0},\mathcal{T}^{3},\mathcal{T}^{10},\mathcal{T}^{10},\mathcal{T}^{5},\mathcal{T}^{3},\mathcal{T}^{3}$$

**Melody III:**       
$$\text{Db}_3, \text{Bb}_3, \text{Bb}_1, \text{Db}_1, \text{Bb}_3, \text{Db}_2, \text{Db}_1, \text{Eb}_2, \text{Ab}_3. \text{Gb}_3 $$

$$\mathcal{T}^{34},\mathcal{T}^{31},\mathcal{T}^{7},\mathcal{T}^{10},\mathcal{T}^{31},\mathcal{T}^{22},\mathcal{T}^{10},\mathcal{T}^{12},\mathcal{T}^{29},\mathcal{T}^{27}$$

$$\mathcal{T}^{10},\mathcal{T}^{7},\mathcal{T}^{7},\mathcal{T}^{10},\mathcal{T}^{7},\mathcal{T}^{10},\mathcal{T}^{10},\mathcal{T}^{0},\mathcal{T}^{5},\mathcal{T}^{3}$$

**Melody IV:**       
$$\text{Bb}_3, \text{Ab}_3, \text{Cb}_1, \text{Gb}_2,\text{Bb}_3. \text{Db}_2,\text{F}_2, \text{Cb}_2,\text{Ab}_3,\text{Gb}_3$$

$$\mathcal{T}^{31},\mathcal{T}^{29},\mathcal{T}^{8},\mathcal{T}^{27},\mathcal{T}^{31},\mathcal{T}^{22},\mathcal{T}^{14},\mathcal{T}^{10},\mathcal{T}^{29},\mathcal{T}^{27}$$

$$\mathcal{T}^{7},\mathcal{T}^{5},\mathcal{T}^{8},\mathcal{T}^{3},\mathcal{T}^{7},\mathcal{T}^{10},\mathcal{T}^{2},\mathcal{T}^{8},\mathcal{T}^{5},\mathcal{T}^{3}$$

**Melody V:**       
$$\text{Ab}_3, \text{Gb}_2,\text{Bb}_3,\text{Db}_2,\text{Ab}_3, \text{Gb}_3$$

$$\mathcal{T}^{29},\mathcal{T}^{15},\mathcal{T}^{31},\mathcal{T}^{22},\mathcal{T}^{29},\mathcal{T}^{27}$$

$$\mathcal{T}^{5},\mathcal{T}^{3},\mathcal{T}^{7},\mathcal{T}^{10},\mathcal{T}^{5},\mathcal{T}^{3}$$

**Melody VI:**       
$$\text{Bb}_3,\text{Ab}_3,\text{Db}_1,\text{Gb}_2, \text{Gb}_3, \text{Db}_2,\text{Ab}_3,\text{Gb}_3$$

$$\mathcal{T}^{31},\mathcal{T}^{29},\mathcal{T}^{10},\mathcal{T}^{15},\mathcal{T}^{27},\mathcal{T}^{22},\mathcal{T}^{29},\mathcal{T}^{27}$$

$$\mathcal{T}^{7},\mathcal{T}^{5},\mathcal{T}^{10},\mathcal{T}^{3},\mathcal{T}^{3},\mathcal{T}^{10},\mathcal{T}^{5},\mathcal{T}^{3}$$

On the third row of each melody category, I've appealed to the case where we disregard notes above $$\mathcal{T}^{12}$$.
The decision just came from wanting to illustrate something a little more clearly.

# Onto the Why
What I want to answer is why does this sound like the same phrase despite some of the notes being different?
Well, notes by themselves don't form any meaning, and this goes the same for chords.
I can play a collection of notes at the same moment in time and it may sound pleasant or cacophonous;
the same goes for a single note played in a moment in time.
It's not until we bring in other notes that we're able to hear more clearly where the notes fit.
Context matters.

One of the really nice things about our system is the illustration of counting.
We can see clearly we can calculate the distance between two consecutive notes,
we yield the distance between them.
We also want to presesrve sign and you'll see why in a bit.

**Melody I $$M_I$$:**       

$$31-34, 7-31, 10-7, 31-10, 22-31, 29-22, 27-29$$       

$$-3, -24, +3, +21, -9, +7, -3=M^*_I$$

$$7-10, 7-7, 10-7, 7-10, 10-7, 5-10, 3-5$$       

$$-3, 0, +3, -3, +3, -5, -3=M_I$$

What we're doing is taking difference between two consecutive notes.
We want to encapsulate the idea of moving up or down $$n$$ tones.
I argue that these four sequences are the same thing.
We're working in $$\mathbb{Z}/12\mathbb{Z}$$, which is just a slick way to write Integers modular $$12$$.
Within this algebra, we can add and subtract elements just as much as we'd like,
and it would feel like the algebra for integers.
$$31 \text{ mod } 12$$ is just $$7$$, and $$34 \text{ mod } 12$$ is $$10$$.
We can add and subtract these as much as we'd like and we'd end up with a valid congruence relation
that holds. In other words, we can say $$31-34 \text{ mod } 12$$ is $$7-10$$ or $$-3$$.
We can conclude that the sequences $$M^*_I$$ and $$M_I$$ are identical.

**Melody II $$M_{II}$$:**      

$$-3,+12,+5,+15,-5,-12,-19,-3,+0 $$      

$$-3,0,-7,+3,+7,+0,-5,-2,+0$$     


**Melody III $$M_{III}$$:**

$$-3,-24,+3,+21,-9,-12,+2,+17,-2$$

$$-3,0,3,-3,3,0,-10,5,-2$$


**Melody IV $$M_{IV}$$:**     

$$-2, -21,-19,+4,-9,-8,-4,+19,-2 $$

$$-2,+3,-5,+4,+3,-8,+6,-3,-2$$

**Melody V $$M_V$$:**      

$$-14,-16,-9,+7,-2$$

$$-2,4,3,-5,-2$$	

**Melody VI $$M_{VI}$$:**

$$ -3,-19,+5,+12,-5,+7,-2$$

$$-3,5,-7,0,7,-5,-2 $$

We can reduce these even further. By remarking the note sequences back into purely elements of $$\matbb{Z}/\mathbb{12Z}$$, or just the numbers $$0-11$$.
As a result $$M_{II}=9,0,5,3,7,0,7,10,0$$.
We just rewrite $$-3$$ as $$9$$ since it is $$-3 \text{ mod } 12$$ and repeat this process for all non-elements of the integers mod $$12$$.

Now we have something a lot more tangible. From here it is easier to see why these melodies sound like the same phrase.
Here is my interpretation.
Melodies II,III, and IV, have the same number of notes.
We can group up their sequences and yield the following.

$$\begin{bmatrix}
9 & 0 & 5 & 3 & 7 & 0 & 7 & 10 & 0 \\
9 & 0 & 3 & 9 & 3 & 0 & 2 & 5 & 10 \\
10& 3 & 7 & 4 & 3 & 4 & 6 & 9 & 10 
\end{bmatrix}$$

Just by simplying looking at it, we can see some of the numbers in a given column are nearly the same.
For example, the first column $$\begin{bmatrix}9\\ 9 \\ 10\end{bmatrix}$$ is nearly a column of $$9$$s.
The second column is nearly a column of $$0$$s; the fifth is nearly a column of $$3$$s,
and the column right by it is nearly a column of $$0$$s. I want to call a little more attention to the last column.
I hypothesize this collection has a closer distance than it presents itself.
Sure, at first glace $$0$$ is $$10$$ units away from $$10$$.
However, recall that $$12$$ is $$0$$ mod $$12$$. 
From this point, $$12$$ is much closer to $$10$$, 
In our context, that is to say, these two notes are not that distant from each other.
Of course, this is a very lazy description of what is actually going on.

Let's look at the other melody sequences.
I claim that each smaller melody sequence is a subsequence of either $$M_{II}$$, $$M_{III}$$, or $$M_{IV}$$, within error.
By subsequence,
I mean if we take a sequence of strictly increasing natural numbers, and take only those markers of a sequence, we yield a subsequence.

Take $$M_{I}$$ for instance, which I have reduced to $$9,0,3,9,3,7,9$$.
This melody is a subsequence of melody $$M_{III}=9,0,3,9,3,0,2,5,10$$ within error.
If we take the first, second, third, fourth, fifth, eighth, and ninth elements of sequence $$M_{III}$$, yield
$$9,0,3,9,3,5,10$$. Compare this to $$M_I$$. 
We're off on the last two notes which are not all too distant from the original melody.
Using this, we see melody IV is sufficiently close to melody V, 
and melody VI is sufficiently close to melody II.

# Conclusions
Our Muse Group gives us a bit of insight into how musical phrases can sound the same,
despite the same notes being played.
This is just due to how transposition works.
We're able to sing or hum any tune out of key, 
but as long as the distance between the notes is preserved,
we have absolutely no trouble recognizing the melody.
Hence, context matters.

We also considered only one way to actually distill the melody.
Assuming there are indeed more ways to distill the melody, 
we can observe what our Muse Group tells us under those circumstances.
It's not a terrible tool, but, once again, it's rather primitive. All we're doing is counting up.


[1]: http://www.piano-keyboard-guide.com/treble-clef.html
[2]: https://youtu.be/ILHG9-FA4yc
