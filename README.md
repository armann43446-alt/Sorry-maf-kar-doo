<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#10091e">
  <title>I'm Sorry ❤️</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --pink: #ff73b9;
      --purple: #a78bfa;
      --white: #fff5fb;
    }

    body {
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow-x: hidden;
      background:
        radial-gradient(ellipse at top, #32143e 0%, transparent 55%),
        linear-gradient(145deg, #090711, #170c27 55%, #10091e);
      color: var(--white);
      font-family: "Segoe UI", Arial, sans-serif;
      padding: 24px 16px;
    }

    .stars {
      position: fixed;
      inset: 0;
      pointer-events: none;
      background-image:
        radial-gradient(2px 2px at 15% 25%, #fff 50%, transparent),
        radial-gradient(2px 2px at 75% 15%, #ffb6df 50%, transparent),
        radial-gradient(1px 1px at 55% 65%, #fff 50%, transparent),
        radial-gradient(2px 2px at 90% 75%, #c4b5fd 50%, transparent),
        radial-gradient(1px 1px at 25% 85%, #fff 50%, transparent);
      opacity: .65;
    }

    .card {
      width: 100%;
      max-width: 430px;
      padding: 35px 24px;
      text-align: center;
      position: relative;
      z-index: 2;
      border: 1px solid rgba(255, 151, 215, .25);
      border-radius: 28px;
      background: rgba(255, 255, 255, .055);
      backdrop-filter: blur(18px);
      -webkit-backdrop-filter: blur(18px);
      box-shadow:
        0 0 55px rgba(208, 77, 185, .12),
        inset 0 0 25px rgba(255, 255, 255, .025);
      animation: appear 1s ease both;
    }

    .tag {
      display: inline-block;
      padding: 8px 15px;
      margin-bottom: 20px;
      border-radius: 30px;
      border: 1px solid rgba(255, 115, 185, .3);
      color: #ffc0e3;
      font-size: 12px;
      letter-spacing: 2px;
      text-transform: uppercase;
    }

    .heart {
      font-size: 65px;
      display: block;
      margin: 0 auto 15px;
      filter: drop-shadow(0 0 18px #ff4eab);
      animation: heartbeat 1.6s infinite;
    }

    h1 {
      font-size: clamp(37px, 10vw, 52px);
      line-height: 1.15;
      margin-bottom: 13px;
      letter-spacing: -1.5px;
      background: linear-gradient(90deg, #fff, #ff91cd, #c4b5fd);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
    }

    .subtitle {
      color: #d6c7e5;
      font-size: 15px;
      line-height: 1.8;
      margin-bottom: 25px;
    }

    .divider {
      height: 1px;
      margin: 20px 0;
      background: linear-gradient(
        90deg, transparent, #ff73b9, #a78bfa, transparent
      );
    }

    .message {
      display: none;
      padding: 18px;
      margin: 18px 0;
      border-radius: 18px;
      text-align: left;
      line-height: 1.9;
      color: #f7e9fa;
      background: rgba(255, 115, 185, .07);
      border: 1px solid rgba(255, 255, 255, .09);
      animation: appear .5s ease;
    }

    .message.show {
      display: block;
    }

    .message strong {
      color: #ffabd8;
    }

    .buttons {
      display: flex;
      flex-direction: column;
      gap: 12px;
      margin-top: 23px;
    }

    button {
      width: 100%;
      min-height: 49px;
      padding: 14px 18px;
      border: 0;
      border-radius: 15px;
      font-size: 15px;
      font-weight: 700;
      font-family: inherit;
      cursor: pointer;
      transition: transform .2s, box-shadow .2s;
      -webkit-tap-highlight-color: transparent;
    }

    button:active {
      transform: scale(.97);
    }

    .primary {
      color: #301029;
      background: linear-gradient(100deg, #ff91cd, #d5a7ff);
      box-shadow: 0 6px 24px rgba(255, 115, 185, .2);
    }

    .secondary {
      color: #ffe3f4;
      background: rgba(255, 255, 255, .06);
      border: 1px solid rgba(255, 165, 218, .3);
    }

    button:hover {
      box-shadow: 0 5px 25px rgba(255, 115, 185, .25);
    }

    .footer {
      margin-top: 24px;
      color: #a99ab9;
      font-size: 12px;
      line-height: 1.7;
    }

    .floating-heart {
      position: fixed;
      bottom: -40px;
      z-index: 1;
      pointer-events: none;
      opacity: 0;
      animation: floatUp 6s linear forwards;
    }

    .final-note {
      display: none;
      margin-top: 18px;
      padding: 16px 12px;
      color: #ffd4eb;
      line-height: 1.8;
      background: rgba(255, 115, 185, .08);
      border-radius: 15px;
      animation: appear .5s ease;
    }

    .final-note.show {
      display: block;
    }

    @keyframes heartbeat {
      0%, 100% { transform: scale(1); }
      15% { transform: scale(1.12); }
      30% { transform: scale(1); }
      45% { transform: scale(1.08); }
    }

    @keyframes appear {
      from {
        opacity: 0;
        transform: translateY(18px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes floatUp {
      0% {
        transform: translateY(0) rotate(0);
        opacity: 0;
      }
      15% { opacity: .7; }
      85% { opacity: .6; }
      100% {
        transform: translateY(-110vh) rotate(35deg);
        opacity: 0;
      }
    }

    @media (max-width: 360px) {
      .card { padding: 28px 18px; }
      .heart { font-size: 55px; }
      .subtitle { font-size: 14px; }
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after {
        animation-duration: .01ms !important;
        animation-iteration-count: 1 !important;
        scroll-behavior: auto !important;
      }
    }
  </style>
</head>

<body>
  <div class="stars"></div>

  <main class="card">
    <span class="tag">A little message for you</span>

    <span class="heart">💗</span>

    <h1>I'm Sorry</h1>

    <p class="subtitle">
      कभी-कभी हमसे गलतियाँ हो जाती हैं,<br>
      लेकिन कुछ लोग हमारे लिए बहुत खास होते हैं। 🥹
    </p>

    <div class="divider"></div>

    <p class="subtitle">
      तुम्हारे लिए एक छोटा-सा मैसेज है...<br>
      क्या तुम पढ़ोगी? 💌
    </p>

    <div class="buttons">
      <button class="primary" id="readBtn">
        💌 मेरा मैसेज पढ़ो
      </button>

      <button class="secondary" id="heartBtn">
        💖 तुम्हारे लिए एक दिल
      </button>
    </div>

    <div class="message" id="message">
      <strong>मेरी प्यारी... ❤️</strong>
      <br><br>
      अगर मेरी किसी बात या हरकत से तुम्हें दुख पहुँचा है,
      तो मुझे सच में माफ़ करना। 🥺
      <br><br>
      मेरा इरादा तुम्हें दुख पहुँचाने का नहीं था।
      लेकिन मैं समझता हूँ कि मेरी वजह से तुम्हें बुरा लगा,
      तो मुझे अपनी गलती सुधारनी चाहिए।
      <br><br>
      तुम मेरे लिए खास हो और तुम्हारी भावनाएँ भी मेरे लिए
      मायने रखती हैं। मैं चाहता हूँ कि हम शांति से बात करें
      और मैं तुम्हारी बात भी समझूँ।
      <br><br>
      <strong>I'm really sorry. Please forgive me if you can. 💗</strong>
    </div>

    <div class="final-note" id="finalNote">
      💖 तुम्हारे लिए एक छोटा-सा दिल! 💖
      <br>
      मेरी माफ़ी सच्ची है। जब तुम तैयार हो,
      हम आराम से बात कर सकते हैं। 🌷
    </div>

    <div class="divider"></div>

    <p class="footer">
      Made with a sincere heart 💗<br>
      Some mistakes deserve an honest apology.
    </p>
  </main>

  <script>
    const readBtn = document.getElementById("readBtn");
    const heartBtn = document.getElementById("heartBtn");
    const message = document.getElementById("message");
    const finalNote = document.getElementById("finalNote");

    readBtn.addEventListener("click", function () {
      message.classList.toggle("show");

      if (message.classList.contains("show")) {
        readBtn.textContent = "💌 मैसेज छुपाओ";
        message.scrollIntoView({
          behavior: "smooth",
          block: "nearest"
        });
      } else {
        readBtn.textContent = "💌 मेरा मैसेज पढ़ो";
      }
    });

    heartBtn.addEventListener("click", function () {
      finalNote.classList.toggle("show");
      heartBtn.textContent = finalNote.classList.contains("show")
        ? "💗 एक और प्यारा दिल"
        : "💖 तुम्हारे लिए एक दिल";

      createHearts(16);

      finalNote.scrollIntoView({
        behavior: "smooth",
        block: "nearest"
      });
    });

    function createHearts(count) {
      const symbols = ["💗", "💖", "💕", "💘", "✨"];

      for (let i = 0; i < count; i++) {
        const heart = document.createElement("span");

        heart.className = "floating-heart";
        heart.textContent =
          symbols[Math.floor(Math.random() * symbols.length)];

        heart.style.left = Math.random() * 100 + "vw";
        heart.style.fontSize = (16 + Math.random() * 20) + "px";
        heart.style.animationDuration = (4 + Math.random() * 3) + "s";

        document.body.appendChild(heart);

        heart.addEventListener("animationend", function () {
          heart.remove();
        });
      }
    }

    // छोटे-छोटे दिल समय-समय पर स्क्रीन पर दिखाई देंगे।
    setInterval(function () {
      if (document.hidden) return;

      const heart = document.createElement("span");
      heart.className = "floating-heart";
      heart.textContent = Math.random() > .5 ? "♡" : "💗";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.fontSize = (15 + Math.random() * 12) + "px";
      heart.style.animationDuration = "7s";

      document.body.appendChild(heart);

      heart.addEventListener("animationend", function () {
        heart.remove();
      });
    }, 1100);
  </script>
</body>
</html>

