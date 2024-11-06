# ACTIVITY 27 CSS_GRID

# Instruction: 

apply it on 5 pages (ex. list of products,list of employees, list of students, etc) - name your repo CSS_GRID - add documentation on README.md of your repo - Submit github repositories

* Products List: A grid showcasing products with images, names, and prices.
* Employees List: Grid cards for employee profiles, with positions and contact details.
* Students List: Cards for student profiles, including names and areas of study.
* Gallery: Display a grid of projects with descriptions.
* Services List: A section highlighting services in a visually appealing grid.

 ## How to Use Grid

* `* { box-sizing: border-box; }` - Ensures padding and border are included in an element’s total width and height, helping with consistent spacing.

*  `display: grid;` - Defines the element as a grid container, enabling the use of grid layout properties within it.

*  `gap: 16px;` - Adds spacing between grid items, both vertically and horizontally.

*  `grid-template-columns: 1fr;` - Sets the grid to one column, making it responsive by default on small screens (mobile-first design).

*  `grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));` - Automatically fills the container with columns that are at least 300px wide. When screen space allows, more columns will fit in, adapting to larger screens.

*  `border: 1px solid #ddd;` - Adds a light border around each card, enhancing separation between items.

*  `border-radius: 8px;` - Rounds the corners of elements (e.g., images, cards) for a softer look.

*  `text-align: center;` - Centers text within elements like headings (h2) and .card, improving visual balance.

*  `padding: 16px;` - Adds internal space around content inside .card, creating a cleaner, less cramped look.

*  `@media (min-width: 600px) { ... }` - Applies responsive adjustments to the layout on screens wider than 600px, helping the layout adapt for desktops and larger tablets.

*  `transition: background-color 0.3s ease;` - Smoothens the color change effect for buttons on hover, making interactions feel more polished.

# product-list.htm
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Flexbox Layout</title>
  <link rel="stylesheet" href="product.css">
</head>
<body>

  <!-- Product Layout Section -->
  <section class="section">
    <h2>Product Layout</h2>
    <div class="container">
      <div class="card">
        <img src="white.jpg" alt="Product 1">
        <h3>Product 1</h3>
        <p>White Mustang 5.0</p>
        <button>Buy Now</button>
      </div>
      <div class="card">
        <img src="red.jpg" alt="Product 2">
        <h3>Product 2</h3>
        <p>Red Mustang 5.0</p>
        <button>Buy Now</button>
      </div>
      <div class="card">
        <img src="blue.jpg" alt="Product 3">
        <h3>Product 3</h3>
        <p>blue Mustang 5.0</p>
        <button>Buy Now</button>
      </div>
      <div class="card">
        <img src="yellow.jpg" alt="Product 1">
        <h3>Product 1</h3>
        <p>yellow Mustang 5.0</p>
        <button>Buy Now</button>
      </div>
    </div>
  </section>
  </body>
```
# product.css
```
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

h2 {
  margin-bottom: 20px;
  font-size: 1.8em;
  text-align: center;
  color: #333;
}

.section {
  margin-bottom: 40px;
}

/* Set display: grid instead of flex */
.container {
  display: grid;                   /* Changed to grid */
  gap: 16px;                       /* Space between grid items */
  grid-template-columns: 1fr; /* Default for mobile */
}

.card {
  background-color: #fff;
  padding: 16px;
  border: 1px solid #ddd;
  border-radius: 8px;
  text-align: center;
}

.card img {
  width: 100%;
  height: auto;
  border-radius: 8px;
}

.card h3 {
  font-size: 1.2em;
  margin-top: 8px;
}

.card p {
  font-size: 0.9em;
  margin: 8px 0;
}

.card button {
  padding: 8px 16px;
  margin-top: 8px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.card button:hover {
  background-color: #0056b3;
}

/* Responsive adjustments (optional, as grid-template-columns handles responsiveness well) */
@media (min-width: 600px) {
  .container {
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); /* More space for larger screens */
  }
}
```
# Employees-list.html
```

