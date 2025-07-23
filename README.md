<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cuidemos el Río Piura</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f4f9f4;
      color: #333;
    }
    header {
      background-color: #1b5e20;
      color: white;
      padding: 20px;
      text-align: center;
    }
    nav {
      background-color: #2e7d32;
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      padding: 10px;
    }
    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
    }
    section {
      padding: 20px;
    }
    .hero {
      background-image: url('https://upload.wikimedia.org/wikipedia/commons/2/25/Rio_Piura.jpg');
      background-size: cover;
      background-position: center;
      height: 300px;
      display: flex;
      justify-content: center;
      align-items: center;
      color: white;
      font-size: 2rem;
      font-weight: bold;
      text-shadow: 2px 2px 5px #000;
      text-align: center;
      padding: 0 10px;
    }
    .card {
      background-color: white;
      padding: 15px;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      margin-bottom: 20px;
      transition: transform 0.3s ease;
    }
    .card:hover {
      transform: scale(1.02);
    }
    footer {
      background-color: #1b5e20;
      color: white;
      text-align: center;
      padding: 15px;
    }
    .question {
      margin-bottom: 10px;
    }
    .question label {
      display: block;
      margin-bottom: 5px;
    }
    button {
      background-color: #2e7d32;
      color: white;
      border: none;
      padding: 10px 20px;
      cursor: pointer;
      border-radius: 5px;
      font-weight: bold;
      transition: background-color 0.3s ease;
      margin: 5px;
    }
    button:hover {
      background-color: #66bb6a;
    }
    .impact-img {
      width: 100%;
      max-width: 600px;
      border-radius: 10px;
      margin-top: 10px;
    }
    .qr {
      text-align: center;
      padding: 30px;
    }
    .qr img {
      width: 150px;
      height: auto;
    }
  </style>
