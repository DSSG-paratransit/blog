---
layout: post
title: "Project Update"
date: 2015-08-07
author: "Kivan Polimis"
---

We spent the last few weeks combining the individual components and functions designed to aid in disaster recovery into one complete bus rescheduling algorithm. Disaster recovery involves rescheduling individuals or entire buses that are at risk for falling behind schedule because of unforeseen conditions such as vehicle breakdown, traffic, etc. Combining, debugging and testing the algorithm has been the most difficult and most rewarding part of this summer. We're hopeful to complete the web interface for dispatchers to use our algorithm soon and may demo our deliverable to King County Metro Access administrators before our program's conclusion.

Additionally, we're trying to create predictive analyses and visuals that take a closer look at the broader operations of Access service such as distance traveled per passenger, proportion of total trip time that involves deadheading (distances traveled without passengers on bus), and cost per boarding to name a few. The goal of these analyses is to understand how operation patterns such as bus routes, amount of clients serviced per bus influence costs. 

<!--more-->

Below we've included some sample output of our Frankenstein algorithm. The screenshot shows the algorithm checking buses within a fixed radius for their feasibility to insert a new passenger on the route. 
  
<img src="/blog/images/CPB_expression.png" alt = "CPB" style="width:480px;">

That is, the cost-per-boarding of client *j* is the sum over all of the 'legs' during which the client is on board the bus of the total seconds the leg takes divided by the number of passengers during the leg. For example, suppose client 123 is on the bus for 2 legs (that is, ze gets on the bus, the bus stops to service another client, and then drops client 123 deboards), the first leg takes 900 seconds and there are 4 total passengers, and the second leg takes 400 seconds and there are 3 passengers. This cost per boarding is $4.86$. Note that the average Access service cost per second is $48.09/3600, i.e. $0.013558 per second.

From the 4-month ridership data (Jan 1, 2015 - April 30, 2015) we received from King County Metro, we can see the distribution of cost per boardings:

<img src="/blog/images/CPB_hist.png" alt = "CPB" style="width:480px;">
 
 
