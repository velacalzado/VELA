<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>VELA | Tienda de Calzado</title>
  <link rel="icon" href="img/vela-icon2.png" type="image/png">
  <style>
    :root {
      --rosa: #F8BBD0;
      --lila: #E1BEE7;
      --azul: #B3E5FC;
      --gris: #FAFAFA;
      --texto: #444;
    }
    body {
      margin: 0;
      font-family: 'Segoe UI', Arial, sans-serif;
      background: var(--gris);
      color: var(--texto);
    }
    header {
      background: var(--rosa);
      color: var(--texto);
      padding: 16px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 1000;
      border-bottom: 1px solid var(--azul);
    }
    header img {
      height: 48px;
      margin-right: 24px;
      display: block;
    }
    nav a {
      color: var(--texto);
      text-decoration: none;
      margin: 0 12px;
      font-size: 15px;
      font-weight: 500;
      padding: 3px 8px;
      border-radius: 12px;
      transition: background 0.2s;
    }
    nav a:hover {
      background: var(--azul);
    }
    .hero {
      height: 55vh;
      background: url('img/calzado.png') center/cover no-repeat;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: var(--texto);
      position: relative;
      border-radius: 0 0 32px 32px;
      margin-bottom: 32px;
    }
    .hero::after {
      content: "";
      position: absolute;
      inset: 0;
      background: rgba(248, 187, 208, 0.13);
      border-radius: 0 0 32px 32px;
    }
    .hero-content {
      position: relative;
      z-index: 1;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 12px;
    }
    .hero-content img {
      height: 72px;
      margin-bottom: 15px;
      display: block;
      background: var(--rosa);
      border-radius: 50%;
      padding: 8px;
      box-shadow: 0 2px 8px rgba(179,229,252,0.10); /* Sombra suave opcional */
    }
    .hero h2 {
      font-size: 36px;
      margin-bottom: 10px;
      color: var(--lila);
      font-weight: 700;
    }
    .hero p {
      font-size: 18px;
      margin-bottom: 20px;
    }
    .btn {
      background: var(--rosa);
      color: var(--texto);
      padding: 10px 24px;
      border: none;
      border-radius: 20px;
      font-size: 15px;
      font-weight: 600;
      cursor: pointer;
      text-decoration: none;
      transition: background 0.2s;
      box-shadow: none;
      display: inline-block;
    }
    .btn:hover {
      background: var(--lila);
      color: var(--texto);
    }
    .productos {
      padding: 44px 10px 28px 10px;
      text-align: center;
    }
    .productos h2 {
      font-size: 26px;
      margin-bottom: 28px;
      color: var(--rosa);
      font-weight: 700;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 26px;
      padding: 0 24px;
    }
    .card {
      background: #fff;
      border-radius: 18px;
      border: 1.5px solid var(--azul);
      overflow: hidden;
      transition: transform 0.2s, border 0.3s;
      padding-bottom: 20px;
    }
    .card:hover {
      transform: translateY(-3px) scale(1.01);
      border-color: var(--rosa);
    }
    .card img {
      width: 100%;
      height: 170px;
      object-fit: cover;
      background: var(--lila);
      border-bottom: 1.5px solid var(--azul);
    }
    .card h3 {
      margin: 16px 0 6px;
      font-size: 18px;
      color: var(--lila);
      font-weight: 600;
    }
    .card p {
      color: var(--texto);
      margin-bottom: 10px;
      font-size: 14px;
    }
    .precio {
      font-size: 16px;
      font-weight: 600;
      color: var(--texto);
      margin-bottom: 10px;
    }
    .card .btn {
      margin-bottom: 0;
      background: var(--rosa);
      color: var(--texto);
      font-size: 14px;
      padding: 8px 18px;
      border-radius: 18px;
    }
    .card .btn:hover {
      background: var(--lila);
    }
    .social-footer {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 24px;
      margin-bottom: 10px;
    }
    .social-footer a {
      display: flex;
      align-items: center;
      text-decoration: none;
      font-weight: 600;
      color: var(--texto);
      font-size: 16px;
      gap: 6px;
      transition: color 0.2s;
    }
    .social-footer a:hover {
      color: var(--azul);
    }
    .icon {
      width: 24px;
      height: 24px;
      display: block;
    }
    footer {
      background: var(--gris);
      color: var(--texto);
      padding: 32px 10px 22px 10px;
      text-align: center;
      margin-top: 44px;
      border-top: 1.5px solid var(--azul);
    }
    footer img {
      height: 30px;
      margin-bottom: 12px;
      display: block;
      margin-left: auto;
      margin-right: auto;
      background: var(--rosa);
      border-radius: 8px;
      padding: 3px 8px;
      border: 1px solid var(--azul);
    }
    footer p {
      margin: 5px 0;
      color: var(--texto);
      font-size: 14px;
    }
    footer a.email {
      color: var(--texto);
      text-decoration: none;
      font-weight: 600;
    }
    @media (max-width: 600px) {
      .hero h2 { font-size: 22px; }
      .productos h2 { font-size: 18px; }
      .grid { padding: 0 5px; }
      .hero-content img { height: 48px; }
      .social-footer { gap: 10px; }
    }
  </style>
  <script>
    // Función para WhatsApp con mensaje dinámico
    function comprar(producto) {
      const numero = "4775809107";
      const mensaje = encodeURIComponent("¡Hola! Me interesa comprar el producto: " + producto);
      window.open(`https://wa.me/52${numero}?text=${mensaje}`, "_blank");
      return false;
    }
  </script>
