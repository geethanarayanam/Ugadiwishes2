<html lang="te">
<head>
    <meta charset="UTF-8">
    <title>Ugadi Unique Wishes 2026</title>
    <style>
        :root {
            --mango-yellow: #FFD700;
            --neem-green: #4CAF50;
            --jaggery-brown: #8B4513;
            --curtain-red: #800000;
        }

        body {
            margin: 0;
            background: var(--mango-yellow);
            font-family: 'Segoe UI', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
            text-align: center;
        }

        /* Interactive Bowl */
        .bowl-container {
            background: rgba(255, 255, 255, 0.3);
            backdrop-filter: blur(10px);
            padding: 40px;
            border-radius: 50%;
            border: 5px solid white;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            cursor: pointer;
            transition: transform 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            width: 300px;
            height: 300px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: relative;
        }

        .bowl-container:hover { transform: scale(1.05); }

        .ingredient-icon {
            font-size: 50px;
            position: absolute;
            transition: all 0.8s ease-in-out;
        }

        /* Final Message Box */
        #finalMessage {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: white;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 20px 50px rgba(0,0,0,0.2);
            z-index: 100;
            width: 80%;
            max-width: 500px;
            animation: popIn 0.6s forwards;
        }

        @keyframes popIn {
            0% { transform: translate(-50%, -50%) scale(0.5); opacity: 0; }
            100% { transform: translate(-50%, -50%) scale(1); opacity: 1; }
        }

        .btn-mix {
            margin-top: 20px;
            padding: 12px 25px;
            background: var(--curtain-red);
            color: white;
            border: none;
            border-radius: 25px;
            font-weight: bold;
            cursor: pointer;
        }

        .floating-flowers {
            position: absolute;
            top: -10%;
            pointer-events: none;
            animation: fall 5s linear infinite;
        }

        @keyframes fall {
            to { transform: translateY(110vh) rotate(360deg); }
        }
    </style>
</head>
<body>

    <div id="intro">
        <h2 style="color: var(--jaggery-brown);">ఉగాది పచ్చడిని కలపండి...</h2>
        <div class="bowl-container" onclick="mixPachadi()">
            <span class="ingredient-icon" style="top:20px; left:50px;">🥭</span> <span class="ingredient-icon" style="top:20px; right:50px;">🌿</span> <span class="ingredient-icon" style="bottom:50px; left:40px;">🍯</span> <span class="ingredient-icon" style="bottom:50px; right:40px;">🌶️</span> <span class="ingredient-icon" style="top:120px; left:120px;">🧂</span> <p style="margin-top: 180px; font-weight: bold; color: #555;">షడ్రుచుల సమ్మేళనం కోసం క్లిక్ చేయండి</p>
        </div>
    </div>

    <div id="finalMessage">
        <h1 style="color: #FF4500;">శోభకృత్ నామ ఉగాది శుభాకాంక్షలు!</h1>
        <div style="font-size: 1.2rem; color: #333; line-height: 1.8;">
            <p>తీపి, వగరు, కారం, ఉప్పు, పులుపు, చేదు...</p>
            <p><strong>మీ జీవితం ఈ షడ్రుచుల వలె సమతుల్యంగా, ఆనందంగా ఉండాలని ఆకాంక్షిస్తూ..</strong></p>
            <hr style="border: 0; border-top: 1px solid #eee;">
            <p style="color: var(--jaggery-brown); font-weight: bold;">శ్రీ వేంకటేశ్వర స్వామి ఆశీస్సులు మీకు ఎల్లవేళలా ఉండాలి.</p>
        </div>
        <button class="btn-mix" onclick="location.reload()">మళ్ళీ చూడండి</button>
    </div>

    <script>
        function mixPachadi() {
            const icons = document.querySelectorAll('.ingredient-icon');
            icons.forEach(icon => {
                icon.style.top = '120px';
                icon.style.left = '120px';
                icon.style.opacity = '0';
            });

            setTimeout(() => {
                document.getElementById('intro').style.display = 'none';
                document.getElementById('finalMessage').style.display = 'block';
                createFlowers();
            }, 800);
        }

        function createFlowers() {
            for(let i=0; i<20; i++) {
                let flower = document.createElement('div');
                flower.className = 'floating-flowers';
                flower.innerHTML = '🌸';
                flower.style.left = Math.random() * 100 + 'vw';
                flower.style.animationDuration = (Math.random() * 3 + 2) + 's';
                document.body.appendChild(flower);
            }
        }
    </script>
</body>
</html>
