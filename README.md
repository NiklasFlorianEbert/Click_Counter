# Click_Counter
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Click Counter</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding-top: 100px;
      background-color: #f8f0f8;
    }
    h1 {
      font-size: 2em;
      margin-bottom: 20px;
    }
    #count {
      font-size: 3em;
      color: #333;
    }
    button {
      padding: 10px 20px;
      font-size: 1.2em;
      margin-top: 20px;
      cursor: pointer;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 8px;
    }
    button:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>

  <h1>Click Counter</h1>
  <div id="count">0</div>
  <button onclick="incrementCount()">Click Me!</button>

  <script>
    // Get saved count from localStorage (or default to 0)
    let count = localStorage.getItem("clickCount") || 0;
    document.getElementById("count").innerText = count;

    // Function to increase count
    function incrementCount() {
      count++;
      document.getElementById("count").innerText = count;
      localStorage.setItem("clickCount", count);
    }
  </script>

</body>
</html>
