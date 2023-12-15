<script>
  import Navbar from "../../lib/Navbar.svelte";
  import Footer from "../../lib/Footer.svelte";
</script>

<Navbar />
<slot></slot>
<!-- pu500 or300 -->
<div class="relative bg-gradient-to-r from-white to-pink-100 overflow-hidden">
  <div class="flex flex-row justify-center items-center pt-20">
  <div class="rounded-full p-5 shadow-xl mt-10">
    <h1 class="text-5xl tracking-widest font-bold font-mono text-gray-600">MENÙ</h1>
  </div>
</div>

<div class="flex flex-col w-full bg-gray">
  <div class="divider"></div> 
</div>

<div class="flex flex-wrap justify-center pt-20 ">
  <div class="card w-96 bg-base-100 shadow-xl m-4">
    <div class="card-body">
      <h2 class="card-title">Margherita</h2>
      <p>Semplicità classica con mozzarella, basilico e salsa di pomodoro ricca</p>
    </div>
    <figure class="h-48 overflow-hidden">
      <img src="ai_pizzas_compressed/1.jpg" alt="Margherita" class="object-cover h-full w-full" />
    </figure>
  </div>



  <div class="card w-96 bg-base-100 shadow-xl m-4">
    <div class="card-body">
      <h2 class="card-title">Peperoni</h2>
      <p>Fette di peperoni piccanti incontrano formaggio filante su crosta aromatizzata.</p>
    </div>
    <figure class="h-48 overflow-hidden">
      <img src="ai_pizzas_compressed/2.jpg" alt="Peperoni" class="object-cover h-full w-full" />
    </figure>
  </div>



  <div class="card w-96 bg-base-100 shadow-xl m-4">
    <div class="card-body">
      <h2 class="card-title">Quattro Formaggi</h2>
      <p>Melodia di quattro formaggi: mozzarella, gorgonzola, parmigiano e fontina.</p>
    </div>
    <figure class="h-48 overflow-hidden">
      <img src="ai_pizzas_compressed/3.jpg" alt="Quattro Formaggi" class="object-cover h-full w-full" />
    </figure>
  </div>



  <div class="card w-96 bg-base-100 shadow-xl m-4">
    <div class="card-body">
      <h2 class="card-title">Vegetariana</h2>
      <p>Medley colorato di verdure su base di formaggio e pomodoro.</p>
    </div>
    <figure class="h-48 overflow-hidden">
      <img src="ai_pizzas_compressed/4.jpg" alt="Vegetariana" class="object-cover h-full w-full" />
    </figure>
  </div>



  <div class="card w-96 bg-base-100 shadow-xl m-4">
    <div class="card-body">
      <h2 class="card-title">Hawaiana
        <div class="badge badge-secondary">NUOVO</div>
      </h2>
      <p>Tocco tropicale con ananas succoso e prosciutto su mozzarella.</p>
    </div>
    <figure class="h-48 overflow-hidden">
      <img src="ai_pizzas_compressed/5.jpg" alt="Hawaiana" class="object-cover h-full w-full" />
    </figure>
  </div>




  <div class="card w-96 bg-base-100 shadow-xl m-4">
    <div class="card-body">
      <h2 class="card-title">Capricciosa</h2>
      <p>Carciofi, prosciutto, funghi, olive nere su mozzarella e salsa di pomodoro.</p>
    </div>
    <figure class="h-48 overflow-hidden">
      <img src="ai_pizzas_compressed/6.jpg" alt="Capricciosa" class="object-cover h-full w-full" />
    </figure>
  </div>


  <div class="card w-96 bg-base-100 shadow-xl m-4">
    <div class="card-body">
      <h2 class="card-title">Calzone</h2>
      <p>Calzone ripieno di ricotta, mozzarella, prosciutto e funghi su crosta dorata.</p>
    </div>
    <figure class="h-48 overflow-hidden">
      <img src="ai_pizzas_compressed/7.jpg" alt="Calzone" class="object-cover h-full w-full" />
    </figure>
  </div>


  <div class="card w-96 bg-base-100 shadow-xl m-4">
    <div class="card-body">
      <h2 class="card-title">Diavola</h2>
      <p>Salame piccante, mozzarella e salsa di pomodoro ardente, crosta croccante.</p>
    </div>
    <figure class="h-48 overflow-hidden">
      <img src="ai_pizzas_compressed/8.jpg" alt="Diavola" class="object-cover h-full w-full" />
    </figure>
  </div>


  <div class="card w-96 bg-base-100 shadow-xl m-4">
    <div class="card-body">
      <h2 class="card-title">Siciliana</h2>
      <p>Crusta spessa, soffice, forma quadrata, salsa, cipolle, acciughe, erbe aromatiche.</p>
    </div>
    <figure class="h-48 overflow-hidden">
      <img src="ai_pizzas_compressed/9.jpg" alt="Siciliana" class="object-cover h-full w-full" />
    </figure>
  </div>

  <div class="card w-96 bg-base-100 shadow-xl m-4 mb-20">
    <div class="card-body">
      <h2 class="card-title">Prosciutto e Funghi</h2>
      <p>Prosciutto sottile, funghi terrosi, mozzarella, salsa di pomodoro, crosta sottile.</p>
    </div>
    <figure class="h-48 overflow-hidden">
      <img src="ai_pizzas_compressed/10.jpg" alt="Prosciutto e Funghi" class="object-cover h-full w-full" />
    </figure>
  </div>









</div>
</div>








<Footer />
<slot></slot>
