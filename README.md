bloxburg.github.io

<!DOCTYPE html>
<html>
<head>
    <title>Bloxburg Cash to Robux Calculator</title>
</head>
<body>
    <h1>Bloxburg Cash to Robux Calculator</h1>
    
    <form id="calculator-form">
        <label for="bloxburg-cash">Enter Bloxburg Cash amount:</label>
        <input type="number" id="bloxburg-cash" name="bloxburg-cash" required>
        <button type="button" onclick="calculateGift()">Calculate</button>
    </form>
    
    <p id="result"></p>

    <script>
        function calculateGift() {
            const bloxburgCash = parseFloat(document.getElementById('bloxburg-cash').value);
            let robuxAmount = 0;

            // Calculate the gift amount based on the input Bloxburg Cash
            robuxAmount = (bloxburgCash / 2000) / 2;

            // Display the result
            document.getElementById('result').innerHTML = `The gifter will receive ${robuxAmount} Robux.`;
        }
    </script>
</body>
</html>