<link rel="stylesheet" href="employees.css">

  <!-- Employee Cards Section -->
  <section class="section">
    <h2>Employee Cards</h2>
    <div class="container">
      <div class="card">
        <img src="bear2.jpg" alt="Employee 1">
        <h3>John</h3>
        <p>Position: Developer</p>
      </div>
      <div class="card">
        <img src="bear2.jpg" alt="Employee 2">
        <h3>Isaac</h3>
        <p>Position: Designer</p>
      </div>
      <div class="card">
        <img src="bear2.jpg" alt="Employee 3">
        <h3>Zaack</h3>
        <p>Position: Manager</p>
      </div>
      <div class="card">
        <img src="bear2.jpg" alt="Employee 3">
        <h3>IJ</h3>
        <p>Position: Assistance Developer</p>
      </div>
    </div>
  </section>
```
# employees.css
```
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  h2 {
    margin-bottom: 20px;
    font-size: 1.8em;
    text-align: center;
    color: #333;
  }
  
  .section {
    margin-bottom: 40px;
  }
  
  /* Set display: grid instead of flex */
  .container {
    display: grid;                   /* Changed to grid */
    gap: 16px;                       /* Space between grid items */
    grid-template-columns: 1fr; /* Default for mobile */
  }
  
  .card {
    background-color: #fff;
    padding: 16px;
    border: 1px solid #ddd;
    border-radius: 8px;
    text-align: center;
  }
  
  .card img {
    width: 100%;
    height: auto;
    border-radius: 8px;
  }
  
  .card h3 {
    font-size: 1.2em;
    margin-top: 8px;
  }
  
  .card p {
    font-size: 0.9em;
    margin: 8px 0;
  }
  
  .card button {
    padding: 8px 16px;
    margin-top: 8px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  .card button:hover {
    background-color: #0056b3;
  }
  
  /* Responsive adjustments (optional, as grid-template-columns handles responsiveness well) */
  @media (min-width: 600px) {
    .container {
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); /* More space for larger screens */
    }
  }

```
# student-list.html
```
<link rel="stylesheet" href="student.css">


  <!-- Student Profiles Section -->
  <section class="section">
    <h2>Student Profiles</h2>
    <div class="container">
      <div class="card">
        <img src="GIRL1.jpg" alt="Student 1">
        <h3>Jane Smith</h3>
        <p>Course: Computer Science</p>
      </div>
      <div class="card">
        <img src="BOY.jpg" alt="Student 2">
        <h3>Mike Johnson</h3>
        <p>Course: Business</p>
      </div>
      <div class="card">
        <img src="GIRL2.jpg" alt="Student 3">
        <h3>Sarah Lee</h3>
        <p>Course: Engineering</p>
      </div>
      <div class="card">
        <img src="BOY.jpg" alt="Student 2">
        <h3>Mike Johnson</h3>
        <p>Course: Business</p>
      </div>
    </div>
  </section>
```
# student.css
```
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

h2 {
  margin-bottom: 20px;
  font-size: 1.8em;
  text-align: center;
  color: #333;
}

.section {
  margin-bottom: 40px;
}

/* Set display: grid instead of flex */
.container {
  display: grid;                   /* Changed to grid */
  gap: 16px;                       /* Space between grid items */
  grid-template-columns: 1fr; /* Default for mobile */
}

.card {
  background-color: #fff;
  padding: 16px;
  border: 1px solid #ddd;
  border-radius: 8px;
  text-align: center;
}

.card img {
  width: 100%;
  height: auto;
  border-radius: 8px;
}

.card h3 {
  font-size: 1.2em;
  margin-top: 8px;
}

.card p {
  font-size: 0.9em;
  margin: 8px 0;
}

