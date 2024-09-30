---
layout: post
title:  "Overnight/weekend shutdown project: A retrospective"
---

Cloud resources can be expensive, and it wasn't long after the march to cloud migration begun that FinOps and cloud cost-optimisation took off. In 2024, cloud cost-optimisation can be a well-established business function, though equally, there can still be plenty of opportunities to help organisations become more sustainable whilst also reducing operational costs. 

WARNING: The relationship between cost and sustainability is complicated though. In his recent article [Asim Hussain discusses the temptation and peril of using cost as a proxy-KPI] (https://asim.dev/articles/cost-carbon-paradox/). Cost reduction _CAN_ easily lead to increased emissions. So be careful about running with this idea.

Back on topic though, earlier this year we got the go-ahead to build out a service which went beyond the default offerings of the major cloud providers - shutting down whole DEV and TEST environments at night and on weekends, and powering them up as required. This included load balancing resource, databases, virtual machines, etc... Looking back at our project, we learnt some things - so here are the interesting parts:

### Resiliency
the last thing we want is to disrupt product development. Thankfully, cloud providers have very robust API mechanisms for managing resources.
Retries
Back-off retries
Alerting

### Transparency
with devs
with leaders 

### Hand over the keys
(and a bunch of documentation)
instil ownership
enpower teams to 

### Tag for Customisation


### The bank holiday headache


### Ensure machines are included in patching solutions


## In conclusion

Someone much wiser than I once told me that "If there are low-hanging fruits, go ahead (and reduce costs)... but you don't go cost-saving to increase your revenue". Perhaps the same applies to GreenOps. So don't be fooled into thinking that shutdown projects are going to be transformative in organisations alone. Buy-in from leadership is essential for true transformative change.

Sustainability through cost-saving might fall short. True sustainability at the heart of a project is always going to win-out.
where leaders are bought into.

Deprecation always wins.
