<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <link rel="stylesheet" href="/Circle Progress Bar/style.css">
    <title></title>
  </head>
  <body>
    <div class="progress-bar">
      <span class="number" data-value="0"></span>
      <svg height="150" width="150" class="circle">
        <circle cx="75" cy="75" r="55" stroke="#d1c5fc" stroke-width="10" fill=""></circle>
      </svg>
    </div>

    <div>
      <label for="input-value">Enter a value:</label>
      <input type="number" id="input-value">
      <button onclick="updateValue()">Update</button>
    </div>

    <script>
      function updateValue() {
        // Get the input value
        const inputValue = document.getElementById('input-value').value;

        // Get the number element
        const numberElement = document.querySelector('.number');

        // Update the data-value attribute and the displayed value
        numberElement.setAttribute('data-value', inputValue);
        numberElement.textContent = inputValue;
      }
    </script>
  </body>
</html>
