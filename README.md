<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Calculator</title>
  <link rel="stylesheet" href="style.css"> <!-- External CSS File -->
</head>
<body>
  <!-- Calculator Section -->
  <div class="calculator">
    <input type="text" id="display" disabled />
    <div class="buttons">
      <!-- Calculator Buttons -->
      <button onclick="appendToDisplay('7')">7</button>
      <button onclick="appendToDisplay('8')">8</button>
      <button onclick="appendToDisplay('9')">9</button>
      <button onclick="appendToDisplay('/')">/</button>
      
      <button onclick="appendToDisplay('4')">4</button>
      <button onclick="appendToDisplay('5')">5</button>
      <button onclick="appendToDisplay('6')">6</button>
      <button onclick="appendToDisplay('*')">*</button>
      
      <button onclick="appendToDisplay('1')">1</button>
      <button onclick="appendToDisplay('2')">2</button>
      <button onclick="appendToDisplay('3')">3</button>
      <button onclick="appendToDisplay('-')">-</button>
      
      <button onclick="appendToDisplay('0')">0</button>
      <button onclick="clearDisplay()">C</button>
      <button onclick="calculate()">=</button>
      <button onclick="appendToDisplay('+')">+</button>
    </div>

    <!-- Profit Percentage Section (Initially Hidden) -->
    <button id="profit-percentage-btn" onclick="toggleProfitPercentageSection()">Profit Percentage</button>
    <div id="profit-percentage-section" style="display:none;">
      <label for="investment">Investment: </label>
      <input type="number" id="investment" placeholder="Enter investment" />

      <label for="profit">Profit: </label>
      <input type="number" id="profit" placeholder="Enter profit" />

      <button onclick="calculateProfitPercentage()">Percentage</button>
    </div>
    <div>
      <h3>Profit Percentage: <span id="profit-percentage">0%</span></h3>
    </div>

    <!-- Guide Section -->
    <button onclick="toggleGuide()">Guide</button>
    <div id="guide-section" style="display:none;">
      <p>1. Use number buttons (0-9) for calculations.</p>
      <p>2. Use operator buttons (+, -, *, /) for operations.</p>
      <p>3. The "C" button clears the display.</p>
      <p>4. Click "Guide" anytime for help.</p>
      <button onclick="closeGuide()">Got it!</button>
    </div>

    <!-- History Section -->
    <button onclick="toggleHistory()">History</button>
    <div id="history-section" style="display:none;">
      <ul id="history-list">
        <!-- History items will appear here -->
      </ul>
    </div>

    <!-- Special Message Section -->
    <button onclick="showSpecialMessage()">❤️</button>
    <div id="special-message" style="display:none;">
      <p>❤️ I love you, Mom! ❤️</p>
    </div>
  </div>

  <script src="script.js"></script> <!-- External JavaScript File -->
</body>
</html>
