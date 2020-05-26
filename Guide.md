# Bootstrap Utilities and Components

Utility classes that provide additional styling and components that each serve distinct purposes
[Kick Start](https://getbootstrap.com/docs/4.2/getting-started/introduction/#starter-template)

quickly style our elements using Bootstrap’s predefined CSS classes and take advantage of Bootstrap’s JavaScript files to incorporate a level of interactivity to our webpages.

## Adding Colors

to change the text color of our paragraph element from the default black to blue

```
<p class="text-primary">This text is blue!</p>
```
According to the documentation, the "text" portion of the class targets the element’s text styling. Appending "primary" after "text" changes the text color to blue. The name of the class, "text-primary"

[Ref](https://getbootstrap.com/docs/4.2/utilities/colors/#color)

change the background color
```
<div class="bg-success">
  Green! This signifies success! 
</div>
```
The "bg" part references the element’s background and "success" changes the background color to green. 

## Styling Text
[Ref](https://getbootstrap.com/docs/4.2/utilities/text/)

```
<p class="font-weight-bold text-uppercase">
  This rendered text is both bold and uppercased. 
</p>
```
text to be bold and uppercased.


## Element Positioning

[Ref 1](https://getbootstrap.com/docs/4.2/utilities/position)
[Ref 2](https://developer.mozilla.org/en-US/docs/Web/CSS/position)

```
<div class="fixed-top">
  This div will be fixed at the top of the screen. 
</div>
```
## Navigation component

 The nav component is slightly different from a navbar component. The nav component is often specific to one or a few webpages, whereas a navbar often appears on all the pages of a website.
 
 [Ref](https://getbootstrap.com/docs/4.2/components/navs/)
 
 Basic nav component
 ```
 <ul class="nav">
  <li class="nav-item">
    <a class="nav-link" href="#">First Link</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Second Link</a>
  </li>
</ul>
 ```
simpler nav component

```
<nav class="nav">
  <a class="nav-link" href="#">First Link</a>
  <a class="nav-link" href="#">Second Link</a>
</nav>
```


