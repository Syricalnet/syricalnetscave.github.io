<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Doxbin Style Site</title>
  <style>
    body {
      margin: 0;
      background-color: #0d0d0d;
      font-family: monospace;
      color: #e6e6e6;
      overflow-x: hidden;
    }

    #particleCanvas {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      z-index: 0;
      background: transparent;
      pointer-events: none;
    }

    nav {
      background-color: #1a1a1a;
      padding: 1rem 2rem;
      display: flex;
      gap: 2rem;
      border-bottom: 1px solid #333;
      position: relative;
      z-index: 1;
    }

    nav a {
      color: #c62828;
      text-decoration: none;
      font-size: 1rem;
      padding: 0.5rem 1rem;
      border-radius: 3px;
    }

    nav a:hover {
      background-color: #2e2e2e;
    }

    main {
      padding: 2rem;
      max-width: 900px;
      margin: 2rem auto;
      position: relative;
      z-index: 1;
    }

    #owes-me, #hall-of-gimps {
      background-color: #121212;
      border: 1px solid #2e2e2e;
      padding: 2rem;
    }

    h1 {
      color: #ff0033;
      font-size: 1.8rem;
      margin-bottom: 1rem;
      border-bottom: 1px solid #2e2e2e;
      padding-bottom: 0.5rem;
    }

    p, li {
      line-height: 1.6;
      color: #cccccc;
    }

    .tab-content {
      display: none;
    }

    .active {
      display: block;
    }

    ul {
      list-style-type: none;
      padding: 0;
    }

    li {
      background-color: #1e1e1e;
      margin-bottom: 0.5rem;
      padding: 0.75rem;
      border-left: 3px solid #ff0033;
      font-size: 0.95rem;
    }

    .gimp-card {
      background-color: #1a1a1a;
      padding: 1rem;
      margin-top: 1rem;
      border: 1px solid #2e2e2e;
      border-left: 4px solid #ff0033;
      color: #ccc;
    }

    .gimp-card img {
      max-width: 150px;
      display: block;
      margin-bottom: 0.5rem;
      border: 1px solid #333;
    }

    .gimp-card h3 {
      margin: 0.5rem 0 0.2rem;
      color: #ff0033;
    }

    .gimp-card a {
      color: #c62828;
      font-size: 0.9rem;
    }

    .ascii-art {
      text-align: center;
      color: #ff0033;
      font-size: 10px;
      line-height: 1;
      white-space: pre;
      margin-bottom: 1rem;
    }

    .intro {
      text-align: center;
      color: #ccc;
      margin-top: 1rem;
      font-size: 0.95rem;
    }

    .intro a {
      font-weight: bold;
      background: linear-gradient(90deg, red, orange, yellow, green, cyan, blue, violet);
      background-size: 400%;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: rainbow 5s linear infinite;
      text-decoration: underline;
    }

    @keyframes rainbow {
      0% { background-position: 0% }
      100% { background-position: 100% }
    }
  </style>
</head>
<body>
  <canvas id="particleCanvas"></canvas>

  <nav>
    <a href="#" onclick="showTab('home')">Home</a>
    <a href="#" onclick="showTab('owes-me')">Owes me</a>
    <a href="#" onclick="showTab('hall-of-gimps')">Hall of gimps</a>
  </nav>

  <main>
    <section id="home" class="tab-content active" style="background: transparent; border: none; box-shadow: none;">
      <pre class="ascii-art">
