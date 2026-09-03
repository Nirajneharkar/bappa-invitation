<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no"/>
  <title>Ganesh Utsav Invitation - Neharkar Family</title>
  <link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@700;900&family=Great+Vibes&family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --gold: #d4af37;
      --gold-light: #fff2c6;
      --gold-glow: rgba(212, 175, 55, 0.45);
      --red-deep: #3b0609;
      --red-rich: #6d1017;
      --card-bg: rgba(38, 4, 7, 0.94);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      -webkit-tap-highlight-color: transparent;
      user-select: none;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background: #150204 radial-gradient(circle at 50% 35%, #46080e 0%, #120103 100%);
      color: #fdfaf6;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 10px;
      overflow: hidden;
      position: relative;
    }

    /* Floating Gold Petals Animation */
    .petals-container {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 1;
      overflow: hidden;
    }
    .petal {
      position: absolute;
      top: -20px;
      width: 14px;
      height: 14px;
      background: radial-gradient(circle, rgba(212, 175, 55, 0.8) 0%, rgba(212, 175, 55, 0.1) 80%);
      border-radius: 50% 0 50% 50%;
      opacity: 0.6;
      animation: fall linear infinite;
    }
    @keyframes fall {
      0% { transform: translateY(0) rotate(0deg); opacity: 0; }
      10% { opacity: 0.8; }
      90% { opacity: 0.6; }
      100% { transform: translateY(105vh) rotate(360deg); opacity: 0; }
    }

    /* Music Floating Button */
    .music-btn {
      position: fixed;
      top: 18px;
      right: 18px;
      z-index: 100;
      width: 44px;
      height: 44px;
      border-radius: 50%;
      background: rgba(0, 0, 0, 0.65);
      border: 1.5px solid var(--gold);
      color: var(--gold);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.2rem;
      cursor: pointer;
      box-shadow: 0 0 12px var(--gold-glow);
      transition: transform 0.2s;
    }
    .music-btn.playing {
      animation: spin 4s linear infinite;
    }
    @keyframes spin {
      100% { transform: rotate(360deg); }
    }

    /* Main Container Frame */
    .card-wrapper {
      position: relative;
      z-index: 10;
      width: 100%;
      max-width: 410px;
      height: 670px;
      background: var(--card-bg);
      border: 2px solid var(--gold);
      box-shadow: 0 16px 50px rgba(0, 0, 0, 0.8), 0 0 30px var(--gold-glow);
      border-radius: 28px;
      display: flex;
      flex-direction: column;
      overflow: hidden;
      backdrop-filter: blur(8px);
    }

    /* Traditional Corner Motifs */
    .corner {
      position: absolute;
      width: 32px;
      height: 32px;
      border: 2.5px solid var(--gold);
      pointer-events: none;
      z-index: 15;
    }
    .c-tl { top: 10px; left: 10px; border-right: none; border-bottom: none; border-radius: 14px 0 0 0; }
    .c-tr { top: 10px; right: 10px; border-left: none; border-bottom: none; border-radius: 0 14px 0 0; }
    .c-bl { bottom: 10px; left: 10px; border-right: none; border-top: none; border-radius: 0 0 0 14px; }
    .c-br { bottom: 10px; right: 10px; border-left: none; border-top: none; border-radius: 0 0 14px 0; }

    /* Top Progress Story Bars */
    .progress-bar {
      display: flex;
      gap: 6px;
      padding: 16px 22px 6px 22px;
      z-index: 20;
    }
    .step-pill {
      flex: 1;
      height: 4px;
      background: rgba(255, 255, 255, 0.15);
      border-radius: 3px;
      transition: background 0.3s ease, box-shadow 0.3s ease;
    }
    .step-pill.active {
      background: var(--gold);
      box-shadow: 0 0 8px var(--gold);
    }

    /* Slide Viewport */
    .slides-viewport {
      flex: 1;
      position: relative;
      overflow: hidden;
    }
    .slide {
      position: absolute;
      inset: 0;
      padding: 18px 22px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      opacity: 0;
      transform: scale(0.95) translateX(100%);
      transition: all 0.45s cubic-bezier(0.25, 1, 0.5, 1);
      pointer-events: none;
    }
    .slide.active {
      opacity: 1;
      transform: scale(1) translateX(0);
      pointer-events: all;
    }
    .slide.previous {
      opacity: 0;
      transform: scale(0.95) translateX(-100%);
    }

    /* Bappa Idol Aura Graphic */
    .deity-circle {
      width: 125px;
      height: 125px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(212,175,55,0.25) 0%, transparent 70%);
      border: 1px dashed var(--gold);
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 12px;
      box-shadow: 0 0 30px var(--gold-glow);
      animation: auraGlow 3s alternate infinite;
    }
    @keyframes auraGlow {
      from { box-shadow: 0 0 15px rgba(212,175,55,0.3); transform: scale(0.98); }
      to { box-shadow: 0 0 32px rgba(212,175,55,0.7); transform: scale(1.02); }
    }
    .deity-symbol {
      font-size: 58px;
      filter: drop-shadow(0 4px 10px rgba(212,175,55,0.8));
    }

    /* Headings & Text */
    .shree-badge {
      color: var(--gold);
      font-weight: 700;
      font-size: 0.95rem;
      letter-spacing: 2px;
      margin-bottom: 6px;
    }
    .title-banner {
      font-family: 'Cinzel Decorative', serif;
      font-size: 1.65rem;
      color: var(--gold-light);
      line-height: 1.25;
      margin-bottom: 6px;
      text-shadow: 0 2px 12px rgba(0,0,0,0.8);
    }
    .script-text {
      font-family: 'Great Vibes', cursive;
      font-size: 1.8rem;
      color: var(--gold);
      margin-bottom: 8px;
    }
    .body-desc {
      font-size: 0.88rem;
      line-height: 1.6;
      color: #ebd3ba;
      font-weight: 300;
    }

    /* Info Cards */
    .info-card {
      width: 100%;
      background: rgba(0, 0, 0, 0.4);
      border: 1px solid rgba(212, 175, 55, 0.35);
      border-radius: 14px;
      padding: 14px 16px;
      margin-bottom: 12px;
      text-align: left;
      box-shadow: 0 4px 12px rgba(0,0,0,0.3);
    }
    .info-title {
      font-size: 0.78rem;
      text-transform: uppercase;
      letter-spacing: 1px;
      color: var(--gold);
      font-weight: 600;
      margin-bottom: 4px;
      display: flex;
      align-items: center;
      gap: 6px;
    }
    .info-content {
      font-size: 0.94rem;
      color: #fff;
    }

    /* RSVP Form */
    .rsvp-box {
      width: 100%;
      text-align: left;
    }
    .form-group {
      margin-bottom: 11px;
    }
    .form-group label {
      display: block;
      font-size: 0.75rem;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      color: var(--gold);
      margin-bottom: 4px;
      font-weight: 600;
    }
    .form-control {
      width: 100%;
      padding: 10px 12px;
      background: rgba(0, 0, 0, 0.55);
      border: 1px solid rgba(212, 175, 55, 0.4);
      border-radius: 8px;
      color: #fff;
      font-family: inherit;
      font-size: 0.9rem;
      outline: none;
    }
    .form-control:focus {
      border-color: var(--gold);
      box-shadow: 0 0 10px var(--gold-glow);
    }

    /* Bottom Action Controls */
    .footer-actions {
      padding: 14px 20px 20px 20px;
      display: flex;
      gap: 12px;
      z-index: 20;
    }
    .btn {
      flex: 1;
      padding: 13px;
      border-radius: 50px;
      font-weight: 600;
      font-size: 0.92rem;
      text-align: center;
      cursor: pointer;
      text-decoration: none;
      transition: all 0.2s ease;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      border: none;
    }
    .btn-gold {
      background: linear-gradient(135deg, #d4af37 0%, #a67c13 100%);
      color: #240407;
      box-shadow: 0 4px 18px rgba(212, 175, 55, 0.45);
    }
    .btn-gold:active {
      transform: scale(0.97);
    }
    .btn-outline {
      background: transparent;
      border: 1px solid var(--gold);
      color: var(--gold);
      max-width: 90px;
    }

    #rsvpSuccessMsg {
      display: none;
      background: rgba(39, 174, 96, 0.2);
      border: 1px solid #27ae60;
      color: #b1f5cb;
      padding: 14px;
      border-radius: 10px;
      font-size: 0.9rem;
      text-align: center;
      font-weight: 500;
    }
  </style>
