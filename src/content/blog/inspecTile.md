---
title: "inspecTile"
description: "A tool for comparing map tiles"
pubDate: "2016-04-05"
---

[inspecTile](http://jmccarth.github.io/inspecTile) was born out of a need to perform side-by-side comparisons of tilesets generated with Mapnik.

![inspecTile](/assets/inspectile.png)

I have been using this tool internally for a while now, but I thought it was time to promote it a bit because others may find it as useful as we have. The way it works is simple. You load a tileset into each frame, and then when you pan or zoom one map, the other map moves accordingly. This makes it easy to do things like compare tilesets before and after changes, and compare different cartographic alternatives.

What you need are two tileset URLs in the form expected by a [Leaflet TileLayer](http://leafletjs.com/reference.html#tilelayer). Something like:

http://{s}.somedomain.com/blabla/{z}/{x}/{y}.png

The directories hosting the tiles must be web accessible. Then it's just a matter of zooming and panning to compare your tilesets.

I'm hoping to add new features in the future, including:

- More methodical tile comparisons, such as stepping through each tile individually at each zoom level.
- Better (or any) documentation.
- Embedding of the tileset URLs and current center point and zoom level in the application's URL so that comparisons can be shared. That way if you need to show a specific view of one or both tilesets you can simply copy the current URL and send it to anyone and they will see what you see.

Feel free to [play with it](http://jmccarth.github.io/inspecTile) and let me know what you think!
