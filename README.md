# Coding-Set-7-
Alg Workbench #1
Scientists = ['Einstein', 'Newton', 'Copernicus', 'Kepler']

Alg Workbench #7
list1 = [40, 50, 60] 
list2 = [10 , 20, 30] 
list3 = list1 + list2 
print(list3)

Programming Exercise #1
def main():
    daily_sales = []

    days = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday']

    for day in days:
        sales = float(input(f"Enter the sales for {day}: $"))
        daily_sales.append(sales)

    total_sales = sum(daily_sales)

    print(f"\nTotal sales for the week: ${total_sales: .2f}")

if __name__ == "__main__":
    main() 

Programming Exercise #14
import matplotlib.pyplot as plt

def main():

    categories = []
    expenses = []

    with open('/expenses.txt', 'r') as file: 
        for line in file:

            category, amount = line.strip().split(', ')
            categories.append(category)
            expenses.append(float(amount))

    plt.figure(figsize=(8,6))
    plt.pie(expenses, labels=catergories, autopct='%1.1f%%', startangle=140)
    plt.title('Expense distribution for Last Month')
    plt.axis('equal')
    plt.show()

if __name__ == "__main__":
    main()

Programming Exercise #6
def display_numbers_greater_than(numbers, n):
    """
    Display numbers in the list that are greater than n.
    
    Parameters:
    - numbers (list): A list of numbers.
    - n (int or float): The threshold number to compare against.
    """
    try:
        n = float(n)
    except ValueError:
        raise TypeError("n must be convertible to float")
    
    results = [num for num in numbers if num > n]

    if results:
        print(f"Numbers greater than {n}: {results}")
    else:
        print(f"There are no numbers greater than {n} in the list.")

if __name__ == "__main__":
    numbers = [12, 5, 8, 15, 3, 10, 20, 7]
    threshold = 10
    display_numbers_greater_than(numbers, threshold)
