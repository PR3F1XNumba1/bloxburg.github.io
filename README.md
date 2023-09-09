bloxburg.github.io
def calculate_gift_amount(bloxburg_cash):
    # Define the conversion rates
    conversion_rates = {
        2000: 1,
        10000: 5,
        20000: 10,
        50000: 25,
        100000: 50,
        200000: 100,
        400000: 200,
        500000: 250,
        1000000: 500
    }

    # Calculate the gift amount based on the input Bloxburg Cash
    gift_amount = 0
    for cash, rate in conversion_rates.items():
        if bloxburg_cash >= cash:
            gift_amount += (bloxburg_cash // cash) * rate
            bloxburg_cash %= cash

    return gift_amount

# Input the amount of Bloxburg Cash
bloxburg_cash_input = int(input("Enter the amount of Bloxburg Cash: "))
gift_amount = calculate_gift_amount(bloxburg_cash_input)

print(f"The gifter will receive {gift_amount} Robux.")

