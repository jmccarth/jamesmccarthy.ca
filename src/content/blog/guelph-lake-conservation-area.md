---
title: "Guelph Lake Conservation Area - Part 1"
description: "Account of a field visit to Guelph Lake Conservation Area"
pubDate: "2016-07-04"
---

A couple of weeks ago I had the chance to go out to Guelph Lake Conservation Area with a group of students who were creating sample plots to count instances of milkweed. They were doing this as part of a fourth year GIS project course. They had done the analysis ahead of time to determine the right number of plots and they went into the field armed with stakes and GPS units. My role was to show them how to use the GPS units to go find the locations of their plots.

They had a list of their plot locations as a printed table, and so the first thing I asked them was what order the points on the paper were in. I could tell by the lack of answers and the looks on their faces that they had not put any thought into ordering the points to minimize their walking distance. Instead they had to go through the points in the sequence they were listed on the paper. This resulted in the following walking path:

![no-order](/assets/no-order.png)

Total distance traveled to get all 33 sites: 2,634 m.

I thought this made a good teachable moment, especially given the hot sunny conditions we faced all day, so I decided I could illustrate that by generating an optimal path to the 33 sites.

To do this I used ArcGIS and Network Analyst. Through a series of steps I generated a network dataset that included a path from each plot to every other plot:![network-dataset](/assets/network-dataset.png)

Then ran a simple Route task, resulting in the following optimized route:

![ordered](/assets/ordered.png)

Total distance traveled on this route: 969 m, almost 1/3 of the path above. The lesson here, plan your field work!

There's more data to come from this study as we did lots of GNSS testing while out in the field. I'm looking forward to diving into that data a bit more to see what we came up with.
