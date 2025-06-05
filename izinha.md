<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>🌟 Apoie o Começo da Jornada da Irys 🌟</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@400;600&display=swap');
    * {
      box-sizing: border-box;
    }
    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(to bottom, #fff0f6, #ffe4ec);
      margin: 0;
      padding: 20px;
      color: #6b3a58;
      text-align: center;
      overflow-x: hidden;
      animation: fadeIn 1.2s ease-in;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    header {
      background-color: #fcd5e5;
      color: #6b3a58;
      padding: 30px 0;
      margin-bottom: 30px;
      border-radius: 14px;
      box-shadow: 0 5px 12px rgba(219,112,147,0.3);
      animation: floatDown 1s ease-in-out;
    }

    @keyframes floatDown {
      from { transform: translateY(-30px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }

    h1 {
      margin: 0;
      font-weight: 600;
      font-size: 2.4em;
      font-family: 'Pacifico', cursive;
    }

    .content {
      max-width: 700px;
      margin: auto;
      background: #fff;
      padding: 30px 35px;
      border-radius: 20px;
      box-shadow: 0 4px 15px rgba(219,112,147,0.25);
      animation: fadeInUp 1.4s ease-in-out;
    }

    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(40px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .section-title {
      font-weight: 600;
      color: #c75a7c;
      margin-top: 25px;
      font-size: 1.4em;
    }

    p {
      font-size: 1.1em;
      line-height: 1.6;
      margin: 15px 0;
    }

    .pix-code {
      margin: 20px auto;
      max-width: 500px;
      background: #fde8ef;
      padding: 18px 15px;
      font-weight: 600;
      font-size: 1em;
      color: #a93d62;
      border-radius: 8px;
      user-select: all;
      word-break: break-word;
      box-shadow: 0 2px 6px rgba(219,112,147,0.2);
      animation: pulse 2s infinite ease-in-out;
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.02); }
      100% { transform: scale(1); }
    }

    .meta-container {
      margin: 25px 0;
    }

    .meta-bar {
      width: 100%;
      background: #fce1ec;
      border-radius: 10px;
      overflow: hidden;
      height: 20px;
      box-shadow: inset 0 1px 3px rgba(0,0,0,0.1);
    }

    .meta-progress {
      width: 0%;
      height: 100%;
      background-color: #f48fb1;
      animation: grow 3s forwards;
    }

    @keyframes grow {
      0% { width: 0%; }
      100% { width: 0%; } /* Pode ajustar para valor real arrecadado depois */
    }

    button {
      background-color: #c75a7c;
      color: white;
      border: none;
      padding: 14px 32px;
      border-radius: 10px;
      font-size: 1em;
      cursor: pointer;
      transition: background-color 0.3s;
      margin-top: 10px;
      box-shadow: 0 4px 8px rgba(199,90,124,0.6);
    }

    button:hover {
      background-color: #a13e5d;
    }

    footer {
      margin-top: 50px;
      font-size: 0.9em;
      color: #a66b87;
    }

    #sakura-canvas {
      position: fixed;
      top: 0;
      left: 0;
      pointer-events: none;
      width: 100%;
      height: 100%;
      z-index: 9999;
    }
  </style>
</head>
<body>
  <header>
    <h1>🌟 Apoie o Começo da Jornada da Irys 🌟</h1>
  </header>

  <div class="content">
    <div class="section">
      <h2 class="section-title">✨ Sobre Mim</h2>
      <p>Oi! Eu sou a <strong>Irys</strong>, tenho 17 aninhos e sonho em fazer lives incríveis para compartilhar alegria, criatividade e momentos especiais com vocês! 💫</p>
    </div>

    <div class="section">
      <h2 class="section-title">🎯 Minha Meta</h2>
      <p>Para começar, preciso de uma placa de vídeo que custa <strong>R$ 1000</strong>. Qualquer contribuição já me ajuda MUITO a chegar mais perto desse sonho! 🥹💕</p>
      <div class="meta-container">
        <div class="meta-bar">
          <div class="meta-progress"></div>
        </div>
        <p><small>R$ 0 arrecadados até agora 💖</small></p>
      </div>
    </div>

    <div class="section">
      <h2 class="section-title">💗 Como Ajudar</h2>
      <p>Você pode me ajudar enviando qualquer valor via PIX. Seu apoio é muito especial pra mim e me dá forças para continuar acreditando! 🌟</p>
      <div class="pix-code">
        00020101021126580014br.gov.bcb.pix01363fe9d501-b3eb-4280-8320-f1f7f22a1c375204000053039865802BR5918IRYS A DA C SANTOS6013NOSSA SENHORA62070503***6304EE03
      </div>
      <button onclick="copyPix()">💌 Copiar código PIX</button>
    </div>
  </div>

  <footer>
    <p>Obrigada por estar aqui e por acreditar no meu sonho! 💕 Com amor, Irys ✨</p>
  </footer>

  <canvas id="sakura-canvas"></canvas>

  <script>
    function copyPix() {
      const pix = document.querySelector('.pix-code').textContent;
      navigator.clipboard.writeText(pix).then(() => {
        alert('Código PIX copiado com sucesso! 💖');
      });
    }

    const canvas = document.getElementById('sakura-canvas');
    const ctx = canvas.getContext('2d');
    let width, height;
    let petals = [];

    function resize() {
      width = window.innerWidth;
      height = window.innerHeight;
      canvas.width = width;
      canvas.height = height;
    }

    window.addEventListener('resize', resize);
    resize();

    class Petal {
      constructor() {
        this.reset();
      }

      reset() {
        this.x = Math.random() * width;
        this.y = Math.random() * height - height;
        this.size = 8 + Math.random() * 8;
        this.speedY = 1 + Math.random() * 2;
        this.speedX = Math.random() * 1 - 0.5;
        this.angle = Math.random() * 2 * Math.PI;
        this.rotationSpeed = 0.01 + Math.random() * 0.02;
        this.opacity = 0.6 + Math.random() * 0.4;
      }

      update() {
        this.y += this.speedY;
        this.x += this.speedX;
        this.angle += this.rotationSpeed;
        if (this.y > height) this.reset();
        if (this.x > width) this.x = 0;
        if (this.x < 0) this.x = width;
      }

      draw(ctx) {
        ctx.save();
        ctx.translate(this.x, this.y);
        ctx.rotate(this.angle);
        ctx.fillStyle = `rgba(252, 182, 193, ${this.opacity})`;
        ctx.beginPath();
        ctx.moveTo(0, 0);
        ctx.bezierCurveTo(5, -3, 7, 5, 0, 7);
        ctx.bezierCurveTo(-7, 5, -5, -3, 0, 0);
        ctx.fill();
        ctx.restore();
      }
    }

    function createPetals(num) {
      petals = [];
      for (let i = 0; i < num; i++) {
        petals.push(new Petal());
      }
    }

    function animate() {
      ctx.clearRect(0, 0, width, height);
      petals.forEach(petal => {
        petal.update();
        petal.draw(ctx);
      });
      requestAnimationFrame(animate);
    }

    createPetals(30);
    animate();
  </script>
</body>
</html>
