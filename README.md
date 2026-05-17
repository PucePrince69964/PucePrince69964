### ꒷꒦ ୨🧑‍💻୧ ***D E S E N V O L V E D O R・F U L L - S T A C K*** ꒱੭

Me chamo Gabriel Yago, tenho 18 anos e sou natural de São Paulo. Desde os meus 13 anos, interessei-me por programação com o desenvolvimento web. Com o tempo, participei de projetos de Arduino e automações, como a OBSAT e o Contador Dimensional Volumétrico apresentado na empresa SIEMENS em Jundiaí. E agora, no Ensino Superior, continuo evoluindo meu nível de desenvolvedor, abrangendo interesses por outros ramos de estudo da tecnologia, como a Engenharia de Prompt, e trazendo algumas produções práticas para contribuir para o meu conhecimento.

Para mais informações, acesse o meu [LinkedIn](www.linkedin.com/in/gabriel-yago-02293a393).

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stand Stats - Gabriel Yago</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 100%);
            font-family: 'Courier New', 'Trebuchet MS', monospace;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        /* Container estilo carta de Stand */
        .stand-card {
            background: rgba(0, 0, 0, 0.85);
            backdrop-filter: blur(10px);
            border: 3px solid #ffd700;
            border-radius: 20px;
            padding: 25px;
            max-width: 800px;
            width: 100%;
            box-shadow: 0 0 30px rgba(255, 215, 0, 0.3);
            transition: transform 0.3s;
        }

        .stand-card:hover {
            transform: scale(1.02);
        }

        /* Cabeçalho estilo anime */
        .stand-header {
            text-align: center;
            border-bottom: 2px dashed #ffd700;
            padding-bottom: 15px;
            margin-bottom: 20px;
        }

        .stand-user {
            font-size: 0.9rem;
            color: #aaa;
            letter-spacing: 2px;
        }

        .stand-user span {
            color: #ffd700;
            font-weight: bold;
        }

        .stand-name {
            font-size: 2rem;
            font-weight: bold;
            color: #ffd700;
            text-shadow: 2px 2px 0 #8b0000;
            margin-top: 5px;
        }

        .stand-dest {
            font-size: 1rem;
            color: #ff6347;
            font-style: italic;
        }

        /* Container do gráfico */
        .graph-container {
            display: flex;
            justify-content: center;
            margin: 20px 0;
        }

        canvas {
            background: rgba(0, 0, 0, 0.6);
            border-radius: 15px;
            padding: 10px;
            max-width: 100%;
            height: auto;
        }

        /* Legenda dos atributos */
        .stats-legend {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px solid #333;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 0.85rem;
            color: #ddd;
            background: rgba(255, 215, 0, 0.1);
            padding: 6px 10px;
            border-radius: 25px;
        }

        .legend-symbol {
            font-size: 1.2rem;
            font-weight: bold;
            width: 35px;
            text-align: center;
        }

        .legend-symbol.A { color: #ff5555; text-shadow: 0 0 3px #ff0000; }
        .legend-symbol.B { color: #ffaa55; }
        .legend-symbol.C { color: #ffff55; }
        .legend-symbol.D { color: #55ff55; }
        .legend-symbol.E { color: #55aaff; }
        .legend-symbol.F { color: #cc55ff; }

        .legend-name { flex: 1; }
        .legend-value { font-weight: bold; color: #ffd700; }

        /* Rodapé */
        .stand-footer {
            text-align: center;
            margin-top: 20px;
            font-size: 0.7rem;
            color: #666;
        }

        /* Responsivo */
        @media (max-width: 500px) {
            .stand-card { padding: 15px; }
            .stand-name { font-size: 1.3rem; }
            .stats-legend { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <div class="stand-card">
        <div class="stand-header">
            <div class="stand-user">
                「 <span>S T A N D   M A S T E R</span> 」
            </div>
            <div class="stand-name">
                ガブリエル・ヤゴ
            </div>
            <div class="stand-dest">
                ✦ Gabriel Yago ✦
            </div>
        </div>

        <div class="graph-container">
            <canvas id="radarChart" width="400" height="400"></canvas>
        </div>

        <div class="stats-legend">
            <div class="legend-item">
                <div class="legend-symbol A">破</div>
                <div class="legend-name">Front-end</div>
                <div class="legend-value">A → 90%</div>
            </div>
            <div class="legend-item">
                <div class="legend-symbol B">填</div>
                <div class="legend-name">Back-end</div>
                <div class="legend-value">B → 75%</div>
            </div>
            <div class="legend-item">
                <div class="legend-symbol C">力</div>
                <div class="legend-name">Hardware/IoT</div>
                <div class="legend-value">C → 65%</div>
            </div>
            <div class="legend-item">
                <div class="legend-symbol D">持</div>
                <div class="legend-name">Lógica & Debug</div>
                <div class="legend-value">D → 80%</div>
            </div>
            <div class="legend-item">
                <div class="legend-symbol E">速</div>
                <div class="legend-name">Aprendizado Rápido</div>
                <div class="legend-value">E → 95%</div>
            </div>
            <div class="legend-item">
                <div class="legend-symbol F">攻</div>
                <div class="legend-name">Comunicação Técnica</div>
                <div class="legend-value">F → 70%</div>
            </div>
        </div>

        <div class="stand-footer">
            「 R E Q U I E M   P O W E R 」
        </div>
    </div>

    <script>
        (function() {
            const canvas = document.getElementById('radarChart');
            const ctx = canvas.getContext('2d');
            
            // Dados dos atributos (valores de 0 a 100)
            const stats = [90, 75, 65, 80, 95, 70]; // A, B, C, D, E, F
            
            // Nomes dos atributos
            const labels = ['破\nFront', '填\nBack', '力\nIoT', '持\nLógica', '速\nAprende', '攻\nComun'];
            
            // Cores
            const bgColor = 'rgba(255, 215, 0, 0.25)';
            const borderColor = '#ffd700';
            const pointColor = '#ffaa00';
            const gridColor = 'rgba(255, 215, 0, 0.4)';
            const textColor = '#ffffff';
            
            const w = canvas.width;
            const h = canvas.height;
            const centerX = w / 2;
            const centerY = h / 2;
            const radius = Math.min(w, h) * 0.35;
            
            // Ângulos (hexágono)
            const angles = [];
            for (let i = 0; i < 6; i++) {
                angles.push((Math.PI * 2 * i / 6) - Math.PI / 2);
            }
            
            function drawRadar() {
                ctx.clearRect(0, 0, w, h);
                
                // === Grade circular (níveis 20%, 40%, 60%, 80%, 100%) ===
                for (let level = 1; level <= 5; level++) {
                    const r = radius * (level / 5);
                    ctx.beginPath();
                    for (let i = 0; i <= 6; i++) {
                        const angle = angles[i % 6];
                        const x = centerX + r * Math.cos(angle);
                        const y = centerY + r * Math.sin(angle);
                        if (i === 0) ctx.moveTo(x, y);
                        else ctx.lineTo(x, y);
                    }
                    ctx.closePath();
                    ctx.strokeStyle = gridColor;
                    ctx.lineWidth = 0.8;
                    ctx.stroke();
                }
                
                // === Linhas radiais ===
                for (let i = 0; i < 6; i++) {
                    const angle = angles[i];
                    const x = centerX + radius * Math.cos(angle);
                    const y = centerY + radius * Math.sin(angle);
                    ctx.beginPath();
                    ctx.moveTo(centerX, centerY);
                    ctx.lineTo(x, y);
                    ctx.strokeStyle = gridColor;
                    ctx.lineWidth = 1;
                    ctx.stroke();
                }
                
                // === Área dos stats ===
                ctx.beginPath();
                for (let i = 0; i < 6; i++) {
                    const value = stats[i] / 100;
                    const r = radius * value;
                    const angle = angles[i];
                    const x = centerX + r * Math.cos(angle);
                    const y = centerY + r * Math.sin(angle);
                    if (i === 0) ctx.moveTo(x, y);
                    else ctx.lineTo(x, y);
                }
                ctx.closePath();
                ctx.fillStyle = bgColor;
                ctx.fill();
                ctx.strokeStyle = borderColor;
                ctx.lineWidth = 2.5;
                ctx.stroke();
                
                // === Pontos nos vértices ===
                for (let i = 0; i < 6; i++) {
                    const value = stats[i] / 100;
                    const r = radius * value;
                    const angle = angles[i];
                    const x = centerX + r * Math.cos(angle);
                    const y = centerY + r * Math.sin(angle);
                    ctx.beginPath();
                    ctx.arc(x, y, 5, 0, 2 * Math.PI);
                    ctx.fillStyle = pointColor;
                    ctx.fill();
                    ctx.shadowBlur = 6;
                    ctx.shadowColor = '#ffd700';
                    ctx.fill();
                    ctx.shadowBlur = 0;
                }
                
                // === Rótulos dos atributos ===
                ctx.font = 'bold 12px "Courier New", monospace';
                ctx.fillStyle = textColor;
                ctx.shadowBlur = 0;
                for (let i = 0; i < 6; i++) {
                    const angle = angles[i];
                    const r = radius + 18;
                    let x = centerX + r * Math.cos(angle);
                    let y = centerY + r * Math.sin(angle);
                    ctx.fillText(labels[i], x - 15, y + 4);
                }
                
                // === Título central ===
                ctx.font = 'bold 18px "Courier New", monospace';
                ctx.fillStyle = '#ffd700';
                ctx.shadowBlur = 3;
                ctx.fillText('S T A T S', centerX - 35, centerY + 5);
                ctx.font = '10px monospace';
                ctx.fillStyle = '#aaa';
                ctx.fillText('DESTRUCTION', centerX - 38, centerY + 25);
                ctx.shadowBlur = 0;
            }
            
            drawRadar();
            
            // Redraw on resize (ajuste fino)
            window.addEventListener('resize', () => setTimeout(drawRadar, 100));
        })();
    </script>
</body>
</html>
