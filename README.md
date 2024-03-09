#calculator
def calculate():
    history = []

    while True:
        operation = input('''
Please type in the math operation you would like to complete:
+ for addition
- for subtraction
* for multiplication
/ for division
''')

        number_1 = float(input('Enter your first number: '))
        number_2 = float(input('Enter your second number: '))

        if operation == '+':
            result = number_1 + number_2
        elif operation == '-':
            result = number_1 - number_2
        elif operation == '*':
            result = number_1 * number_2
        elif operation == '/':
            result = number_1 / number_2
        else:
            print('You have not typed a valid operator, please run the program again.')
            continue

        history.append(f"{number_1} {operation} {number_2} = {result}")
        print("\n".join(history))
        calc_again = input('''
Do you want to calculate again?
Please type Y for YES or N for NO.
''')

        if calc_again.lower() == 'n':
            print("Thanks for using the calculator! Goodbye!")
            break

calculate()
