product = {
    1: ("T-shirt", 250),
    2: ("Shirt", 400),
    3: ("Hat", 100),
    4: ("Shoes", 800),
    5: ("Sandals", 600),
}

print("=== Welcome to Prince Store ===")

print("Available Products:")
for num, (name, price) in product.items():
    print(f"{num}: {name} - {price}")

total = 0

#Ordering
while True:
    choice = int(input("\nEnter your product number (0 to finish): "))
    if choice == 0:
        print("\nThank you for shopping!")
        break
    if choice in product:
        qty = int(input("Enter your quantity: "))
        items, price = product[choice]
        cost = price * qty
        total = cost
        print(f"Added {qty} x {items} = : {cost}")
    else:
        print("Invalid choice")

#Discount if total >= 1300
print("\n=== Bill ===")
print(f"Total before discount: {total}")
if total >= 1300:
    discount = total *0.5
    total -= discount
    print(f"Discount: :{discount:.2f}")

print(f"Final Total: {total}")
print("=== Thank you for using Prince ===")
