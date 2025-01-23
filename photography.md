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

<div id="carousel" style="max-width: 800px; margin: auto; text-align: center;">
  <style>
    .carousel-image {
      max-width: 100%;
      height: auto;
      display: none;
    }
    .carousel-image.active {
      display: block;
    }
    .carousel-caption {
      font-size: 16px;
      padding: 10px;
      color: black;
    }
    .carousel-buttons {
      margin-top: 10px;
    }
    .carousel-buttons button {
      background-color: #007bff;
      color: white;
      border: none;
      padding: 10px 20px;
      margin: 0 5px;
      cursor: pointer;
    }
    .carousel-buttons button:hover {
      background-color: #0056b3;
    }
  </style>

  <!-- Images -->
  <img src="pics/budapest/01.jpg" alt="Slide 1" class="carousel-image active">
  <img src="pics/budapest/02.jpg" alt="Slide 2" class="carousel-image">
  <img src="pics/budapest/03.jpg" alt="Slide 3" class="carousel-image">

  <!-- Caption -->
  <div id="carouselCaption" class="carousel-caption">Caption for Slide 1</div>

  <!-- Buttons -->
  <div class="carousel-buttons">
    <button onclick="prevImage()">&#8592; Previous</button>
    <button onclick="nextImage()">Next &#8594;</button>
  </div>

  <script>
    const images = document.querySelectorAll('.carousel-image');
    const captions = [
      'Caption for Slide 1',
      'Caption for Slide 2',
      'Caption for Slide 3'
    ];
    const captionElement = document.getElementById('carouselCaption');
    let currentIndex = 0;

    function showImage(index) {
      images.forEach((img, i) => {
        img.classList.toggle('active', i === index);
      });
      captionElement.textContent = captions[index];
    }

    function nextImage() {
      currentIndex = (currentIndex + 1) % images.length;
      showImage(currentIndex);
    }

    function prevImage() {
      currentIndex = (currentIndex - 1 + images.length) % images.length;
      showImage(currentIndex);
    }
  </script>
