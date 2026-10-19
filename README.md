<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ABP: El Miedo y la Inteligencia Emocional</title>
    <!-- Importación de tipografía Mont (Fontfabric) / Montserrat fallback -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700;800;900&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --bg-color: #0b0e14;
            --card-bg: #161b22;
            --accent-color: #e67e22;
            --accent-hover: #d35400;
            --text-color: #c9d1d9;
            --heading-color: #ffffff;
            --border-color: #30363d;
            --font-mont: 'Mont', 'Montserrat', -apple-system, BlinkMacSystemFont, sans-serif;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: var(--font-mont);
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.7;
        }

        /* Nav Bar */
        nav {
            background-color: var(--card-bg);
            padding: 15px 20px;
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 1px solid var(--border-color);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav .logo {
            font-family: var(--font-mont);
            font-weight: 800;
            color: var(--heading-color);
            font-size: 1.1rem;
            letter-spacing: 0.5px;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 15px;
        }

        nav a {
            font-family: var(--font-mont);
            color: var(--text-color);
            text-decoration: none;
            font-size: 0.85rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            transition: color 0.2s;
        }

        nav a:hover {
            color: var(--accent-color);
        }

        /* Header / Hero */
        header {
            background: linear-gradient(180deg, rgba(22,27,34,0.95) 0%, rgba(11,14,20,1) 100%);
            text-align: center;
            padding: 90px 20px 60px 20px;
            border-bottom: 2px solid var(--accent-color);
        }

        header h1 {
            font-family: var(--font-mont);
            color: var(--heading-color);
            font-size: 3rem;
            font-weight: 900;
            margin-bottom: 15px;
            letter-spacing: 1px;
            text-shadow: 0 0 20px rgba(230, 126, 34, 0.25);
        }

        header .subtitle {
            font-family: var(--font-mont);
            font-size: 1.2rem;
            color: var(--accent-color);
            max-width: 750px;
            margin: 0 auto 30px auto;
            font-weight: 400;
        }

        /* Sección Integrantes */
        .team-container {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
        }

        .team-label {
            font-family: var(--font-mont);
            color: var(--heading-color);
            font-weight: 700;
            font-size: 1rem;
            margin-right: 5px;
        }

        .team-badge {
            font-family: var(--font-mont);
            background-color: rgba(230, 126, 34, 0.12);
            border: 1px solid var(--accent-color);
            color: var(--heading-color);
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 700;
            letter-spacing: 0.5px;
        }

        .container {
            max-width: 1050px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        .section-title {
            font-family: var(--font-mont);
            color: var(--heading-color);
            font-size: 1.8rem;
            font-weight: 800;
            border-left: 4px solid var(--accent-color);
            padding-left: 14px;
            margin: 50px 0 25px 0;
            letter-spacing: 0.5px;
        }

        .grid-2 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 25px;
        }

        .card {
            background-color: var(--card-bg);
            border-radius: 10px;
            padding: 25px;
            border: 1px solid var(--border-color);
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
            transition: transform 0.2s, border-color 0.2s;
            margin-bottom: 20px;
        }

        .card:hover {
            transform: translateY(-3px);
            border-color: var(--accent-color);
        }

        .card h3 {
            font-family: var(--font-mont);
            color: var(--heading-color);
            margin-bottom: 12px;
            font-size: 1.25rem;
            font-weight: 700;
        }

        /* Pillars list */
        .pillar-item {
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px dashed var(--border-color);
        }

        .pillar-item:last-child {
            border-bottom: none;
        }

        .pillar-item strong {
            color: var(--accent-color);
            font-weight: 700;
        }

        /* Expert quote / highlights */
        .expert-quote {
            font-style: italic;
            color: var(--accent-color);
            font-size: 1.05rem;
            margin-bottom: 15px;
            border-left: 3px solid var(--accent-color);
            padding-left: 12px;
        }

        .expert-list li {
            margin-bottom: 12px;
            margin-left: 20px;
        }

        .btn-video {
            display: inline-block;
            background-color: #21262d;
            color: var(--heading-color);
            border: 1px solid var(--border-color);
            padding: 8px 16px;
            border-radius: 6px;
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 600;
            margin-top: 15px;
            transition: background 0.2s;
        }

        .btn-video:hover {
            background-color: var(--accent-color);
            color: #000;
        }

        /* Transcript box */
        .transcript-box {
            background-color: #21262d;
            border-left: 4px solid var(--accent-color);
            padding: 15px;
            border-radius: 6px;
            margin-top: 15px;
            font-size: 0.95rem;
        }

        .transcript-box p {
            margin-bottom: 10px;
        }

        .transcript-box p:last-child {
            margin-bottom: 0;
        }

        /* Quiz Styling */
        .quiz-box {
            background-color: var(--card-bg);
            padding: 30px;
            border-radius: 12px;
            border: 1px solid var(--border-color);
        }

        .quiz-question {
            font-size: 1.1rem;
            color: var(--heading-color);
            margin-bottom: 15px;
            font-weight: 700;
        }

        .quiz-option {
            display: block;
            width: 100%;
            background: #21262d;
            color: var(--text-color);
            padding: 14px 18px;
            margin: 10px 0;
            border-radius: 6px;
            cursor: pointer;
            border: 1px solid var(--border-color);
            text-align: left;
            font-size: 0.95rem;
            font-family: var(--font-mont);
            font-weight: 600;
            transition: all 0.2s;
        }

        .quiz-option:hover {
            background-color: var(--accent-color);
            color: #000;
            font-weight: 800;
        }

        .result-box {
            margin-top: 20px;
            padding: 15px;
            border-radius: 6px;
            background-color: rgba(230, 126, 34, 0.1);
            border-left: 4px solid var(--accent-color);
            display: none;
        }

        /* Drive Link Button */
        .btn-drive {
            display: inline-block;
            background-color: var(--accent-color);
            color: #ffffff;
            padding: 12px 24px;
            border-radius: 6px;
            text-decoration: none;
            font-family: var(--font-mont);
            font-weight: 700;
            margin-top: 20px;
            transition: background 0.2s;
        }

        .btn-drive:hover {
            background-color: var(--accent-hover);
        }

        /* Interview Questions list */
        .question-list li {
            margin-bottom: 10px;
            list-style-type: square;
            margin-left: 20px;
        }

        footer {
            text-align: center;
            padding: 40px 20px;
            background-color: var(--card-bg);
            color: #8b949e;
            margin-top: 60px;
            border-top: 1px solid var(--border-color);
            font-family: var(--font-mont);
        }

        footer p {
            margin-bottom: 8px;
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo">ABP: Miedo & IE</div>
        <ul>
            <li><a href="#introduccion">Salud Mental</a></li>
            <li><a href="#pilares">Pilares IE</a></li>
            <li><a href="#miedo">El Miedo</a></li>
            <li><a href="#experta">Visión Experta</a></li>
            <li><a href="#entrevistas">Entrevistas</a></li>
            <li><a href="#test">Test</a></li>
        </ul>
    </nav>

    <header>
        <h1>EL MIEDO & LA INTELIGENCIA EMOCIONAL</h1>
        <p class="subtitle">Investigación, producción audiovisual y herramientas de autoconocimiento.</p>
        
        <!-- Integrantes del Grupo con etiqueta -->
        <div class="team-container">
            <span class="team-label">Integrantes:</span>
            <span class="team-badge">Ian Godoy</span>
            <span class="team-badge">Ramiro Córdoba</span>
            <span class="team-badge">Naile Gallizzi</span>
            <span class="team-badge">Naila Díaz</span>
        </div>
    </header>

    <div class="container">

        <!-- BLOQUE 1: INTRODUCCIÓN Y SALUD MENTAL -->
        <section id="introduccion">
            <h2 class="section-title">Salud Mental e Inteligencia Emocional</h2>
            <div class="grid-2">
                <div class="card">
                    <h3>¿Qué es la Salud Mental desde la IE?</h3>
                    <p>Es el estado de bienestar emocional, psicológico y social que nos permite manejar el estrés cotidiano, trabajar de forma productiva y relacionarnos sanamente con los demás.</p>
                </div>
                <div class="card">
                    <h3>El Vínculo Protector</h3>
                    <p>La Inteligencia Emocional (IE) funciona como un factor de protección: a mayor desarrollo de la IE, menor probabilidad de experimentar crisis severas de ansiedad, agotamiento (burnout) o aislamiento.</p>
                </div>
            </div>
        </section>

        <!-- BLOQUE 2: LOS 5 PILARES DE GOLEMAN -->
        <secion id="pilares">
            <h2 class="section-title">Los 5 Pilares de la Inteligencia Emocional</h2>
            <div class="card">
                <div class="pillar-item">
                    <strong>Autoconocimiento:</strong> Capacidad de saber identificar qué sientes en el momento (por ejemplo: <em>"no estoy enojado, estoy triste o frustrado"</em>).
                </div>
                <div class="pillar-item">
                    <strong>Autorregulación:</strong> Capacidad de pausar antes de reaccionar impulsivamente para evitar conductas destructivas.
                </div>
                <div class="pillar-item">
                    <strong>Automotivación:</strong> Canalizar la energía emocional hacia objetivos claros y mantener la resiliencia ante los fallos.
                </div>
                <div class="pillar-item">
                    <strong>Empatía:</strong> Comprender lo que sienten los demás, facilitando la conexión y evitando el aislamiento social.
                </div>
                <div class="pillar-item">
                    <strong>Habilidades Sociales:</strong> Comunicar lo que nos pasa, poner límites sanos y resolver conflictos sin violencia.
                </div>
            </div>
        </secion>

        <!-- BLOQUE 3: EL MIEDO Y LA BIOLOGÍA -->
        <section id="miedo">
            <h2 class="section-title">¿Qué es el Miedo y para qué sirve?</h2>
            <div class="grid-2">
                <div class="card">
                    <h3>¿Sentir miedo es una debilidad?</h3>
                    <p><strong>No.</strong> Sentir miedo es un instinto de supervivencia. Es una alarma física y mental que activa la liberación de adrenalina y acelera el ritmo cardíaco para preparar al cuerpo para la respuesta de <strong>lucha o huida</strong>.</p>
                </div>
                <div class="card">
                    <h3>¿Se puede gestionar el miedo?</h3>
                    <p>Sí. La Inteligencia Emocional no busca eliminar el miedo —ya que es natural y nos protege—, sino evitar que nos paralice o nos haga tomar decisiones impulsivas.</p>
                </div>
            </div>
        </section>

        <!-- BLOQUE NUEVO: OPINIÓN PROFESIONAL / EXPERTA -->
        <section id="experta">
            <h2 class="section-title">Visión Profesional: El Miedo y los Traumas</h2>
            <div class="card">
                <h3>Análisis de Anabel González (Psiquiatra y Experta en Trauma)</h3>
                <p class="expert-quote">“El antídoto contra los miedos es la seguridad, el apego seguro.”</p>
                <p style="margin-bottom: 15px;">A partir de la charla profesional sobre cómo superar los miedos y traumas del pasado, destacamos las siguientes claves fundamentales:</p>
                
                <ul class="expert-list">
                    <li><strong>El origen del condicionamiento:</strong> Los miedos irracionales o crónicos suelen provenir de experiencias del pasado que no se procesaron de forma adecuada, haciendo que el cerebro siga reaccionando como si el peligro estuviera ocurriendo hoy.</li>
                    <li><strong>La trampa de la huida:</strong> Evitar permanentemente lo que nos asusta solo proporciona un alivio temporal. La evitación constante alimenta el miedo y hace que crezca con el tiempo.</li>
                    <li><strong>El rol del vínculo:</strong> Para sanar las heridas y los temores profundos, la persona necesita entornos de seguridad y relaciones de apoyo estables (apego seguro) que regulen su sistema nervioso.</li>
                </ul>

                <a href="https://youtu.be/de5m11tkezI?si=y18SCV2Exzrt5kFN" target="_blank" class="btn-video">▶️ Ver charla completa de Anabel González</a>
            </div>
        </section>

        <!-- BLOQUE 4: VOCES / INVESTIGACIÓN Y TRANSCRIPCIÓN DE ENTREVISTA -->
        <section id="entrevistas">
            <h2 class="section-title">Voces e Investigación en Terreno</h2>
            
            <!-- Transcripción de la Entrevista a la Bibliotecaria -->
            <div class="card">
                <h3>Transcripción de Entrevista: Perspectiva sobre el Miedo</h3>
                <div class="transcript-box">
                    <p><strong>Entrevistador:</strong> El miedo, ¿es una emoción buena o mala y por qué?</p>
                    <p><strong>Bibliotecaria:</strong> Bueno, generalmente lo consideramos algo malo. La gran mayoría la considera así porque nos paraliza, porque no lo sabemos manejar, porque nos trae malos recuerdos, tal vez de tomar malas decisiones por miedo... Es, generalmente, según cómo esté preparado uno.</p>
                    
                    <p style="margin-top: 12px;"><strong>Entrevistador:</strong> ¿Has experimentado crisis repentinas de temor extremo donde sientas que pierdes el control o que vas a morir?</p>
                    <p><strong>Bibliotecaria:</strong> Uy, sí, y mucho y habitualmente. Por mi historia personal, que me criaron con miedo, soy de la época donde todo daba miedo: ir a la playa daba miedo, el sol daba miedo... Y cuando uno vive con eso como si fuera algo normal, después tiene miedo de cosas que no tienen sentido. Y sí he experimentado situaciones más graves donde era lógico tener miedo por algo más urgente o realmente que podía llegar a ser grave.</p>
                    
                    <p style="margin-top: 12px;"><strong>Entrevistador:</strong> ¿Para qué nos sirve el miedo?</p>
                    <p><strong>Bibliotecaria:</strong> Bueno, después de lo que conté, a mí actualmente me sirvió —o sea, en el último tiempo— me sirvió como para estar mejor, en el sentido de que pasé malas experiencias y por el miedo a estar peor que antes o a volver a caer en esos problemas, como que me hizo reaccionar a tiempo y tomar decisiones. La solución es algo que viene después, pero el hecho de decir: "bueno, ante este miedo tomo una decisión y la pienso y la medito y me hago cargo de esa decisión y de esa elección que uno hace". Así que bueno, últimamente me sirvió.</p>

                    <p style="margin-top: 12px;"><strong>Entrevistador:</strong> ¿Cuál ha sido la experiencia paranormal o más real que has vivido?</p>
                    <p><strong>Bibliotecaria:</strong> Ay, se me ocurre que he tenido como intuiciones o sueños premonitorios de miedo que por suerte han sido a favor, digamos. Como relacionados a accidentes y esas cosas que salieron bien, pero bueno... algunas, ahora me estoy acordando de otras que no salieron bien y que de todas maneras, o sea, en ambas yo no tenía nada para hacer, eran como intuiciones, premoniciones de algo malo que iba a pasar, que me generaron mucho miedo en el momento y ahí sí no había nada que yo pudiera hacer, no estaba en mis manos y creo que en las manos de nadie ayudar a otras personas.</p>
                </div>
            </div>

            <!-- Cuestionario general y Botón de Drive -->
            <div class="card">
                <h3>Estructura del Cuestionario de Entrevista</h3>
                <p style="margin-bottom: 15px;">Para indagar la percepción del miedo en la comunidad, estructuramos las siguientes preguntas clave:</p>
                <ul class="question-list">
                    <li>¿Qué es para ti la inteligencia emocional?</li>
                    <li>¿El miedo es una emoción buena o mala? ¿Por qué?</li>
                    <li>¿Has experimentado crisis repentinas de temor extremo donde sientes que pierdes el control?</li>
                    <li>¿Para qué crees que nos sirve el miedo?</li>
                    <li>¿Cuál ha sido la experiencia paranormal o de temor más real que has vivido?</li>
                    <li>¿Le tienes miedo a la oscuridad o a lo que te imaginas que se esconde en ella?</li>
                </ul>
                <a href="https://drive.google.com/drive/folders/1nJ4w3PBWIFYXPAnvYk_3rnOb0ExfJYW1?usp=drive_link" target="_blank" class="btn-drive">🎬 Ver carpeta completa de Videos y Entrevistas en Drive</a>
            </div>
        </section>

        <!-- BLOQUE 5: TEST INTERACTIVO (EMOQUEST) -->
        <section id="test">
            <h2 class="section-title">Auto-Evaluación Interactiva (Radar Emocional)</h2>
            <div class="quiz-box">
                <div class="quiz-question" id="q-text">Cuando te enfrentas a una situación de mucha incertidumbre o temor, ¿cuál suele ser tu primera reacción?</div>
                <button class="quiz-option" onclick="evaluar('paralisis')">A) Me paralizo y me cuesta tomar decisiones.</button>
                <button class="quiz-option" onclick="evaluar('evitacion')">B) Busco distraerme rápido o evitar pensar en el tema.</button>
                <button class="quiz-option" onclick="evaluar('gestion')">C) Hago una pausa, respiro e intento identificar qué me asusta.</button>

                <div id="quiz-res" class="result-box"></div>
            </div>
        </section>

    </div>

    <footer>
        <p><strong>Proyecto ABP: Inteligencia Emocional & Taller Audiovisual</strong></p>
        <p>Integrantes: Ian Godoy, Ramiro Córdoba, Naile Gallizzi y Naila Díaz</p>
    </footer>

    <script>
        function evaluar(tipo) {
            const res = document.getElementById('quiz-res');
            res.style.display = "block";

            if(tipo === 'paralisis') {
                res.innerHTML = "<strong>💡 Recomendación de Autorregulación:</strong> La parálisis ocurre por sobrecarga del sistema nervioso. Prueba la respiración diafragmática (4 segundos inhalar, 4 mantener, 4 exhalar) para indicarle a tu cuerpo que estás a salvo.";
            } else if(tipo === 'evitacion') {
                res.innerHTML = "<strong>💡 Recomendación de Autoconocimiento:</strong> Evitar la emoción la intensifica a largo plazo. Prueba escribir en papel a qué le tienes miedo exactamente para procesarlo de forma estructurada.";
            } else if(tipo === 'gestion') {
                res.innerHTML = "<strong>🌟 ¡Excelente manejo de IE!</strong> Estás aplicando los dos primeros pilares de Goleman: Autoconocimiento y Autorregulación.";
            }
        }
    </script>

</body>
</html>
