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

<p class="text-left ...">So I started to walk into the water... Lorem ipsum dolor sit amet consectetur, adipisicing elit. Odit nihil magni quae, corporis vitae enim error atque eaque saepe at nemo voluptate explicabo dolorum, eligendi vel consequatur incidunt, ipsum omnis!</p>

<p class="font-bold text-center antialiased text-4xl"><br>La vie c'est comme une boite de chocolat, y'a des noirs</p>
<p><br></p>


<section class="relative isolate overflow-hidden bg-white px-6 py-24 sm:py-32 lg:px-8">
    <div class="absolute inset-0 -z-10 bg-[radial-gradient(45rem_50rem_at_top,theme(colors.indigo.100),white)] opacity-20"></div>
    <div class="absolute inset-y-0 right-1/2 -z-10 mr-16 w-[200%] origin-bottom-left skew-x-[-30deg] bg-white shadow-xl shadow-indigo-600/10 ring-1 ring-indigo-50 sm:mr-28 lg:mr-0 xl:mr-16 xl:origin-center"></div>
    <div class="mx-auto max-w-2xl lg:max-w-4xl">
      <img class="mx-auto h-12" src="https://tailwindui.com/img/logos/workcation-logo-indigo-600.svg" alt="">
      <figure class="mt-10">
        <blockquote class="text-center text-xl font-semibold leading-8 text-gray-900 sm:text-2xl sm:leading-9">
          <p>“Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo expedita voluptas culpa sapiente alias molestiae. Numquam corrupti in laborum sed rerum et corporis.”</p>
        </blockquote>
        <figcaption class="mt-10">
          <img class="mx-auto h-10 w-10 rounded-full" src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="">
          <div class="mt-4 flex items-center justify-center space-x-3 text-base">
            <div class="font-semibold text-gray-900">Judith Black</div>
            <svg viewBox="0 0 2 2" width="3" height="3" aria-hidden="true" class="fill-gray-900">
              <circle cx="1" cy="1" r="1" />
            </svg>
            <div class="text-gray-600">CEO of Workcation</div>
          </div>
        </figcaption>
      </figure>
    </div>
  </section>

  


<Footer />
<slot></slot>