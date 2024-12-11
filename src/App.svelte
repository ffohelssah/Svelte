<script>
	import Navbar from './components/Navbar.svelte';
	import SearchBar from './components/SearchBar.svelte';
	import Carousel from './components/Carousel.svelte';
	import Footer from './components/Footer.svelte';
  
	let background = '/images/Deadpool-Galactus-marvel-space-stars.png';
  </script>
  
  <style>
	body {
	  margin: 0;
	  padding: 0;
	  background: url({background}) no-repeat center center fixed;
	  background-size: cover;
	  font-family: Arial, sans-serif;
	}
  
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
	<Footer />
  </div>
  