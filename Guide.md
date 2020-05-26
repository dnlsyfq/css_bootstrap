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
## The Button Component
[Ref](https://getbootstrap.com/docs/4.2/components/buttons/#examples)

```
<button type="button" class="btn btn-danger">Danger</button>
```

## Collapsing a Component
 allows us to quickly add interactivity to a webpage. 
 One way to include interactivity is to toggle the visibility of an element.
 
 [Ref](https://getbootstrap.com/docs/4.2/components/collapse/)
 
 > To add such a feature, we need two elements and a few attributes
 
 ```
 <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
  This button controls the following div's visibility. 
</button>

<div class="collapse" id="collapseExample">
  <p>This content's visibility gets toggled</p>
</div>
 ```

The button has an attribute data-toggle="collapse" which enables button’s toggle ability. Another attribute, data-target="#collapseExample", means that this button toggles the visibility of the element with the id of "collapseExample". The aria-expanded and aria-controls attributes are information for screen readers and other accessibility means.

Focusing our attention on the <div> below the button, notice that it has a class of "collapse", which hides the content when the webpage initially renders. Our <div> also has an id of "collapseExample" which corresponds to the value of the button’s data-target.
  
```
<div class="container">
 <button class="btn btn-link" aria-expanded="false" aria-controls="seedSpecial" data-target="#seedSpecial" data-toggle="collapse">
          Gearing to Grow?
 </button>
        <p class="collapse" id="seedSpecial">
          Use promo code "GGarden" for additional 15% off your entire purchase!
        </p>
</div>        
```
  
## Creating a Navbar
[Ref](https://getbootstrap.com/docs/4.2/components/navbar/#supported-content)

```
<nav class="navbar navbar-light bg-light navbar-expand-sm">
    
    <a class="navbar-brand">
    <img src="https://s3.amazonaws.com/codecademy-content/courses/learn-bootstrap-components/logo.png" 
    alt="Gloria's Gardening Logo" 
    height="30">
    </a>
    
    
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav">
        <li class="nav-item active">
          <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Weekly Specials</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">About</a>
        </li>
      </ul>
    </div>
  </nav>
```

## The Jumbotron Component
makes content stand out.

```
<div class="row">
  <div class="col">
    <div class="jumbotron">
      <h1>Wow this stands out!</h1>
    </div>      
  </div>
</div>  
```
## Adding a Card

card component that serves as a container for smaller customized content. Card components are often grouped together to display a collection of similar content in manageable chunks. We can draw a comparison of the card component to playing cards in deck — in both cases, there are cards grouped together and each one contains something different.

```
<div class="card">
  <img class="card-img-top" src="placeholder.jpg" alt="card example image">
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <p class="card-text">Card description goes here.</p>
    <a href="#" class="card-link">Link to somewhere.</a>
  </div>
</div>
```

## The Carousel Component

 to showcase a group of images but not want to have our users scroll through one picture on top of another. Instead, we could fit our images into a slideshow
 
 
* The id is used later when we want to add controls to click between slides.
* The classes provide the styling and formatting.
* The data-ride attribute provides the interactivity and slide transitions.
 
 ```
 <div id="carouselExampleSlidesOnly" class="carousel slide" data-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img class="d-block w-100" src="example_slide_1.png" alt="First slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="example_slide_2.png" alt="Second slide">
    </div>
  </div>
</div>
 ```
 
 **e.g.**
 ```
 <div class="row">
      <div class="col">
        <!-- Edit the elements below to make a carousel component: -->
        <!-- Parent Carousel div -->
        <div id="gardeningAlbum" class="carousel slide" data-ride="carousel">
          <!-- Inner Carousel div -->
          <div class="carousel-inner">
            <!-- First slide div -->
            <div class="carousel-item active">
              <img src="https://s3.amazonaws.com/codecademy-content/courses/learn-bootstrap-components/garden-slide1.jpg" class="d-block w-100" alt="butterfly in field">
            </div>
            <!-- End of first slide -->
            <!-- Second slide div -->
            <div class="carousel-item">
              <img src="https://s3.amazonaws.com/codecademy-content/courses/learn-bootstrap-components/garden-slide2.jpg" class="d-block w-100" alt="colorful tulips">
            </div>
            <!-- End of second slide -->
            <!-- Third slide div -->
            <div class="carousel-item">
              <img src="https://s3.amazonaws.com/codecademy-content/courses/learn-bootstrap-components/garden-slide3.jpg" class="d-block w-100" alt="inside of a greenhouse">
            </div>
            <!-- End of third slide -->
          </div>
          <!-- End of inner carousel -->
          <!-- Add code for controls below: -->
          <a class="carousel-control-prev" href="#gardeningAlbum" role="button" data-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="sr-only">Previous</span>
          </a>
          <a class="carousel-control-next" href="#gardeningAlbum" role="button" data-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="sr-only">Next</span>
          </a>
        </div>
        <!-- End of carousel component -->
      </div>
    </div>
 ```

