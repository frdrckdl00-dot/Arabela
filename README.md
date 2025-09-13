<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Test Invite</title>
  <style>
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: linear-gradient(to bottom right, #dff6ff, #fef9f4);
      margin: 0;
      font-family: Arial, sans-serif;
    }
    .container {
      text-align: center;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Ara, will you go on a date with me?</h1>
    <button>Yes</button>
    <button>No</button>
  </div>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Invitation for Ara</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      height: 100vh;
      background: linear-gradient(to bottom right, #dff6ff, #fef9f4);
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      color: #333;
    }

    .container {
      max-width: 600px;
    }

    h1 {
      font-size: 2em;
      margin-bottom: 20px;
    }

    .buttons {
      margin: 20px 0;
    }

    button {
      padding: 12px 24px;
      font-size: 18px;
      margin: 10px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: background 0.3s;
    }

    #yesBtn {
      background: #ff6b81;
      color: white;
    }

    #yesBtn:hover {
      background: #ff4757;
    }

    #noBtn {
      background: #a29bfe;
      color: white;
    }

    #noBtn:hover {
      background: #6c5ce7;
    }

    .message {
      margin-top: 15px;
      font-style: italic;
      font-size: 1.1em;
    }

    .popup {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.6);
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .popup-content {
      background: white;
      padding: 30px;
      border-radius: 15px;
      text-align: center;
      max-width: 400px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
      animation: fadeIn 0.5s ease;
    }

    .popup-content img {
      width: 150px;
      margin-bottom: 15px;
    }

    @keyframes fadeIn {
      from {opacity: 0; transform: scale(0.8);}
      to {opacity: 1; transform: scale(1);}
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Ara, will you go on a date with me?</h1>

    <div class="buttons">
      <button id="yesBtn">Yes</button>
      <button id="noBtn">No</button>
    </div>

    <div class="message" id="message"></div>
  </div>

  <!-- Popup -->
  <div class="popup" id="popup">
    <div class="popup-content">
      <img src="stitch-flowers.png" alt="Stitch giving flowers">
      <p><strong>“Let all that you do be done in love.”</strong><br>— 1 Corinthians 16:14</p>
    </div>
  </div>

  <script>
    const noBtn = document.getElementById('noBtn');
    const yesBtn = document.getElementById('yesBtn');
    const message = document.getElementById('message');
    const popup = document.getElementById('popup');

    const messages = [
      "Are you sure, Ara? I promise it'll be fun!",
      "Come on, don't say no.",
      "One little yes won't hurt!",
      "I think you’ll enjoy it!",
      "Please? Just this once?",
      "You're too special to say no!"
    ];

    let clickCount = 0;

    noBtn.addEventListener('click', () => {
      if (clickCount < messages.length) {
        message.textContent = messages[clickCount];
        clickCount++;
      } else {
        noBtn.style.display = 'none';
        message.textContent = "Looks like 'No' is no longer an option.";
      }
    });

    yesBtn.addEventListener('click', () => {
      popup.style.display = 'flex';
    });
  </script>
</body>
</html>
