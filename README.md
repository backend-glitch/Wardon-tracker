# Wardon-tracker
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Wardon Tracker - Community Polls</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #f4f4f4;
      color: #333;
    }
    header {
      background: #007bff;
      color: white;
      padding: 1rem;
      text-align: center;
    }
    main {
      max-width: 600px;
      margin: 2rem auto;
      background: white;
      padding: 2rem;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    h2 {
      color: #007bff;
    }
    .option {
      margin-bottom: 10px;
    }
    button {
      background-color: #007bff;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .result {
      margin-top: 20px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <header>
    <h1>Wardon Tracker</h1>
    <p>Vote on Community Polls</p>
  </header>
  <main>
    <h2>Poll: What should be improved in the community?</h2>
    <form id="pollForm">
      <div class="option">
        <input type="radio" name="vote" value="Roads" id="opt1" required />
        <label for="opt1">Roads</label>
      </div>
      <div class="option">
        <input type="radio" name="vote" value="Water Supply" id="opt2" />
        <label for="opt2">Water Supply</label>
      </div>
      <div class="option">
        <input type="radio" name="vote" value="Electricity" id="opt3" />
        <label for="opt3">Electricity</label>
      </div>
      <div class="option">
        <input type="radio" name="vote" value="Sanitation" id="opt4" />
        <label for="opt4">Sanitation</label>
      </div>
      <button type="submit">Submit Vote</button>
    </form>
    <div class="result" id="resultMessage"></div>
  </main>

  <script>
    document.getElementById('pollForm').addEventListener('submit', function(e) {
      e.preventDefault();
      const selected = document.querySelector('input[name="vote"]:checked').value;
      document.getElementById('resultMessage').innerText = `Thank you for voting for: ${selected}`;
    });
  </script>
</body>
</html>
