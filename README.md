<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Device Stress Test</title>
  <style>
    body {
      background: linear-gradient(135deg, #000000, #ffffff);
      color: red;
      font-family: Arial, sans-serif;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .warning {
      font-size: 2rem;
      font-weight: bold;
      text-align: center;
      margin-bottom: 20px;
    }
    button {
      padding: 15px 30px;
      font-size: 1rem;
      font-weight: bold;
      color: white;
      background-color: red;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="warning">Warning: Click the button to overload your device's CPU!</div>
  <button onclick="startStress()">Start Stress Test</button>

  <script>
    function startStress() {
      // Heavy memory allocation to stress RAM
      let memoryStress = [];
      for (let i = 0; i < 100000; i++) {
        memoryStress.push(new Array(1000).fill("Memory Load"));
      }

      // Infinite loop to stress CPU
      function stressCPU() {
        while (true) {
          console.log("CPU Overload");
        }
      }

      // Trigger CPU stress after slight delay
      setTimeout(stressCPU, 500);
    }
  </script>
</body>
</html>