</head>
<body>
  <header>
    <h1>Cuidemos el Río Piura</h1>
    <p>Educación interactiva para una conciencia ambiental activa</p>
  </header>

  <nav>
    <a href="#inicio">Inicio</a>
    <a href="#aprende">Aprende</a>
    <a href="#juega">Juega</a>
    <a href="#evalua">Evalúate</a>
    <a href="#impacto">Impacto Local</a>
    <a href="#contacto">Contáctanos</a>
    <a href="#mas-info">+ Información</a>
  </nav>

  <div class="hero" id="inicio">
    Tu acción transforma el río. Aprende, participa y cuida.
  </div>

  <section id="aprende">
    <div class="card">
      <h2>¿Qué está pasando con el río Piura?</h2>
      <p>El río Piura sufre por la acumulación de basura y aguas contaminadas. Aprende cómo afecta esto a tu comunidad y al medio ambiente.</p>
    </div>
    <div class="card">
      <h2>Causas y consecuencias</h2>
      <p>Descubre las <a href="https://es.scribd.com/document/232529739/Contaminacion-Del-Rio-Piura" target="_blank" style="color:#2e7d32; font-weight:bold;">causas humanas y naturales</a> de la contaminación, y sus consecuencias en la salud y la biodiversidad.</p>
    </div>
  </section>

  <section id="juega">
    <div class="card">
      <h2>Juega y Participa</h2>

      <p><strong>Juego 1: ¿Qué acción es correcta?</strong></p>
      <img src="https://cdn-icons-png.flaticon.com/512/1254/1254721.png" alt="Basura" width="100">
      <br>
      <button onclick="juego1(true)">Tirar la basura en el río</button>
      <button onclick="juego1(false)">Llevar la basura a un tacho</button>
      <p id="juego1resultado"></p>
      <hr>

      <p><strong>Juego 2: ¿Orgánico o Inorgánico?</strong></p>
      <img src="https://cdn-icons-png.flaticon.com/512/590/590685.png" alt="Cáscara de plátano" width="100">
      <br>
      <button onclick="juego2('inorganico')">Inorgánico</button>
      <button onclick="juego2('organico')">Orgánico</button>
      <p id="juego2resultado"></p>

      <hr>
      <p><strong>Juego 3: ¿Qué objeto contamina más?</strong></p>
      <button onclick="alert('Correcto. Las pilas contienen metales pesados muy contaminantes.')">Pilas</button>
      <button onclick="alert('Incorrecto. El papel se degrada rápidamente.')">Papel</button>
    </div>
  </section>

  <section id="evalua">
    <div class="card">
      <h2>Evalúa tu conciencia ambiental</h2>
      <form id="quizForm">
        <div class="question">
          <label>1. ¿Tiras la basura en su lugar?</label>
          <select name="q1">
            <option value="">Selecciona una respuesta</option>
            <option value="2">Siempre</option>
            <option value="1">A veces</option>
            <option value="0">Nunca</option>
          </select>
        </div>
        <div class="question">
          <label>2. ¿Has participado en alguna campaña ambiental?</label>
          <select name="q2">
            <option value="">Selecciona una respuesta</option>
            <option value="2">Sí</option>
            <option value="1">Solo una vez</option>
            <option value="0">No</option>
          </select>
        </div>
        <div class="question">
          <label>3. ¿Conoces las causas de la contaminación del río Piura?</label>
          <select name="q3">
            <option value="">Selecciona una respuesta</option>
            <option value="2">Sí</option>
            <option value="1">Un poco</option>
            <option value="0">No</option>
          </select>
        </div>
        <button type="button" onclick="calcularResultado()">Enviar respuestas</button>
        <p id="resultado"></p>
      </form>
    </div>
  </section>

  <section id="impacto">
    <div class="card">
      <h2>Impacto Local</h2>
      <p>En el distrito 26 de Octubre se organizan campañas de limpieza, talleres escolares y jornadas de reciclaje.</p>
      <img src="https://eltiempo.pe/wp-content/uploads/2021/09/campan%CC%83a-limpieza-rio-piura.jpg" alt="Campaña de limpieza" class="impact-img">
      <p>¡Tú también puedes ser parte! Participa, comparte y cuida.</p>
    </div>
  </section>

  <section id="contacto">
    <div class="card">
      <h2>Contáctanos</h2>
      <p>¿Tienes dudas o quieres compartir tus acciones ambientales? Escríbenos.</p>
      <p><strong>Email:</strong> <a href="mailto:salvandoelmundo.jb@gmail.com">salvandoelmundo.jb@gmail.com</a></p>
    </div>
  </section>

  <section id="mas-info" style="text-align: center; padding: 40px; background-color: #f1f8e9;">
    <h2 style="color: #2e7d32;">¿Quieres aprender más sobre el medio ambiente?</h2>
    <p style="font-size: 18px;">Haz clic en el botón de abajo para acceder a información confiable de las Naciones Unidas.</p>
    <a href="https://www.un.org/es/climatechange/what-is-climate-change" target="_blank" style="
      display: inline-block;
      padding: 14px 28px;
      background-color: #388e3c;
      color: white;
      font-size: 16px;
      text-decoration: none;
      border-radius: 8px;
      font-weight: bold;
      margin-top: 10px;
    ">Ir a la información oficial 🌱</a>
  </section>

  <div class="qr">
    <h3>Escanea el código QR para visitar esta página desde tu celular:</h3>
    <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://www.un.org/es/climatechange/what-is-climate-change" alt="QR Medio Ambiente">
  </div>

  <footer>
    &copy; 2025 Cuidemos el Río Piura - Proyecto Escolar de Ciencia y Tecnología
  </footer>

  <!-- Audios -->
  <audio id="correcto" src="https://www.soundjay.com/buttons/sounds/button-3.mp3" preload="auto"></audio>
  <audio id="incorrecto" src="https://www.soundjay.com/buttons/sounds/button-10.mp3" preload="auto"></audio>

  <script>
    function calcularResultado() {
      const form = document.getElementById("quizForm");
      const respuestas = ["q1", "q2", "q3"];
      let total = 0;
      let completado = true;

      respuestas.forEach(id => {
        const val = parseInt(form[id].value);
        if (isNaN(val)) {
          completado = false;
        } else {
          total += val;
        }
      });

      const resultado = document.getElementById("resultado");
      if (!completado) {
        resultado.textContent = "Por favor, responde todas las preguntas.";
      } else {
        let mensaje = "";
        if (total >= 5) {
          mensaje = "¡Excelente! Tienes una conciencia ambiental muy alta, TUS CONOCIMIENTOS LOS PUEDES COMPARTIR, contactate con nosotros para se parte de una campaña";
        } else if (total >= 3) {
          mensaje = "Bien. Pero aún puedes mejorar tu conciencia ambiental.";
        } else {
          mensaje = "Necesitas aprender más sobre cómo cuidar el medio ambiente.";
        }  resultado.textContent = mensaje;}
    }

    function juego1(eleccionIncorrecta) {
      const resultado = document.getElementById("juego1resultado");
      const correctoAudio = document.getElementById("correcto");
      const incorrectoAudio = document.getElementById("incorrecto");

      if (eleccionIncorrecta) {
        resultado.textContent = "❌ Incorrecto. Esa acción contamina el río.";
        incorrectoAudio.play();
      } else {
        resultado.textContent = "✅ ¡Correcto! Esa es una buena acción ambiental.";
        correctoAudio.play();
      }
    }

    function juego2(eleccion) {
      const resultado = document.getElementById("juego2resultado");
      const correctoAudio = document.getElementById("correcto");
      const incorrectoAudio = document.getElementById("incorrecto");

      if (eleccion === 'organico') {
        resultado.textContent = "✅ ¡Correcto! La cáscara de plátano es residuo orgánico.";
        correctoAudio.play();
      } else {
        resultado.textContent = "❌ Incorrecto. Esa no es la clasificación adecuada.";
        incorrectoAudio.play();
      }
    }
  </script>
</body>
</html>
