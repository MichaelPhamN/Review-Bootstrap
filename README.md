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
The classes for text colors are: .text-muted, .text-primary (blue), .text-success (green), .text-info (viridian), .text-warning (yellow), .text-danger (red), .text-secondary (gray), .text-white, .text-dark, .text-body (default body color/often black) and .text-light

#### III.2. Background colors
The classes for background colors are: .bg-primary (blue), .bg-success (green), .bg-info (viridian), .bg-warning (yellow), .bg-danger (red), .bg-secondary (gray), .bg-dark and .bg-light

### IV. Components
#### IV.1. Forms
- Block input form
```html
<!-- Input Text -->
<div class="form-group">
  <label>Email address</label>
  <input type="text" class="form-control" placeholder="Email address"/>
</div>

<!-- Select -->
<div class="form-group">
  <label>Nationality</label>
  <select class="form-control">
    <option>United States</option>
    <option>Vietnam</option>
    <option>Brasil</option>
  </select>
</div>

<!-- Textarea -->
<div class="form-group">
  <label>Description</label>
  <textarea class="form-control" rows="4"></textarea>
</div>

<!-- Upload -->
<div class="form-group">
  <label>Calendar</label>
  <input type="date" class="form-control-file"/>
</div>

<!-- Calendar -->
<div class="form-group">
  <label>Calendar</label>
  <input type="date" class="form-control"/>
</div>

<!-- Checkbox -->
<div class="form-check">
  <input type="checkbox" class="form-check-input"/>
  <label class="form-check-label">Checkbox</label>
</div>  

<!-- Radio Button -->
<div class="form-check">
  <input type="radio" class="form-check-input" checked/>
  <label class="form-check-label">Radio Button</label>
</div>    
```
https://codepen.io/michaelphamngo/pen/NWYgoeE

- Inline input form
```html
<!-- Input Text -->
<div class="row form-group">
  <label class="col-2 col-form-label">Email address</label>
  <div class="col-10">
    <input type="email" class="form-control" placeholder="Email address">
  </div>
</div>  

<!-- Select -->
<div class="row form-group">
  <label class="col-2 col-form-label">Nationality</label>
  <div class="col-10">
    <select class="form-control">
      <option>United States</option>
      <option>Vietnam</option>
      <option>Brasil</option>
    </select>
  </div>
</div>

<!-- Textarea -->
<div class="row form-group">
  <label class="col-2 col-form-label">Description</label>
  <div class="col-10">
    <textarea class="form-control" rows="4"></textarea>
  </div>
</div>

<!-- Upload -->
<div class="row form-group">
  <label class="col-2 col-form-label">Upload</label>
  <div class="col-10">
    <input type="file" class="form-control-file"/>
  </div>
</div>

<!-- Calendar -->
<div class="row form-group">
  <label class="col-2 col-form-label">Calendar</label>
  <div class="col-10">
    <input type="date" class="form-control"/>
  </div>
</div>

<!-- Checkbox -->
<div class="row form-group">
  <div class="col-2">Checkboxes</div>
  <div class="col-10">
    <div class="form-check">
      <input type="checkbox" class="form-check-input"/>
      <label class="form-check-label">Checkbox 1</label>        
    </div>      
    <div class="form-check">
      <input type="checkbox" class="form-check-input"/>
      <label class="form-check-label">Checkbox 2</label>        
    </div>      
    <div class="form-check">
      <input type="checkbox" class="form-check-input"/>
      <label class="form-check-label">Checkbox 3</label>        
    </div>      
  </div>
</div>  

<!-- Radio Button -->
 <div class="row form-group">
  <label class="col-2 col-form-label">Radio Buttons</label>
  <div class="col-10">
      <div class="form-check form-check-inline">
        <input type="radio" class="form-check-input" checked/>
        <label class="form-check-label">Radio Button 1</label>
      </div>
      <div class="form-check form-check-inline">
        <input type="radio" class="form-check-input"/>
        <label class="form-check-label">Radio Button 2</label>     
      </div>
  </div>
</div>   

```
https://codepen.io/michaelphamngo/pen/XWEgGPg/c93830a8a46f27b822d5543307bfdc6b

