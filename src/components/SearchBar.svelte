<script>
    let logo = '/images/Logo.png'; 
  </script>
  
  <style>
    .search-bar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      width: 100%;
      padding: 10px;
      
    }
  
    .logo {
      width: 100px;
    }
  
    .search-input {
      flex-grow: 1;
      margin: 0 20px;
    }
  
    .buttons {
      display: flex;
      gap: 10px;
    }
  
    .button {
      display: flex;
      align-items: center;
      background: #CC1E72;
      color: white;
      padding: 5px 10px;
      border: none;
      cursor: pointer;
      border-radius: 5px;
    }
  </style>
  
  <div class="search-bar">
    <img class="logo" src={logo} alt="Logo" />
    <input class="search-input" type="text" placeholder="Buscar..." />
    <div class="buttons">
      <button class="button">Mi Cuenta</button>
      <button class="button">Mi Carro</button>
    </div>
  </div>
  