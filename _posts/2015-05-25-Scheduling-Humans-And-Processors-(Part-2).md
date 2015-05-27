---
layout: post
published: true
---


Catch the previous post [here](http://kfang.github.io/Scheduling-Humans-And-Processors-%28Part-1%29/)

##TL;DR
You can't multitask, you suck at doing context switches, you want to do as much as possible, and you want to make sure you eventually finish stuff.  Just finishing the shortest jobs first isn't going to cut it since you won't finish the long stuff if short jobs keep trickling in.  Splitting your time equally between all the tasks isn't going to work since you'll have to switch back and forth between the tasks all day. Maybe we should just give up and randomly finish tasks or at the very least find some way to prioritize everything we want to do.

## Step 3, Winning the Lottery
We've already looked at two strategies in trying to balance our growing TODO list and neither seems to work for us.  Maybe its time to give up and just pick something off the list at random and just do it.  At least we're not task switching and there's a non-zero probability for every task to get done. Seems to solve the problems with the previous two algorithms we tried.  Well, what we just decided to do is [Lottery Scheduling](http://en.wikipedia.org/wiki/Lottery_scheduling). You give each task a 'lottery ticket' and whenever you finish a task, you just play the lottery to find out which task to do next. 

You can even adapt this lottery system to prioritize important stuff without completing screwing over your non-priority tasks. How? Who says that each task can only get one lottery ticket?  Just like in the real lottery, you can just give a task more lottery tickets. Similar to how you can buy several lottery tickets in order to increase your chances of winning, you can also give a task more lottery tickets to increase its chances of being the next task to do.

This sounds great and all but the this causes absolute havoc when you have tasks that depend on each other.  Its not always that each of your tasks and independent of each other.  Doing the laundry requires you to do things in a specific order. If you have broken your task down into washing your clothes and folding them, using the lottery system to schedule these tasks means you have a non-zero probability of first folding your clothes then washing them. Maybe this is what you want, but for most of us, its not ideal.

## more to come...