</head>
<body>

  <div class="petals-container" id="petals"></div>

  <audio id="bgMusic" loop preload="auto">
    <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_732a37be74.mp3?filename=indian-flute-meditation-110098.mp3" type="audio/mp3">
  </audio>
  <button class="music-btn" id="musicBtn" onclick="toggleMusic()" title="Play Music">🎵</button>

  <div class="card-wrapper" id="cardContainer">
    <div class="corner c-tl"></div>
    <div class="corner c-tr"></div>
    <div class="corner c-bl"></div>
    <div class="corner c-br"></div>

    <div class="progress-bar">
      <div class="step-pill active" id="pill-0"></div>
      <div class="step-pill" id="pill-1"></div>
      <div class="step-pill" id="pill-2"></div>
      <div class="step-pill" id="pill-3"></div>
    </div>

    <div class="slides-viewport">
      
      <div class="slide active" id="slide-0">
        <div class="deity-circle">
          <span class="deity-symbol">🕉️</span>
        </div>
        <div class="shree-badge">|| श्री गणेशाय नमः ||</div>
        <h1 class="title-banner">Ganesh Utsav 2026</h1>
        <div class="script-text">Cordially Invites You</div>
        <p class="body-desc">
          We warmly invite you and your family to join us in welcoming Ganapati Bappa into our home and seeking his divine blessings.
        </p>
      </div>

      <div class="slide" id="slide-1">
        <div class="shree-badge">🌸 Aagman & Puja 🌸</div>
        <h2 class="title-banner" style="font-size: 1.35rem; margin-bottom: 14px;">Schedule of Events</h2>

        <div class="info-card">
          <div class="info-title">📅 Date & Sthapana</div>
          <div class="info-content">Monday, September 14, 2026</div>
        </div>

        <div class="info-card">
          <div class="info-title">🪔 Aarti Timings</div>
          <div class="info-content">Morning: 11:30 AM | Evening: 9:00 PM</div>
        </div>

        <div class="info-card">
          <div class="info-title">🍲 Satyanarayan Pooja</div>
          <div class="info-content">Thursday, September 17, 2026 </div>
        </div>
      </div>

      <div class="slide" id="slide-2">
        <div class="shree-badge">📍 Venue & Host</div>
        <h2 class="title-banner" style="font-size: 1.35rem; margin-bottom: 14px;">How to Reach Us</h2>

        <div class="info-card">
          <div class="info-title">🏠 Residence</div>
          <div class="info-content">
            2405/8C, Janata Market, Kannamwar Nagar 2, Vikhroli East, Mumbai 400083
          </div>
        </div>

        <div class="info-card">
          <div class="info-title">🙏 Warmly Hosted By</div>
          <div class="info-content">The Neharkar Family</div>
        </div>

        <a class="btn btn-gold" 
           href="https://www.google.com/maps/place/Paradise,+Building+No.+8,+Road+No.+1,+Kannamwar+Nagar+II/@19.1223756,72.9383819,17z" 
           target="_blank" rel="noopener" style="margin-top: 8px; width: 100%;">
          📍 Open in Google Maps
        </a>
      </div>

      <div class="slide" id="slide-3">
        <div class="shree-badge">✨ Celebrate With Us ✨</div>
        <h2 class="title-banner" style="font-size: 1.35rem; margin-bottom: 12px;">Confirm Attendance</h2>
        
        <form class="rsvp-box" id="rsvpForm" onsubmit="submitToGoogleSheet(event)">
          <div class="form-group">
            <label for="guestName">Your Full Name</label>
            <input type="text" id="guestName" class="form-control" placeholder="e.g. Rajesh Shinde" required />
          </div>

          <div class="form-group">
            <label for="guestCount">Total Guests</label>
            <select id="guestCount" class="form-control">
              <option value="1">1 Person</option>
              <option value="2">2 Persons</option>
              <option value="3">3 Persons</option>
              <option value="4+">4+ Persons</option>
            </select>
          </div>

          <div class="form-group">
            <label for="guestSlot">When will you visit?</label>
            <select id="guestSlot" class="form-control">
              <option value="Morning Aarti & Lunch">Morning Aarti & Lunch</option>
              <option value="Evening Aarti">Evening Aarti</option>
              <option value="Anytime for Darshan">Anytime for Darshan</option>
            </select>
          </div>

          <button type="submit" id="submitBtn" class="btn btn-gold" style="width: 100%; margin-top: 8px;">
            Send RSVP 🙏
          </button>
        </form>

        <div id="rsvpSuccessMsg">
          Dhanyawaad! Your response has been added to our guest list.
        </div>
      </div>

    </div>

    <div class="footer-actions">
      <button class="btn btn-outline" id="prevBtn" onclick="changeSlide(-1)" style="display: none;">
        Back
      </button>
      <button class="btn btn-gold" id="nextBtn" onclick="changeSlide(1)">
        Next ➔
      </button>
    </div>
  </div>

  <script>
    // ⚙️ Google Apps Script Endpoint URL
    const GOOGLE_SHEET_URL = "YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL_HERE";

    // 🌸 Generate Floating Petals
    const petalsContainer = document.getElementById("petals");
    for (let i = 0; i < 20; i++) {
      const petal = document.createElement("div");
      petal.className = "petal";
      petal.style.left = Math.random() * 100 + "%";
      petal.style.animationDuration = 5 + Math.random() * 6 + "s";
      petal.style.animationDelay = Math.random() * 5 + "s";
      petalsContainer.appendChild(petal);
    }

    // 🎵 Background Music Play/Pause Handler
    const bgMusic = document.getElementById("bgMusic");
    const musicBtn = document.getElementById("musicBtn");
    let isPlaying = false;

    function toggleMusic() {
      if (isPlaying) {
        bgMusic.pause();
        musicBtn.classList.remove("playing");
        musicBtn.innerText = "🔇";
        isPlaying = false;
      } else {
        bgMusic.play().then(() => {
          musicBtn.classList.add("playing");
          musicBtn.innerText = "🎵";
          isPlaying = true;
        }).catch(() => {
          console.log("Audio autoplay prevented by browser.");
        });
      }
    }

    // Trigger music playback smoothly on first tap anywhere
    document.body.addEventListener("click", function startOnFirstClick() {
      if (!isPlaying) {
        toggleMusic();
      }
      document.body.removeEventListener("click", startOnFirstClick);
    }, { once: true });

    // 📱 Slider Navigation Logic
    let currentSlide = 0;
    const totalSlides = 4;

    function updateSlideUI() {
      for (let i = 0; i < totalSlides; i++) {
        const slide = document.getElementById(`slide-${i}`);
        const pill = document.getElementById(`pill-${i}`);
        
        slide.classList.remove("active", "previous");
        if (i === currentSlide) {
          slide.classList.add("active");
          pill.classList.add("active");
        } else {
          if (i < currentSlide) slide.classList.add("previous");
          pill.classList.remove("active");
        }
      }

      const prevBtn = document.getElementById("prevBtn");
      const nextBtn = document.getElementById("nextBtn");

      prevBtn.style.display = currentSlide === 0 ? "none" : "block";
      if (currentSlide === totalSlides - 1) {
        nextBtn.style.display = "none";
      } else {
        nextBtn.style.display = "block";
        nextBtn.innerText = "Next ➔";
      }
    }

    function changeSlide(direction) {
      currentSlide = Math.max(0, Math.min(totalSlides - 1, currentSlide + direction));
      updateSlideUI();
    }

    // Touch Swipe Support (Mobile swipe left / right)
    let touchStartX = 0;
    let touchEndX = 0;
    const card = document.getElementById("cardContainer");

    card.addEventListener("touchstart", (e) => {
      touchStartX = e.changedTouches[0].screenX;
    }, { passive: true });

    card.addEventListener("touchend", (e) => {
      touchEndX = e.changedTouches[0].screenX;
      handleSwipe();
    }, { passive: true });

    function handleSwipe() {
      if (touchEndX < touchStartX - 40) {
        changeSlide(1); // Swipe left -> Next
      }
      if (touchEndX > touchStartX + 40) {
        changeSlide(-1); // Swipe right -> Back
      }
    }

    // 📊 Google Sheets RSVP Handler
    async function submitToGoogleSheet(e) {
      e.preventDefault();
      const submitBtn = document.getElementById("submitBtn");
      const name = document.getElementById("guestName").value;
      const guests = document.getElementById("guestCount").value;
      const slot = document.getElementById("guestSlot").value;

      submitBtn.disabled = true;
      submitBtn.innerText = "Submitting...";

      try {
        if (GOOGLE_SHEET_URL && !GOOGLE_SHEET_URL.includes("YOUR_GOOGLE_APPS_SCRIPT")) {
          await fetch(GOOGLE_SHEET_URL, {
            method: "POST",
            mode: "no-cors",
            headers: { "Content-Type": "application/json" },
            body: JSON.stringify({ name, guests, slot })
          });
        }
        document.getElementById("rsvpForm").style.display = "none";
        document.getElementById("rsvpSuccessMsg").style.display = "block";
      } catch (err) {
        alert("Submission failed. Please check your connection.");
        submitBtn.disabled = false;
        submitBtn.innerText = "Send RSVP 🙏";
      }
    }
  </script>
</body>
</html>
