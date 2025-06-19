<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Custom Google</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: white;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }

    .search-box {
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    input[type="text"] {
      width: 500px;
      padding: 10px;
      font-size: 18px;
      border: 1px solid #ccc;
      border-radius: 24px;
      outline: none;
      text-align: center;
    }

    .answer {
      color: red;
      font-size: 45px; /* roughly 34pt */
      margin-top: 30px;
      visibility: hidden;
    }
  </style>
</head>
<body>

  <div class="search-box">
    <input type="text" id="search" placeholder="Search...">
    <div class="answer" id="response">yes ❤️</div>
  </div>

  <script>
    const input = document.getElementById('search');
    const response = document.getElementById('response');

    input.addEventListener('keydown', function(e) {
      if (e.key === 'Enter') {
        const value = input.value.trim().toLowerCase();
        if (value === "do i love my girlfriend more?") {
          response.style.visibility = 'visible';
        } else {
          response.style.visibility = 'hidden';
        }
      }
    });
  </script>

</body>
</html>
