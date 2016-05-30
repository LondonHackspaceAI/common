# AI group: using Julia

## Documentation

* [Wikipedia](https://en.wikipedia.org/wiki/Julia_%28programming_language%29)
* [julialang.org](http://julialang.org/)

## Using Julia from the browser

julialang.org recommends [JuliaBox](https://www.juliabox.org/).

You can alo run Julia in the browser using [Project Jupyter](http://jupyter.org/) ("*Open source, interactive data science and scientific computing across over 40 programming languages.*"). Peter has more knowledge on this.

## Using Julia on your computer

On Debian/Ubuntu: `apt install julia`.

For other operating systems, check [julialang.org/downloads/](http://julialang.org/downloads/).

## Using Julia on the Borg

You need a login on the Borg, and get permission(?) to turn on and use the Borg (it is a bit involved to turn on and uses a lot of power). These are provided at our events.

Then you need a way to synchronize files, so that you can run the text editor on your computer while saving the file to the Borg. On Linux, use [SSHFS](https://en.wikipedia.org/wiki/SSHFS) (`apt install sshfs`), on Windows perhaps [WinSCP](https://en.wikipedia.org/wiki/WinSCP) offers the best solution (I'm not using Windows so don't know). To run your program, ssh into Borg and enter `julia yourfile.jl`.

You could also run `emacs` or `vim` from your ssh login on the Borg, if you're comfortable with that.

Perhaps we should look into installing Juno and IJulia as well as a VNC server on the Borg and then access those over VNC.

## Interesting Links

[Compiling Julia for NVIDIA GPUs](http://blog.maleadt.net/2015/01/15/julia-cuda/) ([HN](https://news.ycombinator.com/item?id=8991622))

[High-level GPU programming in Julia](http://arxiv.org/abs/1604.03410)

[Talk by one of the Julia creators](https://www.youtube.com/watch?v=dK3zRXhrFZY&index=11&list=PLA66mD-6yK8xqd5XKxzwVBIqf1d3QQXpv) (youtube)
