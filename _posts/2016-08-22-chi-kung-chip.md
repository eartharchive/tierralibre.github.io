---
layout: post
title: C.H.I.P Chi Kung 
subtitle: Chi Kung assistant with C.H.I.P proof of concept
---
Welcome!
In today's post I would like to discuss a new project I am working on, which is to use the [Wii Balance Board](https://en.wikipedia.org/wiki/Wii_Balance_Board) as a source of input to help with Chi Kung postures.

So the plan is:  
1) Connect the Balance Board to the [C.H.I.P](https://www.getchip.com) or Raspberry Pi so we can read its values.
2) Make a backend that we can subscribe too to get event data. (The balance board gives us the weight in its four corners)
3) Display the data on the web browser.

So here we have a quick demo of the proof of concept:

<iframe src="https://player.vimeo.com/video/179723181" width="640" height="400" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

It's a work in progress and the calculations for the data still need to be adjusted and improved. 
But the basics are there:  
  
- Backend end with [Crossbar.io](https://crossbar.io)
- Front end with React
- Drawing [Konva](http://konvajs.github.io/)

From a technical point of view the backend uses WAMP messaging great for IoT, the client subscribes to topics and gets messages pushed from the server via websockets. So it's all realtime.

To do:  
  
- Improve the UI
- Improve the calculations
- Users and record trainning data in sessions so it can be analyzed later. (Graphs etc ...)
- Add connection to heartbeat data. (To measure heartbit during treainning together with posture)
- Make it adapt to phones, tablets, desktop

If you have any ideas on how to improve it or functionality that should be interesting, feel free to comment.

Full code is on: [Wii Chikung](https://github.com/tierralibre/wii-chikung)

More posts will come with the progress and detailed setup, so it can be easily replicated. But if you have a Pi or C.H.I.P and a Balance Board around it can be put to Chi Kung use :)

Thank you!

Have a great day!
