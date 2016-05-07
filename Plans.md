# AI group plans

## Objectives

- learn Julia

- implement machine learning algorithms in it so as to learn how modern AI works

- see how to use AI on selected problems: see [Project Ideas](Project%20Ideas.md)

Julia (while a general purpose programming language) is really "made"
for scientific computing and should thus be a very good match for us
to implement AI algorithms in (it's likely always possible to get an
edge on performance by directly coding in CUDA/OpenCL/C/Rust/... but
investing effort there is probably not sensible as we probably won't
beat existing libraries anyway, and Julia is going to be much easier
to handle and already very fast (and when accessing existing libraries
in C etc. then it doesn't matter anyway).)

We didn't know what sources to follow for learning about AI, and so I
had just fired up a search for online courses and found the Stanford
one, and given that one of the two teachers is the rather well-known
Peter Norvig, I figured that will be a good choice. I think the videos
are somewhat slow-going, and at first they didn't appear very exciting
to me, but my attitude towards them has changed a bit since now I
think they are valuable to get an overview on what the AI (research)
community is doing, and to get a hold on their vocabulary. Also, those
algorithms like the path search do seem like nice examples to base
learning Julia on.

## Done so far

* watched "Intro to AI" videos 1-34 on Youtube (see
  [README](README.md)). Have implemented the first two path search
  algorithms presented in the videos [in Scheme](https://github.com/LondonHackspaceAI/stanford-intro-ai/tree/master/scheme).

* Borg is usable with Ubuntu (but it's outdated, Debian testing would
  always give access to recent stuff, and Jasper prefers it from an
  admin point of view)

## Next steps

* install Debian on the Borg

* install [Torch](http://torch.ch/) on the Debian on the Borg? (Bob
  has been using it.) Figure out why it doesn't use the available
  cores much. Install Tensorflow, Leaf (see [More links](More
  links.md)).

* Tony reads [Paradigms of Artificial Intelligence Programming: Case Studies in Common Lisp](http://norvig.com/paip.html)

* reimplement the Scheme program(s) in Julia, continue watching the
  "Intro to AI" videos and implement them in Julia.

* decide whether and when to jump forward to neural network
  algorithms? 

* play a bit with Tensorflow (and/or  and/or Torch) anyway already?

## Suggestions

* watch course [Stanford University CS224d: Deep Learning for Natural Language Processing](http://cs224d.stanford.edu/syllabus.html)

* read books, find articles? Read through Wikipedia articles (see [More links](More links.md))? Then present it?

