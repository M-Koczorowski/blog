---
title: "Automating Blog Updates"
date: 2021-08-29T14:30:09+02:00
draft: false
---
## How I update my blog with a stupid simple ten line bash script.
This post can sound like stating the obvious, but if something can be done by script, it is better decision to automate it. When I finished setting up the whole website, I had to solve one annoying problem. Do I really have to input like 9 separate commands and switch between directories to update just one blog post?

Prior to it I didn't have any experience scripting in bash, of course I used install scripts for some software and knew I had to give scripts some permissions, but it was a whole new thing for me.
I expected that script would be somewhat different than just using terminal, but it turns out it's just the same. Of course I can make variables, loops and all of this useful stuff, but all i needed was to have some commands executed.

## So how it looks?
Honestly? I know this could be done better but I just copied my terminal history from the last time i was updating and pasted it into *.sh* file.

And that's it. All  done in less than a minute.

```
  1 #!/bin/bash                                                                          
  2 
  3 cd blog
  4 git add .
  5 git commit -m "script updating"
  6 git push
  7 hugo -d ../m-koczorowski.github.io
  8 cd ../m-koczorowski.github.io
  9 git add .
 10 git commit -m "scripts updating"
 11 git push

```
