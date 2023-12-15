<script>
  import { onMount, onDestroy } from 'svelte';

  let navbarOpacity = 1; // Initial opacity is 100%

  function updateOpacity() {
    const scrollY = window.scrollY;
    const maxScroll = 200; // Maximum scroll value to reach 40% opacity
    navbarOpacity = Math.max(0.7, 1 - scrollY / maxScroll);
  }

  let showReductions = false;
  let reductionsBox;

  function toggleReductions() {
    showReductions = !showReductions;
  }

  function handleClickOutside(event) {
    if (reductionsBox && !reductionsBox.contains(event.target)) {
      showReductions = false;
    }
  }

  onMount(() => {
    if (typeof window !== 'undefined') {
      window.addEventListener('scroll', updateOpacity);
      window.addEventListener('click', handleClickOutside);
    }
  });

  onDestroy(() => {
    if (typeof window !== 'undefined') {
      window.removeEventListener('scroll', updateOpacity);
      window.removeEventListener('click', handleClickOutside);
    }
  });


  let sus = 0;

function secretFunc() {
  sus += 1;
  if (sus >= 666) {
    window.location.replace('/sus');
    sus = 0;
  }
}
</script>

<div class="navbar bg-base-100 fixed top-0 left-0 w-full z-10" style="opacity: {navbarOpacity}">
  <div class="navbar-start">
    <div class="dropdown">
      <div tabindex="0" role="button" class="btn btn-ghost btn-circle">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h7" /></svg>
      </div>
      <ul tabindex="-1" class="menu menu-sm dropdown-content mt-3 z-[1] p-2 shadow bg-base-100 rounded-box w-52">
        <li><a href="/menu">Menù</a></li>
        <li><a href="/reservation">Prenotazione</a></li>
        <li><a href="/events">Eventi</a></li>
      </ul>
    </div>
  </div>
  <div class="navbar-center" on:click={secretFunc}>
    <a href="/" class="btn btn-ghost text-2xl">Forno D'oro</a>
  </div>
  <div class="navbar-end">
    <button class="btn btn-ghost btn-circle">
      <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" /></svg>
    </button>
    <button class="btn btn-ghost btn-circle" on:click|stopPropagation={toggleReductions}>
      <div class="indicator">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9" /></svg>
        <span class="badge badge-xs badge-primary indicator-item"></span>
      </div>
    </button>
  </div>
  {#if showReductions}
    <div bind:this={reductionsBox} class="absolute top-full right-0 mt-2 p-4 bg-gray-100 text-gray-800 border border-gray-300 rounded shadow-lg z-20">
        <p>Tutte le pizze tradizionali al -30%!</p>
    </div>
  {/if}
</div>
