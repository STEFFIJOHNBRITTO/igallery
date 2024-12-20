# Ex.08 Design of Interative Image Gallery
## Date:18.12.2024
 
 ## AIM:
 To design a web application for an interactive image gallery with minimum five images.

 ## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change setttings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Interactive Car Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: rgb(244, 247, 63);
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 10px;
            padding: 20px;
        }

        .gallery img {
            width: 100%;
            height: auto;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .gallery img:hover {
            transform: scale(1.1);
            box-shadow: 0 4px 15px rgba(45, 176, 197, 0.2);
        }

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgb(232, 229, 62);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .modal img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 10px;
        }

        .modal-close {
            position: absolute;
            top: 20px;
            right: 30px;
            font-size: 2rem;
            color: rgb(39, 131, 108);
            cursor: pointer;
        }
        footer {
            text-align: center;
            font-size: 16px;
            margin-top: 40px; 
            color: rgb(1, 1, 1);
        }

    </style>
</head>
<body>

<div class="gallery">
    <img src="car.png" alt="Image 1">
    <img src="car2.png" alt="Image 2">
    <img src="car3.png" alt="Image 3">
    <img src="car4.png" alt="Image 4">
    <img src="car6.png" alt="Image 5">
    <img src="Screenshot 2024-12-17 193615.png" alt="Image 6">

</div>

<div class="modal" id="modal">
    <span class="modal-close" id="modalClose">&times;</span>
    <img id="modalImage" src="" alt="Expanded Image">
</div>
<footer >
    Designed and developed by STEFFI J &copy; 2024
</footer>


<script>
    const gallery = document.querySelector('.gallery');
    const modal = document.getElementById('modal');
    const modalImage = document.getElementById('modalImage');
    const modalClose = document.getElementById('modalClose');

    gallery.addEventListener('click', (e) => {
        if (e.target.tagName === 'IMG') {
            modalImage.src = e.target.src;
            modal.style.display = 'flex';
        }
    });

    modalClose.addEventListener('click', () => {
        modal.style.display = 'none';
    });

    modal.addEventListener('click', (e) => {
        if (e.target === modal) {
            modal.style.display = 'none';
        }
    });

</script>

</body>
</html>

```
## OUTPUT:
![alt text](<Screenshot (102).png>)
![alt text](<Screenshot (103).png>)


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript
