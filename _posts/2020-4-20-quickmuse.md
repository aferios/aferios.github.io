---
layout: post
title: Quick Analysis
date: 2020-4-20
categories: jekyll-update
---
Following up on the post on neo-Riemannian music theory,
I think I may have underestimated this model's potency.
It's primitive. But let's just do some quick analysis.

I may have lied about analyzing key signatures. We definitely can represent key signatures. It's just sloppy.

A while ago, I transcribed a song onto guitar for someone's birthday, thus the sheet music exists.
The song I transcribed was [this]][1], or "Your Birth Date".

It's a cute song, and it was a bit difficult to transcribe because my guitar is locked up in her case.
So I had to go into this a bit blind.

What I want to look at are the instances of where the notes "sing" the phrase *happy birthday to you*.

```lilypond
\relative {
  <c' e g>
}
```
