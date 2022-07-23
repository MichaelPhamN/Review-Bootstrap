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

#### II.2. Grid classes

