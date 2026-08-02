<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Feliz 5 Meses, Mi Amor</title>
    <style>
        :root {
            --color-fondo: #0a0a0a;
            --color-tarjeta: #141414;
            --color-texto: #ffffff;
            --color-rosa: #ffb7c5;
            --color-rosa-oscuro: #ff8da1;
            --color-verde-manga: #a3e635; /* Color verde característico del manga */
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background-color: var(--color-fondo);
            color: var(--color-texto);
            line-height: 1.6;
            overflow-x: hidden;
            position: relative;
        }

        body::before {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background-image: 
                radial-gradient(white, rgba(255,255,255,.2) 2px, transparent 40px),
                radial-gradient(white, rgba(255,255,255,.15) 1px, transparent 30px);
            background-size: 550px 550px, 350px 350px;
            background-position: 0 0, 40px 60px;
            z-index: -1;
            opacity: 0.4;
        }

        main {
            max-width: 600px;
            margin: 0 auto;
            padding: 1.5rem;
        }

        section {
            background-color: var(--color-tarjeta);
            border: 1px solid rgba(163, 230, 53, 0.2);
            border-radius: 16px;
            padding: 2rem 1.5rem;
            margin-bottom: 2.5rem;
            text-align: center;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.5);
        }

        h1, h2, h3 {
            color: var(--color-verde-manga);
            margin-bottom: 1rem;
        }

        blockquote {
            font-style: italic;
            color: #ccc;
            padding: 0.5rem 1rem;
            margin: 1rem 0;
            border-left: 3px solid var(--color-verde-manga);
            background: rgba(163, 230, 53, 0.05);
            border-radius: 0 8px 8px 0;
        }

        .boton {
            display: inline-block;
            background-color: transparent;
            color: var(--color-rosa);
            border: 2px solid var(--color-rosa);
            padding: 0.6rem 1.5rem;
            border-radius: 25px;
            text-decoration: none;
            font-weight: bold;
            margin-top: 1rem;
            transition: all 0.3s ease;
        }

        .boton:hover {
            background-color: var(--color-rosa);
            color: var(--color-fondo);
            box-shadow: 0 0 15px var(--color-rosa);
        }

        .contador-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1rem;
            margin-top: 1.5rem;
        }
        .contador-item {
            background: rgba(255,255,255,0.03);
            padding: 1rem;
            border-radius: 12px;
            border: 1px solid rgba(163, 230, 53, 0.1);
        }
        .contador-num {
            font-size: 2rem;
            font-weight: bold;
            color: var(--color-verde-manga);
            display: block;
        }

        .galeria {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }
        
        .foto-caja {
            background: #1a1a1a;
            border-radius: 12px;
            overflow: hidden;
            border: 1px solid rgba(163, 230, 53, 0.2);
            box-shadow: 0 4px 15px rgba(0,0,0,0.3);
        }

        .foto-real {
            width: 100%;
            height: 380px;
            object-fit: cover;
            display: block;
        }

        .foto-frase {
            padding: 1rem;
            font-size: 0.95rem;
            color: var(--color-rosa);
        }

        .contenedor-ojitos {
            position: relative;
            padding: 1rem 0;
        }

        .imagen-ojitos {
            width: 190px;
            height: 190px;
            border-radius: 50%;
            object-fit: cover;
            margin: 0 auto;
            border: 3px solid var(--color-verde-manga);
            display: block;
            box-shadow: 0 0 15px rgba(163, 230, 53, 0.3);
        }

        /* PALABRAS INTERACTIVAS Y FLOTANTES */
        .nube-palabras {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 0.8rem;
            margin-top: 2rem;
        }
        
        .palabra-tag {
            background: rgba(255, 183, 197, 0.15);
            color: #ffffff;
            padding: 0.4rem 0.9rem;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 500;
            border: 1px solid rgba(255, 183, 197, 0.3);
            display: inline-block;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
            animation: flotarTags 3s ease-in-out infinite alternate;
        }

        .palabra-tag:nth-child(2n) { animation-duration: 3.5s; animation-delay: 0.2s; }
        .palabra-tag:nth-child(3n) { animation-duration: 4s; animation-delay: 0.5s; }
        .palabra-tag:nth-child(4n) { animation-duration: 2.7s; animation-delay: 0.1s; }

        @keyframes flotarTags {
            0% { transform: translateY(0px) rotate(0deg); }
            100% { transform: translateY(-12px) rotate(2deg); box-shadow: 0 8px 15px rgba(255, 183, 197, 0.3); }
        }

        .contenedor-sobre {
            display: flex;
            justify-content: center;
            margin: 2rem 0;
            cursor: pointer;
        }
        .sobre {
            position: relative;
            width: 200px;
            height: 140px;
            background-color: #2a1b22;
            border-radius: 0 0 8px 8px;
            border: 2px solid var(--color-rosa);
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
        }
        .sobre::before {
            content: "";
            position: absolute;
            top: -2px; left: -2px;
            width: 0; height: 0;
            border-left: 102px solid transparent;
            border-right: 102px solid transparent;
            border-top: 80px solid var(--color-rosa);
            transform-origin: top;
            transition: transform 0.5s ease;
            z-index: 2;
        }
        .sobre.abierto::before {
            transform: rotateX(180deg) translateY(2px);
            z-index: 0;
        }
        .corazon-sello {
            position: absolute;
            top: 30px; left: 50%;
            transform: translateX(-50%);
            font-size: 2rem;
            z-index: 3;
            transition: opacity 0.3s;
        }
        .sobre.abierto .corazon-sello { opacity: 0; }
        
        .carta-contenido {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.8s ease, padding 0.5s ease;
            background: #ffffff;
            color: #222222;
            border-radius: 12px;
            text-align: left;
        }
        .sobre.abierto + .carta-contenido {
            max-height: 1000px;
            padding: 1.5rem;
            margin-top: 1.5rem;
            border: 2px solid var(--color-rosa);
        }

        .corazon-flotante {
            position: fixed;
            color: rgba(255, 183, 197, 0.6);
            font-size: 1.5rem;
            pointer-events: none;
            z-index: 999;
            animation: subiendo 4s linear forwards;
        }
        @keyframes subiendo {
            0% { transform: translateY(100vh) translateX(0) scale(0); opacity: 1; }
            100% { transform: translateY(-10vh) translateX(50px) scale(1.2); opacity: 0; }
        }
    </style>
