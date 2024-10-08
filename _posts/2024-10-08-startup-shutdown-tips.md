---
layout: post
title:  "Overnight/Weekend shutdown project: a retrospective"
---

Cloud resources can be expensive, and it wasn't long after the march to cloud migration begun that FinOps and cloud cost-optimisation took off. In 2024, cloud cost-optimisation is a well-established function in many organisations, though equally, as time passes and our platforms, products and requirements change - new opportunities to reduce operational costs emerge. As do opportunities for improving the sustainability of our tech, and sometimes these opportunities align.

WARNING: The relationship between cost and sustainability is complicated. In a recent article [Asim Hussain discusses the temptation and peril of using cost as a proxy-KPI](https://asim.dev/articles/cost-carbon-paradox/). Cost reduction _CAN_ easily lead to increased emissions. So, adopt caution when running with the link between these two.

Back on topic, earlier this year we got the go-ahead to build out a service which went beyond the default offerings of the major cloud providers - shutting down the entirety of our cloud-hosted DEV and TEST environments at night, on weekends, and public holidays (more on public holidays later) and starting them up as required. This had emerged as a cost-saving exercise and the intention of the project was to shutdown as many resources as possible: load balancers, databases, virtual machines, etc... Having recently undergone a digital sustainability awakening, the team got very excited to take some steps to reduce our carbon footprint with this project, and as often happens when a team is excited about a project - we gave the it a lot of thought and consideration. So here are some interesting takeaways:


### Robust solutions
From the beginning of the project, a risk in the forefront of our minds was that - if the solution was unreliable, it would disrupt the work of the development teams, giving them reason to circumvent shutdowns. We also didn't want to add to our operational costs (for supporting and maintaining the solution). Therefore reliability was essential for this project.

Thankfully, cloud providers have very robust API mechanisms for managing resources and we made use of these. We also made use of the exponential backoff pattern for retries - to account for the occasional transient issue or outage. Last but not least, we implemented some alerting to make us quickly aware of any issues.

### Transparency is essential
This project required co-ordination with the development teams whose environments we were looking to turn off, and naturally most of those teams had a TODO list longer than that of a new incoming government. Whilst we found that transparency on the cost savings generated some engagement, adoption of the project really kicked off when we were able to share the estimated kg CO2e reduction that the first team had made.

Leadership hadn't initially expected positive sustainability results, so being able to share the reductions and have conversations about digital sustainability was certainly encouraging. Engagement and sponsorship from leadership is essential for achieving more in this space.

### Hand over the keys (and some documentation)
It quickly became clear that teams had different working hours, overnight tests, database restores, etc... and that the individual teams would be best placed to set and manage their own shutdown/startup schedules. So we made it easy for teams to configure this with a flexible scheduling system, that they could manage and alter.

In case of emergency, environments can be quickly brought back online by a team, or if someone is working late, they can adjust the shutdown schedule. Empowering teams to have control over their schedule is important for the project's ongoing operation.

### Tag for Customisation
Cloud providers offer tagging functionality on resources, and this can facilitate some clever operations. For example, you could use tagging to exclude certain resources from being shutdown, or exclude certain resources from being started up.

### The public holiday headache
Public/bank holiday's get complicated in international organisations. We started out optimistically trying to solve this problem - noting that some governments offer a [public holiday API](https://www.api.gov.uk/gds/bank-holidays/#bank-holidays). Though it quickly became clear that only a subset of holidays are observed in some countries, and that teams can often span multiple countries. The complexity of this problem escalated quickly, and we therefore ended up manually building some JSON data sources through til the end of 2026 which can be consumed/configured by teams depending on their location.

### Don't forget compatibility with patching
A final point is to ensure that your solution is compatible with any patching mechanisms - we ensured that our IaaS resources could be automatically powered on and any associated schedules disabled during maintenance windows.

## Results and Conclusion

Interestingly, after completing the project and reviewing its associated cost savings and estimated carbon savings - we found that shutting down the databases was responsible for the bulk of reducing our costs, though shutting down the Virtual Machines was responsible for the bulk of the reduction in CO2e emissions. We hadn't expected this, though this perhaps demonstrates how the relationship between cost and sustainability can be directionally aligned, but might not be completely aligned.

Also, a final thought - someone much wiser than I once told me that "If there are low-hanging fruits, go ahead (and reduce costs)... but you don't go cost-saving to increase your revenue". Perhaps such wisdom could be applied to GreenOps - certainly "shutdown" projects are a great step to reduce emissions, but such action won't be transformative alone. True sustainability at the heart of a project or organisation will always win-out over tackling sustainability through the proxy of cost.
