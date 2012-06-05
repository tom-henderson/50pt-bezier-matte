50pt-bezier-matte
=================

50 point garbage matte with bezier curves for Final Cut


What is it?
-----------

50 Point Bezier Matte is a filter for Final Cut Pro (and Final Cut Express) that lets you create a garbage matte with up to 50 points. Unlike the 4 and 8 point garbage matte filters that come with Final Cut Pro, 50 Point Bezier Matte lets you create curves between the points instead of straight lines. This allows you to easily create a mask to extract almost any element you need.

Each point can be turned on and off independently, so you only have to position the points you need, and the points can be animated using keyframes, allowing you to extract a moving object for instance.


27 Sep 2004 - Version 2
-----------------------

Version 2 is now available. This version mainly fixes a bug that has been annoying me about the filter since I first released it - that it destroyed the existing alpha channel of the clip you apply it to. Version 2 now has the option to preserve the alpha channnel of the original clip.

I have also improved point labels a bit, which can now be colored to distinguish multiple paths. You can also display a name for the path.

Finally, I have added an option to blur the mask. Unlike applying the Mask Feather filter after the 50 Point Bezier Matte, this option does not blur the on screen controls in preview mode, so you can see exactly what the matte will look like rendered.

Many thanks to all those who wrote in with feature ideas, your feedback was always appreciated and welcome.

5 June 2012
-----------

Since I had to take the original site off .Mac I've decided to release the source under the MIT licence.

I have not used Final Cut for several years and am not sure this even still works with the current version. 


What's a Bezier Curve?
----------------------

A Bezier Curve is a line drawn between two points that is bent according to two control points. If you've ever used vector graphics applications such as Illustrator, Freehand or Flash you will already be familiar with the way the control points alter the shape of the curve. If you haven't, these examples demonstrate how the line from point a to point b is altered by the position of the control points c1 and c2.

How to use
----------

The first step is, of course, to select a clip on the timeline and apply the filter, by selecting Video Filters > Tom's Filters > 50 Point Bezier Matte from the Effects menu.

Next we need to open the clip in the Viewer, either by double clicking it, or dragging it from the timeline to the Viewer window (you will need to drag if you are applying the filter to nested clips, since double clicking will open the nested clip's timeline).

By clicking on the Filters tab we can start to set the point positions. Each point defaults to the center of the screen, and initially only 2 points are active. Points 1 and 2 can't be turned off. More points can be activated by clicking on the 'activate' check box for a particular point.

Each point has two Bezier control points associated with it. The Bezier Control In point affects the line coming from the previous point, and the Bezier Control Out point affects the line going to the next point. Bezier control point positions are set relative to the yellow Bezier Target in the middle of the frame. When setting the control points, start close to the target to begin, and drag the point around to get used to how this works. Don't just click where you want the control point to be or you'll end up in a mess.


Controls
--------

These controls turn on and off the various GUI elements of the filter. None of these will be visible on rendered material, which will just show the mask.
Labels are only visible during previewing. You can enter a name for the path and show it on screen to help identify multiple paths. You can also change the color of the labels.

Alpha Settings affect weather the mask will reveal an area or cut a hole, weather the existing alpha will be preserved, and the softness of the alpha channel.

Curve Resolution is the number of steps between each point. Higher is not necessarily better. 10 - 20 is a good range.

The controls for each point are the same, and function as described above. The smooth option automatically calculates the Bezier Control In point to create symmetrical curves. Points 1 and 2 are always active. All points default to the center of the frame.

Points 3 to 50 must be turned on using the Activate checkbox before they can be set.

Known Issues
------------

Point Positioning: If you apply the 50 Point Bezier Matte to a clip that has had adjustments made under the Motion tab (rotation, positioning, scaling etc) you will have dificulty positioning the points. To get around this problem, select the clip on the timeline and from the Sequence menu select 'Nest Item(s)...'. Enter a name for the new sequence and click OK. Now apply the 50 Point Bezier Matte to the nested clip which will be on the timeline in place of the original clip. To edit the filter's controls drag the nested clip to the Viewer window. To edit the motion effects open the nested clip's timeline by double clicking it.


License
=======

Copyright (C) 2003 Tom Henderson

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.