<style>
    .navbar {
      width: 100%;
      height:50px;
      display: flex;
      justify-content: center;
      background-color: black;
      padding: 10px 0;
    }
  
    .nav-button {
      color: white;
      background: #CC1E72;
      padding: 5px 15px;
      text-transform: uppercase;
      cursor: pointer;
      border: none;
    }

    .navbar button:first-child {
    border-top-left-radius: 5px;
    border-bottom-left-radius: 5px;
  }

    .navbar button:last-child {
    border-top-right-radius: 5px;
    border-bottom-right-radius: 5px;
  }
  </style>
  
  <div class="navbar">
    <button class="nav-button">Inicio</button>
    <button class="nav-button">Cómics</button>
    <button class="nav-button">Manga</button>
    <button class="nav-button">Novedades</button>
    <button class="nav-button">Intercambio</button>
  </div>
  