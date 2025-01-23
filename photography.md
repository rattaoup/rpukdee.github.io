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
  font-size: 12px; /* Smaller font size for caption */
  color: #555; /* Softer color for text */
  margin-top: 10px; /* Add spacing from the image */
  display: flex; /* Flexbox for horizontal alignment */
  justify-content: center; /* Center the caption and arrows */
  align-items: center; /* Vertically align the caption text and arrows */
  gap: 10px; /* Space between arrows and caption */
}
 .carousel-buttons button {
  background: none; /* Remove background from buttons */
  border: none; /* Remove border */
  color: black; /* Default color for arrows */
  font-size: 24px; /* Large, clear arrow size */
  cursor: pointer; /* Pointer cursor for interactivity */
  padding: 5px 10px; /* Add a bit of padding for easier clicking */
  transition: color 0.3s ease; /* Smooth hover effect */
}
.carousel-buttons button:hover {
  color: #007bff; /* Blue color for hover effect */
}
  </style>

  <!-- Images -->
  <img src="pics/slideshows/01.jpg" class="carousel-image active">
  <img src="pics/slideshows/02.jpg" class="carousel-image">
  <img src="pics/slideshows/03.jpg" class="carousel-image">
  <img src="pics/slideshows/04.jpg" class="carousel-image">
  <img src="pics/slideshows/05.jpg" class="carousel-image">
  <img src="pics/slideshows/06.jpg" class="carousel-image">
  <img src="pics/slideshows/07.jpg" class="carousel-image">
  <img src="pics/slideshows/08.jpg" class="carousel-image">
  <img src="pics/slideshows/09.jpg" class="carousel-image">
  <img src="pics/slideshows/10.jpg" class="carousel-image">
  <img src="pics/slideshows/11.jpg" class="carousel-image">
  <img src="pics/slideshows/12.jpg" class="carousel-image">
  <img src="pics/slideshows/13.jpg" class="carousel-image">
  <img src="pics/slideshows/14.jpg" class="carousel-image">
  <img src="pics/slideshows/15.jpg" class="carousel-image">
  <img src="pics/slideshows/16.jpg" class="carousel-image">
  <img src="pics/slideshows/17.jpg" class="carousel-image">
  <img src="pics/slideshows/18.jpg" class="carousel-image">


  <div id="carouselCaption" class="carousel-caption">
  <button onclick="prevImage()">&#8592;</button>
  <span>Caption for Slide 1</span>
  <button onclick="nextImage()">&#8594;</button>
</div>

  <script>
    const images = document.querySelectorAll('.carousel-image');
    const captions = [
      'Marrakech',
      'Budapest',
      'Ha Long Bay',
      'Taipei',
      'Vienna',
      'Taipei',
      'Marrakech',
      'Bangkok',
      'Cancun',
      'Hanoi',
      'Marrakech',
      'New york',
      'Lima',
      'Pittsburgh',
      'Pittsburgh',
      'Pittsburgh',
      'Toronto',
      'Las Vegas'
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
