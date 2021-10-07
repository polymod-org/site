+++
title = "Making Nice Switches for Polymod's UI"
date = "2021-10-07"
description = "Making good lucking UI elements can be a surprising amount of work, let's see."
disableComments = true
+++

## About

Making seemingly simple UI elements like switches seems easy but making ones which look good, act functional, are understanding to the user, etc. can be a surprisingly complex task. This short writeup post details some work into the switches made for Polymod's UI.


## Switches

Switches are essentially an alternative form of a checkbox, with an on or off state. Instead of being conveyed with being empty or checked, it is either toggled or not. Commonly, toggled (on) switches:
- Handle to the right
- Different, usually highlighted, background color

With untoggled (off) switches being the opposite:
- Handle to the left
- More neutral, dull, background color


## Why are switches like this?

Toggled switches are highlighted as we (UI / UX designers, developers, etc.) want the user to easily see what they have on or off. The handle helps with this as positional information can be seen quite easy (not needing to understand colors or see contrast), but having a more highlighted background color can ease with quickly seeing what state a switch is in. This is especially apparant with a large list of switches (closely) together. Having a vibrant background color, commonly the accent color to help fit in with the rest of the app's UI.


## Design Revisions

### Initial Design

Originally, I went for a square / boxy design for the first UI. This initially looked good as it was more striking and unique looking, however although it didn't seem obvious at the time, it looked rather amature and generally unpolished. Even when trying to aim for a look / aesthetic, the look can actually be flawed even if you (or people you know) like it initially. What you like does not equal what your users or most people will like, unfortunately.

![Screenshot](https://media.discordapp.net/attachments/617405420071550989/889540992636694568/unknown.png?width=220&height=353)


### Second Revision (Inset)

Whilst the square design remains for the second revision and this is mostly the same, the main difference is an inset for the handle. Whilst this is a small tweak, it makes a surprisingly large difference to the overall quality and polish of the switches. I feel this is because it makes the handle being part of the switch and controlling it more apparant as it looks more as if it is inside of it.

![Screenshot](https://media.discordapp.net/attachments/617405420071550989/889595554378706954/unknown.png?width=218&height=355)


### Third Revision (Rounded)

In the third revision, the undoing of the original square / box design is swapped with a more modern rounded look. Whilst I initially liked the old design, after switching to this roounded look I immediately liked it more than any past revisions. Specifically the switches even more, as rounded looks are generally more modern and appealing to most end users as it, for the most part, appears simpler and more friendly (in my opinion and testing).

![Screenshot](https://media.discordapp.net/attachments/617405420071550989/889612773011632228/unknown.png?width=218&height=353)


## Advice

- Spacing around switch handle to be inset
- Enabled switches having background as accent color
- Changing state (on or off) at a nice time after interaction, usually just after half way through animation
- Have animations and transitions not too short to feel unneeded or janky but not too long to feel slow, I personally found:
  - .3s for handle movement
  - .2s for background color transition, after .16s delay