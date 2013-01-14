---
layout: post
title: Debugging Mobile Web Apps on OS X
comments: true
---
While working on a mobile web application today that involves mapping, I ran into an issue that the map would load on a desktop browser but not the Safari browser within the iPhone Simulator app. After a bit of googling I learned that by enabling the Developer menu in Safari on OS X that it gives you the option to load up a remote debugger to the iPhone simulator's instance of Safari.

To enable the developer menu and debug your web application in Safari on OS X follow this path. 

* Hit `command + ,`
* Click `Advanced`
* Check `Show Develop menu in menu bar`
* Launch your web application in the iPhone Simulator
* Click `Develop > iPhone Simulator > <YourWebApp>`

Hopefully this will help someone else who is trying to debug a remote application on a mobile device.