# Project Name: smart-shopping

# Import necessary libraries
import random

# Dictionary of products with their corresponding categories
products = {
    "Shoes": ["Sports", "Casual", "Formal"],
    "Clothing": ["Tops", "Bottoms", "Dresses"],
    "Electronics": ["Laptops", "Smartphones", "Earphones"]
}

# Dictionary of discounts with their corresponding categories
discounts = {
    "Sports": "10% off on sports products",
    "Casual": "Buy one get one free on casual wear",
    "Smartphones": "20% off on all smartphones"
}

# Function to suggest products based on user preferences
def suggest_products(category):
    if category in products:
        return random.choice(products[category])
    else:
        return "No products available for this category"

# Function to suggest discounts based on user preferences
def suggest_discounts(category):
    if category in discounts:
        return discounts[category]
    else:
        return "No discounts available for this category"

# Main function
def main():
    try:
        # Getting user input for preferred category
        user_category = input("Enter your preferred category (Shoes, Clothing, Electronics): ").capitalize()

        # Suggesting a product and discount based on user preferences
        suggested_product = suggest_products(user_category)
        suggested_discount = suggest_discounts(user_category)

        # Displaying the suggested product and discount
        print("Product suggestion: {}".format(suggested_product))
        print("Discount suggestion: {}".format(suggested_discount))
    
    except Exception as e:
        print("An error occurred: {}".format(e))

if __name__ == "__main__":
    main()