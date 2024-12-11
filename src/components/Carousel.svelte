<script>
    let images = [
      '/images/Dandadan.png',
      '/images/MARVEL_universe.png',
      '/images/X-men.png',
      '/images/One_Piece.png',
    ];
    let current = 0;
  
    function next() {
      current = (current + 1) % images.length;
    }
  
    function prev() {
      current = (current - 1 + images.length) % images.length;
    }
  </script>
  
  <style>
    .carousel {
      position: relative;
      width: 80%;
      max-width: 800px;
      margin: 20px auto;
      overflow: hidden;
      border: 2px solid black;
    }
  
    .image-container {
      display: flex;
      transition: transform 0.5s ease;
      transform: translateX(-{current * 100}%);
    }
  
    .image {
      width: 100%;
      flex-shrink: 0;
    }
  
    .button {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      background: black;
      color: white;
      border: none;
      cursor: pointer;
      padding: 10px;
    }
  
    .prev {
      left: 10px;
    }
  
    .next {
      right: 10px;
    }
  
    .dots {
      display: flex;
      justify-content: center;
      margin-top: 10px;
    }
  
    .dot {
      width: 10px;
      height: 10px;
      margin: 0 5px;
      background: gray;
      border-radius: 50%;
      cursor: pointer;
    }
  
    .dot.active {
      background: blue;
    }
  </style>
  
  <div class="carousel">
    <div class="image-container" style="transform: translateX(-{current * 100}%)">
      {#each images as img}
        <img class="image" src={img} alt="Imagen" />
      {/each}
    </div>
    <button class="button prev" on:click={prev}>&lt;</button>
    <button class="button next" on:click={next}>&gt;</button>
  </div>
  
  <div class="dots">
    {#each images as _, i}
      <div
        class="dot {current === i ? 'active' : ''}"
        on:click={() => (current = i)}
      ></div>
    {/each}
  </div>
  