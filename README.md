<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Quieres ser mi novia?</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f9f9f9;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        #container {
            text-align: center;
            padding: 20px;
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        h1 {
            color: #333;
            margin-bottom: 20px;
        }

        #mensaje {
            font-size: 1.2em;
            margin-bottom: 20px;
            color: #555;
        }

        #botones {
            display: flex;
            justify-content: center;
        }

        button {
            padding: 10px 20px;
            margin: 0 10px;
            font-size: 1em;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            transition: all 0.3s ease;
        }

        #aceptar {
            background-color: #4CAF50;
            color: white;
        }

        #rechazar {
            background-color: #f44336;
            color: white;
        }

        button:hover {
            transform: translateY(-3px);
        }

        #corazon-grande {
            margin-top: 20px;
            font-size: 3em;
            display: none;
        }
    </style>
</head>

<body>
    <div id="container">
        <h1>¡Hola, Mi Yanee <3!</h1>
                <p>Desde el momento en que te conocí, supe que eras especial.</p>
                <p>He querido decirte algo muy importante...</p>
                <p>Aunque estamos separados, mi corazón está contigo.</p>
                <p>No puedo dejar de pensar en ti y en todo lo que significas para mí.</p>
                <p>Espero con ansias poder construir algo hermoso juntos.</p>
                <h2>¿Te gustaría ser mi novia?</h2>
                <div id="mensaje">Por favor, presiona un botón para responder</div>
                <div id="botones">
                    <button id="aceptar" onclick="responder(true)">Sí</button>
                    <button id="rechazar" onmouseover="moverBotonNo()" onclick="responder(false)">No</button>
                </div>
                <div id="corazon-grande">&#10084;&#65039;</div>
    </div>

    <script>
        function responder(acepta) {
            var mensaje = document.getElementById("mensaje");
            if (acepta) {
                mensaje.innerHTML = "<strong>¡Sí!</strong> ¡Por supuesto que quiero ser tu novia!¡Te amo wil! 😊❤️";
                document.getElementById("corazon-grande").style.display = "block";
            } else {
                mensaje.innerHTML = "Lo siento, no puedo aceptar en este momento. 😔";
            }
            // Aquí puedes agregar más acciones según la respuesta, como redireccionar a otra página, mostrar un mensaje adicional, etc.
        }

        function moverBotonNo() {
            var botonNo = document.getElementById("rechazar");
            botonNo.style.position = "absolute";
            var nuevaPosicionX = Math.random() * (window.innerWidth - botonNo.clientWidth);
            var nuevaPosicionY = Math.random() * (window.innerHeight - botonNo.clientHeight);
            botonNo.style.left = nuevaPosicionX + "px";
            botonNo.style.top = nuevaPosicionY + "px";
        }
    </script>
    <body>
        <audio controls autoplay loop>
            <source src="AUDIO/cancion.mp3" type="audio/mpeg">
        </audio>
    </body>
</body>
