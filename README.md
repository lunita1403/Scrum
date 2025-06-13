<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Search Movies - Login</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }
    body {
      height: 100vh;
      background: linear-gradient(to bottom, #ffffff, #d2691e);
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
    }
    .logo-container {
      position: absolute;
      top: 20px;
      left: 20px;
      display: flex;
      align-items: center;
    }
    .logo-container img {
      height: 60px;
      margin-right: 10px;
    }
    .logo-container span {
      font-size: 26px;
      font-weight: 600;
      color: #8B4513;
    }
    .container {
      width: 400px;
      height: 450px;
      position: relative;
      perspective: 1200px;
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .form-box {
      width: 100%;
      height: 100%;
      position: relative;
      transform-style: preserve-3d;
      transition: transform 0.8s ease-in-out;
    }
    .form-box.show-register {
      transform: rotateY(180deg);
    }
    .form-panel {
      position: absolute;
      width: 100%;
      height: 100%;
      background: rgba(255, 255, 255, 0.15);
      backdrop-filter: blur(20px);
      border-radius: 20px;
      padding: 35px;
      box-shadow: 0 8px 30px rgba(0,0,0,0.1);
      backface-visibility: hidden;
      display: flex;
      flex-direction: column;
      justify-content: center;
      transform-style: preserve-3d;
    }
    .form-panel h2 {
      text-align: center;
      color: #8B4513;
      margin-bottom: 25px;
      font-weight: 600;
    }
    .form-panel input {
      padding: 12px 14px;
      margin-bottom: 15px;
      border: 1px solid #8B4513;
      border-radius: 10px;
      background-color: rgba(255, 255, 255, 0.6);
      outline: none;
      font-size: 14px;
      transition: all 0.3s ease;
    }
    .form-panel input:focus {
      border-color: #d2691e;
      background-color: #fff;
    }
    .form-panel button {
      background: transparent;
      border: 2px solid #d2691e;
      color: #8B4513;
      padding: 12px;
      border-radius: 10px;
      font-weight: 500;
      cursor: pointer;
      transition: background 0.3s ease;
    }
    .form-panel button:hover {
      background-color: #d2691e1a;
    }
    .toggle-link {
      text-align: center;
      margin-top: 15px;
    }
    .toggle-link a {
      text-decoration: none;
      color: #8B4513;
      font-weight: bold;
      font-size: 14px;
      border-bottom: 1px dashed #8B4513;
      transition: color 0.3s ease;
    }
    .toggle-link a:hover {
      color: #d2691e;
    }
    .register-panel {
      transform: rotateY(180deg);
    }
  </style>
</head>
<body>

  <div class="logo-container">
    <img src="searchmovies.png" alt="Search Movies Logo">
    <span>Search Movies</span>
  </div>

  <div class="container">
    <div class="form-box" id="formBox">
      <!-- Login Panel -->
      <div class="form-panel login-panel">
        <h2>Iniciar Sesión</h2>
        <form><center>
          <input type="email" placeholder="Correo electrónico" required>
          <input type="password" placeholder="Contraseña" required>
          <button type="submit">Ingresar</button></center>
        </form>
        <div class="toggle-link">
          <p>¿No tienes cuenta? <a href="#" onclick="toggleForm()">Regístrate aquí</a></p>
        </div>
      </div>

      <!-- Register Panel -->
      <div class="form-panel register-panel">
        <h2>Crear Cuenta</h2>
        <form><center>
          <input type="text" placeholder="Nombre completo" required>
          <input type="email" placeholder="Correo electrónico" required>
          <input type="password" placeholder="Contraseña" required>
          <button type="submit">Registrarse</button></center>
        </form>
        <div class="toggle-link">
          <p>¿Ya tienes cuenta? <a href="#" onclick="toggleForm()">Inicia sesión</a></p>
        </div>
      </div>
    </div>
  </div>

  <script>
    function toggleForm() {
      document.getElementById('formBox').classList.toggle('show-register');
    }
  </script>

</body>
</html>
