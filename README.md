# cis129_lab03_coffeeShop.py
# Module 3 lab work
def calculate_total_coffee_muffin():
    # Asking user for the number of coffee and muffins
    num_coffee = int(input("Enter the number of coffees: "))
    num_muffins = int(input("Enter the number of muffins: "))

    # Calculating subtotal
    coffee_price = 5
    muffin_price = 4
    subtotal = (num_coffee * coffee_price) + (num_muffins * muffin_price)

    # Calculating tax
    tax_rate = 0.06
    tax = subtotal * tax_rate

    # Calculating total
    total = subtotal + tax

    # Printing the total amount including tax
    print(f"Subtotal: ${subtotal:.2f}")
    print(f"Tax (6%): ${tax:.2f}")
    print(f"Total: ${total:.2f}")

# Calling the function to calculate total
calculate_total_coffee_muffin()
