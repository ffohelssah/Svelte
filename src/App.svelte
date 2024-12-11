<script>
	import Navbar from './components/Navbar.svelte';
	import SearchBar from './components/SearchBar.svelte';
	import Carousel from './components/Carousel.svelte';
	import Footer from './components/Footer.svelte';
	import Tendencias from './components/Tendencias.svelte';
  
  </script>
  
  <style>
	.main-container {
	  display: flex;
	  flex-direction: column;
	  align-items: center;
	}
  </style>
  
  <div class="main-container">
	<SearchBar />
	<Navbar />
	<Carousel />
	<Tendencias />
	<Footer />
	
  </div>
  