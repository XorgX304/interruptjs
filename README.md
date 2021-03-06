# interrupt.js
 
interrupt.js exploits the interrupt-timing side channel in JavaScript. 
Using this implementation, it is possible to detect hardware interrupts, such as key presses or touchscreen interactions on mobile devices. 

## Demo

Try the live demo at [https://iaik.github.io/interruptjs/](https://iaik.github.io/interruptjs/)

1. Load the page (either on a mobile device or on your computer) - the PIN pad has no function, don't worry if it doesn't do anything. 
2. Press "Start"
3. Interact with your touch screen (tap, swipe), type, or click with your mouse.
4. Press "Stop"
5. A trace appears where you should be able to see every event (tap, swipe, click, ...) you issued as a peak - either upwards or downwards, depending on your device. 
6. If you don't see anything, try again by clicking on "Restart"

A trace might look something like this:

| Xiaomi Redmi Note 3 | Google Nexus 5 |
|---------|---------|
| <img src="https://github.com/iaik/interruptjs/raw/master/screenshots/trace1.png" width="200"> | <img src="https://github.com/iaik/interruptjs/raw/master/screenshots/trace2.png" width="200"> |
| Touch 2x, Swipe, Touch 3x | Touch 2x, Swipe, Touch 3x  |

## Compatibility

We tested the code in Chrome and Firefox on both Android and Ubuntu. 
The code should work on every modern browser and any operating system using interrupts for I/O (that is virtually every operating system). 
