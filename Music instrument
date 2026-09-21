<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Band Organ Studio</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background: #111;
            color: white;
            min-height: 100vh;
        }

        header {
            background: #181818;
            padding: 20px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid #333;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin-left: 25px;
        }

        nav a:hover {
            color: #ffcc00;
        }

        .hero {
            text-align: center;
            padding: 60px 20px 30px;
        }

        .hero h1 {
            font-size: 48px;
            margin-bottom: 10px;
        }

        .hero p {
            color: #bbb;
            font-size: 18px;
        }

        .studio {
            width: 90%;
            max-width: 1100px;
            margin: 30px auto;
            background: #1d1d1d;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.5);
        }

        .controls {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
            margin-bottom: 30px;
        }

        button {
            border: none;
            padding: 12px 20px;
            border-radius: 8px;
            background: #333;
            color: white;
            cursor: pointer;
            font-size: 15px;
        }

        button:hover {
            background: #ffcc00;
            color: #111;
        }

        .volume {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        input[type="range"] {
            cursor: pointer;
        }

        /* ORGAN */

        .organ {
            background: #292929;
            padding: 25px;
            border-radius: 12px;
            border: 2px solid #444;
        }

        .organ-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
        }

        .organ-name {
            font-size: 22px;
            font-weight: bold;
        }

        .screen {
            background: #080808;
            color: #00ff88;
            padding: 10px 20px;
            border-radius: 5px;
            font-family: monospace;
        }

        .keys {
            display: flex;
            justify-content: center;
            position: relative;
            height: 220px;
            overflow-x: auto;
        }

        .key {
            width: 65px;
            height: 210px;
            background: white;
            color: #111;
            border: 1px solid #777;
            border-radius: 0 0 7px 7px;
            display: flex;
            align-items: flex-end;
            justify-content: center;
            padding-bottom: 15px;
            cursor: pointer;
            user-select: none;
            position: relative;
            z-index: 1;
        }

        .key:hover,
        .key.active {
            background: #ffcc00;
            transform: translateY(4px);
        }

        .black-key {
            width: 40px;
            height: 125px;
            background: #111;
            color: white;
            position: absolute;
            z-index: 2;
            top: 0;
            border-radius: 0 0 6px 6px;
            display: flex;
            align-items: flex-end;
            justify-content: center;
            padding-bottom: 12px;
            cursor: pointer;
        }

        .black-key:hover,
        .black-key.active {
            background: #444;
        }

        /* DRUMS */

        .drums {
            margin-top: 35px;
            text-align: center;
        }

        .drum-buttons {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }

        .drum {
            width: 100px;
            height: 70px;
            background: #252525;
            border: 2px solid #555;
            font-weight: bold;
        }

        .drum.active {
            background: #ffcc00;
            color: #111;
        }

        footer {
            text-align: center;
            padding: 30px;
            color: #777;
        }

        @media(max-width: 700px) {

            .hero h1 {
                font-size: 34px;
            }

            .studio {
                width: 95%;
                padding: 15px;
            }

            .key {
                width: 50px;
                height: 180px;
            }

            .keys {
                height: 190px;
            }

            nav {
                display: none;
            }
        }
    </style>
</head>

<body>

<header>

    <div class="logo">
        🎹 BAND ORGAN
    </div>

    <nav>
        <a href="#organ">Organ</a>
        <a href="#drums">Drums</a>
        <a href="#about">About</a>
    </nav>

</header>


<section class="hero">

    <h1>Play Your Music</h1>

    <p>
        A simple virtual organ and band instrument studio.
    </p>

</section>


<div class="studio">

    <div class="controls">

        <button onclick="stopAll()">
            ⏹ Stop
        </button>

        <button onclick="playChord()">
            🎵 Play Chord
        </button>

        <div class="volume">

            🔊 Volume

            <input
                type="range"
                id="volume"
                min="0"
                max="1"
                step="0.01"
                value="0.5"
            >

        </div>

    </div>


    <!-- ORGAN -->

    <section id="organ" class="organ">

        <div class="organ-top">

            <div class="organ-name">
                🎹 Virtual Organ
            </div>

            <div class="screen" id="screen">
                READY
            </div>

        </div>


        <div class="keys">

            <!-- WHITE KEYS -->

            <div class="key" data-note="C4">C</div>
            <div class="key" data-note="D4">D</div>
            <div class="key" data-note="E4">E</div>
            <div class="key" data-note="F4">F</div>
            <div class="key" data-note="G4">G</div>
            <div class="key" data-note="A4">A</div>
            <div class="key" data-note="B4">B</div>
            <div class="key" data-note="C5">C</div>

            <!-- BLACK KEYS -->

            <div
                class="black-key"
                data-note="C#4"
                style="left: 7%;"
            >
                C#
            </div>

            <div
                class="black-key"
                data-note="D#4"
                style="left: 19%;"
            >
                D#
            </div>

            <div
                class="black-key"
                data-note="F#4"
                style="left: 44%;"
            >
                F#
            </div>

            <div
                class="black-key"
                data-note="G#4"
                style="left: 56%;"
            >
                G#
            </div>

            <div
                class="black-key"
                data-note="A#4"
                style="left: 68%;"
            >
                A#
            </div>

        </div>

    </section>


    <!-- DRUMS -->

    <section id="drums" class="drums">

        <h2>🥁 Band Drums</h2>

        <div class="drum-buttons">

            <button class="drum" data-sound="kick">
                KICK
            </button>

            <button class="drum" data-sound="snare">
                SNARE
            </button>

            <button class="drum" data-sound="hihat">
                HI-HAT
            </button>

            <button class="drum" data-sound="tom">
                TOM
            </button>

            <button class="drum" data-sound="clap">
                CLAP
            </button>

        </div>

    </section>

