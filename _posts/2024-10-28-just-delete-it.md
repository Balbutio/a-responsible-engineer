---
layout: post
title:  "Just delete it all: elimination is essential for net zero"
---

### Will the real Product Owner, please stand up?

I recently listened to a great talk by [François Burra in which he discusses becoming a climate-conscious product manager](https://www.youtube.com/watch?v=9RisfJhzU50). Whilst I am no product manager myself, there is undoubtedly some crossover between aspects of product management and DevOps engineering. We identify use-cases for automation, research and decide appropriate solutions, validate their usefulness, and refine them.

Though on reflection, I perhaps don’t go back and review my work and the work of my peers as often as a product manager might do. I do regularly stumble upon some undocumented automation that a team member setup long ago – some of which is quietly carrying out important processes, and some of which have become irrelevant as time has gone on. It’s clear though, that a holistic examination of our assets is key to minimising our environmental impact.

### The zombie apocalypse

Holly Cummins coined the term ***zombie workloads*** for applications or services which are running but no longer required. These can be incredibly wasteful, and “killing them off” represents a great opportunity for carbon saving.

I’m sure many of us could be more mindful of identifying zombie workloads, so a great takeaway from this article would be to keep your eyes peeled for these. Though this is more difficult where staff turnover has occurred, or team sizes have been reduced. We can feel like we don’t want to switch stuff off for fear of causing problems. This is of course not sustainable, so we should be mindful of avoiding this trap.

Though, perhaps the true messy reality is that there are many more semi-useful workloads than zombie workloads. So, we should be similarly conscious of decoupling useful processing from un-useful processing. Likewise, we should regularly re-evaluate and adjust the frequency of our workloads to reflect how much we use them. For example, we might have arbitrary workloads running every day which could be weekly, or intelligently triggered when a change is made. Or we might be triggering workloads every change, where a nightly bulk task is more appropriate.

### Be less impressed and more involved

When maintaining software or inheriting an existing software stack, change can be daunting, and it is sometimes easy to overly revere the work of our peers or past colleagues. However, we shouldn’t be deterred from making changes or improving things. Good practice moves forward. So, we should also move forward, with respect and gratitude (or perhaps a grumble) for the work which has shaped our software and supporting infrastructure, and with the knowledge that updates to make workloads leaner and more efficient are a great way to respect past work.

Similarly, we shouldn’t overly revere our own work. The IKEA effect is a phenomenon whereby we value something more if we helped make (or assemble) it, and this can certainly apply to digital solutions – we should strive to maintain objectivity around the usefulness of our work. Not everything we produce is going to be useful or stay useful forever, and there is overlooked wisdom in retiring our work.

### Question everything

New development seems to steal much of the spotlight when we discuss the greening of software, though efforts and carbon savings are important in product maintenance also. Many of the principles that François discusses are especially relevant to this area, particularly in teams that don’t have a dedicated product owner. A great early step in developing our green software maturity is to look back at our software stacks and assets, re-evaluate their usefulness, refine what we have and retire what we can. So here is a smorgasbord of questions inspired by those in this field, to evoke thinking on this topic.

- Is the software/service/workload still useful?
- Are there environments or workloads which could be switched off?
- Have the requirements of our users stayed the same?
- Are there features which could be removed?
- Is there "dark data" which can be removed?

I will end this article with the wise words that Sarah Hsu delivered at a recent Green Software Foundation summit - efficiency is a starting point, but not the whole story... elimination is essential if we are to reach net zero.