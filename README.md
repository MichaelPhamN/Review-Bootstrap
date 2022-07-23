# Review-Bootstrap

## Table of content


### I. Basic Html Template
```html
<!DOCTYPE html>  
<html>  
  <head> 
    <title>Bootstrap 101 Template</title>  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="css/bootstrap.min.css" rel="stylesheet">
    <!--[if lt IE 9]>  
      <script src="https://oss.maxcdn.com/libs/html5shiv/3.7.0/ html5shiv.js"></script>  
      <script src="https://oss.maxcdn.com/libs/respond.js/1.3.0/ respond.min.js"></script>  
    <![endif]--> 
  </head> 
  <body>  
    <h1>Hello, world!</h1>   
    <script src="https://code.jquery.com/jquery.js"></script>
    <script src="js/bootstrap.min.js"></script>  
  </body> 
</html> 
```

### II. Layout
#### II.1. Containers
Containers are used to pad the content inside of them. There are two container classes:
- The **_.container_** class provide a fixed container
<table>
  <tr>
    <td></td>
    <td><strong>Extra small </br>< 576px</strong></td>
    <td><strong>Small </br>>= 576px && < 768px</strong></td>
    <td><strong>Medium </br>>= 768px && < 992px</strong></td>
    <td><strong>Large </br>>= 992px && < 1200px</strong></td>
    <td><strong>Extra large </br>>= 1200px</strong></td>
  <tr>
  <tr>
    <td>max-width</td>
    <td>100%</td>
    <td>540px</td>
    <td>720px</td>
    <td>960px</td>
    <td>1140px</td>
  <tr>
</table>
- Bootstrap grid system has 5 classes: <br/>
1. <b>.col-</b> (Extra small devices < 576px) <br/>
2. <b>.col-sm-</b> (Small devices >= 576px && < 768px) <br/>
3. <b>.col-md-</b> (Medium devices >= 768px && < 992px) <br/>
4. <b>.col-lg-</b> (Large devices >= 992px && < 1200px) <br/>
5. <b>.col-xl-</b> (Extra large devices >= 1200px) <br/>
<br/>
- The <b><i>.container-fluid</i></b> class provide a full container. It always span the entire width of the screen (<b><i>width</i></b> is always <b><i>100%</i></b>)

![Container vs Container-Fluid](https://user-images.githubusercontent.com/19525412/180586705-9b8ebbc6-04e7-434e-a650-801b2c876f98.png)

#### II.2. Bootstrap Grid System
- Bootstrap is built with flexbox and represents 12 columns across a webpage.

![Bootstrap Grid System](https://miro.medium.com/max/2342/1*Wg3dRY_fGQUvwhBplltkoQ.png)

- Auto Layout Columns

![Auto-Layout-Columns](http://apycom.com/bootstrap-components/data/upload/2017/04/equalcolumn.jpg)
```html
<div class="container">
  <div class="row">
    <div class="col">1 of 2</div> <!-- Auto recognize col is col-6 -->
    <div class="col">1 of 2</div> <!-- Auto recognize col is col-6 -->
  </div>
  <div class="row">
    <div class="col">1 of 3</div> <!-- Auto recognize col is col-4 -->
    <div class="col">1 of 3</div> <!-- Auto recognize col is col-4 -->
    <div class="col">1 of 3</div> <!-- Auto recognize col is col-4 -->
  </div>
</div>
```

- Setting one fixed width

![Setting-one-fixed-width](https://designmodo.com/wp-content/uploads/2021/03/11.png)
```html
<div class="container">
  <div class="row">
    <div class="col">Column 1</div> <!-- Auto recognize width -->
    <div class="col">Column 2</div> <!-- Auto recognize width -->
    <div class="col">Column 3</div> <!-- Auto recognize width -->
  </div>
  <div class="row">
    <div class="col">Column 3/12</div> <!-- Auto recognize width -->
    <div class="col-6">Column 6/12</div> <!-- Fixed width -->
    <div class="col">Column 3/12</div> <!-- Auto recognize width -->
  </div>
</div>
```



- Mix and match

![Mix-And-Match](https://s1.o7planning.com/en/11963/images/21452841.gif)

```html
<div class="container">
  <div class="row">
    <div class="col-md-2 col-sm-6"> 6 columns if width < 768px and > 567px | 2 columns if width > 768 px </div>
    <div class="col-md-10 col-sm-6"> 6 columns if width < 768px and > 567px | 10 columns if width > 768 px </div>      
  </div>
</div>  
```

- Nested Columns

![Nested-Columns](https://i.stack.imgur.com/D8J1p.jpg)

```html
<div class="container">
  <div class="row">
    <div class="col-md-9"> <!-- Left column col-md-9 -->
      <div class="row">
        <div class="col">col-md-9</div>
      </div>
      <div class="row">
        <div class="col">col-md-9</div>
      </div>
    </div>
    <div class="col-md-3"> <!-- Right column col-md-3 -->
      <div class="row">
        <div class="col">col-md-3</div>
      </div>
    </div>
  </div>
</div>
```

### III. Colors
#### III.1. Text colors
The classes for text colors are: .text-muted, .text-primary (blue), .text-success (green), .text-info, .text-warning (yellow), .text-danger (red), .text-secondary (gray), .text-white, .text-dark, .text-body (default body color/often black) and .text-light

#### III.2. Background colors
The classes for background colors are: .bg-primary (blue), .bg-success (green), .bg-info, .bg-warning (yellow), .bg-danger (red), .bg-secondary (gray), .bg-dark and .bg-light
