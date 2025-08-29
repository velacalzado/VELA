<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>VELA | Tienda de Calzado</title>
  <style>
    /* ====== Estilos Generales ====== */
    body {
      margin: 0;
      font-family: 'Segoe UI', Arial, sans-serif;
      background: #f9f9f9;
      color: #333;
    }

    header {
      background: linear-gradient(90deg, #000, #444);
      color: #fff;
      padding: 20px 50px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    header h1 {
      font-size: 28px;
      letter-spacing: 2px;
      font-weight: bold;
    }

    nav a {
      color: #fff;
      text-decoration: none;
      margin: 0 15px;
      font-size: 16px;
      transition: color 0.3s;
    }

    nav a:hover {
      color: #ffcc00;
    }

    /* ====== Hero ====== */
    .hero {
      height: 80vh;
      background: url('https://images.unsplash.com/photo-1542291026-7eec264c27ff?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80') center/cover no-repeat;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: #fff;
      position: relative;
    }

    .hero::after {
      content: "";
      position: absolute;
      inset: 0;
      background: rgba(0,0,0,0.5);
    }

    .hero-content {
      position: relative;
      z-index: 1;
    }

    .hero h2 {
      font-size: 48px;
      margin-bottom: 15px;
    }

    .hero p {
      font-size: 20px;
      margin-bottom: 25px;
    }

    .btn {
      background: #ffcc00;
      color: #000;
      padding: 12px 25px;
      border: none;
      border-radius: 25px;
      font-size: 16px;
      cursor: pointer;
      text-decoration: none;
      transition: 0.3s;
    }

    .btn:hover {
      background: #e6b800;
      transform: scale(1.05);
    }

    /* ====== Productos ====== */
    .productos {
      padding: 60px 20px;
      text-align: center;
    }

    .productos h2 {
      font-size: 32px;
      margin-bottom: 40px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
      padding: 0 50px;
    }

    .card {
      background: #fff;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      overflow: hidden;
      transition: transform 0.3s;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .card img {
      width: 100%;
      height: 220px;
      object-fit: cover;
    }

    .card h3 {
      margin: 15px 0 5px;
      font-size: 20px;
    }

    .card p {
      color: #777;
      margin-bottom: 15px;
    }

    .precio {
      font-size: 18px;
      font-weight: bold;
      color: #0077cc;
      margin-bottom: 15px;
    }

    /* ====== Footer ====== */
    footer {
      background: #000;
      color: #fff;
      padding: 40px 20px;
      text-align: center;
      margin-top: 40px;
    }

    footer p {
      margin: 5px 0;
    }

    footer a {
      color: #ffcc00;
      text-decoration: none;
    }
  </style>
</head>
<body>

  <!-- 🔹 Encabezado -->
  <header>
    <h1>VÉLA</h1>
    <nav>
      <a href="#">Inicio</a>
      <a href="#productos">Productos</a>
      <a href="#contacto">Contacto</a>
    </nav>
  </header>

  <!-- 🔹 Sección principal (Hero) -->
  <section class="hero">
    <div class="hero-content">
      <h2>Calzado que define tu estilo</h2>
      <p>Encuentra los mejores modelos de la marca VÉLA</p>
      <a href="#productos" class="btn">Ver colección</a>
    </div>
  </section>

  <!-- 🔹 Productos -->
  <section id="productos" class="productos">
    <h2>Nuestros Productos</h2>
    <div class="grid">
      <!-- Producto 1 -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1606813907291-4d93fdbe2c88?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Tenis deportivos">
        <h3>Tenis Urban</h3>
        <p>Comodidad y estilo para tu día a día.</p>
        <div class="precio">$1,299 MXN</div>
        <a href="#" class="btn">Comprar</a>
      </div>
      <!-- Producto 2 -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1525966222134-fcfa99b8ae77?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Botines">
        <h3>Botines Elegance</h3>
        <p>Perfectos para ocasiones especiales.</p>
        <div class="precio">$1,899 MXN</div>
        <a href="#" class="btn">Comprar</a>
      </div>
      <!-- Producto 3 -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1600180758895-7be1d81d3317?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Sandalias">
        <h3>Sandalias Breeze</h3>
        <p>Frescura y ligereza para el verano.</p>
        <div class="precio">$999 MXN</div>
        <a href="#" class="btn">Comprar</a>
      </div>
    </div>
  </section>

  <!-- 🔹 Footer -->
  <footer id="contacto">
    <p>© 2025 VELA - Todos los derechos reservados.</p>
    <p>📧 Contacto: <a href="mailto:contacto@vela.com">contacto@vela.com</a></p>
    <p>📍 Ubicación: San Francisco del Rincon, Gto, MX</p>
  </footer>

</body>
</html>
