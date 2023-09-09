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

            // Define the conversion rates
            const conversionRates = {
                2000: 1,
                10000: 5,
                20000: 10,
                50000: 25,
                100000: 50,
                200000: 100,
                400000: 200,
                500000: 250,
                1000000: 500
            };

            // Calculate the gift amount based on the input Bloxburg Cash
            for (const cash in conversionRates) {
                if (bloxburgCash >= cash) {
                    const rate = conversionRates[cash];
                    const cashCount = Math.floor(bloxburgCash / cash);
                    robuxAmount += cashCount * rate;
                    bloxburgCash -= cashCount * cash;
                }
            }

            // Divide the Robux amount by 2 (50%)
            robuxAmount /= 2;

            // Display the result
            document.getElementById('result').innerHTML = `The gifter will receive ${robuxAmount} Robux.`;
        }
    </script>
</body>
</html>

