# Ex.08 Design of Interactive Image Gallery
## Date: 18/12/2025
## Register: 25011764

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :

~~~
gallery.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Classroom of the Elite - Image Gallery</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: Arial, Helvetica, sans-serif;
    }

    body {
      background: #0f172a;
      color: #ffffff;
      padding: 20px;
    }

    h1 {
      text-align: center;
      margin-bottom: 20px;
    }

    /* Gallery Grid */
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 15px;
      max-width: 1100px;
      margin: auto;
    }

    .gallery img {
      width: 100%;
      height: 300px;
      object-fit: cover;
      border-radius: 12px;
      cursor: pointer;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .gallery img:hover {
      transform: scale(1.05);
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.6);
    }

    /* Lightbox */
    .lightbox {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.85);
      justify-content: center;
      align-items: center;
      z-index: 1000;
    }

    .lightbox img {
      max-width: 90%;
      max-height: 90%;
      border-radius: 12px;
    }

    .close {
      position: absolute;
      top: 20px;
      right: 30px;
      font-size: 32px;
      cursor: pointer;
      color: #ffffff;
    }
  </style>
</head>
<body>

  <h1>Classroom – Image Gallery</h1>

  <div class="gallery">
    <!-- Five images -->
    <img src="https://images.unsplash.com/photo-1524995997946-a1c2e315a42f" alt="Classroom of the Elite 1" onclick="openLightbox(this.src)">
    <img src="https://images.unsplash.com/photo-1523240795612-9a054b0db644" alt="Classroom of the Elite 2" onclick="openLightbox(this.src)">
    <img src="https://images.unsplash.com/photo-1503676260728-1c00da094a0b" alt="Classroom of the Elite 3" onclick="openLightbox(this.src)">
    <img src="https://images.unsplash.com/photo-1513258496099-48168024aec0" alt="Classroom of the Elite 4" onclick="openLightbox(this.src)">
    <img src="https://images.unsplash.com/photo-1509062522246-3755977927d7" alt="Classroom of the Elite 5" onclick="openLightbox(this.src)">
  </div>

  <!-- Lightbox -->
  <div class="lightbox" id="lightbox">
    <span class="close" onclick="closeLightbox()">&times;</span>
    <img id="lightboxImg" src="" alt="Preview">
  </div>

  <script>
    function openLightbox(src) {
      document.getElementById("lightbox").style.display = "flex";
      document.getElementById("lightboxImg").src = src;
    }

    function closeLightbox() {
      document.getElementById("lightbox").style.display = "none";
    }
  </script>

</body>
</html>

~~~


## OUTPUT:

<img width="1919" height="1079" alt="Screenshot 2025-12-18 135320" src="https://github.com/user-attachments/assets/d05dd511-f9cf-43db-86d9-a5892d9a7169" />


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
