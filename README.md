# Function to display the header of the bill
def print_header():
    print("**************************************")
    print("           SUPER MARKET BILL")
    print("**************************************")
    print("Item Name\tPrice\tQuantity\tTotal")
    print("--------------------------------------")

# Function to calculate the total cost for each item
def calculate_total(price, quantity):
    return price * quantity

# Function to calculate the final amount including tax
def calculate_final_amount(sub_total, tax_rate=0.05):
    tax = sub_total * tax_rate
    final_amount = sub_total + tax
    return final_amount, tax

# Main program to generate the bill
def generate_bill():
    items = []
    prices = []
    quantities = []
    while True:
        # Input item details
        item_name = input("Enter item name (or 'done' to finish): ")
        if item_name.lower() == 'done':
            break
        
        try:
            price = float(input(f"Enter price of {item_name}: $"))
            quantity = int(input(f"Enter quantity of {item_name}: "))
        except ValueError:
            print("Invalid input. Please enter numerical values for price and quantity.")
            continue
        
        items.append(item_name)
        prices.append(price)
        quantities.append(quantity)

    # Calculate and print the bi

