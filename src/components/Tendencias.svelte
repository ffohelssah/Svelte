<script>
    let comicImages = [
      '/images/Avengers_Portada.png',
      '/images/Spiderman_Marvel.png',
    ];
  </script>
  
  <style lang="scss">
    .tendencias {
      width: 100%;
    }
  
    .bar {
      background-color: black;
      color: white;
      padding: 10px 0;
      text-align: center;
    }
  
    .button-tendencias {
      background-color: #CC1E72;
      color: white;
      border: none;
      padding: 10px 20px;
      font-size: 16px;
      cursor: pointer;
      border-radius: 5px;
    }
  
    .content {
      background-color: white;
      display: flex;
      justify-content: space-between;
      padding: 20px;
    }
  
    .comic {
      width: 49%;
      border: 2px solid black;
    }
  
    .comic img {
      width: 100%;
      height: 100%;
    }
  </style>
  
  <div class="tendencias">
    
    <div class="bar">
      <button class="button-tendencias">Tendencias</button>
    </div>
    <div class="content">
      <div class="comic">
        <img src={comicImages[0]} alt="Comic 1" />
      </div>
      <div class="comic">
        <img src={comicImages[1]} alt="Comic 2" />
      </div>
    </div>
  </div>
  