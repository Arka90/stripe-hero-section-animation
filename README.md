# Stripe hero section animation 

## Method 1: Using Pure css

html code
```
<div className="animated-gradient-container"></div>
```

css code

```
.animated-gradient-container {
  background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
  background-size: 400% 400%;
  animation: gradient 10s ease infinite;
  height: 100vh;
  position: relative;
}

@keyframes gradient {
  0% {
    background-position: 0% 50%;
  }
  25% {
    background-position: 50% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  75% {
    background-position: 75% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}
```

In the CSS, we are targeting the div and applying a linear gradient. We can adjust the angles and colors to achieve the desired result. Additionally, we are defining an animation; we can also modify the animation keyframes.

## Pros
1) Easy to implement
2) Lightweight. Does not cause any performance issues.

## Cons
1) Too simple

## Method 2: Using Canvas plus the external js file.

- Step 1 : Download the source code by [clicking here](https://kevinhufnagl.com/download/2895/)
- Step 2 : Extract the .zip file
- Step 3 : You will get two file Gradient.html and Gradient.css
- Step 4 : Open the HTML file

```
<html>
  <head>
    <title>Stripe Gradient</title>
    <script src="Gradient.js"></script>
  </head>
  <style>
    body {
      margin: 0;
      padding: 0;
    }
    #gradient-canvas {
      --gradient-color-1: #6ec3f4;
      --gradient-color-2: #3a3aff;
      --gradient-color-3: #ff61ab;
      --gradient-color-4: #e63946;
    }
  </style>
  <body>
    <canvas id="gradient-canvas" style="width: 100vw; height: 100vh"></canvas>

    <script>
      var gradient1 = new Gradient();
      gradient1.initGradient("#gradient-canvas");
    </script>
  </body>
</html>
```

You will see the above code here. The main concept is the JavaScript file provides a class called 'Gradient',. Here, we are creating an instance of the Gradient class and initializing the gradient by passing our canvas ID. Additionally, we are declaring a canvas element and providing four different colors through variables.

## Pros
1) Exact animation like Stripe Hero section

## Cons
1) Hard to impletent with react
2) Unreadble minified js code
