# COSC-9
COSC 9 again sorry for how late this is.
# Constant values based on company determinations
SQ_FT_PER_UNIT = 112
HOURS_PER_UNIT = 8
LABOR_RATE_PER_HOUR = 35.00

def main():
    # Prompt user for inputs
    wall_space = float(input("Enter the square feet of wall space to be painted: "))
    paint_price = float(input("Enter the price of the paint per gallon: "))
    
    # Calculate required resources
    # Note: Depending on your class requirements, you can keep gallons as a float 
    # or round up using math.ceil(). This code uses exact decimal ratios.
    gallons_required = wall_space / SQ_FT_PER_UNIT
    hours_required = (wall_space / SQ_FT_PER_UNIT) * HOURS_PER_UNIT
    
    # Calculate costs
    paint_cost = gallons_required * paint_price
    labor_charges = hours_required * LABOR_RATE_PER_HOUR
    total_cost = paint_cost + labor_charges
    
    # Display the results formatted to 2 decimal places
    print("\n--- Paint Job Estimate ---")
    print(f"Gallons of paint required: {gallons_required:.2f}")
    print(f"Hours of labor required:   {hours_required:.2f}")
    print(f"Cost of the paint:        ${paint_cost:.2f}")
    print(f"Labor charges:            ${labor_charges:.2f}")
    print(f"Total cost of paint job:  ${total_cost:.2f}")

if __name__ == "__main__":
    main()
