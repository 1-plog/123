# 123
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>太乙真人四重小游戏合集</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a0a2e, #2d0b50);
            min-height: 100vh;
            color: #fff;
            padding: 20px;
            overflow-x: hidden;
        }
        
        .header {
            text-align: center;
            padding: 20px 0;
            margin-bottom: 30px;
            position: relative;
        }
        
        h1 {
            font-size: 3.5rem;
            color: #ffcc00;
            text-shadow: 0 0 15px rgba(255, 204, 0, 0.7);
            margin-bottom: 15px;
            letter-spacing: 3px;
        }
        
        .subtitle {
            font-size: 1.5rem;
            color: #aaccff;
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.6;
        }
        
        .games-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 25px;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .game-card {
            background: rgba(25, 15, 50, 0.85);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            border: 2px solid #6a3093;
            transition: transform 0.4s ease, box-shadow 0.4s ease;
            height: 500px;
            display: flex;
            flex-direction: column;
        }
        
        .game-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.7);
            border-color: #ff9933;
        }
        
        .game-header {
            background: linear-gradient(90deg, #ff3366, #ff9933);
            padding: 20px;
            text-align: center;
            border-bottom: 3px solid #ffcc00;
        }
        
        .game-title {
            font-size: 2rem;
            font-weight: bold;
            color: white;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.4);
        }
        
        .game-content {
            padding: 25px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }
        
        .game-description {
            font-size: 1.1rem;
            line-height: 1.6;
            margin-bottom: 25px;
            color: #d0d0ff;
            min-height: 80px;
        }
        
        .game-area {
            background: rgba(40, 20, 70, 0.6);
            border-radius: 15px;
            padding: 15px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: relative;
            overflow: hidden;
        }
        
        /* 游戏1：太乙真人打太极 */
        .taiyi-character {
            width: 200px;
            height: 200px;
            position: relative;
            margin: 20px auto;
        }
        
        .taiyi-body {
            width: 120px;
            height: 120px;
            background: #ffcc99;
            border-radius: 50%;
            position: absolute;
            top: 40px;
            left: 40px;
            z-index: 2;
        }
        
        .taiyi-robe {
            width: 180px;
            height: 180px;
            background: linear-gradient(135deg, #4a86e8, #1c4587);
            border-radius: 50%;
            position: absolute;
            top: 10px;
            left: 10px;
            z-index: 1;
        }
        
        .taiyi-yin-yang {
            width: 100px;
            height: 100px;
            background: linear-gradient(to right, #000 50%, #fff 50%);
            border-radius: 50%;
            position: absolute;
            top: 50px;
            left: 50px;
            z-index: 3;
            animation: rotate 10s linear infinite;
        }
        
        .taiyi-yin-yang::before,
        .taiyi-yin-yang::after {
            content: "";
            position: absolute;
            width: 40px;
            height: 40px;
            border-radius: 50%;
        }
        
        .taiyi-yin-yang::before {
            background: #fff;
            top: 10px;
            left: 30px;
        }
        
        .taiyi-yin-yang::after {
            background: #000;
            bottom: 10px;
            right: 30px;
        }
        
        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        
        .taiyi-actions {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            width: 100%;
            margin-top: 20px;
        }
        
        .action-btn {
            background: linear-gradient(135deg, #ff3366, #ff9933);
            color: white;
            border: none;
            padding: 15px;
            font-size: 1.2rem;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(255, 51, 102, 0.4);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }
        
        .action-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 51, 102, 0.6);
        }
        
        /* 游戏2：哪吒打怪兽拼音匹配 */
        .monsters-row {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 15px 0;
        }
        
        .monster-card {
            width: 80px;
            height: 100px;
            background: rgba(40, 20, 70, 0.8);
            border-radius: 15px;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 10px;
            border: 2px solid transparent;
            transition: all 0.3s ease;
        }
        
        .monster-card:hover {
            transform: translateY(-5px);
            border-color: #ffcc00;
        }
        
        .monster-image {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 30px;
            margin-bottom: 8px;
        }
        
        .dragon { background: linear-gradient(135deg, #4a86e8, #1c4587); }
        .leopard { background: linear-gradient(135deg, #e69138, #783f04); }
        .rat { background: linear-gradient(135deg, #b7b7b7, #666666); }
        
        .monster-name {
            font-size: 16px;
            font-weight: bold;
        }
        
        .pinyin-row {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 15px 0;
        }
        
        .pinyin-btn {
            width: 80px;
            height: 50px;
            background: #ff9933;
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 2px solid #ff6600;
        }
        
        .pinyin-btn:hover {
            background: #ffcc00;
            transform: translateY(-3px);
        }
        
        .match-feedback {
            margin-top: 15px;
            font-size: 18px;
            min-height: 30px;
            text-align: center;
        }
        
        /* 游戏3：风火轮跑酷 */
        .runway {
            width: 100%;
            height: 200px;
            background: linear-gradient(to bottom, #3a1c71, #d76d77, #ffaf7b);
            border-radius: 10px;
            position: relative;
            overflow: hidden;
            margin-top: 10px;
        }
        
        .nezha-runner {
            width: 60px;
            height: 60px;
            position: absolute;
            bottom: 20px;
            left: 50px;
            z-index: 10;
        }
        
        .nezha-head {
            width: 25px;
            height: 25px;
            background: #ffcc99;
            border-radius: 50%;
            position: absolute;
            top: 0;
            left: 18px;
            z-index: 2;
        }
        
        .nezha-body {
            width: 30px;
            height: 30px;
            background: #e63946;
            position: absolute;
            top: 20px;
            left: 15px;
            border-radius: 10px 10px 0 0;
            z-index: 1;
        }
        
        .fire-wheel {
            width: 40px;
            height: 40px;
            background: radial-gradient(circle, #ffcc00, #ff6600);
            border-radius: 50%;
            position: absolute;
            top: 35px;
            left: 10px;
            z-index: 0;
            animation: rotate 1s linear infinite;
        }
        
        .obstacle {
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, #4a86e8, #1c4587);
            position: absolute;
            bottom: 20px;
            right: -50px;
            border-radius: 10px;
        }
        
        .controls {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
        }
        
        .control-btn {
            width: 60px;
            height: 60px;
            background: rgba(255, 153, 51, 0.8);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 24px;
            cursor: pointer;
            border: 2px solid #ff6600;
        }
        
        /* 游戏4：乾坤圈投掷 */
        .throwing-area {
            width: 100%;
            height: 200px;
            background: linear-gradient(to bottom, #56ab2f, #a8e063);
            border-radius: 10px;
            position: relative;
            overflow: hidden;
            margin-top: 10px;
        }
        
        .nezha-thrower {
            width: 50px;
            height: 80px;
            position: absolute;
            bottom: 10px;
            left: 50px;
        }
        
        .target {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #ff3366, #cc0044);
            border-radius: 50%;
            position: absolute;
            bottom: 30px;
            right: 50px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 24px;
        }
        
        .qiankun-quan {
            width: 30px;
            height: 30px;
            background: radial-gradient(circle, #ffcc00, #ff6600);
            border-radius: 50%;
            position: absolute;
            bottom: 60px;
            left: 80px;
            display: none;
        }
        
        .throw-controls {
            display: flex;
            flex-direction: column;
            gap: 10px;
            margin-top: 15px;
        }
        
        .slider-container {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .slider {
            flex-grow: 1;
            height: 20px;
            -webkit-appearance: none;
            background: linear-gradient(to right, #ff3366, #ff9933);
            border-radius: 10px;
            outline: none;
        }
        
        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 25px;
            height: 25px;
            border-radius: 50%;
            background: #ffcc00;
            cursor: pointer;
            box-shadow: 0 0 5px rgba(0,0,0,0.5);
        }
        
        .throw-btn {
            background: linear-gradient(135deg, #ff3366, #ff9933);
            color: white;
            border: none;
            padding: 12px;
            font-size: 1.1rem;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-top: 10px;
        }
        
        .throw-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(255, 51, 102, 0.4);
        }
        
        .footer {
            text-align: center;
            padding: 30px 0;
            margin-top: 40px;
            color: #aaccff;
            border-top: 1px solid #6a3093;
        }
        
        @media (max-width: 768px) {
            .games-container {
                grid-template-columns: 1fr;
            }
            
            h1 {
                font-size: 2.5rem;
            }
            
            .subtitle {
                font-size: 1.2rem;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>太乙真人四重小游戏合集</h1>
        <div class="subtitle">
            体验中国神话主题的趣味小游戏，包含打太极、拼音匹配、风火轮跑酷和乾坤圈投掷
        </div>
    </div>
    
    <div class="games-container">
        <!-- 游戏1：太乙真人打太极 -->
        <div class="game-card">
            <div class="game-header">
                <div class="game-title">太乙真人打太极</div>
            </div>
            <div class="game-content">
                <div class="game-description">
                    模仿太乙真人的太极动作！按照提示做出相应动作，完成一套太极拳法。
                </div>
                <div class="game-area">
                    <div class="taiyi-character">
                        <div class="taiyi-robe"></div>
                        <div class="taiyi-body"></div>
                        <div class="taiyi-yin-yang"></div>
                    </div>
                    
                    <div class="taiyi-actions">
                        <button class="action-btn"><i class="fas fa-wind"></i> 吸气</button>
                        <button class="action-btn"><i class="fas fa-arrow-up"></i> 向上</button>
                        <button class="action-btn"><i class="fas fa-wind"></i> 呼气</button>
                        <button class="action-btn"><i class="fas fa-arrow-down"></i> 向下</button>
                    </div>
                    
                    <div style="margin-top: 20px; text-align: center;">
                        <button class="action-btn" style="grid-column: span 2;">
                            <i class="fas fa-video"></i> 上传练习视频
                        </button>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- 游戏2：哪吒打怪兽拼音匹配 -->
        <div class="game-card">
            <div class="game-header">
                <div class="game-title">哪吒打怪兽拼音匹配</div>
            </div>
            <div class="game-content">
                <div class="game-description">
                    帮助哪吒打败怪兽！将每个怪兽与正确的拼音匹配，全部正确即可获胜。
                </div>
                <div class="game-area">
                    <div class="monsters-row">
                        <div class="monster-card">
                            <div class="monster-image dragon">🐉</div>
                            <div class="monster-name">龙</div>
                        </div>
                        <div class="monster-card">
                            <div class="monster-image leopard">🐆</div>
                            <div class="monster-name">豹</div>
                        </div>
                        <div class="monster-card">
                            <div class="monster-image rat">🐀</div>
                            <div class="monster-name">鼠</div>
                        </div>
                    </div>
                    
                    <div class="pinyin-row">
                        <div class="pinyin-btn">bào</div>
                        <div class="pinyin-btn">lóng</div>
                        <div class="pinyin-btn">shǔ</div>
                    </div>
                    
                    <div class="match-feedback">
                        请选择怪兽和对应的拼音
                    </div>
                    
                    <div style="margin-top: auto;">
                        <button class="action-btn">
                            <i class="fas fa-sync-alt"></i> 重新开始游戏
                        </button>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- 游戏3：风火轮跑酷 -->
        <div class="game-card">
            <div class="game-header">
                <div class="game-title">风火轮跑酷</div>
            </div>
            <div class="game-content">
                <div class="game-description">
                    控制哪吒躲避障碍物！使用方向键或下方按钮控制哪吒上下移动。
                </div>
                <div class="game-area">
                    <div class="runway">
                        <div class="nezha-runner">
                            <div class="nezha-head"></div>
                            <div class="nezha-body"></div>
                            <div class="fire-wheel"></div>
                        </div>
                        <div class="obstacle"></div>
                    </div>
                    
                    <div class="controls">
                        <div class="control-btn"><i class="fas fa-arrow-up"></i></div>
                        <div class="control-btn"><i class="fas fa-arrow-down"></i></div>
                    </div>
                    
                    <div style="margin-top: 15px; text-align: center; width: 100%;">
                        <div>得分: <span id="score">0</span></div>
                        <div>生命: <span id="lives">3</span></div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- 游戏4：乾坤圈投掷 -->
        <div class="game-card">
            <div class="game-header">
                <div class="game-title">乾坤圈投掷</div>
            </div>
            <div class="game-content">
                <div class="game-description">
                    使用乾坤圈击中目标！调整角度和力度，精准投掷乾坤圈。
                </div>
                <div class="game-area">
                    <div class="throwing-area">
                        <div class="nezha-thrower">
                            <div class="nezha-head"></div>
                            <div class="nezha-body"></div>
                        </div>
                        <div class="target">🎯</div>
                        <div class="qiankun-quan"></div>
                    </div>
                    
                    <div class="throw-controls">
                        <div class="slider-container">
                            <span>角度:</span>
                            <input type="range" min="0" max="90" value="45" class="slider" id="angle-slider">
                            <span id="angle-value">45°</span>
                        </div>
                        
                        <div class="slider-container">
                            <span>力度:</span>
                            <input type="range" min="10" max="100" value="50" class="slider" id="power-slider">
                            <span id="power-value">50%</span>
                        </div>
                        
                        <button class="throw-btn">
                            <i class="fas fa-bullseye"></i> 投掷乾坤圈
                        </button>
                    </div>
                    
                    <div style="margin-top: 10px; text-align: center;">
                        <div>命中次数: <span id="hits">0</span></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <div class="footer">
        <p>太乙真人四重小游戏合集 | 中国神话主题趣味游戏</p>
        <p>使用HTML5、CSS3和JavaScript实现 | 无需安装，在线畅玩</p>
    </div>
    
    <script>
        // 游戏2：哪吒打怪兽拼音匹配逻辑
        document.querySelectorAll('.monster-card').forEach(card => {
            card.addEventListener('click', function() {
                document.querySelectorAll('.monster-card').forEach(c => {
                    c.style.borderColor = 'transparent';
                });
                this.style.borderColor = '#ffcc00';
                document.querySelector('.match-feedback').textContent = `已选择: ${this.querySelector('.monster-name').textContent}`;
            });
        });
        
        document.querySelectorAll('.pinyin-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                const selectedMonster = document.querySelector('.monster-card[style*="border-color: rgb(255, 204, 0)"]');
                if (selectedMonster) {
                    const monsterName = selectedMonster.querySelector('.monster-name').textContent;
                    const correctPinyins = {
                        '龙': 'lóng',
                        '豹': 'bào',
                        '鼠': 'shǔ'
                    };
                    
                    if (this.textContent === correctPinyins[monsterName]) {
                        document.querySelector('.match-feedback').textContent = `正确！${monsterName}的拼音是${this.textContent}`;
                        document.querySelector('.match-feedback').style.color = '#00cc99';
                        this.style.background = '#00cc99';
                        
                        // 重置选择
                        document.querySelectorAll('.monster-card').forEach(c => {
                            c.style.borderColor = 'transparent';
                        });
                    } else {
                        document.querySelector('.match-feedback').textContent = `错误！${monsterName}的拼音是${correctPinyins[monsterName]}`;
                        document.querySelector('.match-feedback').style.color = '#ff3366';
                        this.style.background = '#ff3366';
                        
                        // 短暂恢复颜色
                        setTimeout(() => {
                            this.style.background = '#ff9933';
                        }, 500);
                    }
                } else {
                    document.querySelector('.match-feedback').textContent = '请先选择一个怪兽';
                    document.querySelector('.match-feedback').style.color = '#ffcc00';
                }
            });
        });
        
        // 游戏4：乾坤圈投掷逻辑
        const angleSlider = document.getElementById('angle-slider');
        const powerSlider = document.getElementById('power-slider');
        const angleValue = document.getElementById('angle-value');
        const powerValue = document.getElementById('power-value');
        const throwBtn = document.querySelector('.throw-btn');
        const qiankunQuan = document.querySelector('.qiankun-quan');
        const hitsElement = document.getElementById('hits');
        let hits = 0;
        
        angleSlider.addEventListener('input', function() {
            angleValue.textContent = `${this.value}°`;
        });
        
        powerSlider.addEventListener('input', function() {
            powerValue.textContent = `${this.value}%`;
        });
        
        throwBtn.addEventListener('click', function() {
            const angle = parseInt(angleSlider.value);
            const power = parseInt(powerSlider.value);
            
            // 显示乾坤圈
            qiankunQuan.style.display = 'block';
            qiankunQuan.style.bottom = '60px';
            qiankunQuan.style.left = '80px';
            
            // 模拟投掷动画
            let posX = 80;
            let posY = 60;
            let velocityX = power * Math.cos(angle * Math.PI / 180) / 10;
            let velocityY = -power * Math.sin(angle * Math.PI / 180) / 10;
            const gravity = 0.2;
            
            const throwAnimation = setInterval(() => {
                posX += velocityX;
                posY += velocityY;
                velocityY += gravity;
                
                qiankunQuan.style.left = `${posX}px`;
                qiankunQuan.style.bottom = `${posY}px`;
                
                // 检查是否击中目标 (目标位置：right:50px, bottom:30px)
                if (posX > 250 && posX < 310 && posY > 20 && posY < 50) {
                    hits++;
                    hitsElement.textContent = hits;
                    document.querySelector('.target').style.transform = 'scale(1.2)';
                    setTimeout(() => {
                        document.querySelector('.target').style.transform = 'scale(1)';
                    }, 300);
                    clearInterval(throwAnimation);
                    setTimeout(() => {
                        qiankunQuan.style.display = 'none';
                    }, 300);
                }
                
                // 检查是否超出边界
                if (posX > 350 || posY > 200) {
                    clearInterval(throwAnimation);
                    setTimeout(() => {
                        qiankunQuan.style.display = 'none';
                    }, 300);
                }
            }, 30);
        });
        
        // 游戏3：风火轮跑酷简单模拟
        const scoreElement = document.getElementById('score');
        const livesElement = document.getElementById('lives');
        const obstacle = document.querySelector('.obstacle');
        let score = 0;
        let lives = 3;
        
        // 简单模拟障碍物移动
        setInterval(() => {
            const currentRight = parseInt(obstacle.style.right || '-50px');
            obstacle.style.right = `${currentRight + 5}px`;
            
            if (currentRight > 350) {
                obstacle.style.right = '-50px';
                score += 5;
                scoreElement.textContent = score;
            }
        }, 100);
        
        // 控制按钮事件
        document.querySelectorAll('.control-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                const nezha = document.querySelector('.nezha-runner');
                const currentBottom = parseInt(nezha.style.bottom || '20px');
                
                if (this.querySelector('i').classList.contains('fa-arrow-up')) {
                    nezha.style.bottom = `${Math.min(currentBottom + 30, 140)}px`;
                } else {
                    nezha.style.bottom = `${Math.max(currentBottom - 30, 20)}px`;
                }
            });
        });
        
        // 键盘控制事件
        document.addEventListener('keydown', (e) => {
            const nezha = document.querySelector('.nezha-runner');
            const currentBottom = parseInt(nezha.style.bottom || '20px');
            
            if (e.key === 'ArrowUp') {
                nezha.style.bottom = `${Math.min(currentBottom + 30, 140)}px`;
            } else if (e.key === 'ArrowDown') {
                nezha.style.bottom = `${Math.max(currentBottom - 30, 20)}px`;
            }
        });
    </script>
</body>
</html>
