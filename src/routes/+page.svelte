<script>
    import Navbar from '../lib/Navbar.svelte';
    import Footer from '../lib/Footer.svelte';



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
          Pizza, Tradizione, Natale!
        </p>
    </div>
</div>

<div class="flex flex-col w-full bg-grey">
    <div class="divider"></div> 
</div>

<div class="bg-white flex justify-center items-center h-32">
  <h1 class="text-gray-700 text-center hover:text-sky-400 underline rounded underline-offset-7 text-4xl font-sans subpixel-antialiased tracking-widest font-extrabold">Le origini del Forno d'Oro</h1>
</div>


<div class="flex flex-row bg-white">
  <!-- Left side div -->
  <div class="flex justify-center items-center w-1/2 pt-11 pb-10">
    <img src="/pizzas/2.jpg" alt="" class="object-cover max-w-md max-h-full rounded-lg">
  </div>
  <!-- Right side div -->
  <div class="flex items-center w-1/2 p-8">
    <div class="text-gray-600 font-bold text-xl p-6 rounded-lg shadow-lg">
      <p>
        Forno d'Oro, una gemma nel cuore dell'Italia, esalta la tradizione secolare della pizza napoletana. Fondato nel 1990 da Luca Bianchi, un vero maestro pizzaiolo, il ristorante è rinomato per le sue pizze autentiche cotte in forno a legna e gli ingredienti locali freschi e di alta qualità. Un luogo dove il gusto incontra la tradizione in ogni morso.
      </p>
    </div>
  </div>
</div>



<div class="flex flex-col w-full bg-white">
  <div class="divider"></div> 
</div>


<section class="relative isolate overflow-hidden bg-white px-6 py-24 sm:py-20 lg:px-8">
    <div class="absolute inset-0 -z-10 bg-[radial-gradient(45rem_50rem_at_top,theme(colors.indigo.100),white)] opacity-20"></div>
    <div class="absolute inset-y-0 right-1/2 -z-10 mr-16 w-[200%] origin-bottom-left skew-x-[-30deg] bg-white shadow-xl shadow-indigo-600/10 ring-1 ring-indigo-50 sm:mr-28 lg:mr-0 xl:mr-16 xl:origin-center"></div>
    <div class="mx-auto max-w-2xl lg:max-w-4xl">
      <figure class="mt-10">
        <blockquote class="text-center text-xl font-semibold leading-8 text-gray-900 sm:text-2xl sm:leading-9">
          <p>“Da appassionato di cucina italiana, la visita a Forno D'oro è stata un'esperienza indimenticabile! La pizza, un vero capolavoro, ricca di sapori autentici e cotta alla perfezione. Ambiente accogliente e personale cordiale hanno reso la serata speciale. Complimenti!”</p>
        </blockquote>
        <figcaption class="mt-10">
          <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"><img class="mx-auto h-10 w-10 rounded-full" src="review-alessandro.jpg" alt="alessandro img"></a>
          <div class="mt-4 flex items-center justify-center space-x-3 text-base">
            <div class="font-semibold text-gray-900">Alessandro Bianchi</div>
            <svg viewBox="0 0 2 2" width="3" height="3" aria-hidden="true" class="fill-gray-900">
              <circle cx="1" cy="1" r="1" />
            </svg>
            <div class="text-gray-600">Chef Stellato</div>
          </div>
        </figcaption>
      </figure>
    </div>
  </section>


<Footer />
<slot></slot>