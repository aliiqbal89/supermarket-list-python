# supermarket-list-python

from collections import OrderedDict

# Read number of items
n = int(input())

# Initialize OrderedDict
ordered_dict = OrderedDict()

# Process each item entry
for _ in range(n):
    *item_name, price = input().split()
    item_name = " ".join(item_name)  # Join words to form the item name
    price = int(price)  # Convert price to integer
    
    # Update OrderedDict
    if item_name in ordered_dict:
        ordered_dict[item_name] += price
    else:
        ordered_dict[item_name] = price

# Print the result
for item, net_price in ordered_dict.items():
    print(item, net_price)
