# Learning. Basic examples for the learning ╯

# Vacation cost calculator!
def hotel_cost(nights):
    #if each night costs $140
    return 140 * nights
def plane_ride_cost(city):
    if city == "Charlotte":
        return 183
    elif city == "Tampa":
        return 220
    elif city == "Pittsburgh":
        return 222
    elif city == "Los Angeles":
        return 475
def rental_car_cost(days):
    rental_car_cost = 40 * days
    if days >= 7:
        rental_car_cost -= 50
    elif days >= 3:
        rental_car_cost -= 20
    return rental_car_cost
def trip_cost(city, days, spending_money):
    return hotel_cost(days) + plane_ride_cost(city) + rental_car_cost(days) + spending_money

print trip_cost("Los Angeles", 5, 600)

# WHAT IS WRONG WITH THIS CODE?:
def total(points, half_points):
    print "Adding %s points and %s half points" % (points, half_points)
    return points + (half_points * .5)
    print "Your team scored a total of %s points!" % (total) 

points = int(raw_input("How many points did your team score?"))
half_points = int(raw_input("How many half points did your team score?"))

# FOR FUN:
name = raw_input("What is your name?")
if name.isalpha():
    length = len(name)
    number = str(length)
    print "Your name has " + number + " letters"
else:
    print "I didn't get that."
name2 = raw_input("Please tell me your real name: ")

if name2 != "Jason":
    print "Go fuck yourself!"
else:
    print "Here is your breakfast sir."

# FUNCTION
def distance_from_zero(cheese):
    if type(cheese) == int or type(cheese) == float:
        return abs(cheese)
    else: 
        return "Nope"
cheese = max(4,5,6,7)
print distance_from_zero(cheese)

# USING/ABUSING DICTIONARIES/LISTS/INDEXES (prints c)
my_dict = {
    "fish": ["c", "a", "r", "p"],
    "cash": -4483,
    "luck": "good"
}
print my_dict["fish"][0]

# Keys, lists, etc
inventory = {
    'gold' : 500,
    'pouch' : ['flint', 'twine', 'gemstone'], 
    'pocket' : ['seashell', 'strange berry', 'lint'],
    'backpack' : ['xylophone', 'dagger', 'bedroll', 'bread loaf']
}

# Adding a key 'burlap bag' and assigning a list to it
inventory['burlap bag'] = ['apple', 'small ruby', 'three-toed sloth']

# Sorting the list found under the key 'pouch'
inventory['pouch'].sort() 
inventory['backpack'].sort()
inventory['backpack'].remove('dagger')
inventory['gold'] += 50
# Your code here
print inventory

# CALCULATING HEIGHT IN METERS, CENTIMETERS
print "Tell me your height. Feet first, then inches."
height_feet = float(raw_input("Feet:"))
inches = float(raw_input("Inches:"))

feet_to_inches = height_feet * 12
total_inches = feet_to_inches + inches
cm = total_inches * 2.54

print cm
cm = str(cm)
print len(cm)
meters = cm[0]
cm_ = cm[1:]
if meters == "1":
    print "Your height is %s meter, %s centimeters." % (meters, cm_) 
elif len(cm) == 5:
    print "Your height is %s centimeters." % (cm)
else:
    print "Your height is %s meters, %s centimeters." % (meters, cm_) 
