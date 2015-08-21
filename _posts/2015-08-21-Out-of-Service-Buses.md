---
layout: post
title: "Out-of-Service Buses"
date: 2015-08-21
author: "Kivan Polimis" 
---

As part of our historical analysis for King County Metro (KCM) we looked into the possibility of predicting out-of-service buses. Buses become out-of-service generally after breaking down or if they are unable to arrive at their destinations. Predicting out-of-service buses is important from an operational perspective because KCM and their contractors can better manage their vehicle fleet by having adequate standby vehicles each day. 

Using time series techniques, we analyze over 18 months (January 2014 to May 2015) of transit data and draw the following conclusions about out-of-service buses.

Our time series model uses the daily percentage of out-of-service buses (relative to all buses in operation that day). We observed:
<ul>
<li>On average, 7.47% of the buses are out of service each day</li>
<li>No deterministic trend over time</li>
<li>Some weekly seasonal variation (more on that later)</li>
<li>A snowstorm on <a href="http://www.seattleweatherblog.com/snow/winter-wonderland-seattle-sees-biggest-february-snowfall-in-13-years/">February 9th 2014</a> coincided with the highest daily percentage of out-of buses</li>
</ul>

<img src="/blog/images/Plot - Out-of-Service Time Series.png" align = "middle" alt = "out-of-service buses time series" style="width:480px;">


<!--more-->

For those with more knowledge of time series, additional analyses revealed:
<ul>
<li>Out-of-service bus percentages may not be stationary</li> 
<li>Despite unit root suggesting non-stationarity, cross validation comparisons between ARIMA models indicate an AR(2)MA(2) may be the best model to forecast future daily percentages of out-of-service buses</li>
</ul>
 
<img src="/blog/images/Plot - ARIMA Cross-Validation.png" align = "middle" alt = "ARIMA Cross-Validation" style="width:480px;">


Back to the weekly seasonal variation. Although t-test between the means of daily out-of-service events did not reveal statistical differences across weekdays, we did notice the average Friday count seems below the average Monday count. The seasonal difference between Friday and Monday is also shown in our weekly time series analysis which lead to us wondering why we observed weekly trends in reporting out of service buses. One guess (your guess is <strike> as good</strike> better than ours) is that out-of-service counts could be lower on Friday (relative to Monday) because drivers want to head home for the weekend and report buses as out-of-service when they return on Monday  

<img src="/blog/images/Plot - Out-of-Service Boxplots by Day of the Week.png" align = "middle" alt = "Out-of-Service Boxplots" style="width:480px;">
 
