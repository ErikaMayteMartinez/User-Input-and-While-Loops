# User-Input-and-While-Loops
#rental car
car = input("What kind of car would you like to rent?")
#input the car you want into the terminal
print(f"\nLets see if we cna find you a {car}.")

#restaurant seating
seating = input("How many people will be in your dinner party tonight?")
seating = int(seating)
#input the number of people in your party into the terminal
if seating <= 8:
    print(f"\nGreat, well get a table started for you.")
else:
    print(f"\nSorry, we will need you to wait for a table before you can be seated.") 

#multiples of ten
number = input("Enter a number and I'll tell you if its a multiple of 10:")
number = int(number)
#input the number into the terminal
if number % 10 == 0:
    print(f"\nThe number {number} is a multiple of 10.")
else:
    print(f"\nThe number {number} is not a multiple of 10.")

#Pizza toppings
pizza = "\nI'll add that to your pizza."
pizza += "\nEnter 'quit' to end the program."
message = ""
while message != 'quit':
    message = input(pizza)
    print(message)

#movie tickets by age
age = input("What is your age?")
age = int(age)
ticket1 = "\nYour ticket is free!"
ticket2 = "\nYour ticket is $10 please."
ticket3 = "\nYour ticket is $15 please."
#is there a cleaner way to input this? like a short cut???
if age == 0:
    print(ticket1)
if age == 1:
    print(ticket1)
if age == 2:
    print(ticket1)
if age == 3:
    print(ticket1)
if age == 4:
    print(ticket2)
if age == 5:
    print(ticket2)
if age == 6:
    print(ticket2)
if age == 7:
    print(ticket2)
if age == 8:
    print(ticket2)
if age == 9:
    print(ticket2)
if age == 10:
    print(ticket2)
if age == 11:
    print(ticket2)
if age == 12:
    print(ticket2)
if age >=13:
    print(ticket3)

#Deli Orders
sandwich_orders = ['turkey sandwich', 'meatball panini', 'ham and cheese sandwich', 'pastrami sandwich']
finished_orders = []
#No pastrami
while 'pastrami sandwich' in sandwich_orders:
    sandwich_orders.remove('pastrami sandwich')
    print("\nSorry, the deli has ran out of pastrami today.")
while sandwich_orders:
    current_sandwich = sandwich_orders.pop()
    print(f"The {current_sandwich.title()} is being made.")
    finished_orders.append(current_sandwich)
print("\nThe following sandwiches are ready for pickup:")
for finished_order in finished_orders:
    print(finished_order.title())


#Dream vacation
responses = {}
polling_active = True
while polling_active:
    question = input("\nIf you could go anywhere in the world for your dream vacation, where would you go?")
    response = input("\nWhat made you pick that place in particular?")
    responses[question] = response
    repeat = input("\nWould you like to let another person respond to thier dream vacation? (yes/no)")
    if repeat == "no":
        polling_active = False
print("n\ --- Poll Results ---")
for question, response in responses.items():
    print(f"\nI would like to go to {question} because {response}.")
