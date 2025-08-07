# To-Do-Listv3
<html lang="es">
<head>
<meta charset="UTF-8" />
<title>Planificación</title>

<!-- Fuentes -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Barlow:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Bebas+Neue&family=Bitcount+Prop+Double:wght@100..900&family=Bungee&family=Goldman:wght@400;700&family=Jost:ital,wght@0,100..900;1,100..900&family=Libertinus+Sans:ital,wght@0,400;0,700;1,400&family=Luckiest+Guy&family=Oswald:wght@200..700&family=Playwrite+AU+QLD:wght@100..400&family=Saira:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">

<style>
  /* Reset y estilo básico para centrar todo */
body, html {
    margin: 0; padding: 0; height: 100%;
  font-family: "Bungee", sans-serif;
    background: #121212;
    color: rgb(248, 7, 148);
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .container {
    background: rgba(255 255 255 / 0.05);
    padding: 3rem 4rem;
    border-radius: 10px;
    box-shadow: 0 0 20px rgba(138, 43, 226, 0.3);
    text-align: center;
    max-width: 420px;
    width: 90%;
    position: relative;
    z-index: 1;
  }

  h1{
    font-weight: 1000;
    font-size: 2.5rem;
    margin-bottom: 1.5rem;
  }
  h2 {
    font-family: "Luckiest Guy", cursive;
    font-weight: 400;
    font-style: normal;
    font-size: 1.8rem;
    margin-bottom: 2rem;
    color: blueviolet;
  }

  select, input[type="text"], input[type="date"] {
  font-family: "Bungee", sans-serif;
  font-weight: 400;
  font-style: normal;
}
    font-weight: 700;
    font-size: 1.1rem;
    padding: 0.6rem 1rem;
    margin: 0.5rem 0.3rem;
    border: 2px solid rgb(0, 213, 255);
    border-radius: 6px;
    background: transparent;
    color: rgb(235, 13, 13);
    outline: none;
    transition: border-color 0.3s ease;
    width: calc(100% - 2rem);
    max-width: 320px;
  select:hover, input:hover, select:focus, input:focus {
    border-color: #7b3fbf;
  }

  /* Contenedor para inputs de texto y fecha */
  .inputs {
    margin: 1rem 0 2rem;
  }

  button {
    background-color: blueviolet;
    border: none;
    padding: 0.8rem 2rem;
    font-size: 1.2rem;
    font-weight: 700;
    color: #fff;
    border-radius: 8px;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }
  button:hover {
    background-color: #7b3fbf;
  }

  /* Fondo animado con triángulos */
  body::before {
    content: "";
    position: fixed;
    top: 0; left: 0;
    width: 100vw;
    height: 100vh;
    pointer-events: none;
    background:
      repeating-radial-gradient(circle at 20% 20%, rgba(138,43,226,0.15), rgba(138,43,226,0) 40px),
      repeating-radial-gradient(circle at 80% 80%, rgba(138,43,226,0.15), rgba(138,43,226,0) 40px);
    animation: bgMove 20s linear infinite;
    z-index: 0;
  }

  /* Triángulos animados */
  .triangle {
    position: fixed;
    width: 50px;
    height: 50px;
    background: transparent;
    border-left: 25px solid transparent;
    border-right: 25px solid transparent;
    border-bottom: 50px solid blueviolet;
    opacity: 0.1;
    animation: floatUpDown 6s ease-in-out infinite;
  }
  .triangle:nth-child(1) {
    top: 30%;
    left: 10%;
    animation-delay: 0s;
  }
  .triangle:nth-child(2) {
    top: 70%;
    left: 25%;
    animation-delay: 2s;
  }
  .triangle:nth-child(3) {
    top: 50%;
    left: 80%;
    animation-delay: 4s;
  }
  .triangle:nth-child(4) {
    top: 20%;
    left: 70%;
    animation-delay: 1s;
  }
  .triangle:nth-child(5) {
    top: 80%;
    left: 50%;
    animation-delay: 3s;
  }

  @keyframes floatUpDown {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-20px); }
  }

  @keyframes bgMove {
    0% { background-position: 0 0, 0 0; }
    100% { background-position: 200px 200px, -200px -200px; }
  }
</style>
</head>
<body>

  <!-- Figuras geométricas para animación -->
  <div class="triangle"></div>
  <div class="triangle"></div>
  <div class="triangle"></div>
  <div class="triangle"></div>
  <div class="triangle"></div>

  <div class="container">
    <h1>BIENVENIDO AL MENÚ DE PLANIFICACIÓN</h1>
    <h2>Seleccione materia</h2>
    <select id="materia" aria-label="Seleccione materia">
      <option>Estudios Sociales</option>
      <option>MUCI</option>
      <option>Matemáticas</option>
      <option>Informática</option>
      <option>Biología</option>
      <option>Física</option>
      <option>Química</option>
      <option>Lenguaje y Literatura</option>
      <option>Religión</option>
      <option>Estadística</option>
      <option>Seminario</option>
      <option>Filosofía</option>
    </select>

    <div class="inputs">
      <input type="text" id="tarea" placeholder="Nombre de la tarea" aria-label="Nombre de la tarea" />
      <input type="date" id="fecha" aria-label="Fecha de entrega" />
    </div>

    <button onclick="guardar()">Guardar</button>
   <a href="https://charlillos.github.io/To-Do-Listv4"><button>Siguiente</button></a>
  </div>

  <script>
    function guardar() {
      const materia = document.getElementById("materia").value;
      const tarea = document.getElementById("tarea").value.trim();
      const fecha = document.getElementById("fecha").value;
      if (!tarea) {
        alert("Por favor, ingrese el nombre de la tarea.");
        return;
      }
      const tareas = JSON.parse(localStorage.getItem("tareas") || "[]");
      tareas.push({ materia, tarea, fecha, entregada: false });
      localStorage.setItem("tareas", JSON.stringify(tareas));
      alert("Guardado correctamente");
      document.getElementById("tarea").value = "";
      document.getElementById("fecha").value = "";
    }
  </script>
</body>
</html>
