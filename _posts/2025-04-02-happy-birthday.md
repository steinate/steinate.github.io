---
layout: full
title: "Happy Birthday, 周丹!"
date: 2025-04-02 00:00:00 +0800
category: celebration
thumbnail: /style/image/birthday.jpg
icon: cake
comments: false
---

<!DOCTYPE html>
<html>
<head>
    <title>🎂 Happy Birthday [Name]! 🌟</title>
    <meta charset="utf-8">
    <style>
        :root {
            --primary-color: #ff6b6b;
            --secondary-color: #4ecdc4;
        }

        body {
            margin: 0;
            overflow: hidden;
            font-family: 'Comic Sans MS', cursive;
            background: linear-gradient(45deg, #2c3e50, #3498db);
        }

        /* 粒子背景 */
        #particles-js {
            position: fixed;
            width: 100%;
            height: 100%;
            z-index: -1;
        }

        /* 3D贺卡容器 */
        .card-container {
            perspective: 1000px;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        /* 可翻转的3D贺卡 */
        .card {
            width: 400px;
            height: 500px;
            transform-style: preserve-3d;
            transition: all 1s;
            cursor: pointer;
        }

        .card:hover {
            transform: rotateY(180deg);
        }

        /* 贺卡正反面 */
        .front, .back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }

        .front {
            background: url('birthday-bg.jpg') center/cover;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .back {
            background: #fff;
            transform: rotateY(180deg);
            text-align: center;
        }

        /* 文字动画 */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0px); }
        }

        .title {
            font-size: 2.5em;
            color: var(--primary-color);
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            animation: float 3s infinite;
        }

        /* 按钮特效 */
        .btn {
            padding: 15px 30px;
            background: var(--secondary-color);
            border: none;
            border-radius: 25px;
            color: white;
            font-size: 1.2em;
            cursor: pointer;
            transition: all 0.3s;
        }

        .btn:hover {
            transform: scale(1.1);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
    </style>
</head>
<body>
    <!-- 粒子背景 -->
    <div id="particles-js"></div>

    <!-- 3D贺卡 -->
    <div class="card-container">
        <div class="card">
            <div class="front">
                <h1 class="title">Happy Birthday!</h1>
                <p>🎈 Click to open your surprise 🎁</p>
            </div>
            <div class="back">
                <h2>Dear 周丹</h2>
                <p>✨ On your special day, I wish you:</p>
                <ul>
                    <li>Endless Joy 🌈</li>
                    <li>Exciting Adventures 🚀</li>
                    <li>Amazing Success 💎</li>
                </ul>
                <button class="btn" onclick="showFireworks()">Claim Your Blessing!</button>
            </div>
        </div>
    </div>

    <!-- 音频 -->
    <audio id="bgm" loop>
        <source src="happy-birthday.mp3" type="audio/mpeg">
    </audio>

    <script src="https://cdn.jsdelivr.net/particles.js/2.0.0/particles.min.js"></script>
    <script>
        // 粒子背景配置
        particlesJS('particles-js', {
            particles: {
                number: { value: 80 },
                color: { value: '#ffffff' },
                shape: { type: 'circle' },
                opacity: { random: true },
                size: { random: true },
                move: {
                    enable: true,
                    speed: 2,
                    direction: 'none',
                    straight: false
                }
            }
        });

        // 烟花特效
        function showFireworks() {
            const colors = ['#ff0000', '#00ff00', '#0000ff'];
            for(let i=0; i<50; i++) {
                const particle = document.createElement('div');
                particle.style = `
                    position: fixed;
                    left: ${Math.random()*100}%;
                    top: ${Math.random()*100}%;
                    width: 5px;
                    height: 5px;
                    background: ${colors[Math.floor(Math.random()*3)]};
                    border-radius: 50%;
                    animation: explode 1s forwards;
                `;
                document.body.appendChild(particle);
            }
            document.getElementById('bgm').play();
        }

        // 自动播放音乐（可能需要用户交互）
        document.body.onclick = () => {
            document.getElementById('bgm').play();
        }
    </script>
</body>
</html>