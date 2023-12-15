<script>
    import { onMount, onDestroy } from 'svelte';
  
    let currentSlide = 1;
    const totalSlides = 4;
    let interval;
  
    onMount(() => {
      interval = setInterval(() => {
        currentSlide = currentSlide < totalSlides ? currentSlide + 1 : 1;
      }, 1000); // Change image every 1000ms (1 second)
    });
  
    onDestroy(() => {
      clearInterval(interval);
    });
  
    function isActiveSlide(slideNumber) {
      return currentSlide === slideNumber ? 1 : 0;
    }
  </script>
  
  <style>
    .carousel-item {
      transition: opacity 0.5s ease-in-out;
      opacity: 0;
    }
  </style>
  
  <div class="carousel w-full">
    <div id="slide1" class="carousel-item relative w-full" style:opacity={isActiveSlide(1)}>
      <img src="https://daisyui.com/images/stock/photo-1625726411847-8cbb60cc71e6.jpg" class="w-full" />
    </div>
    <div id="slide3" class="carousel-item relative w-full" style:opacity={isActiveSlide(1)}>
        <img src="https://daisyui.com/images/stock/photo-1625726411847-8cbb60cc71e6.jpg" class="w-full" />
    </div>
    <div id="slide2" class="carousel-item relative w-full" style:opacity={isActiveSlide(1)}>
        <img src="https://daisyui.com/images/stock/photo-1625726411847-8cbb60cc71e6.jpg" class="w-full" />
    </div>
    <!-- Repeat for other slides -->
  </div>
  