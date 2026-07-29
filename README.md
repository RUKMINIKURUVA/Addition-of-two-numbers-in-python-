def add_two_numbers():
    print("--- Safe Addition Calculator ---")
    
    # Get the first valid number
    while True:
        try:
            num1 = float(input("Enter the first number: "))
            break
        except ValueError:
            print("Invalid input! Please enter a valid number (e.g., 5 or 3.14).")

    # Get the second valid number
    while True:
        try:
            num2 = float(input("Enter the second number: "))
            break
        except ValueError:
            print("Invalid input! Please enter a valid number.")

    # Calculate the sum
    total = num1 + num2

    # Display the result beautifully, formatting to drop trailing zeros if whole
    formatted_num1 = int(num1) if num1.is_integer() else num1
    formatted_num2 = int(num2) if num2.is_integer() else num2
    formatted_total = int(total) if total.is_integer() else total

    print(f"\nResult: {formatted_num1} + {formatted_num2} = {formatted_total}")

# Run the program
if __name__ == "__main__":
    add_two_numbers()
    
