# Module 3 Lab

    def calculate_total(coffee_qty, muffin_qty, croissant_qty, tea_qty):
    coffee_price = 5
    muffin_price = 4
    croissant_price = 6
    tea_price = 3

    subtotal = (coffee_qty * coffee_price) + (muffin_qty * muffin_price) + (croissant_qty * croissant_price) + (tea_qty * tea_price)
    tax_rate = 0.06
    tax_amount = subtotal * tax_rate
    total = subtotal + tax_amount
    return total

    def main():
    print("Welcome to the Coffee Shop!")
    print("Menu:")
    print("1. Coffee - $5")
    print("2. Muffin - $4")
    print("3. Croissant - $6")
    print("4. Tea - $3")

    coffee_qty = int(input("Enter the number of coffees: "))
    muffin_qty = int(input("Enter the number of muffins: "))
    croissant_qty = int(input("Enter the number of croissants: "))
    tea_qty = int(input("Enter the number of teas: "))

    total = calculate_total(coffee_qty, muffin_qty, croissant_qty, tea_qty)

    print("\nReceipt:")
    if coffee_qty > 0:
        print(f"{coffee_qty} Coffee(s) - ${coffee_qty * 5:.2f}")
    if muffin_qty > 0:
        print(f"{muffin_qty} Muffin(s) - ${muffin_qty * 4:.2f}")
    if croissant_qty > 0:
        print(f"{croissant_qty} Croissant(s) - ${croissant_qty * 6:.2f}")
    if tea_qty > 0:
        print(f"{tea_qty} Tea(s) - ${tea_qty * 3:.2f}")
    
    print(f"Subtotal: ${total - (total * 0.06):.2f}")
    print(f"Tax (6%): ${total * 0.06:.2f}")
    print(f"Total: ${total:.2f}")

    print("\nThank you for visiting the Coffee Shop! We hope to see you again soon!")

    if __name__ == "__main__":
    main()
