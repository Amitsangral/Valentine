<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Valentine Question 💘</title>
  <style>
    body {
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
    }

    .container {
      text-align: center;
      position: relative;
      width: 100%;
      height: 100%;
    }

    h1 {
      margin-top: 100px;
      color: #fff;
    }

    .buttons {
      margin-top: 40px;
    }

    button {
      padding: 15px 30px;
      font-size: 18px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    #yes {
      background-color: #28a745;
      color: white;
      margin-right: 20px;
    }

    #no {
      background-color: #dc3545;
      color: white;
      position: absolute;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>Will you be my Valentine, Lay Lay Myint? 💖</h1>

    <div class="buttons">
      <button id="yes" onclick="yesClicked()">Yes 💕</button>
      <button id="no" onmouseover="moveNo()">No 💔</button>
    </div>
  </div>

  <script>
    function moveNo() {
      const noBtn = document.getElementById("no");

      const x = Math.random() * (window.innerWidth - 100);
      const y = Math.random() * (window.innerHeight - 100);

      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    }

    function yesClicked() {
      alert("Yayyy! 💘 I knew it 😍");
    }
  </script>

</body>
</html>
