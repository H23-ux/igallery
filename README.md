# Ex.08 Design of Interactive Image Gallery
## Date:18.05.25

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
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Tiffany & Co. Jewellery</title>
    <style>
        h1 {
            color: #0abab5;
            text-shadow: 0 0 10px white, 0 0 20px #b2ffff;
            position: relative;
            bottom: 10px;
            font-family: 'Georgia', serif;
            font-size: 45px;
        }
        html {
            background-color: #e0f7f7;
        }
        body {
            background: radial-gradient(white, #d0f0f5);
            border-radius: 30px;
            height: 850px;
            width: 100%;
            margin: 0;
            overflow: hidden;
        }
        .main {
            background-color: white;
            height: 80%;
            width: 70%;
            border-radius: 20px;
            display: inline-flex;
            justify-content: center;
            align-items: center;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            box-shadow: 0 0 20px #b2ffff;
        }
        .m1 {
            background-color: #e0f7f7;
            margin: 10px;
            height: 650px;
            width: 900px;
            display: flex;
            flex-wrap: wrap;
            overflow-y: scroll;
            justify-content: center;
            align-items: center;
            border-radius: 20px;
            transition: all 1.5s ease;
        }
        .m1::-webkit-scrollbar {
            width: 6px;
        }
        .m1::-webkit-scrollbar-thumb {
            background: #0abab5;
            border-radius: 10px;
        }
        .m2 {
            position: absolute;
            top: 50%;
            right: 10px;
            margin: 10px;
            opacity: 0;
            width: 0px;
            height: 0px;
            transition: all 1.5s ease, opacity 0.4s;
            visibility: hidden;
        }
        img {
            margin: 10px;
            width: 220px;
            height: 220px;
            object-fit: cover;
            transition: transform 0.5s ease;
            cursor: pointer;
            border-radius: 12px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        img:hover {
            transform: scale(1.1);
        }
        #ii {
            border-radius: 12px;
            width: 100%;
            height: auto;
        }
        .m1.shrink {
            position: absolute;
            top: 10px;
            left: 10px;
            width: 350px;
            overflow-y: scroll;
            transition: all 1.5s ease;
        }
        .m2.grow {
            position: absolute;
            top: 10px;
            right: 10px;
            width: 650px;
            height: 650px;
            opacity: 1;
            visibility: visible;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        footer {
            background-color: white;
            border-radius: 20px;
            width: 30%;
            position: absolute;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            text-align: center;
            font-family: 'Georgia', serif;
            color: #0abab5;
            padding: 10px;
            box-shadow: 0 0 10px #b2ffff;
        }
    </style>
</head>
<body>
    <h1 align="center">Tiffany & Co. Jewellery Collection</h1>
    <div class="main">
        <div class="m1">
            <img src="C:\Users\admin\Videos\New folder\igallery\gallery\igalleryapp\static\ring.png.png" alt="Ring" onclick="f(this)">
            <img src="C:\Users\admin\Videos\New folder\igallery\gallery\igalleryapp\static\necklace.png.png" alt="Necklace" onclick="f(this)">
            <img src="C:\Users\admin\Videos\New folder\igallery\gallery\igalleryapp\static\bracelet.png.png" alt="Bracelet" onclick="f(this)">
            <img src="C:\Users\admin\Videos\New folder\igallery\gallery\igalleryapp\static\earring.png.png" alt="Earrings" onclick="f(this)">
            <img src="C:\Users\admin\Videos\New folder\igallery\gallery\igalleryapp\static\peendant.png.png" alt="Pendant" onclick="f(this)">
            <img src="C:\Users\admin\Videos\New folder\igallery\gallery\igalleryapp\static\brooch.png.png" alt="Brooch" onclick="f(this)">
        </div>
        <div class="m2" id="iii" onclick="c()">
            <img src="" alt="Zoomed View" id="ii">
        </div>
    </div>
    <footer>
        DESIGNED & DEVELOPED by Harsheni.S
    </footer>

    <script>
        var a = document.getElementById('iii');
        var b = document.getElementById('ii');
        const d = document.querySelector('.m1');
        const d1 = document.querySelector('.m2');

        function f(img) {
            d1.classList.add('grow');
            d.classList.add('shrink');
            b.src = img.src;
        }

        function c() {
            d1.classList.remove('grow');
            d.classList.remove('shrink');
        }
    </script>
</body>
</html>

```
## OUTPUT:

![alt text](<Screenshot 2025-05-18 130749.png>)


![alt text](<Screenshot 2025-05-18 130814.png>)


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