</div>


<section id="about" class="hero">

    <h2>🎶 Create Your Own Sound</h2>

    <p>
        Play the keyboard, experiment with chords,
        and build your own rhythm.
    </p>

</section>


<footer>

    © 2026 Band Organ Studio · Made for Music Lovers

</footer>


<script>

    let audioContext;

    const activeOscillators = [];


    function getAudioContext() {

        if (!audioContext) {

            audioContext =
                new (window.AudioContext ||
                window.webkitAudioContext)();

        }

        return audioContext;
    }


    // Piano frequencies

    const frequencies = {

        "C4": 261.63,
        "C#4": 277.18,
        "D4": 293.66,
        "D#4": 311.13,
        "E4": 329.63,
        "F4": 349.23,
        "F#4": 369.99,
        "G4": 392.00,
        "G#4": 415.30,
        "A4": 440.00,
        "A#4": 466.16,
        "B4": 493.88,
        "C5": 523.25

    };


    function playNote(note, element) {

        const ctx = getAudioContext();

        const oscillator =
            ctx.createOscillator();

        const gain =
            ctx.createGain();

        oscillator.type = "sine";

        oscillator.frequency.value =
            frequencies[note];

        gain.gain.value =
            document.getElementById("volume").value;

        oscillator.connect(gain);

        gain.connect(ctx.destination);

        oscillator.start();

        oscillator.stop(ctx.currentTime + 0.7);

        element.classList.add("active");

        document.getElementById("screen").textContent =
            note;

        setTimeout(() => {

            element.classList.remove("active");

        }, 200);

    }


    // Keyboard keys

    document.querySelectorAll(".key, .black-key")
        .forEach(key => {

            key.addEventListener("mousedown", () => {

                playNote(
                    key.dataset.note,
                    key
                );

            });

        });


    // Computer keyboard

    const keyboardMap = {

        "a": "C4",
        "w": "C#4",
        "s": "D4",
        "e": "D#4",
        "d": "E4",
        "f": "F4",
        "t": "F#4",
        "g": "G4",
        "y": "G#4",
        "h": "A4",
        "u": "A#4",
        "j": "B4",
        "k": "C5"

    };


    document.addEventListener("keydown", event => {

        const note =
            keyboardMap[event.key.toLowerCase()];

        if (!note) return;

        const key =
            document.querySelector(
                `[data-note="${note}"]`
            );

        if (key) {

            playNote(note, key);

        }

    });


    // Chord

    function playChord() {

        const notes = [
            "C4",
            "E4",
            "G4"
        ];

        notes.forEach(note => {

            const key =
                document.querySelector(
                    `[data-note="${note}"]`
                );

            playNote(note, key);

        });

    }


    function stopAll() {

        document.getElementById("screen")
            .textContent = "STOPPED";

    }


    // Drum sound generator

    document.querySelectorAll(".drum")
        .forEach(button => {

            button.addEventListener("click", () => {

                playDrum(button.dataset.sound);

                button.classList.add("active");

                setTimeout(() => {

                    button.classList.remove("active");

                }, 150);

            });

        });


    function playDrum(type) {

        const ctx = getAudioContext();

        const oscillator =
            ctx.createOscillator();

        const gain =
            ctx.createGain();


        if (type === "kick") {

            oscillator.frequency.setValueAtTime(
                150,
                ctx.currentTime
            );

            oscillator.frequency.exponentialRampToValueAtTime(
                50,
                ctx.currentTime + 0.15
            );

            gain.gain.setValueAtTime(
                1,
                ctx.currentTime
            );

            gain.gain.exponentialRampToValueAtTime(
                0.01,
                ctx.currentTime + 0.2
            );

        }


        else if (type === "snare") {

            oscillator.type = "triangle";

            oscillator.frequency.value = 180;

            gain.gain.setValueAtTime(
                0.7,
                ctx.currentTime
            );

            gain.gain.exponentialRampToValueAtTime(
                0.01,
                ctx.currentTime + 0.15
            );

        }


        else if (type === "hihat") {

            oscillator.type = "square";

            oscillator.frequency.value = 800;

            gain.gain.setValueAtTime(
                0.3,
                ctx.currentTime
            );

            gain.gain.exponentialRampToValueAtTime(
                0.01,
                ctx.currentTime + 0.08
            );

        }


        else if (type === "tom") {

            oscillator.frequency.value = 120;

            gain.gain.setValueAtTime(
                0.8,
                ctx.currentTime
            );

            gain.gain.exponentialRampToValueAtTime(
                0.01,
                ctx.currentTime + 0.3
            );

        }


        else if (type === "clap") {

            oscillator.type = "square";

            oscillator.frequency.value = 300;

            gain.gain.setValueAtTime(
                0.5,
                ctx.currentTime
            );

            gain.gain.exponentialRampToValueAtTime(
                0.01,
                ctx.currentTime + 0.12
            );

        }


        oscillator.connect(gain);

        gain.connect(ctx.destination);

        oscillator.start();

        oscillator.stop(
            ctx.currentTime + 0.4
        );

    }

</script>

</body>
</html>
