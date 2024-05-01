# index.html
calculating B.M.I
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BMI Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            text-align: center;
        }
        .container {
            margin-top: 50px;
        }
        input[type="text"], input[type="number"] {
            padding: 10px;
            width: 200px;
            margin-bottom: 10px;
        }
        button {
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>BMI Calculator</h1>
        <label for="weight">Weight (kg):</label>
        <input type="number" id="weight"><br>
        <label for="height">Height (cm):</label>
        <input type="number" id="height"><br>
        <button onclick="calculateBMI()">Calculate BMI</button><br>
        <p id="result"></p>
    </div>

    <script>
        function calculateBMI() {
            var weight = parseFloat(document.getElementById('weight').value);
            var height = parseFloat(document.getElementById('height').value) / 100; // Convert height from cm to meters
            var bmi = weight / (height ** 2);
            document.getElementById('result').innerText = "Your BMI: " + bmi.toFixed(2);
        }
    </script>
</body>
</html>
