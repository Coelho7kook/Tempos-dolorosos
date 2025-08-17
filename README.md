echo "# Tempos-dolorosos" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/Coelho7kook/Tempos-dolorosos.git
git push -u origin main


<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Amor por Você</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Montserrat:wght@400;600&family=Pacifico&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background: linear-gradient(135deg, #1a1a2e, #16213e, #0f3460);
            background-size: 400% 400%;
            animation: gradientBG 15s ease infinite;
            height: 100vh;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #fff;
            position: relative;
        }
        
        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .container {
            width: 90%;
            max-width: 800px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 25px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
            overflow: hidden;
            position: relative;
            z-index: 10;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            animation: fadeIn 1.5s ease-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        header {
            background: linear-gradient(to right, #e94560, #e11d74);
            padding: 30px 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        h1 {
            font-family: 'Pacifico', cursive;
            font-size: 3.5rem;
            color: white;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
            margin-bottom: 10px;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .heart-loader {
            font-size: 4rem;
            color: #ff6b6b;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            opacity: 0;
            z-index: 5;
            animation: pulse 1.5s infinite;
        }
        
        .content {
            padding: 30px;
            text-align: center;
        }
        
        .question-container {
            min-height: 250px;
            position: relative;
            border: 3px dashed rgba(255, 175, 189, 0.5);
            border-radius: 15px;
            margin: 20px 0;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 30px;
            background: rgba(255, 235, 238, 0.1);
            transition: all 0.5s ease;
        }
        
        .question-container h2 {
            font-size: 1.8rem;
            margin-bottom: 30px;
            color: #ffb8c6;
            font-weight: 600;
            text-shadow: 0 0 10px rgba(255, 184, 198, 0.5);
        }
        
        .buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        button {
            padding: 15px 40px;
            font-size: 1.2rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        #yesBtn {
            background: linear-gradient(to right, #4CAF50, #2E7D32);
            color: white;
            z-index: 2;
        }
        
        #yesBtn:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(46, 125, 50, 0.4);
        }
        
        #noBtn {
            background: linear-gradient(to right, #f44336, #c62828);
            color: white;
            position: absolute;
            transition: all 0.3s ease;
        }
        
        .result-container {
            display: none;
            text-align: center;
            padding: 20px;
            animation: fadeIn 1s ease;
        }
        
        .result-container h2 {
            font-family: 'Dancing Script', cursive;
            font-size: 3rem;
            color: #ffb8c6;
            margin: 20px 0;
            text-shadow: 0 0 15px rgba(255, 184, 198, 0.7);
        }
        
        .message {
            font-size: 1.2rem;
            line-height: 1.8;
            margin: 20px 0;
            padding: 20px;
            background: rgba(255, 235, 238, 0.1);
            border-radius: 15px;
            text-align: left;
            animation: slideIn 1s ease;
            border: 1px solid rgba(255, 184, 198, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        @keyframes slideIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .message p {
            margin-bottom: 15px;
            position: relative;
            z-index: 2;
        }
        
        .message::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, rgba(233, 69, 96, 0.1), rgba(225, 29, 116, 0.1));
            z-index: 1;
        }
        
        .gif-container {
            margin: 20px 0;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
            animation: float 3s ease-in-out infinite;
            border: 2px solid rgba(255, 184, 198, 0.5);
        }
        
        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0); }
        }
        
        .gif-container img {
            width: 100%;
            max-width: 500px;
            display: block;
            border-radius: 15px;
        }
        
        .audio-control {
            margin: 20px 0;
            background: rgba(255, 235, 238, 0.2);
            padding: 15px 30px;
            border-radius: 50px;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 184, 198, 0.3);
            font-weight: 600;
        }
        
        .audio-control:hover {
            transform: scale(1.05);
            background: rgba(255, 235, 238, 0.3);
            box-shadow: 0 0 15px rgba(255, 184, 198, 0.3);
        }
        
        .audio-control i {
            font-size: 1.5rem;
            color: #ffb8c6;
        }
        
        .hearts {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }
        
        .heart {
            position: absolute;
            width: 20px;
            height: 20px;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path fill="%23ff6b6b" d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>') no-repeat;
            background-size: contain;
            opacity: 0;
        }
        
        .distance-bar {
            height: 6px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 3px;
            margin: 30px auto;
            max-width: 500px;
            position: relative;
            overflow: hidden;
        }
        
        .distance-progress {
            position: absolute;
            height: 100%;
            width: 70%;
            background: linear-gradient(to right, #e94560, #ffb8c6);
            border-radius: 3px;
            animation: progressPulse 3s infinite;
        }
        
        @keyframes progressPulse {
            0% { opacity: 0.7; }
            50% { opacity: 1; }
            100% { opacity: 0.7; }
        }
        
        .distance-text {
            margin-top: 10px;
            font-size: 1rem;
            color: #ffb8c6;
        }
        
        footer {
            text-align: center;
            padding: 20px;
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
            background: rgba(0, 0, 0, 0.2);
            border-top: 1px solid rgba(255, 182, 193, 0.1);
        }
        
        /* Responsividade */
        @media (max-width: 768px) {
            h1 { font-size: 2.5rem; }
            .question-container h2 { font-size: 1.5rem; }
            button { padding: 12px 30px; font-size: 1rem; }
            .result-container h2 { font-size: 2.5rem; }
        }
        
        @media (max-width: 480px) {
            .buttons { flex-direction: column; align-items: center; }
            #noBtn { position: relative; margin-top: 10px; }
        }
    </style>
</head>
<body>
    <div class="hearts" id="hearts"></div>
    
    <div class="container">
        <header>
            <h1>Para Minha Estrela Distante</h1>
            <div class="heart-loader" id="heartLoader">❤️</div>
        </header>
        
        <div class="content">
            <div class="question-container" id="questionContainer">
                <h2>Minha Querida, mesmo à distância, você aceita continuar sendo minha para sempre?</h2>
                <div class="buttons">
                    <button id="yesBtn">SIM, para todo o sempre!</button>
                    <button id="noBtn">Ainda não</button>
                </div>
            </div>
            
            <div class="result-container" id="resultContainer">
                <h2>Ebaaa! Você me faz o homem mais feliz, mesmo de longe!</h2>
                
                <div class="message">
                    <p>Meu amor, mesmo estando longe fisicamente, sinto você perto de mim a cada batida do meu coração. Cada dia longe de você é um dia a menos para o nosso tão esperado encontro.</p>
                    
                    <p>Seu sorriso, mesmo visto apenas por fotos, ilumina meus dias. Sua voz, mesmo vindo de longe, é a melodia que acalma minha alma. E seu amor, mesmo à distância, é o que me dá força para seguir em frente.</p>
                    
                    <p>Eu conto os minutos para o momento em que poderei te ver, te tocar, te abraçar e sentir o calor do seu corpo junto ao meu. Até lá, prometo preencher sua vida com amor, carinho e mensagens que te façam sentir o quanto você é especial para mim.</p>
                    
                    <p>Você é a estrela que guia meus passos, a musa que inspira meus sonhos e o amor que preenche cada pedacinho do meu ser. Obrigado por existir e por me permitir te amar.</p>
                </div>
                
                <div class="gif-container">
                    <img id="gifResult" src="amorr.gif" alt="Nosso amor à distância">
                </div>
                
                <div class="distance-bar">
                    <div class="distance-progress"></div>
                </div>
                <div class="distance-text">Distância entre nós: 70% percorrida até nosso encontro</div>
                
                <div class="audio-control" id="musicToggle">
                    <i>🎵</i>
                    <span>Nossa Música Especial</span>
                </div>
            </div>
        </div>
        
        <footer>
            Feito com todo o amor do mundo para você, minha eterna paixão
        </footer>
    </div>
    
    <audio id="bgMusic" loop>
        <source src="musica1.mp3" type="audio/mpeg">
        Seu navegador não suporta o elemento de áudio.
    </audio>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // Elementos DOM
            const noBtn = document.getElementById('noBtn');
            const yesBtn = document.getElementById('yesBtn');
            const questionContainer = document.getElementById('questionContainer');
            const heartLoader = document.getElementById('heartLoader');
            const resultContainer = document.getElementById('resultContainer');
            const musicToggle = document.getElementById('musicToggle');
            const bgMusic = document.getElementById('bgMusic');
            const heartsContainer = document.getElementById('hearts');
            
            // Criar corações flutuantes
            function createHearts() {
                setInterval(() => {
                    const heart = document.createElement('div');
                    heart.classList.add('heart');
                    
                    // Tamanho aleatório
                    const size = Math.random() * 30 + 10;
                    heart.style.width = `${size}px`;
                    heart.style.height = `${size}px`;
                    
                    // Posição inicial
                    heart.style.left = Math.random() * 100 + 'vw';
                    heart.style.top = '-50px';
                    
                    // Animação
                    const duration = Math.random() * 5 + 5;
                    heart.style.animation = `fall ${duration}s linear forwards`;
                    
                    // Adicionar ao container
                    heartsContainer.appendChild(heart);
                    
                    // Remover após animação
                    setTimeout(() => {
                        heart.remove();
                    }, duration * 1000);
                    
                    // Criar regra de animação
                    const keyframes = `@keyframes fall {
                        0% { transform: translateY(0) rotate(0deg); opacity: 0; }
                        10% { opacity: 1; }
                        90% { opacity: 0.8; }
                        100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
                    }`;
                    
                    const styleSheet = document.styleSheets[0];
                    styleSheet.insertRule(keyframes, styleSheet.cssRules.length);
                    
                }, 300);
            }
            
            // Iniciar animação de corações
            createHearts();
            
            // Botão "Não" foge do mouse
            noBtn.addEventListener("mouseover", () => {
                const containerRect = questionContainer.getBoundingClientRect();
                const btnRect = noBtn.getBoundingClientRect();
                
                const maxX = containerRect.width - btnRect.width - 30;
                const maxY = containerRect.height - btnRect.height - 30;
                
                const newX = Math.floor(Math.random() * maxX);
                const newY = Math.floor(Math.random() * maxY);
                
                noBtn.style.transform = `translate(${newX}px, ${newY}px)`;
                
                // Criar corações quando o botão foge
                for(let i = 0; i < 5; i++) {
                    const heart = document.createElement('div');
                    heart.classList.add('heart');
                    heart.style.width = '15px';
                    heart.style.height = '15px';
                    heart.style.left = `${newX + btnRect.width/2}px`;
                    heart.style.top = `${newY + btnRect.height/2}px`;
                    heart.style.animation = `fall ${Math.random() * 2 + 1}s linear forwards`;
                    heartsContainer.appendChild(heart);
                    
                    setTimeout(() => {
                        heart.remove();
                    }, 2000);
                }
            });
            
            // Botão "Sim" mostra resultado
            yesBtn.addEventListener("click", () => {
                // Animação de transição
                questionContainer.style.opacity = "0";
                questionContainer.style.transform = "translateY(-20px)";
                
                // Mostrar loader
                setTimeout(() => {
                    heartLoader.style.opacity = "1";
                    questionContainer.style.display = "none";
                }, 500);
                
                // Tocar música após 1s
                setTimeout(() => {
                    bgMusic.play();
                    musicToggle.querySelector('span').textContent = "Pausar Música";
                }, 1000);
                
                // Mostrar resultado após 3s
                setTimeout(() => {
                    heartLoader.style.opacity = "0";
                    setTimeout(() => {
                        heartLoader.style.display = "none";
                        resultContainer.style.display = "block";
                        
                        // Criar explosão de corações
                        for(let i = 0; i < 50; i++) {
                            const heart = document.createElement('div');
                            heart.classList.add('heart');
                            heart.style.width = `${Math.random() * 30 + 10}px`;
                            heart.style.height = heart.style.width;
                            heart.style.left = '50%';
                            heart.style.top = '50%';
                            
                            const angle = Math.random() * Math.PI * 2;
                            const distance = Math.random() * 300;
                            const x = Math.cos(angle) * distance;
                            const y = Math.sin(angle) * distance;
                            
                            heart.style.animation = `explode 1s forwards`;
                            
                            document.styleSheets[0].insertRule(`
                                @keyframes explode {
                                    0% { transform: translate(-50%, -50%) scale(0); opacity: 1; }
                                    100% { transform: translate(${x}px, ${y}px) scale(1); opacity: 0; }
                                }
                            `, document.styleSheets[0].cssRules.length);
                            
                            heartsContainer.appendChild(heart);
                            setTimeout(() => heart.remove(), 1000);
                        }
                    }, 500);
                }, 3000);
            });
            
            // Controle de música
            musicToggle.addEventListener("click", () => {
                if (bgMusic.paused) {
                    bgMusic.play();
                    musicToggle.querySelector('span').textContent = "Pausar Música";
                } else {
                    bgMusic.pause();
                    musicToggle.querySelector('span').textContent = "Tocar Música";
                }
            });
            
            // Efeito de digitação na mensagem
            const messageParagraphs = document.querySelectorAll('.message p');
            messageParagraphs.forEach((p, index) => {
                const text = p.textContent;
                p.textContent = "";
                
                setTimeout(() => {
                    let i = 0;
                    
