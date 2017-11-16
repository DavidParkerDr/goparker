---
title: Code snippet test
author: David Parker
date: 2014-11-15T20:22:05+00:00
tags: ["test", "code"]
---
If you want to get the first fault tree in my ExampleFaultTrees object, then the following code is for you:

```javascript
var exampleFaultTrees = new ExampleFaultTrees();
topNode = exampleFaultTrees.getFaultTree(0);
```

You first need to instantiate an ExampleFaultTrees object and then you can ask it for the zeroth element in its internal array of fault trees.

You can then simply call the topNode&#8217;s draw function, giving it the 2d context of the canvas as a parameter to draw to.

```javascript
topNode.draw(context);
```