---
layout: post
title: "Project Update"
date: 2015-08-07
author: "Kivan Polimis"
---

We spent the last few weeks combining the individual components and functions designed to aid in disaster recovery into one complete bus rescheduling algorithm. Disaster recovery involves rescheduling individuals or entire buses that are at risk for falling behind schedule because of unforeseen conditions such as vehicle breakdown, traffic, etc. Combining, debugging and testing the algorithm has been the most difficult and most rewarding part of this summer. We're hopeful to complete the web interface for dispatchers to use our algorithm soon and may demo our deliverable to King County Metro Access administrators before our program's conclusion.

Additionally, we're trying to create predictive analyses and visuals that take a closer look at the broader operations of Access service such as distance traveled per passenger, proportion of total trip time that involves deadheading (distances traveled without passengers on bus), and cost per boarding to name a few. The goal of these analyses is to understand how operation patterns such as bus routes, amount of clients serviced per bus influence costs. 

<!--more-->

Below we've included some sample output of our Frankenstein algorithm <a href="http://stsc3000.github.io/images/posts/frankenstein/frankenstein_excited.jpg" target="_blank"> (it's alive!)</a>. The screenshot shows the algorithm checking buses within a fixed radius for their feasibility to insert a new passenger on the route. 
  
<img src="/blog/images/feasibility_screenshot.png" style="width:480px;">

