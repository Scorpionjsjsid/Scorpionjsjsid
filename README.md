<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Menu de Aplicativos</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.2.0/css/all.min.css">
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(to bottom, #DCDCDC, #D3D3D3);
      background-size: cover;
      overflow-x: hidden;
    }

    .container {
      max-width: 1000px;
      margin: 0 auto;
      padding: 20px;
    }

    .profile-container {
      text-align: center;
      margin-bottom: 20px;
    }

    .profile-container img {
      border-radius: 50%;
      width: 100px;
      height: 100px;
      object-fit: cover;
      margin-bottom: 10px;
      transition: transform 0.3s ease;
      cursor: pointer;
    }

    .profile-container img:hover {
      transform: scale(1.1);
    }

    .profile-container h2 {
      margin: 0;
    }

    h1, h2 {
      text-align: center;
      margin-bottom: 20px;
      color: #333;
    }

    .app-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      justify-content: center;
    }

    .app-icon {
      background-color: #FFFFFF;
      border-radius: 15px;
      padding: 20px;
      text-align: center;
      width: 100px;
      height: 100px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      opacity: 0;
      transform: translateY(20px);
      animation: fadeInUp 0.6s forwards;
    }

    .app-icon:nth-child(1) { animation-delay: 0.1s; }
    .app-icon:nth-child(2) { animation-delay: 0.2s; }
    .app-icon:nth-child(3) { animation-delay: 0.3s; }
    .app-icon:nth-child(4) { animation-delay: 0.4s; }
    .app-icon:nth-child(5) { animation-delay: 0.5s; }
    .app-icon:nth-child(6) { animation-delay: 0.6s; }
    .app-icon:nth-child(7) { animation-delay: 0.7s; }
    .app-icon:nth-child(8) { animation-delay: 0.8s; }
    .app-icon:nth-child(9) { animation-delay: 0.9s; }
    .app-icon:nth-child(10) { animation-delay: 1.0s; }
    .app-icon:nth-child(11) { animation-delay: 1.1s; }
    .app-icon:nth-child(12) { animation-delay: 1.2s; }
    
    @keyframes fadeInUp {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .app-icon:hover {
      transform: scale(1.1);
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
    }

    .app-icon i {
      font-size: 36px;
      color: #1C1C1C;
      transition: color 0.3s ease;
    }

    .app-icon:hover i {
      color: #007BFF;
    }

    .app-icon p {
      margin: 5px 0 0;
      font-size: 12px;
      color: #666;
    }

    .app-icon a {
      text-decoration: none;
      color: inherit;
    }

    @media (min-width: 768px) {
      .app-icon {
        width: 120px;
        height: 120px;
      }
    }

    @media (min-width: 1024px) {
      .app-icon {
        width: 150px;
        height: 150px;
      }
    }

    /* Estilos para o Navbar inspirado na Twitch mobile */
    .navbar {
      display: flex;
      justify-content: space-around;
      padding: 10px;
      background-color: #18181b;
      position: fixed;
      bottom: 0;
      width: 100%;
      box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.5);
    }

    .navbar-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      color: #fff;
      cursor: pointer;
      flex: 1;
    }

    .navbar-item i {
      font-size: 24px;
      margin-bottom: 5px;
    }

    .navbar-item span {
      font-size: 12px;
    }

    .online-list {
      display: none;
      position: absolute;
      bottom: 60px;
      right: 10px;
      background-color: #333;
      border-radius: 10px;
      padding: 10px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
      z-index: 1000;
      max-width: 200px;
    }

    .online-list.active {
      display: block;
    }

    .friend {
      display: flex;
      align-items: center;
      margin-bottom: 10px;
    }

    .friend-avatar {
      width: 30px;
      height: 30px;
      border-radius: 50%;
      margin-right: 10px;
    }

    .friend:last-child {
      margin-bottom: 0;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="profile-container">
      <img id="profile-pic" src="https://via.placeholder.com/100" alt="Foto do perfil" onclick="changeProfilePic()">
      <input type="file" id="fileInput" style="display: none;" accept="image/*">
    </div>

    <h2>APP ESSENCIAIS</h2>
    <div class="app-grid">
      <div class="app-icon">
        <a href="https://md8vrt.csb.app/">
          <i class="fa-solid fa-house"></i>
          <p>APP ADAGIO</p>
        </a>
      </div>
      <div class="app-icon">
        <a href="https://contacts.google.com/">
          <i class="fa-solid fa-address-book"></i>
          <p>CONTATOS</p>
        </a>
      </div>
      <div class="app-icon">
        <a href="https://photos.google.com/">
          <i class="fa-solid fa-photo-film"></i>
          <p>GALERIA</p>
        </a>
      </div>
      <div class="app-icon">
        <a href="https://news.google.com/foryou?hl=pt-BR&gl=BR&ceid=BR:pt-419">
          <i class="fa-solid fa-newspaper"></i>
          <p>NOTICIAS</p>
        </a>
      </div>  
      <div class="app-icon">
        <a href="https://www.msn.com/pt-br/clima/forecast/in-S%C3%A3o-Paulo,Brasil?loc=eyJsIjoiU8OjbyBQYXVsbyIsInIiOiJTw6NvIFBhdWxvIiwiYyI6IkJyYXNpbCIsImkiOiJCUiIsImciOiJwdC1iciIsIngiOiItNDYuNjM0OTYzOTg5MjU3ODEiLCJ5IjoiLTIzLjUyMzI1ODIwOTIyODUxNiJ9&weadegreetype=C&ocid=hpmsn&cvid=bda29d892f774ff4bbcd9f375f53f574&ocid=hpmsn&ei=12">
          <i class="fa-solid fa-cloud"></i>
          <p>CLIMA</p>
        </a>
      </div>
      <div class="app-icon">
        <a href="https://www.google.com/maps">
          <i class="fa-solid fa-map"></i>
          <p>MAPS</p>
        </a>
      </div>  
      <div class="app-icon">
        <a href="https://account.microsoft.com/account/privacy?fref=home.drawers.privacy.privacy-dashboard&refd=beacons.ai">
          <i class="fa-solid fa-user-shield"></i>
          <p>PRIVACIDADE</p>
        </a>
      </div>  
      <div class="app-icon">
        <a href="https://account.microsoft.com/security?fref=home.drawers.security.security-dashboard&refd=beacons.ai">
          <i class="fa-solid fa-shield-halved"></i>
          <p>SEGURANÇA</p>
        </a>
      </div>  
      <div class="app-icon">
        <a href="https://one.google.com/?utm_source=app_launcher&utm_medium=web&utm_campaign=all&utm_content=google_oo&g1_landing_page=1">
          <i class="fa-duotone fa-solid fa-database"></i>
          <p>MEMORIA</p>
        </a>
      </div> 
    </div>
    <h2>ADAGIO OFFICE</h2>
    <div class="app-grid">
      <div class="app-icon">
        <a href="https://xff9wt.csb.app/">
          <i class="fa-sharp-duotone fa-solid fa-calendar-days"></i>
          <p>CALENDARIO</p>
        </a>
      </div>  
      <div class="app-icon">
        <a href="https://44z98z.csb.app/">
          <i class="fa-duotone fa-solid fa-image"></i>
          <p>EDITOR FOTOS</p>
        </a>
      </div>  
      <div class="app-icon">
        <a href="https://3gwd2z.csb.app/">
          <i class="fa-solid fa-lightbulb"></i>
          <p>ANOTAÇÕES</p>
        </a>
      </div>  
      <div class="app-icon">
        <a href="https://yly2pk.csb.app/">
          <i class="fa-solid fa-calculator"></i>
          <p>CALCULADORA</p>
        </a>
      </div>  
    </div>
  </div>

  <div class="navbar">
    <div class="navbar-item">
      <i class="fas fa-home"></i>
      <span>Homepage</span>
    </div>
    <div class="navbar-item">
      <i class="fas fa-search"></i>
      <span>Search</span>
    </div>
    <div class="navbar-item" onclick="toggleOnlineList()">
      <i class="fas fa-users"></i>
      <span>Friends</span>
      <div class="online-list" id="onlineList">
        <div class="friend">
          <img class="friend-avatar" src="https://via.placeholder.com/30" alt="Friend 1">
          <span>Friend 1</span>
        </div>
        <div class="friend">
          <img class="friend-avatar" src="https://via.placeholder.com/30" alt="Friend 2">
          <span>Friend 2</span>
        </div>
      </div>
    </div>
    <div class="navbar-item">
      <i class="fa-solid fa-store"></i>
      <span>Store</span>
    </div>
  </div>

  <script>
    const fileInput = document.getElementById('fileInput');
    const profilePic = document.getElementById('profile-pic');

    // Carregar foto de perfil do localStorage
    window.addEventListener('load', () => {
      const savedProfilePic = localStorage.getItem('profilePic');
      if (savedProfilePic) {
        profilePic.src = savedProfilePic;
      }
    });

    function changeProfilePic() {
      fileInput.click();
    }

    fileInput.addEventListener('change', (event) => {
      const file = event.target.files[0];
      if (file) {
        const reader = new FileReader();
        reader.onload = function(e) {
          profilePic.src = e.target.result;
          // Salvar a foto de perfil no localStorage
          localStorage.setItem('profilePic', e.target.result);
        }
        reader.readAsDataURL(file);
      }
    });

    function toggleOnlineList() {
      const onlineList = document.getElementById('onlineList');
      onlineList.classList.toggle('active');
    }
  </script>
</body>
</html>
