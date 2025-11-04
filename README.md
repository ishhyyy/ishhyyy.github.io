<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>The Cholilah Goes to Lenirra 🌿</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <style>
    /* --- Base --- */
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background-color: #F5F4EE; /* Cream White */
      color: #333;
      scroll-behavior: smooth;
    }

    /* --- Header --- */
    header {
      background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), 
                  url('https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?fit=crop&w=1350&q=80') center/cover no-repeat;
      color: #F5F4EE; /* Cream White text */
      text-align: center;
      padding: 120px 20px;
    }

    header h1 {
      font-size: 2.8em;
      margin-bottom: 10px;
      color: #C99A9A; /* Dusty Rose */
    }

    header p {
      font-size: 1.2em;
      letter-spacing: 1px;
      color: #F5F4EE;
    }

    /* --- Sections --- */
    section {
      padding: 60px 20px;
      text-align: center;
      max-width: 900px;
      margin: auto;
    }

    .card {
      background-color: #E8DCC0; /* Beige */
      margin: 20px auto;
      border-radius: 15px;
      padding: 25px;
      box-shadow: 0 3px 10px rgba(0,0,0,0.1);
    }

    h2 {
      color: #A9B9A1; /* Sage Green */
      font-size: 1.8em;
    }

    /* --- Gallery --- */
    .gallery {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
    }

    .gallery img {
      width: 100%;
      max-width: 240px;
      border-radius: 10px;
      margin: 10px;
      transition: transform 0.3s ease;
    }

    .gallery img:hover {
      transform: scale(1.05);
    }

    /* --- Buttons --- */
    .btn {
      display: inline-block;
      background-color: #C99A9A; /* Dusty Rose */
      color: #F5F4EE;
      padding: 10px 25px;
      border-radius: 30px;
      text-decoration: none;
      transition: background 0.3s ease;
      margin-top: 10px;
    }

    .btn:hover {
      background-color: #A87F7F; /* Slightly darker Dusty Rose */
    }

    /* --- Footer --- */
    footer {
      background-color: #A9B9A1; /* Sage Green */
      color: #F5F4EE;
      text-align: center;
      padding: 20px;
    }
  </style>
</head>
<body>
  <header>
    <h1>🎬 The Cholilah Goes to Lenirra</h1>
    <p>Family Glamping Adventure — 6–7 December 2025</p>
  </header>

  <section>
    <div class="card">
      <h2>🏕 Trip Details</h2>
      <p>📍 Location: Lenirra Glamping, Cijeruk — Kabupaten Bogor<br>
         🗓 Date: 6–7 December 2025<br>
         🕒 Arrival: 11:00 AM</p>
      <p>🌾 Highlights: Walk in the sawah, enjoy mountain views, jump in the pool, ride ATV, go biking, and eat at cozy restaurant!</p>
    </div>

    <div class="card">
      <h2>📸 Photo Gallery</h2>
      <div class="gallery">
        <img src="https://images.unsplash.com/photo-1551318851-660c9ed26a2d?fit=crop&w=500&q=80" alt="Glamping Tent">
        <img src="https://images.unsplash.com/photo-1565372918674-6b4f1e5b52de?fit=crop&w=500&q=80" alt="Mountain View">
        <img src="https://images.unsplash.com/photo-1519821172141-b5d8b1f0a2c4?fit=crop&w=500&q=80" alt="Family Fun">
        <img src="https://images.unsplash.com/photo-1517816743773-6e0fd518b4a6?fit=crop&w=500&q=80" alt="Nature Walk">
      </div>
    </div>

    <div class="card">
      <h2>💚 About the Trip</h2>
      <p>Fun, laughter, and a whole lot of memories — let’s enjoy the mountains, sawah, and cozy glamping tents together! 🌞🌿</p>
    </div>

    <div class="card">
      <h2>💌 RSVP</h2>
      <p>Please confirm your attendance via email:</p>
      <a class="btn" href="mailto:thecholilahfamily@gmail.com?subject=Lenirra%20RSVP">Send RSVP 💌</a>
    </div>
  </section>

  <footer>
    🌿 The Cholilah Family · “The smiles, the chaos, the love — let’s capture it all.” 🌄
  </footer>
</body>
</html>