#### IV.2. Alerts
```html
<div class="alert alert-primary">
  .alert .alert-primary
</div>
```
https://codepen.io/michaelphamngo/pen/JjLJabe

#### IV.3. Badge
```html
<!-- Button with badge span -->
<button type="button" class="btn btn-primary">
  Notifications <span class="badge badge-light">4</span>
</button>

<!-- Badge span -->
<span class="badge badge-primary">Primary</span>

<!-- Pill Badge span -->
<span class="badge badge-pill badge-primary">Primary</span>

<!-- Badge link -->
<a href="#" class="badge badge-pill badge-primary">Link Primary</a>
```
https://codepen.io/michaelphamngo/pen/xxWrapM

#### IV.4. Breadcrumb
```html
<nav>
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item"><a href="#">Library</a></li>
    <li class="breadcrumb-item active">Data</li>
  </ol>
</nav>
```
https://codepen.io/michaelphamngo/pen/JjLJmEd

#### IV.5. Buttons and Group Buttons 
```html
<!-- Button .btn .btn-primary -->
<button type="button" class="btn btn-primary">Primary</button>

<!-- Link button .btn .btn-primary -->
<a class="btn btn-primary" href="#" role="button">Link</a>

<!-- Input button .btn .btn-primary -->
<input class="btn btn-primary" type="button" value="Input">

<!-- Outline Button .btn .btn-outline-primary -->
<button type="button" class="btn btn-outline-primary">Outline Button Primary</button>

<!-- Large Button .btn .btn-primary btn-lg-->
<button type="button" class="btn btn-primary btn-lg">Large Primary Button</button>

<!-- Small Button .btn .btn-primary btn-sm-->
<button type="button" class="btn btn-primary btn-sm">Small Primary Button</button>

<!-- Large Block Button .btn .btn-primary btn-lg btn-block-->
<button type="button" class="btn btn-primary btn-lg btn-block">Large Block Primary Button</button>

<!-- Button with active state -->
<button type="button" class="btn btn-primary active">Primary</button>

<!-- Button with disable state -->
<button type="button" class="btn btn-primary disabled">Primary</button>

<!-- Group buttons -->
<div class="btn-group" role="group">
  <button type="button" class="btn btn-secondary">Left</button>
  <button type="button" class="btn btn-secondary">Middle</button>
  <button type="button" class="btn btn-secondary">Right</button>
</div>

<!-- Dropdown buttons -->
<div class="btn-group" role="group">
  <button id="btnGroupDrop1" type="button" class="btn btn-secondary dropdown-toggle" data-toggle="dropdown">
      Dropdown
    </button>
    <div class="dropdown-menu" aria-labelledby="btnGroupDrop1">
      <a class="dropdown-item">Dropdown link</a>
      <a class="dropdown-item">Dropdown link</a>      
    </div>
</div>

<!-- Group vertical buttons -->
<div class="btn-group-vertical" role="group">
  <button type="button" class="btn btn-secondary">Left</button>
  <button type="button" class="btn btn-secondary">Middle</button>
  <button type="button" class="btn btn-secondary">Right</button>
</div>
```
https://codepen.io/michaelphamngo/pen/QWmgzgv