</head>
<body id="inicio">

    <main>
        <section>
            <h2>🖤 Bienvenida</h2>
            <h1>❤️ Feliz 5 meses, mi amor ❤️</h1>
            <blockquote>
                "Cinco meses no cuentan nuestra historia, solo son el comienzo de todo lo que quiero vivir contigo."
            </blockquote>
            <a href="#tiempo" class="boton">✨ Comenzar</a>
        </section>

        <section id="tiempo">
            <h2>⏳ Todo este tiempo contigo...</h2>
            <blockquote>
                "Cada segundo a tu lado se ha convertido en uno de mis recuerdos favoritos."
            </blockquote>
            <div class="contador-grid">
                <div class="contador-item"><span class="contador-num" id="dias">0</span>Días</div>
                <div class="contador-item"><span class="contador-num" id="horas">0</span>Horas</div>
                <div class="contador-item"><span class="contador-num" id="minutos">0</span>Minutos</div>
                <div class="contador-item"><span class="contador-num" id="segundos">0</span>Segundos</div>
            </div>
        </section>

        <!-- SECCIÓN DE FOTOS REALES DE MITSUKI KOGA Y AYA OSAWA -->
        <section>
            <div class="galeria">
                <div class="foto-caja">
                    <img class="foto-real" src="https://images.unsplash.com/photo-1618336753974-aae8e04506aa?w=600" alt="Mitsuki Koga manga art">
                    <div class="foto-frase">🌸 "Desde que llegaste, mi mundo es un lugar más bonito."</div>
                </div>
                <div class="foto-caja">
                    <img class="foto-real" src="https://images.unsplash.com/photo-1542208998-f6dbbb27a72f?w=600" alt="Aya Osawa manga style">
                    <div class="foto-frase">🌸 "Mi lugar favorito siempre será a tu lado."</div>
                </div>
            </div>
        </section>

        <section>
            <h2>👀 Mi niña de ojitos bonitos</h2>
            <blockquote>
                🤍 Mi niña de ojitos bonitos...<br>
                "Dicen que los ojos son el reflejo del alma. Si eso es cierto, en los tuyos encontré el lugar donde mi corazón siempre quiere volver."
            </blockquote>
            
            <div class="contenedor-ojitos">
                <img class="imagen-ojitos" src="https://images.unsplash.com/photo-1579546929518-9e396f3cc809?w=500" alt="Manga aesthetic illustration">
            </div>

            <blockquote>
                "Tus ojitos bonitos son el lugar donde siempre encuentro paz, ternura y el motivo para sonreír." 🌸
            </blockquote>

            <div class="nube-palabras">
                <span class="palabra-tag">🤍 Amor</span><span class="palabra-tag">🏡 Hogar</span>
                <span class="palabra-tag">🌸 Paz</span><span class="palabra-tag">✨ Calma</span>
                <span class="palabra-tag">❤️ Sonrisa</span><span class="palabra-tag">🦋 Ternura</span>
                <span class="palabra-tag">🌙 Destino</span><span class="palabra-tag">💗 Felicidad</span>
                <span class="palabra-tag">🌷 Siempre</span><span class="palabra-tag">⭐ Mi persona favorita</span>
                <span class="palabra-tag">💌 Mi niña de ojitos bonitos</span><span class="palabra-tag">🥹 Mi lugar seguro</span>
                <span class="palabra-tag">💕 Mi inspiración</span><span class="palabra-tag">🌹 Mi felicidad</span>
                <span class="palabra-tag">♾️ Infinito</span>
            </div>
        </section>

        <!-- TU CARTA DE LA OPCIÓN 2 TOTALMENTE INTEGRADA -->
        <section>
            <h2>💌 Una carta para ti</h2>
            <p style="font-size: 0.9rem; color: #aaa;">(Toca el sobre rosa para abrirlo)</p>
            <div class="contenedor-sobre">
                <div class="sobre" id="sobreElemento" onclick="abrirCarta()">
                    <div class="corazon-sello">💝</div>
                </div>
            </div>
            <div class="carta-contenido" id="cartaContenido">
                <p style="white-space: pre-line; line-height: 1.8; padding: 1.5rem; font-weight: 500; font-size: 1.05rem;">
                    Hola mi vida hermosa. 💕 
                    
                    Hoy cumplimos 5 meses juntos y quería hacerte este detalle para recordarte lo mucho que te amo. Gracias por ser mi lugar seguro, por escucharme cuando estoy cansada y por tener siempre las palabras perfectas. 

                    Cada momento contigo es hermoso y espero que este sea solo el inicio de muchísimos meses más. ¡Te amo con todo mi corazón! 🐰❤️
                </p>
            </div>
        </section>

        <section>
            <h2>🎵 Una canción que siempre me recuerda a ti</h2>
            <blockquote>
                "No importa cuántas veces la escuche, siempre termina recordándome a ti." ❤️
            </blockquote>
            <a href="https://www.youtube.com/results?search_query=i+wanna+be+yours" target="_blank" class="boton">🎧 Escuchar "I Wanna Be Yours"</a>
        </section>

        <section>
            <h2>❤️ Final</h2>
            <blockquote style="text-align: left; border: none; background: transparent;">
                "Gracias por estos cinco meses. Gracias por cada sonrisa, cada conversación y cada momento compartido. Espero que este sea solo el comienzo de una historia llena de recuerdos, sueños y mucho amor. Te amo con todo mi corazón. Feliz aniversario, mi amor. ❤️"
            </blockquote>
            <a href="#inicio" class="boton">✨ Volver al inicio</a>
        </section>
    </main>

    <script>
        // Cambia aquí la fecha si necesitas ajustar el día exacto
        const fechaInicio = new Date(2026, 2, 2, 0, 0, 0); 

        function actualizarContador() {
            const ahora = new Date();
            const diferencia = ahora - fechaInicio;

            const d = Math.floor(diferencia / (1000 * 60 * 60 * 24));
            const h = Math.floor((diferencia % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const m = Math.floor((diferencia % (1000 * 60 * 60)) / (1000 * 60));
            const s = Math.floor((diferencia % (1000 * 60)) / 1000);

            document.getElementById('dias').innerText = d;
            document.getElementById('horas').innerText = h;
            document.getElementById('minutos').innerText = m;
            document.getElementById('segundos').innerText = s;
        }
        setInterval(actualizarContador, 1000);
        actualizarContador();

        function abrirCarta() {
            const sobre = document.getElementById('sobreElemento');
            sobre.classList.toggle('abierto');
        }

        function crearCorazon() {
            const corazon = document.createElement('div');
            corazon.classList.add('corazon-flotante');
            corazon.innerText = '💗';
            corazon.style.left = Math.random() * 100 + 'vw';
            corazon.style.animationDuration = Math.random() * 2 + 3 + 's';
            document.body.appendChild(corazon);
            setTimeout(() => { corazon.remove(); }, 5000);
        }
        setInterval(crearCorazon, 400);
    </script>
</body>
</html>
