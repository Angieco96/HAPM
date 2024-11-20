<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Descifrar Mensaje</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 50px;
      background-color: #f9f9f9;
    }
    input, button {
      margin: 10px;
      padding: 10px;
      font-size: 16px;
    }
    .result {
      margin-top: 20px;
      font-weight: bold;
      font-size: 18px;
    }
    .success {
      color: green;
    }
    .error {
      color: red;
    }
  </style>
</head>
<body>
  <h1>Descifrar Mensaje</h1>
  <p>Introduce la contraseña para acceder al mensaje:</p>
  <input type="password" id="password" placeholder="Contraseña">
  <br>
  <button onclick="checkPassword()">Validar</button>
  <div id="result" class="result"></div>

  <script>
    // Contraseña correcta
    const correctPassword = "mi_contraseña_segura"; // Cambia esto por tu contraseña

    function checkPassword() {
      const userPassword = document.getElementById("password").value;
      const resultDiv = document.getElementById("result");

      // Verificar la contraseña
      if (userPassword === correctPassword) {
        resultDiv.innerHTML = "¡Acceso concedido! Este es el mensaje descifrado: <b>Mensaje confidencial</b>";
        resultDiv.className = "result success";
      } else {
        resultDiv.innerHTML = "Contraseña incorrecta. Inténtalo de nuevo.";
        resultDiv.className = "result error";
      }
    }
  </script>
</body>
</html>
