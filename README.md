# Bootstrap Framework 
Bootstrap uses classes to apply CSS rulesets — these rulesets dictate the layout and styling of the element.

## Incorporating bootstrap 
There are also some optional JavaScript libraries if we want to add some interactivity to our website and these are inserted at the end of our $<body>$ element


$<script>$ elements at the bottom of the $<body>$

    
[Bootstrap's Getting Started Documentation](https://getbootstrap.com/docs/4.1/getting-started/introduction/)
    
    
```
<head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- Bootstrap CSS for styling and layout-->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
</head>
```

## Intro Grid 
Bootstrap simplifies the layout of a website using a grid system.
[Grid Documentation](https://getbootstrap.com/docs/4.1/layout/grid/)

containers are the basis of Bootstrap’s grid. Inside containers, we nest rows as immediate children. Then, nested inside rows are columns. Inside columns, we put our actual content. 

```
<div class="container">
  <div class="row">
    <div class="col">
      <!-- A column inside a row inside a container! -->
    </div>
  </div>
</div>
```

## Bootstrap Containers

Bootstrap uses a grid system based on CSS Flexbox which organizes content in rows or columns. 

To create a container, necessary for Bootstrap’s grid :

```
<div class="container"></div>
```

<div> from the example above becomes a Bootstrap container which has a width relative to a user’s screen size, becomes horizontally centered, and has a left and right margin.
    
If we wanted the container to take up the entire width of the screen we can assign a class of "container-fluid"


```
<div class="container-fluid"></div>
```

## Bootstrap Rows

Rows are nested within containers. Also, we can add as many rows as we want inside a container

By default, a row will take up the entire width of its parent container. To create a row we assign a class of "row" to an element.

```
<div class="container">
  <div class="row">
  </div>
</div>
```

## Bootstrap Columns

Columns are the immediate children of rows and store content. 

By default, a column will take up the entire width of its parent row. 
Columns take on a default width based on the size of the row.
As we add more columns inside a row, the default behavior is for each column’s width to be readjusted to fit in the row — each column will have the same width. At most, a row will accommodate 12 columns.

```
<div class="container">
  <div class="row">
    <div class="col">
    </div>
  </div>
</div> 
```

**Setting Column Widths**

customization options so that we can make columns of varying widths.

```
# row still has 4 columns worth of space

<div class="col-8">
  <p>This is the width of 8 columns.</p>
</div>
```

If we decide to add an adjacent column

```
<div class="row">
  <div class="col-8">
    <p>This is the width of 8 columns.</p>
  </div>
  <div class="col-4">
    <p>This has the width of 4 columns.</p>
  </div>
</div>
```

**Setting Column Width with Content**

to use the content to set a column’s width, we append "auto" to the class of the column,

```
<div class="col-auto">
  <p>This content determines the width of the parent column</p>
</div>
```

## Bootstrap Breakpoints

Bootstrap categorizes screen sizes into 5 categories or as breakpoints: extra small, small, medium, large, and extra large. Each breakpoint has a range measured in pixels.

|Category|	Breakpoint Range|	Device Type|
|---|---|---|
|Extra small|	< 576 px	|portrait smartphones|
|Small|	≥ 576 px	|landscape smartphones|
|Medium	|≥ 768 px	|tablets|
|Large	|≥ 992 px	|desktops|
|Extra Large|	≥ 1200 px	|large desktop|

**Breakpoint Naming Convention**

We can even customize how our content on the grid changes based on breakpoints (extra small, small, medium, large, extra large)

The naming convention follows a pattern of **"col-{breakpoint}-{width}"**

> col-{breakpoint}-{width}

* As seen before "col" refers to a column.
* {breakpoint} can be sm, md, lg, or xl. Notice that there is no extra small or xs breakpoint. If we omit {breakpoint}, it is by default for extra small screens.
* {width} can be set from 1 to 12 and assigns a width to the column.
* When we set a {breakpoint}-{width}, it means that we want our column to have that set width for screens that fit in the specified breakpoint range and other larger screens.

```
<div class="col-sm-8"> 
</div>
```

## Combining Bootstrap Classes
add multiple classes to our columns for additional control over the rendering of our content

From the example, we have a column that renders a different width based on a user’s screen size. On extra small and small sized screens, the column has a width of 12 individual columns. For medium and large sized screens, the column has a width of 8 individual columns. Lastly, for extra large screens, the column has a width of 6 individual columns.

```
<div class="col-12 col-md-8 col-xl-6">
</div>
```