</head>
<body>

  <!-- Encabezado con logo principal -->
  <header>
    <img src="img/vela-logo.png" alt="Logo VELA">
    <nav>
      <a href="#">Inicio</a>
      <a href="#productos">Productos</a>
      <a href="#contacto">Contacto</a>
    </nav>
  </header>

  <!-- Sección principal (Hero) con icono V -->
  <section class="hero">
    <div class="hero-content">
      <img src="img/vela-icon.png" alt="Icono VELA">
      <h2>Calzado que define tu estilo</h2>
      <p>Encuentra los mejores modelos de la marca VELA</p>
      <a href="#productos" class="btn">Ver colección</a>
    </div>
  </section>

  <!-- Productos -->
  <section id="productos" class="productos">
    <h2>Nuestros Productos</h2>
    <div class="grid">
      <!-- Producto 1 -->
      <div class="card">
        <img src="img/calzado.png" alt="Tenis deportivos">
        <h3>Tenis Urban</h3>
        <p>Comodidad y estilo para tu día a día.</p>
        <div class="precio">$299 MXN</div>
        <a href="#" class="btn" onclick="return comprar('Tenis Urban');">Comprar</a>
      </div>
      <!-- Producto 2 -->
      <div class="card">
        <img src="img/calzado.png" alt="Botines">
        <h3>Botines Elegance</h3>
        <p>Perfectos para ocasiones especiales.</p>
        <div class="precio">$899 MXN</div>
        <a href="#" class="btn" onclick="return comprar('Botines Elegance');">Comprar</a>
      </div>
      <!-- Producto 3 -->
      <div class="card">
        <img src="img/calzado.png" alt="Sandalias">
        <h3>Sandalias Breeze</h3>
        <p>Frescura y ligereza para el verano.</p>
        <div class="precio">$999 MXN</div>
        <a href="#" class="btn" onclick="return comprar('Sandalias Breeze');">Comprar</a>
      </div>
    </div>
  </section>

  <!-- Footer con logo VÉLA texto y redes sociales -->
  <footer id="contacto">
    <img src="img/vela-text.png" alt="VELA">
    <div class="social-footer">
      <!-- WhatsApp -->
      <a href="https://wa.me/524775809107" target="_blank" title="WhatsApp">
        <svg class="icon" viewBox="0 0 32 32" fill="none">
          <circle cx="16" cy="16" r="16" fill="#25D366"/>
          <path d="M22.2 18.4c-.3-.2-1.6-.8-1.8-.9-.2-.1-.4-.2-.6.2-.2.4-.7.9-.9 1.1-.2.2-.4.2-.7.1-.3-.1-1.3-.5-2.5-1.4-.9-.8-1.5-1.7-1.7-1.9-.2-.2-.1-.4.1-.5.2-.2.4-.5.6-.8.2-.2.2-.4 0-.6-.1-.2-.6-1.4-.8-1.9-.2-.5-.4-.4-.6-.4-.2 0-.4 0-.6 0-.2.1-.5.2-.7.5-.2.3-.7.8-.7 2 0 1.2.8 2.3 1 2.5.2.2 2 3.2 4.9 4.4 2.9 1.2 3.2.8 3.8.7.5-.1 1.6-1.1 1.9-2.1.2-1-.1-1.2-.3-1.3z" fill="#fff"/>
        </svg>
        WhatsApp
      </a>
      <!-- Instagram -->
      <a href="https://instagram.com/" target="_blank" title="Instagram">
        <svg class="icon" viewBox="0 0 32 32" fill="none">
          <circle cx="16" cy="16" r="16" fill="#E1306C"/>
          <rect x="10" y="10" width="12" height="12" rx="4" fill="#fff"/>
          <circle cx="16" cy="16" r="3" fill="#E1306C"/>
          <circle cx="22" cy="12" r="1.2" fill="#E1306C"/>
        </svg>
        CALZADO VELA
      </a>
    </div>
    <p>© 2025 VELA - Todos los derechos reservados.</p>
    <p>📧 Contacto: <a class="email" href="mailto:velacalzado@gmail.com">velacalzado@gmail.com</a></p>
    <p>📍 Ubicación: San Francisco del Rincon, Gto, MX</p>
  </footer>
