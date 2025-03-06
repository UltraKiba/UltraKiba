# Medi's Developer Portfolio 🌐

## 🌐 Social Profiles
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/Medi) 
[![Reddit](https://img.shields.io/badge/Reddit-%23FF4500.svg?logo=Reddit&logoColor=white)](https://reddit.com/user/MediKun) 
[![X](https://img.shields.io/badge/X-black.svg?logo=X&logoColor=white)](https://x.com/UltraKiba) 
[![Email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:www.medikibambe@gmail.com)

---

## 💻 Tech Stack & Animations
| Tech Stack | Snake Game | JJK Animation |
|------------|------------|---------------|
| **Frontend**<br>![React](https://img.shields.io/badge/react-%2320232a.svg?logo=react&logoColor=%2361DAFB)<br>![Vue.js](https://img.shields.io/badge/vue.js-%2335495e.svg?logo=vuedotjs&logoColor=%234FC08D)<br>![Angular](https://img.shields.io/badge/angular-%23DD0031.svg?logo=angular&logoColor=white) | <canvas id="game" width="200" height="200"></canvas> | ![JJK](https://media.tenor.com/bkA2JqxxfGwAAAAj/mlbb-jjk-jjk-mlbb.gif) |
| **Backend**<br>![NodeJS](https://img.shields.io/badge/node.js-6DA55F?logo=node.js&logoColor=white)<br>![NestJS](https://img.shields.io/badge/nestjs-%23E0234E.svg?logo=nestjs&logoColor=white)<br>![.NET](https://img.shields.io/badge/.NET-5C2D91?logo=.net&logoColor=white) |  |  |
| **Mobile**<br>![Flutter](https://img.shields.io/badge/Flutter-%2302569B.svg?logo=Flutter&logoColor=white)<br>![Kotlin](https://img.shields.io/badge/kotlin-%237F52FF.svg?logo=kotlin&logoColor=white) |  |  |
| **DevOps**<br>![Azure](https://img.shields.io/badge/azure-%230072C6.svg?logo=microsoftazure&logoColor=white)<br>![Google Cloud](https://img.shields.io/badge/GoogleCloud-%234285F4.svg?logo=google-cloud&logoColor=white) |  |  |
| **Design**<br>![Blender](https://img.shields.io/badge/blender-%23F5792A.svg?logo=blender&logoColor=white)<br>![Adobe](https://img.shields.io/badge/adobe-%23FF0000.svg?logo=adobe&logoColor=white) |  |  |

<script>
// Simple Snake Game Implementation
const canvas = document.getElementById('game');
const ctx = canvas.getContext('2d');

const gridSize = 20;
let snake = [{x: 10, y: 10}];
let direction = 'right';
let food = {x: 5, y: 5};
let score = 0;

function draw() {
  ctx.fillStyle = '#000';
  ctx.fillRect(0, 0, canvas.width, canvas.height);
  
  ctx.fillStyle = 'lime';
  snake.forEach(segment => ctx.fillRect(segment.x*gridSize, segment.y*gridSize, gridSize, gridSize));
  
  ctx.fillStyle = 'red';
  ctx.fillRect(food.x*gridSize, food.y*gridSize, gridSize, gridSize);
}

function update() {
  const head = {x: snake[0].x, y: snake[0].y};
  
  switch(direction) {
    case 'up': head.y--; break;
    case 'down': head.y++; break;
    case 'left': head.x--; break;
    case 'right': head.x++; break;
  }
  
  if (head.x === food.x && head.y === food.y) {
    score++;
    food = {
      x: Math.floor(Math.random() * (canvas.width/gridSize)),
      y: Math.floor(Math.random() * (canvas.height/gridSize))
    };
  } else {
    snake.pop();
  }
  
  snake.unshift(head);
}

document.addEventListener('keydown', e => {
  switch(e.key) {
    case 'ArrowUp': if(direction !== 'down') direction = 'up'; break;
    case 'ArrowDown': if(direction !== 'up') direction = 'down'; break;
    case 'ArrowLeft': if(direction !== 'right') direction = 'left'; break;
    case 'ArrowRight': if(direction !== 'left') direction = 'right'; break;
  }
});

setInterval(() => {
  update();
  draw();
}, 150);
</script>

---

## 📊 GitHub Stats Dashboard
| Main Stats | Detailed Breakdown |
|------------|--------------------|
| [![GitHub Stats](https://github-readme-stats.vercel.app/api?username=UltraKiba&theme=nightowl&hide_border=false)](https://github.com/UltraKiba) | [![Streak](https://nirzak-streak-stats.vercel.app/?user=UltraKiba&theme=nightowl)](https://github.com/UltraKiba)<br><br>[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=UltraKiba&theme=nightowl&layout=compact)](https://github.com/UltraKiba) |

---

## 🏆 Achievements
[![GitHub Trophies](https://github-profile-trophy.vercel.app/?username=UltraKiba&theme=radical)](https://github.com/UltraKiba)
[![Top Contributions](https://github-contributor-stats.vercel.app/api?username=UltraKiba&limit=5&theme=dark)](https://github.com/UltraKiba)

---

## ✍️ Developer Wisdom
![Dev Quote](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical)

---

## 🎵 Spotify Activity
| Recently Played | Sora Floating |
|-----------------|---------------|
| [![Spotify](https://spotify-recently-played-readme.vercel.app/api?user=6atdqjokxb3w6gz2qbs0s8bop&count=5&unique=true)](https://open.spotify.com/user/6atdqjokxb3w6gz2qbs0s8bop) | ![Sora](https://i.imgur.com/f83frkB.gif) |
