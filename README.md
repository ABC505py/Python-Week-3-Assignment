# Python-Week-3-Assignment

# Define a function to calculate the discounted price
def calculate_discount(price, discount_percent):
    """
    This function calculates the final price after applying the discount.
    If the discount percent is 20 or more, the discount is applied.
    Otherwise, the original price is returned.
    """
    if discount_percent >= 20:
        # Calculate the discount amount
        discount_amount = (discount_percent / 100) * price
        # Subtract discount from original price
        final_price = price - discount_amount
        return final_price
    else:
        # Return original price if discount is less than 20%
        return price

# Prompt user to enter the original price
try:
    original_price = float(input("Enter the original price of the item: "))
    discount_percent = float(input("Enter the discount percentage: "))

    # Call the function with user inputs
    final_price = calculate_discount(original_price, discount_percent)

    # Display the result
    if discount_percent >= 20:
        print(f"Discount applied. Final price: ${final_price:.2f}")
    else:
        print(f"No discount applied. Final price: ${final_price:.2f}")

except ValueError:
    # Handle the case when input is not a number
    print("Please enter valid numbers for price and discount.")
