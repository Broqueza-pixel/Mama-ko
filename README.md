<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        @font-face {
            font-family: "Exoct";
            src: url("https://assets.codepen.io/1480814/films.EXH.ttf");
        }

        figure {
            width: 100%;
            aspect-ratio: 1;
            margin: 0 60px; /* Corrected margin */
            padding: 5px 20px 0;
            box-sizing: border-box;
            display: grid;
            grid-template-rows: 100%;
            cursor: pointer;
            position: relative;
            filter: drop-shadow(0 0 20px rgba(0, 0, 0, 0.5)); /* Corrected drop-shadow */
        }

        figure::before { /* Corrected ::before selector */
            content: "";
            position: absolute;
            z-index: -1;
            inset: 0;
            background-size: cover; /* Corrected background-size */
            background-position: top; /* Added background-position */
            transform-origin: bottom;
            filter: brightness(0.9);
            transition: filter 0.5s; /* Corrected transition */
        }

        figure:nth-child(1)::before { /* Added specificity for first figure */
            background-image: url("https://assets.codepen.io/1480814/necro-back.jpg");
        }

        figure:nth-child(2)::before { /* Added specificity for second figure */
            background-image: url("https://assets.codepen.io/1480814/druid-bac.jpg");
        }

        img {
            grid-area: 1/1;
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top;
        }

        figure {
            filter: contrast(0.8) brightness(0.7);
            place-self: end center;
            transition: .5s;
        }

        figcaption {
            grid-area: 1/1;
            width: calc(100% + 40px);
            font-family: Exoct;
            color: #fff;
            font-size: min(32px, 5vmin);
            text-align: center;
            place-self: end center;
            transform: perspective(500px) translateY(100%) rotateX(-90deg);
            backface-visibility: hidden;
            transform-origin: top;
            background: #000;
            transition: .5s;
        }

        figure:hover img {
            width: 130%;
            height: 255%;
            filter: contrast(1);
        }

        figure:hover::before {
            filter: brightness(0.3);
        }

        figure {
            transform: perspective(500px) rotateX(60deg);
        }

        figure:hover figcaption {
            transform: perspective(500px) translateY(100%) rotateX(-30deg);
        }

        body {
            margin: 0;
            min-height: 100vh;
            display: grid;
            grid-auto-flow: column;
            grid-auto-columns: min(230px, 35vmin);
            place-content: end center;
            gap: 50px;
            background: linear-gradient(to bottom, #0000, rgba(50, 50, 50, 0.88)), url("https://assets.codepen.io/1480814/diablo-reaper-of-souls-mw-1360x768.jpg") top/cover;
        }
    </style>
    <title>Document</title>
</head>
<body>
    <figure>
        <img src="https://assets.codepen.io/1480814/necro.png" alt="Necromancer">
        <figcaption>The Necro</figcaption>
    </figure>
    <figure>
        <img src="https://assets.codepen.io/1480814/druide.png" alt="Druid">
        <figcaption>The Druid</figcaption>
    </figure>
</body>
</html>
