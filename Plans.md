# AI group plans

## Objectives

- learn Julia

- implement machine learning algorithms in it so as to learn how modern AI works

- see how to use AI on selected problems: see [Project Ideas](ProjectIdeas.md)

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

* May 8: decision to have at most one meeting per week. Look out for possibilities of working individually or in subgroups and then present the results, to progress a bit faster.

* Meeting to start learning Julia on Fri May 13 (7pm (or really 8pm,
  Christian and the Borg were late and the TV showed remarkable
  resistance, too)). Bob did a short presentation, then we did some
  [hello
  world](https://github.com/LondonHackspaceAI/julia-experiments/blob/master/meeting-1/foo.jl)
  (check the history using `gitk`) level programming. Due to running
  out of time we haven't managed to work in subgroups, and haven't
  managed to see parallelism yet. Discussed further plans. Thinking
  that it is on individuals and subgroups to work out things between
  meetings; list of things to work on for such individuals or
  subgroups:

    - using matrices in Julia (using small interesting example(s)?)
      (perhaps Nick)

    - path search in Julia (Sam)

    - what is coming up in the course? Is there an alternative we
      should take? (Christian)

  Mentioned but not written down during meeting:

    - reading up about neural networks (and AI in general?) (Paul)

      (Note from Christian: check "Wikipedia" and "Online books"
      sections in [Teaching](Teaching.md).)

  Not listed during meeting:

    - parallel programming in Julia (Christian)

* installed Debian and Julia on the Borg (Christian), Debian is still
  in the chroot, but it works now for (non-LDAP) user accounts
  (switched over to sysv init)


## Next steps

* install LDAP user accounts in the chroot (and separate home from
  ubuntu)?

* install [Torch](http://torch.ch/) on the Debian on the Borg? (Bob
  has been using it.) Figure out why it doesn't use the available
  cores much. Install Tensorflow, Leaf (see [More links](MoreLinks.md)).

* Tony reads [Paradigms of Artificial Intelligence Programming: Case Studies in Common Lisp](http://norvig.com/paip.html)

* reimplement the Scheme program(s) in Julia, continue watching the
  "Intro to AI" videos and implement them in Julia.

* decide whether and when to jump forward to neural network
  algorithms? 

* play a bit with Tensorflow (and/or [Leaf](https://github.com/autumnai/leaf) and/or Torch) anyway already?

## Suggestions


* Interesting links from Bob about the hairyness of advanced
  algorithms:

  * [Minimal character-level language model with a Vanilla Recurrent Neural Network, in Python_numpy](https://gist.github.com/karpathy/d4dee566867f8291f086)

  * [char-rnn/train.lua](https://github.com/karpathy/char-rnn/blob/master/train.lua) (requires matrix weight sharing but retention of old X state (what exactly?))

* (Bob) Good intro to neural nets:
    http://neuralnetworksanddeeplearning.com

* read books, find articles? Read through Wikipedia articles (see [More links](MoreLinks.md))? Then present it?

