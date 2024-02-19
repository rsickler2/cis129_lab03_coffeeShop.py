# cis129_lab03_coffeeShop.py
# Module 3 lab work
def calculate_total():
    menu = {
        "Coffee": 5,
        "Muffin": 4,
        "Tea": 3,
        "Croissant": 6
    }

    # Asking user for the number of items ordered
    num_items = {}
    for item in menu:
        num_items[item] = int(input(f"Enter the number of {item}s: "))

    # Calculating subtotal
    subtotal = sum(menu[item] * num_items[item] for item in menu)

    # Calculating tax
    tax_rate = 0.06
    tax = subtotal * tax_rate

    # Calculating total
    total = subtotal + tax

    # Printing the receipt
    print("\n----- Receipt -----")
    for item in menu:
        if num_items[item] > 0:
            print(f"{item} x {num_items[item]}: ${menu[item] * num_items[item]:.2f}")
    print(f"Subtotal: ${subtotal:.2f}")
    print(f"Tax (6%): ${tax:.2f}")
    print(f"Total: ${total:.2f}")

    # Thanking the user
    print("\nThank you for your purchase! We hope to see you again soon.")

# Calling the function to calculate total
calculate_total()

