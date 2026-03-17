---
title: Macro-sprint SDG
layout: default
---

# Macro-sprint SDG 10.3: Beyond Accessibility: - Design for Elderly in the Digital Divide

<div class="slideshow-container">

  <div class="slide fade">
    <img src="images/macrosprint-1.png" style="width:100%">
  </div>

  <div class="slide fade">
    <img src="images/macrosprint-2.png" style="width:100%">
  </div>

  <div class="slide fade">
    <img src="images/macrosprint-3.png" style="width:100%">
  </div>

  <div class="slide fade">
    <img src="images/macrosprint-4.png" style="width:100%">
  </div>

  <div class="slide fade">
    <img src="images/macrosprint-5.png" style="width:100%">
  </div>

  <div class="slide fade">
    <img src="images/macrosprint-6.png" style="width:100%">
  </div>

  <div class="slide fade">
    <img src="images/macrosprint-7.png" style="width:100%">
  </div>

  <div class="slide fade">
    <img src="images/macrosprint-8.png" style="width:100%">
  </div>

  <div class="slide fade">
    <img src="images/macrosprint-9.png" style="width:100%">
  </div>

  <div class="slide fade">
    <img src="images/macrosprint-10.png" style="width:100%">
  </div>

  <div class="slide fade">
    <img src="images/macrosprint-11.png" style="width:100%">
  </div>

  <div class="slide fade">
    <img src="images/macrosprint-12.png" style="width:100%">
  </div>

  <div class="slide fade">
    <img src="images/macrosprint-13.png" style="width:100%">
  </div>

  <div class="slide fade">
    <img src="images/macrosprint-14.png" style="width:100%">
  </div>

  <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
  <a class="next" onclick="plusSlides(1)">&#10095;</a>

</div>

<br>

<div style="text-align:center">
  <span class="dot" onclick="currentSlide(1)"></span>
  <span class="dot" onclick="currentSlide(2)"></span>
  <span class="dot" onclick="currentSlide(3)"></span>
  <span class="dot" onclick="currentSlide(4)"></span>
  <span class="dot" onclick="currentSlide(5)"></span>
  <span class="dot" onclick="currentSlide(6)"></span>
  <span class="dot" onclick="currentSlide(7)"></span>
  <span class="dot" onclick="currentSlide(8)"></span>
  <span class="dot" onclick="currentSlide(9)"></span>
  <span class="dot" onclick="currentSlide(10)"></span>
  <span class="dot" onclick="currentSlide(11)"></span>
  <span class="dot" onclick="currentSlide(12)"></span>
  <span class="dot" onclick="currentSlide(13)"></span>
  <span class="dot" onclick="currentSlide(14)"></span>
</div>

<style>
.slideshow-container {
  max-width: 800px;
  position: relative;
  margin: auto;
}
.slide {display: none;}
img, video {border-radius: 10px;}
.prev, .next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  margin-top: -22px;
  padding: 16px;
  color: black;
  font-weight: bold;
  font-size: 18px;
  transition: 0.3s ease;
  border-radius: 0 3px 3px 0;
  user-select: none;
}
.next {right: 0;border-radius: 3px 0 0 3px;}
.prev:hover, .next:hover {
  background-color: rgba(0,0,0,0.05);
  color: black;
}
.caption {
  color: black;
  font-size: 16px;
  padding: 8px 12px;
  text-align: center;
}
.dot {
  cursor: pointer;
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: #ccc;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}
.active, .dot:hover {background-color: #555;}
.fade {
  animation-name: fade;
  animation-duration: 1.2s;
}
@keyframes fade {
  from {opacity: .4} 
  to {opacity: 1}
}
</style>

<script>
let slideIndex = 1;
showSlides(slideIndex);

function plusSlides(n) { showSlides(slideIndex += n); }
function currentSlide(n) { showSlides(slideIndex = n); }

function showSlides(n) {
  let i;
  let slides = document.getElementsByClassName("slide");
  let dots = document.getElementsByClassName("dot");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";  
  }
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";  
  dots[slideIndex-1].className += " active";
}
</script>
