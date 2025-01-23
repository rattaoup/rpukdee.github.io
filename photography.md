---
layout: post
title: "Photography 📸"
categories: misc
---

<!-- Africa
- [Marrakech](photography/marrakech.md) 


Central / South America
- [Cancun](photography/cancun.md)
- [Peru](photography/cusco.md)

Europe
- [Budapest](photography/budapest.md)
- [Vienna](photography/vienna.md)

North America
- [Pittsburgh](photography/pittsburgh.md)
- [New york](photography/newyork.md)
- [Las Vegas](photography/vegas.md)
- [Toronto](photography/toronto.md)
 -->




<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dynamic Image Carousel</title>
    <style>
        .carousel-container {
            max-width: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .carousel {
            position: relative;
            width: 100%;
            max-width: 800px;
        }
        .carousel-inner {
            display: flex;
            transition: transform 0.5s ease;
            overflow: hidden;
        }
        .carousel-item {
            flex: 0 0 100%;
            width: 100%;
        }
        .carousel-item img {
            width: 100%;
            height: auto;
            object-fit: contain;
        }
        .carousel-controls {
            display: flex;
            justify-content: center;
            margin-top: 10px;
        }
        .nav-arrow {
            background: none;
            border: none;
            font-size: 2rem;
            cursor: pointer;
            color: #333;
        }
        .carousel-caption {
            text-align: center;
            margin-top: 10px;
            color: #666;
        }
    </style>
</head>
<body>
    <div class="carousel-container">
        <div class="carousel">
            <div class="carousel-inner" id="carouselInner">
                <div class="carousel-item">
                    <img src="./pics/budapest/01.jpg" alt="First Image">
                </div>
                <div class="carousel-item">
                    <img src="./pics/budapest/02.jpg" alt="Second Image">
                </div>
                <div class="carousel-item">
                    <img src="./pics/budapest/03.jpg" alt="Third Image">
                </div>
            </div>
        </div>
        <div class="carousel-controls">
            <button class="nav-arrow prev" onclick="changeSlide(-1)">←</button>
            <div class="carousel-caption">Image Caption</div>
            <button class="nav-arrow next" onclick="changeSlide(1)">→</button>
        </div>
    </div>

    <script>
        let currentSlide = 0;
        const slides = document.querySelectorAll('.carousel-item');
        const carouselInner = document.getElementById('carouselInner');
        const caption = document.querySelector('.carousel-caption');

        const captions = [
            "First Image Caption",
            "Second Image Caption", 
            "Third Image Caption"
        ];

        function changeSlide(direction) {
            currentSlide += direction;
            
            if (currentSlide >= slides.length) {
                currentSlide = 0;
            }
            if (currentSlide < 0) {
                currentSlide = slides.length - 1;
            }
            
            const offset = -currentSlide * 100;
            carouselInner.style.transform = `translateX(${offset}%)`;
            
            caption.textContent = captions[currentSlide];
        }
    </script>
</body>
</html>