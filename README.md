FORK
======
This is a fork of package nl.qbus.sizemeup, the original app does not seem to be receiving published updates.

1. Put on GitHub where developers are more likely to spot it
2. Update Play Store published resource
3. Update new values

ToDo:

1. Add immersive option button or menu, handy for end-users who use app to send back screen shots of oddball devices.
2. Add some basic Android buttons/checkboxes on main layout XML so that screen shots sent back from users depict general fit.
3. Show density factor on-screen.
4. Use the AutoFitTextView for known strings in the system-default font and show the resulting point size?


Research
==========
Recent discussion on APK variations:
https://github.com/opengapps/opengapps/issues/16


README
======
This is an example app for [Hugo Visser's](https://twitter.com/botteaap) "Embracing Fragmentation" talk that he gave at Apps World 2013, [Mobile Down South](http://www.mobiledownsouth.nl/8/sprekers.html#HugoVisser) and earlier (2012) at [mdevcon](http://mdevcon.com/2012/01/10/hugo-visser/).

The app shows the screen class, dpi, the screen size and the available space or view size  of an Android in both pixels and device independent pixels (dips).

The goal of the app is to show you which technical mechanisms Android has to help you create apps that run on many devices:

 - The app consists of a single Activity containing a Fragment to (trivially) show how you can reuse UI and UI behaviour.
 - The main background is a gradient, defined in a [drawable xml](https://bitbucket.org/hvisser/sizemeup/src/3e5dbf5281d0/res/drawable/background.xml). Scaling gradients contained in a bitmap will result in visible artifacts, but since a drawable is rendered at runtime, it will always show nice and crisp, no matter what the screen size of device is.
 - The arrows that indicate screen width and height are defined as 9 patch images, making them stretchable. There are variants for mdpi, hdpi and xhdpi screens (ldpi will get scaled down by Android).
 - There's no logic in the fragment to determine screen dpi or screen class; this is entirely controlled by referencing a string resource in the layout, keeping the code simple.
 - For "large" screens the font sizes are adjusted to cater for the larger screen. Two methods are demostrated: using dimensions referenced as a resource from the layout file and using a [style](https://bitbucket.org/hvisser/sizemeup/src/3e5dbf5281d0/res/values-large/style.xml) on the TextViews in the layout.
 - [Styles](https://bitbucket.org/hvisser/sizemeup/src/3e5dbf5281d0/res/values-v11/style.xml) are used to inherit from either Theme or Theme.Holo so that on newer devices running Android 3.x or up the ActionBar is shown and styled.

This only shows the tip of the iceberg of what is possible; the resource system is very powerful and keeps your code simple. I highly recommend to read up on [providing resources on the Android developer site](http://developer.android.com/guide/topics/resources/providing-resources.html)

Contact
-------
Original author:
~~If you want to get in touch just [contact Hugo Visser on twitter](https://twitter.com/botteaap) or [Google+](https://google.com/+hugovisser)~~