<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Happy Valentine’s Day, Gowri</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg-start: #faf7f5;
      --bg-end: #f1ece9;
      --primary: #1f1f1f;
      --muted: #6b6b6b;
      --accent: #c89b8c;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: linear-gradient(180deg, var(--bg-start), var(--bg-end));
      color: var(--primary);
      height: 100vh;
      overflow: hidden;
    }

    .slides {
      height: 100vh;
      display: flex;
      transition: transform 1s cubic-bezier(0.77, 0, 0.175, 1);
    }

    .slide {
      min-width: 100vw;
      height: 100vh;
      padding: 10vh 8vw;
      display: flex;
      flex-direction: column;
      justify-content: center;
      position: relative;
    }

    .slide::after {
      content: "❤";
      position: absolute;
      bottom: 40px;
      right: 40px;
      font-size: 14px;
      opacity: 0.2;
    }

    h1 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2.5rem, 5vw, 4rem);
      font-weight: 600;
      margin-bottom: 20px;
      animation: fadeUp 1.2s ease forwards;
    }

    h2 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2rem, 4vw, 3rem);
      font-weight: 500;
      margin-bottom: 20px;
    }

    p {
      font-size: 1.05rem;
      line-height: 1.9;
      color: var(--muted);
      max-width: 620px;
    }

    .name {
      color: var(--accent);
      font-style: italic;
    }

    .signature {
      margin-top: 40px;
      font-family: 'Playfair Display', serif;
      font-size: 1.2rem;
    }

    .nav {
      position: fixed;
      bottom: 30px;
      width: 100%;
      display: flex;
      justify-content: center;
      gap: 20px;
    }

    button {
      background: none;
      border: 1px solid rgba(0,0,0,0.15);
      padding: 10px 22px;
      border-radius: 30px;
      font-family: 'Inter', sans-serif;
      font-size: 0.9rem;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    button:hover {
      background: rgba(0,0,0,0.05);
      transform: translateY(-2px);
    }

    @keyframes fadeUp {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @media (max-width: 600px) {
      .slide {
        padding: 12vh 6vw;
      }
    }
  </style>
</head>

<body>

  <div class="slides" id="slides">

    <!-- Slide 1 -->
    <section class="slide">
      <h1>Happy Valentine’s Day</h1>
      <h2>My Better Half, <span class="name">Gowri</span></h2>
      <p>
        This is not just a wish.  
        It’s a quiet pause in time — to remind you how deeply you are loved.
      </p>
    </section>

    <!-- Slide 2 -->
    <section class="slide">
      <h1>What You Mean to Me</h1>
      <p>
        You are comfort in chaos.  
        Calm in noise.  
        A feeling that words will never fully explain — yet my heart understands perfectly.
      </p>
    </section>

    <!-- Slide 3 -->
    <section class="slide">
      <h1>Everyday Love</h1>
      <p>
        Not the dramatic kind —  
        but the gentle, steady love that grows stronger in silence, smiles, and shared moments.
      </p>
    </section>

    <!-- Slide 4 -->
    <section class="slide">
      <h1>Forever, Slowly</h1>
      <p>
        No rush. No pressure.  
        Just choosing you — again and again — in all the little ways that matter.
      </p>
    </section>

    <!-- Slide 5 -->
    <section class="slide">
      <h1>Always Yours</h1>
      <p>
        Happy Valentine’s Day, <span class="name">Gowri</span>.  
        Thank you for being you.
      </p>

      <div class="signature">
        — With all my love,<br>
        <strong>Suneesh</strong>
      </div>
    </section>

  </div>

  <div class="nav">
    <button onclick="prev()">Previous</button>
    <button onclick="next()">Next</button>
  </div>

  <script>
    let index = 0;
    const slides = document.getElementById("slides");

    function updateSlide() {
      slides.style.transform = `translateX(-${index * 100}vw)`;
    }

    function next() {
      if (index < 4) {
        index++;
        updateSlide();
      }
    }

    function prev() {
      if (index > 0) {
        index--;
        updateSlide();
      }
    }

    document.addEventListener("keydown", (e) => {
      if (e.key === "ArrowRight") next();
      if (e.key === "ArrowLeft") prev();
    });
  </script>

</body>
</html>
