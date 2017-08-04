---
layout: post
category: updates
title:  "Getting acquainted with our city"
date:   2017-07-03
author: Cruising Team
---

One of the pitfalls of data science is that there's often little incentive to acquire domain knowledge. Systems under study can be easily reduced to abstractions and shoved into models that may or may not acccount for relevant details. For data science aimed at effecting social good, the inclusion of such detail is of particular importance, as social systems are often intricate and nuanced, such that modification of any one structure impacts other connected parts of the system. So it is with transportation management, and so it was that the Cruising team took to the city, to meet with stakeholders in our project and to scope out the neighborhoods we'll be studying this summer.

<!--excerpt-->

The problem we're investigating is that a considerable portion of urban traffic (between 20 and 50% by most estimates) is made up not of drivers passing through from point A to point B, but of those who have already arrived at point B and are now circling (i.e. _cruising_) around trying to find a parking space. In most cities, the price of curbside parking is markedly lower than that of private lots, which gives people a strong incentive to drive around for 3, 5, even 10 minutes despite high available of off-street spaces. Let's assume the average circling time is 3 minutes, and that curbside spots see about 10 different cars throughout a typical day. Let's also assume the average speed of a cruising car is 10 mph. That's 5 Vehicle Miles Traveled per spot per day (10 mph * 0.5 h). Over a year, that amounts to 1,825 miles _per parking space_ ([Shoup 2007](http://shoup.bol.ucla.edu/CruisingForParkingAccess.pdf))!

Our goal for the summer is to help the transportation planners of Seattle identify where cruising is most prevalent within downtown. Essentially, we hope to create a "heat map" of the area between Pioneer Square, South Lake Union, and I-5, showing streets where cruisers congregate. The city can then modify routes, create spaces, or adjust parking times and rates if they choose, in order to even out the flow of traffic.

In order to get more familiar with our study system, we met with stakeholders and experts in the Seattle Department of Transportation. We learned that curbside makes up a tiny fraction of city parking, and that the city has limited power to adjust its rates. For example, the maximum legal price of parking is fixed at $5/hr. In order to change this, the city would have to pass new legislation. Also, the _paid occupancy_ rate for parking within city limits varies by time and location and can be somewhere around 30%! That means the other 70% is made up of transportation network companies, vehicles with disabled tags, and people who just don't pay. We finished our field trip with a bird's eye view of the city from Columbia Center.

Before we can put our machine learning models to work, we have a lot of planning and setup to do (and thus new tools to learn). We're currently building a database with RethinkDB and representing the downtown grid as a directed graph in Python. We've also acquired street and intersection attributes via OpenStreetMaps. Once everything is in place, we'll be ready to start searching for cruising. Stay tuned.
