<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>hi ht - Luxury Experience</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700&family=Montserrat:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        :root {
            --gold-gradient: linear-gradient(135deg, #BF953F 0%, #FCF6BA 25%, #B38728 50%, #FBF5B7 75%, #AA771C 100%);
            --gold-solid: #D4AF37;
            --gold-light: #F3E5AB;
            --dark-bg: #0b0b0b;
            --card-bg: rgba(20, 20, 20, 0.75);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: var(--dark-bg);
            color: #ffffff;
            font-family: 'Montserrat', sans-serif;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow-x: hidden;
            position: relative;
        }

        /* Ambient Background Glow */
        .ambient-glow {
            position: absolute;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(212, 175, 55, 0.12) 0%, rgba(11, 11, 11, 0) 70%);
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 1;
            pointer-events: none;
            animation: pulseGlow 6s ease-in-out infinite alternate;
        }

        @keyframes pulseGlow {
            0% { transform: translate(-50%, -50%) scale(0.9); opacity: 0.7; }
            100% { transform: translate(-50%, -50%) scale(1.1); opacity: 1; }
        }

        /* Main Container Card */
        .luxury-card {
            position: relative;
            z-index: 2;
            width: 90%;
            max-width: 650px;
            background: var(--card-bg);
            border: 1px solid rgba(212, 175, 55, 0.3);
            border-radius: 16px;
            padding: 60px 40px;
            text-align: center;
            backdrop-filter: blur(12px);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.8), 
                        inset 0 1px 0 rgba(255, 255, 255, 0.1);
        }

        /* Elegant Corner Accents */
        .luxury-card::before, .luxury-card::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            border-color: var(--gold-solid);
            border-style: solid;
            transition: all 0.3s ease;
        }
        .luxury-card::before {
            top: 12px;
            left: 12px;
            border-width: 1px 0 0 1px;
        }
        .luxury-card::after {
            bottom: 12px;
            right: 12px;
            border-width: 0 1px 1px 0;
        }

        /* Typography */
        h1 {
            font-family: 'Cinzel', serif;
            font-size: 3.5rem;
            font-weight: 700;
            letter-spacing: 6px;
            margin-bottom: 15px;
            background: var(--gold-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-transform: uppercase;
        }

        .subtitle {
            font-size: 0.95rem;
            letter-spacing: 4px;
            color: var(--gold-light);
            text-transform: uppercase;
            margin-bottom: 35px;
            opacity: 0.85;
            font-weight: 300;
        }

        .divider {
            width: 80px;
            height: 2px;
            background: var(--gold-gradient);
            margin: 0 auto 35px auto;
            border: none;
        }

        p {
            font-weight: 300;
            color: #cccccc;
            line-height: 1.8;
            font-size: 1.05rem;
            max-width: 460px;
            margin: 0 auto 40px auto;
        }

        /* Luxury Button */
        .gold-button {
            display: inline-block;
            padding: 16px 36px;
            font-family: 'Cinzel', serif;
            font-size: 0.9rem;
            font-weight: 600;
            letter-spacing: 2px;
            text-decoration: text-none;
            color: #111111;
            background: var(--gold-gradient);
            border: none;
            border-radius: 4px;
            cursor: pointer;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            box-shadow: 0 4px 15px rgba(191, 149, 63, 0.3);
            text-transform: uppercase;
        }

        .gold-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(252, 246, 186, 0.4);
        }

        /* Subtle Sparkles */
        .sparkle {
            position: absolute;
            background: #fff;
            border-radius: 50%;
            pointer-events: none;
            animation: twinkle 3s infinite ease-in-out;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.2; transform: scale(0.8); }
            50% { opacity: 1; transform: scale(1.2); }
        }
    </style>
</head>
<body>

    <div class="ambient-glow"></div>

    <!-- Random background decorative sparkles -->
    <div class="sparkle" style="width: 3px; height: 3px; top: 20%; left: 15%; animation-delay: 0s;"></div>
    <div class="sparkle" style="width: 2px; height: 2px; top: 75%; left: 80%; animation-delay: 1.2s;"></div>
    <div class="sparkle" style="width: 4px; height: 4px; top: 30%; left: 85%; animation-delay: 2.5s;"></div>
    <div class="sparkle" style="width: 2px; height: 2px; top: 80%; left: 20%; animation-delay: 1.8s;"></div>

    <div class="luxury-card">
        <h1>hi ht</h1>
        <div class="subtitle">Excellence in Craftsmanship</div>
        <hr class="divider">
        <p>Welcome to an experience defined by sophistication, refined aesthetics, and timeless golden luxury.</p>
        <button class="gold-button" onclick="alert('Welcome to hi ht.')">Explore Collection</button>
    </div>

</body>
</html>
