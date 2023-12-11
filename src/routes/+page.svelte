<script>
    import Navbar from '../lib/Navbar.svelte';
    import Footer from '../lib/Footer.svelte';
    import HomepageCarousel1 from '../lib/HomepageCarousel1.svelte';
</script>

<Navbar />
<slot></slot>

<div class="video-background">
    <video autoplay loop muted>
        <source src="christmas-video.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
    <!-- Your content goes here -->
    <div class="content absolute inset-0 flex justify-center items-center" style="transform: translateY(-15%);">
        <p class="text-white text-6xl font-bold bg-opacity-50 bg-black p-4 rounded">
            THIS IS CONTENT
        </p>
    </div>
</div>

<div class="flex flex-col w-full">
    <div class="divider"></div> 
  </div>

<HomepageCarousel1 />
<slot></slot>

<p><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br></p>



<Footer />
<slot></slot>