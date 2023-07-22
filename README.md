- 👋 Hi, I’m @Nguyenduc2k3
- 👀 I’m interested in ... computer
- 🌱 I’m currently learning ... coding
- 💞️ I’m looking to collaborate on ... github
- 📫 How to reach me ...

<!---
Nguyenduc2k3/Nguyenduc2k3 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<!DOCTYPE html>
<html>
<head>
  <title>Con rắn chuyển động</title>
  <style>
    body {
      margin: 0;
      overflow: hidden;
    }
    canvas {
      display: block;
    }
  </style>
</head>
<body>
  <canvas id="snakeCanvas"></canvas>
  <script src="snake.js">

    const canvas = document.getElementById('snakeCanvas');
const ctx = canvas.getContext('2d');

// Kích thước của canvas
const canvasWidth = window.innerWidth;
const canvasHeight = window.innerHeight;

canvas.width = canvasWidth;
canvas.height = canvasHeight;

// Khởi tạo tọa độ ban đầu cho con rắn
let x = 50;
let y = 50;
let speedX = 2;
let speedY = 2;

function drawSnake() {
  // Xóa canvas để vẽ lại con rắn
  ctx.clearRect(0, 0, canvasWidth, canvasHeight);

  // Vẽ con rắn
  ctx.fillStyle = 'green';
  ctx.fillRect(x, y, 50, 50);

  // Di chuyển con rắn
  x += speedX;
  y += speedY;

  // Kiểm tra va chạm với biên của canvas
  if (x + 50 > canvasWidth || x < 0) {
    speedX = -speedX;
  }
  if (y + 50 > canvasHeight || y < 0) {
    speedY = -speedY;
  }

  // Lặp lại việc vẽ con rắn sau 100ms
  requestAnimationFrame(drawSnake);
}

// Bắt đầu vẽ con rắn
drawSnake();

  </script>
</body>
</html>

