# motion-design
### Introduction 
These works utilize [anime.js](http://anime-js.com) open source javascript library to construct transition animation design.  
There will be 8 examples below to illustrate differnent ways of utilizing the library.

Remember to put anime.js into the same directory and include below line into html script.  
```javascript
<script src="anime.js"></script>
```
### Transform Object
![horizontalLeft](././material/horizontalLeft.gif)
![veriticalTop](././material/verticalTop.gif)

```html
<g fill="#FFFFFF">
  <circle cx="-350" cy="540" r="100"/>
</g>
```
```javascript
<script>
  var moveAnimation = anime({
  targets: 'g',
  translateX: 350 + (1920/2), 
  /* 350 = start position 
  1920/2 = half the horzirontal viewing area */
  delay: 1000,
  duration: 1366,
  easing: 'easeInOutCirc',
  });
  moveAnimation.play();
</script>
```

##### Circle
If you create a circle, the anchor point is in the middle.
![circle](././material/figure-02.jpg)

##### Rectangle
If you create a rectangle, the anchor point is in the upper-left corner.
![rectangle](././material/figure-01.jpg)

##### SVG graphic
If you want to replace the item with a SVG object, please follow below steps.  
1. Create a illustrator file with size 200px * 200px. If you want to use other size, the parameter in animation function must be modified as well.
2. ...


### Scale Object
![zoom](././material/zoom.gif)
```html
<g fill="#FFFFFF">
  <circle cx="960" cy="540" r="1"/>
</g>
```
```javascript
<script>
  var scaleAnimation = anime({
    targets: 'g',
    transform: ['translate(0 0) scale(1)', 'translate(-95040 -53460) scale(100)'],
    /* scale 100 times mean cx'=96000 cy'=54000 r'=100
    To be able to compensate the poisition change, translate is required
    960 = 96000-95040, 540 = 54000 - 53460
    */
    delay: 1000,
    duration: 1366,
    autoplay: false,
    easing: 'easeInOutQuart',
  });
  scaleAnimation.play();
</script>
```

### Scale Object with compensation
![menuOpenalt](././material/menuOpenalt.gif)
![fig3](././material/figure-03.jpg)
![fig4](././material/figure-04.jpg)
### Scale Object with compensation in two steps

![menuOpen](././material/menuOpen.gif)

### Method to Delay Animation
![buttonPress](././material/buttonPress.gif)

### Transform Window
![swipe](././material/swipe.gif)

### Transform Window in two steps
![Blink](././material/Blink.gif)