#### IV.6. Dropdowns
```html
<!-- Dropdown -->
<!-- Step 1: .btn-group -->
<!-- Step 2: button [dropdown-toggle ~ down arrow] -->
<!-- Step 3: dropdown menu -->
<!-- Step 4: dropdown item -->
<div class="btn-group">
  <button class="btn btn-secondary dropdown-toggle" data-toggle="dropdown">Dropdown</button>
  <div class="dropdown-menu">
    <a class="dropdown-item">Dropdown item</a>
    <a class="dropdown-item">Dropdown item</a>
  </div>
</div>

<!-- Split Button -->
<div class="btn-group">
  <button class="btn btn-primary">Split Button</button>
  <button class="btn btn-primary dropdown-toggle" data-toggle="dropdown"></button>
  <div class="dropdown-menu">
    <a class="dropdown-item">Action</a>
    <a class="dropdown-item">Another Action</a>
    <a class="dropdown-item">Something else here</a>
    <div class="dropdown-divider"></div>
    <a class="dropdown-item">Separated link</a>
  </div>
</div>

<!-- Dropdown Toggle Arrow Direction -->
<div class="btn-group"> <!-- Down -->        
  <button class="btn btn-primary dropdown-toggle" data-toggle="dropdown">Down</button>
  <div class="dropdown-menu">
    <a class="dropdown-item">Action</a>
    <a class="dropdown-item">Another Action</a>
    <a class="dropdown-item">Something else here</a>
    <div class="dropdown-divider"></div>
    <a class="dropdown-item">Separated link</a>
  </div>
</div>
<div class="btn-group dropup"> <!-- Up -->               
  <button class="btn btn-secondary dropdown-toggle" data-toggle="dropdown">Up</button>
  <div class="dropdown-menu">
    <a class="dropdown-item">Action</a>
    <a class="dropdown-item">Another Action</a>
    <a class="dropdown-item">Something else here</a>
    <div class="dropdown-divider"></div>
    <a class="dropdown-item">Separated link</a>
  </div>
</div>
<div class="btn-group dropright">  <!-- Right -->               
  <button class="btn btn-danger dropdown-toggle" data-toggle="dropdown">Left</button>
  <div class="dropdown-menu">
    <a class="dropdown-item">Action</a>
    <a class="dropdown-item">Another Action</a>
    <a class="dropdown-item">Something else here</a>
    <div class="dropdown-divider"></div>
    <a class="dropdown-item">Separated link</a>
  </div>
</div>
<div class="btn-group dropleft">  <!-- Left -->                     
  <button class="btn btn-warning dropdown-toggle" data-toggle="dropdown">Right</button>
  <div class="dropdown-menu">
    <a class="dropdown-item">Action</a>
    <a class="dropdown-item">Another Action</a>
    <a class="dropdown-item">Something else here</a>
    <div class="dropdown-divider"></div>
    <a class="dropdown-item">Separated link</a>
  </div>
</div>

<!-- Menu display position -->
<div class="btn-group">        
  <button class="btn btn-primary dropdown-toggle" data-toggle="dropdown">Margin Left</button>
  <div class="dropdown-menu">
    <a class="dropdown-item">Action</a>
    <a class="dropdown-item">Another Action</a>
    <a class="dropdown-item">Something else here</a>
    <div class="dropdown-divider"></div>
    <a class="dropdown-item">Separated link</a>
  </div>
</div>
<div class="btn-group">        
  <button class="btn btn-info dropdown-toggle" data-toggle="dropdown">Margin Right</button>
  <div class="dropdown-menu dropdown-menu-right">
    <a class="dropdown-item">Action</a>
    <a class="dropdown-item">Another Action</a>
    <a class="dropdown-item">Something else here</a>
    <div class="dropdown-divider"></div>
    <a class="dropdown-item">Separated link</a>
  </div>
</div>
```
https://codepen.io/michaelphamngo/pen/rNdwPaP

#### IV.7. Menu

#### IV.8. Card

#### IV.9. Carousel

#### IV.10. Collapse

#### IV.11. Input group

#### IV.12. Jumbotron

#### IV.13. List group

#### IV.14. Modal

#### IV.15. Navs

#### IV.16. Navbar

#### IV.17. Pagination

#### IV.18. Popovers

#### IV.19. Progress

#### IV.20. Scrollspy

#### IV.21. Tooltips