.card button {
  padding: 8px 16px;
  margin-top: 8px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.card button:hover {
  background-color: #0056b3;
}

/* Responsive adjustments (optional, as grid-template-columns handles responsiveness well) */
@media (min-width: 600px) {
  .container {
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); /* More space for larger screens */
  }
}
```
# gallery-list.html
```

<link rel="stylesheet" href="gallery.css">

  <!-- Gallery Section -->
  <section class="section">
    <h2>Gallery</h2>
    <div class="container">
      <div class="card">
        <img src="bear1.jpg" alt="Gallery Image 1">
      </div>
      <div class="card">
        <img src="bearpic.jpg" alt="Gallery Image 2">
      </div>
      <div class="card">
        <img src="bear3.jpg" alt="Gallery Image 3">
      </div>
      <div class="card">
        <img src="bear2.jpg" alt="Gallery Image 3">
      </div>
    </div>
  </section>
```
# gallery.css
```
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

h2 {
  margin-bottom: 20px;
  font-size: 1.8em;
  text-align: center;
  color: #333;
}

.section {
  margin-bottom: 40px;
}

/* Set display: grid instead of flex */
.container {
  display: grid;                   /* Changed to grid */
  gap: 16px;                       /* Space between grid items */
  grid-template-columns: 1fr; /* Default for mobile */
}

.card {
  background-color: #fff;
  padding: 16px;
  border: 1px solid #ddd;
  border-radius: 8px;
  text-align: center;
}

.card img {
  width: 100%;
  height: auto;
  border-radius: 8px;
}

.card h3 {
  font-size: 1.2em;
  margin-top: 8px;
}

.card p {
  font-size: 0.9em;
  margin: 8px 0;
}

.card button {
  padding: 8px 16px;
  margin-top: 8px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.card button:hover {
  background-color: #0056b3;
}

/* Responsive adjustments (optional, as grid-template-columns handles responsiveness well) */
@media (min-width: 600px) {
  .container {
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); /* More space for larger screens */
  }
}
```
# service-lis.html
```

<link rel="stylesheet" href="service.css">

  <!-- Services Section -->
  <section class="section">
    <h2>Our Services</h2>
    <div class="container">
      <div class="card">
        <h3>Service 1</h3>
        <img src="Exceptional-Customer-Service.jpg" alt="Gallery Image 2">
      </div>
      <div class="card">
        <h3>Service 2</h3>
        <img src="Exceptional-Customer-Service.jpg" alt="Gallery Image 2">
      </div>
      <div class="card">
        <h3>Service 3</h3>
        <img src="Exceptional-Customer-Service.jpg" alt="Gallery Image 2">
      </div>
      <div class="card">
        <h3>Service 4</h3>
        <img src="Exceptional-Customer-Service.jpg" alt="Gallery Image 2">
      </div>
    </div>
  </section>
```
# service.css
```
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

h2 {
  margin-bottom: 20px;
  font-size: 1.8em;
  text-align: center;
  color: #333;
}

.section {
  margin-bottom: 40px;
}

/* Set display: grid instead of flex */
.container {
  display: grid;                   /* Changed to grid */
  gap: 16px;                       /* Space between grid items */
  grid-template-columns: 1fr; /* Default for mobile */
}

.card {
  background-color: #fff;
  padding: 16px;
  border: 1px solid #ddd;
  border-radius: 8px;
  text-align: center;
}

.card img {
  width: 100%;
  height: auto;
  border-radius: 8px;
}

.card h3 {
  font-size: 1.2em;
  margin-top: 8px;
}

.card p {
  font-size: 0.9em;
  margin: 8px 0;
}

.card button {
  padding: 8px 16px;
  margin-top: 8px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.card button:hover {
  background-color: #0056b3;
}

/* Responsive adjustments (optional, as grid-template-columns handles responsiveness well) */
@media (min-width: 600px) {
  .container {
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); /* More space for larger screens */
  }
}
```
