---
layout: default
title: How to tag cycle lanes
---

{{ page.title }}
================

> A cycle lane is a traffic lane marked on an existing roadway or carriageway and generally restricted to cycle traffic. (from [wikipedia](http://en.wikipedia.org/wiki/Cycle_lane))

In OSM you can add cycle lane information to any road type. For example, to indicate that the road has cycle lanes on both sides, add the `cycleway = lane` tag.

{% highlight ini %}
highway = residential
cycleway = lane
{% endhighlight %}

Alternatively, if the road only has a cycle lane on one side, you need to figure out if the cycle lane is on the "left" or "right" side of the road. Note that left/right depends entirely on the direction of the road in OSM - it's nothing to do with which side of the road you drive on or anything like that. Use the toolbox direction arrow in Potlatch2 to figure out which way the road is pointing, and figure out which is the left and right side depending on the arrow.

{% highlight ini %}
highway = residential
cycleway:right = lane
{% endhighlight %}

or

{% highlight ini %}
highway = residential
cycleway:left = lane
{% endhighlight %}

Lane widths
-----------

Cycle lanes can vary hugely in their width, and narrow lanes are a particular campaign issue for many Cycling Campaign groups. It's tricky (and usually dangerous) to measure them exactly, so estimates are  usually used. Depending on circumstances, you might have lanes the same width on both sides of the road, or need to tag them individually. Widths are in metres.

{% highlight ini %}
cycleway:width = 1.25
{% endhighlight %}
or
{% highlight ini %}
cycleway:right:width = 1.25
cycleway:left:width = 2.5
{% endhighlight %}


Further Reading
---------------

[Bicycle (OSM wiki)](http://wiki.openstreetmap.org/wiki/Bicycle)