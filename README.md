
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy New Year!</title>
  <style>
    body {
      text-align: center;
      font-family: 'Arial', sans-serif;
      background-color: #000;
      color: #fff;
      margin: 0;
      padding: 0;
      overflow: hidden;
    }

    h1 {
      font-size: 48px;
      animation: rainbowText 3s infinite;
      margin: 50px 0;
    }

    @keyframes rainbowText {
      0% { color: #ff0000; }
      16.666% { color: #ff9900; }
      33.333% { color: #ffcc00; }
      50% { color: #33cc33; }
      66.666% { color: #3399ff; }
      83.333% { color: #cc66ff; }
      100% { color: #ff0000; }
    }

    #fireworks-container {
      display: none;
    }

    #fireworks {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      margin-top: 20px;
      cursor: pointer;
      background-color: #4285f4;
      color: #fff;
      border: none;
      border-radius: 5px;
    }

    #nsfw-button {
      padding: 5px 10px;
      font-size: 12px;
      cursor: pointer;
      background-color: #4285f4;
      color: #fff;
      border: none;
      border-radius: 5px;
    }

    #youtube-player {
      display: none;
      width: 640px;
      height: 360px;
      margin: 20px auto;
    }
  </style>
</head>
<body>
  <h1>HAPPY NEW YEAR EVERYONE!!!</h1>
  <div id="fireworks-container">
    <canvas id="fireworks"></canvas>
  </div>
  <button onclick="startFireworks()">PRESS FOR FIREWORKS</button>
  <button id="nsfw-button" onclick="openNSFWLink()">PRESS = TRUST</button>
  <div id="youtube-player"></div>

  <script>
    function startFireworks() {
      // Play audio
      const audio = new Audio('https://drive.google.com/file/d/1TDxj-vIperYLVS7JCDMk34-xNb5XIjF2/view?usp=drive_link');
      audio.play();

      document.getElementById('fireworks-container').style.display = 'block';

      const fireworksCanvas = document.getElementById('fireworks');
      const ctx = fireworksCanvas.getContext('2d');

      fireworksCanvas.width = window.innerWidth;
      fireworksCanvas.height = window.innerHeight;

      function drawFireworks() {
        ctx.fillStyle = 'rgba(0, 0, 0, 0.2)';
        ctx.fillRect(0, 0, fireworksCanvas.width, fireworksCanvas.height);

        // Fireworks bursts
        const colors = ['#ff0000', '#ff9900', '#ffcc00', '#33cc33', '#3399ff', '#cc66ff'];

        for (let i = 0; i < 5; i++) {
          const x = Math.random() * fireworksCanvas.width;
          const y = Math.random() * fireworksCanvas.height;
          const radius = Math.random() * 20 + 5;
          const color = colors[Math.floor(Math.random() * colors.length)];

          ctx.beginPath();
          ctx.arc(x, y, radius, 0, Math.PI * 2);
          ctx.fillStyle = color;
          ctx.fill();
        }
      }

      // Update fireworks animation every 100 milliseconds
      const fireworksInterval = setInterval(drawFireworks, 100);

      // Stop the fireworks after 5 seconds and show YouTube video
      setTimeout(() => {
        document.getElementById('fireworks-container').style.display = 'none';
        clearInterval(fireworksInterval);

        // Embed YouTube video with autoplay
        const youtubePlayer = document.getElementById('youtube-player');
        youtubePlayer.style.display = 'block';
        youtubePlayer.innerHTML = '<iframe width="640" height="360" src="https://www.youtube.com/embed/rWwhteesVhA?autoplay=1" frameborder="0" allowfullscreen></iframe>';
      }, 5000);
    }

    function openNSFWLink() {
      window.open('https://matias.ma/nsfw/', '_blank');
    }
  </script>
</body>
</html>
