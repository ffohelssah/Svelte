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
  
  <style lang="scss">
    /* Contenedor general del carrusel */
    .carousel-container {
      width: 100%;
      height: 400px; 
      position: relative;
      background-color: rgba(255, 255, 255, 0.9); /* Fondo blanco y ligeramente transparente */
      display: flex;
      flex-direction: column; /* Alinea todo de arriba hacia abajo */
      justify-content: center; /* Centra el contenido verticalmente */
      align-items: center; /* Centra el contenido horizontalmente */
    }
  
    /* Contenedor para la imagen y los botones */
    .image-container {
      width: 80%;
      height: 80%; /* La imagen ocupará un 80% del alto del carrusel */
      display: flex;
      flex-direction: column; /* Coloca los botones y los círculos debajo de la imagen */
      justify-content: center; /* Centra la imagen verticalmente */
      align-items: center; /* Centra los botones y círculos debajo de la imagen */
      position: relative;
      overflow: hidden;
    }
  
    .image {
      max-width: 100%; /* La imagen no se desborda en el ancho */
      max-height: 80%; /* La imagen se ajusta al alto disponible */
      object-fit: contain; /* Mantiene la proporción sin distorsionar */
    }
  
    /* Estilo para los botones de navegación debajo de la imagen */
    .buttons-container {
      display: flex;
      justify-content: space-between; /* Espacio entre los botones */
      width: 100%;
      padding: 10px 0; /* Separación vertical entre imagen y botones */
    }
  
    .button {
      background-color: rgba(0, 0, 0, 0.5);
      color: white;
      border: none;
      padding: 10px;
      cursor: pointer;
      border-radius: 50%;
      font-size: 20px;
      width: 40px;
      height: 40px;
    }
  
    /* Estilo para los círculos dentro del contenedor blanco */
    .dots {
      display: flex;
      justify-content: center; /* Centra los círculos */
      margin-top: 10px;
      width: 100%;
      position: absolute; /* Permite posicionar los círculos debajo de la imagen */
      bottom: 10px; /* Los coloca 10px por encima del fondo */
    }
  
    .dot {
      width: 12px;
      height: 12px;
      margin: 0 5px;
      background-color: rgba(0, 0, 0, 0.3);
      border-radius: 50%;
      cursor: pointer;
      transition: background-color 0.3s, transform 0.3s;
    }
  
    .dot.active {
      background-color: #CC1E72;
      transform: scale(1.2); /* Efecto de escala para el dot activo */
    }
  
    /* Alineación de los botones de navegación a los lados */
    .prev, .next {
      position: absolute;
      top: 50%; /* Centramos los botones verticalmente */
      transform: translateY(-50%);
    }
  
    .prev {
      left: 10px; /* Botón izquierdo */
    }
  
    .next {
      right: 10px; /* Botón derecho */
    }
  </style>
  
  <!-- Contenedor principal del carrusel -->
  <div class="carousel-container">
    <!-- Caja para mostrar la imagen, los botones y los círculos -->
    <div class="image-container">
      <img class="image" src={images[current]} alt="Imagen" />
      
      <!-- Contenedor de los botones debajo de la imagen -->
      <div class="buttons-container">
        <button class="button prev" on:click={prev}>&lt;</button>
        <button class="button next" on:click={next}>&gt;</button>
      </div>
    </div>
  
    <!-- Círculos debajo de la imagen y dentro del contenedor blanco -->
    <div class="dots">
      {#each images as _, i}
        <button
          class="dot"
          class:active={current === i}
          on:click={() => (current = i)}
          on:keydown={(e) => e.key === 'Enter' && (current = i)} 
          tabindex="0" 
        ></button>
      {/each}
    </div>
  </div>
  