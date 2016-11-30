# motion-design
### Introduction 
These works utilize [anime.js](http://anime-js.com) open source javascript library to construct transition animation design.  
There will be 8 examples below to illustrate differnent ways of utilizing the library.  
Remember to include below command into html.  
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
![circle](././material/figure-02.jpg)

##### Rectangle
![rectangle](././material/figure-01.jpg)

##### SVG graphic

### Scale Object
![zoom](././material/zoom.gif)

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
