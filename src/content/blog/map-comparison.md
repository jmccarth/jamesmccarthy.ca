---
title: "Map Comparison"
description: "Finding ways to compare maps"
pubDate: "2015-07-29"
---

Lately I've found  myself with the need to compare tilesets generated from Mapnik for our [campus map project](https://uwaterloo.ca/map-beta). We are generating our tilesets by pulling data from OpenStreetMap, loading those data into a PostGIS database, and running mapnik with a couple of stylesheets we've put a lot of work into. The workflow is good for us because we end up with something that's relatively automated.

One manual intervention step that we currently have is the need to compare the old and new tiles when we generate a new tileset. Suppose a new building comes online on our campus and we put that building into OpenStreetMap, pull the data into our DB, and generate new tiles. Since OSM is collaboratively edited by anyone on the web there is always the potential that something on our campus has been changed other than the new building we're interested in. The trouble, of course, is finding those changes.

One approach is to look at the differences in the data before generating tiles and determining if anything is relevant, and there are tools to do that. There are also ways to find all of the edits since I specific date (I think), and there are tools to handle that case as well. When we get to the point of having more automatic updating of the data we use to render our tiles we'll probably need to investigate that.

What I wanted, though, was a simple way to look at two tilesets side by side and compare them visually by browsing through them. I found myself doing this by having one version of the tileset attached to one instance of our map in one Git repository, and another attached to another instance of the repository. Since we load our tile URLs from config files that are outside of the code base all we need to do is edit the config files and we're in business. However this left me with the need to open two windows, split them across my monitor, and move and pan them in tandem. In other words I would zoom the one on the left, then zoom the one on the right, pan the one on the left, pan the one on the right, etc. After doing that a few times I sketched out the first draft of a UI for a tool that would handle this for me. I would give it two tile URLs and they would be loaded into two Leaflet maps. I would then tie the zoom and pan animations together and voila, an easier way to compare tilesets visually.

I put together the first draft of this tool in about forty minutes tonight and have the basics ready to go. I'll iterate on this over the next few weeks and hopefully will have something to publish shortly!