⠄⠄⠄⠄⠄⠄⣠⣤⣶⣶⣿⣶⣶⣤⣀⠄⣀⣤⣴⣶⣶⣶⣦⣀⠄⠄⠄⠄⠄⠄
⠄⠄⠄⢀⣤⣿⠡⢟⡿⠿⣛⣛⣛⠿⢿⡆⢻⣿⣿⣿⣿⣯⣃⣸⣧⡀⠄⠄⠄⠄
⠄⠄⢀⣾⣿⣿⣋⣵⣾⣿⣿⣿⣿⣿⣷⣶⡄⣩⣴⣶⣶⣶⣶⣶⣭⣉⣀⠄⠄⠄
⠄⢀⣿⡟⣻⣿⣿⣿⣿⠟⢋⣭⣴⣶⣶⣶⣦⣮⡙⠟⢛⣭⣭⣶⣶⣶⣮⣭⣄⠄
⣴⣸⣿⠑⣛⣿⠟⢩⣶⣿⣿⣿⣿⣿⡏⡋⠉⣿⣿⡌⣿⣿⣿⣿⣿⠋⡋⠛⣿⣧
⢿⣿⣿⣿⣿⣿⣶⣶⣭⣝⡻⠿⣿⣿⣷⣧⣵⠿⢟⡑⠿⠿⠿⠿⠿⠶⠭⠶⠟⠃
⣬⣿⣿⣿⣿⣿⣿⣿⣷⣬⣙⣛⣒⠠⢤⣤⡔⢚⣛⣴⣿⣿⣿⣿⣿⣿⣿⡿⠛⠄
⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⡿⠿⣋⣱⣾⣿⣿⣿⣎⡙⢛⣋⣉⣉⣅⠄⠄⠄⠄
⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⢏⣭⡝⢿⣿⣿⣿⣦⠄⠄⠄
⣿⣿⣿⣿⣿⣿⠿⣛⣩⣭⣭⣭⣛⣛⠿⠿⢿⣿⣿⡏⣾⣿⡇⢸⣿⡿⠿⢛⣃⠄
⣿⣿⣿⣿⣿⡏⢾⣿⣯⣭⣍⣛⣛⣛⡻⠶⠶⣮⣭⢡⣿⣿⢇⣭⣵⣶⠾⠿⠋⠄
⣿⣿⣿⣿⣟⢿⣦⣤⣭⣭⣭⣝⣛⡻⠿⠿⠿⠶⠶⢸⣿⣿⢠⣤⣤⣶⠾⠛⠄⠄
⠿⢿⣿⣿⣿⣷⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⡇⣾⣿⡿⠰⠖⠄⠄⠄⠄⠄⠄
⣭⣕⠒⠲⣭⣭⣝⣛⠛⠛⠛⠛⠛⠛⠛⢛⣛⣭⠄⣿⡟⢣⣴⣾⠟⢂⣤⡀⠄⠄
⣿⣿⣿⣿⣶⣶⣮⣭⣭⣭⣍⣛⣛⣉⣭⣭⣭⣶⢸⣿⣿⣿⣯⣴⠞⣛⣭⣶⣷⠄
      </pre>

      <div class="intro">
        <p>
          This website is made as a personal database full of gimps and retards that owe me money.<br/>
          I might add more to this website at some point but atm it's just for this.<br/>
          A Telegram link below has my GC where you can learn everything about OSINT/OPSEC.
        </p>
        <p><a href="https://t.me/YOUR_GROUP_LINK" target="_blank">Join my Telegram Group</a></p>
      </div>
    </section>

    <section id="owes-me" class="tab-content">
      <h1>Money Owed</h1>
      <ul id="owedList"></ul>
    </section>

    <section id="hall-of-gimps" class="tab-content">
      <h1>Hall of Gimps</h1>
      <div id="gimpList"></div>
    </section>
  </main>

  <script>
    function showTab(tabId) {
      const sections = document.querySelectorAll('.tab-content');
      sections.forEach(section => section.classList.remove('active'));
      document.getElementById(tabId).classList.add('active');
    }

    function loadOwedList() {
      const list = document.getElementById("owedList");
      const oweList = JSON.parse(localStorage.getItem("moneyOwed")) || [];
      list.innerHTML = "";
      oweList.forEach(({ name, amount }) => {
        const li = document.createElement("li");
        li.textContent = `${name} owes $${amount}`;
        list.appendChild(li);
      });
    }

    function loadGimps() {
      const container = document.getElementById("gimpList");
      container.innerHTML = "";
      const gimpList = JSON.parse(localStorage.getItem("hallOfGimps")) || [];
      gimpList.forEach(({ name, image, description, link }) => {
        const div = document.createElement("div");
        div.className = "gimp-card";

        const img = document.createElement("img");
        img.src = image;
        img.alt = name;

        const h3 = document.createElement("h3");
        h3.textContent = name;

        const p = document.createElement("p");
        p.textContent = description;

        div.appendChild(img);
        div.appendChild(h3);
        div.appendChild(p);

        if (link) {
          const a = document.createElement("a");
          a.href = link;
          a.target = "_blank";
          a.textContent = "Link";
          div.appendChild(a);
        }

        container.appendChild(div);
      });
    }

    window.onload = function () {
      loadOwedList();
      loadGimps();
    };

    // Red particle snow effect
    const canvas = document.getElementById('particleCanvas');
    const ctx = canvas.getContext('2d');
    let particles = [];
    const numParticles = 100;

    function resizeCanvas() {
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;
    }

    window.addEventListener('resize', resizeCanvas);
    resizeCanvas();

    class Particle {
      constructor() {
        this.reset();
      }
      reset() {
        this.x = Math.random() * canvas.width;
        this.y = Math.random() * -canvas.height;
        this.radius = Math.random() * 2 + 1;
        this.speed = Math.random() * 1 + 0.5;
      }
      update() {
        this.y += this.speed;
        if (this.y > canvas.height) this.reset();
      }
      draw() {
        ctx.beginPath();
        ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
        ctx.fillStyle = '#ff0033';
        ctx.fill();
      }
    }

    function initParticles() {
      particles = [];
      for (let i = 0; i < numParticles; i++) {
        particles.push(new Particle());
      }
    }

    function animate() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      particles.forEach(p => {
        p.update();
        p.draw();
      });
      requestAnimationFrame(animate);
    }

    initParticles();
    animate();
  </script>
</body>
</html>
