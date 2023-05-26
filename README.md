# codehs

# UNIT 3
3.1.3: Respond: What is Software
> > ANSWER: I already knew that computers process information and perform tasks. I was surprised to learn that programming languages are like specialized tools for specific problems. I want to learn more about the compilation process. One question I have is: What are other programming languages and their unique characteristics?



----------------------
# UNIT 4

## **4.6.2 For Loops Quiz**

Question: 1
> How many times will the following program print "hello"
> > ANSWER: 5

Question: 2
> In the following code, what will be the last number to print to the screen before the program finishes?
> > ANSWER: 18

## **4.6.4 Meme Text Generator**
```
# Enter your code here
for i in range(50):
    print("Takes one political science class. Knows how to solve the world's problems.")
```

## **4.6.5 The Worm**
```
NUM_CIRCLES = 15

# This graphics program should draw a worm. 
# A worm is made up of NUM_CIRCLES circles. 
# Use a for loop to draw the worm, 
# centered vertically in the screen. 
# Also, be sure that the worm is still drawn across 
# the whole canvas, even if the value of NUM_CIRCLES is changed.




# Constants
NUM_CIRCLES = 10
circle_radius = 30
circle_gap = 10

# Set up the canvas
set_canvas_size(400, 400)

# Calculate the vertical center of the screen
screen_center = get_height() / 2

# Calculate the total height occupied by the worm
worm_height = NUM_CIRCLES * (circle_radius * 2 + circle_gap) - circle_gap

# Calculate the starting y-coordinate for the first circle
start_y = screen_center - worm_height / 2 + circle_radius

# Loop to draw the worm
for i in range(NUM_CIRCLES):
    # Create the circle
    circle = Circle(circle_radius, (get_width() / 2, start_y))
    circle.set_color(Color.blue)

    # Add the circle to the screen
    add(circle)

    # Update the y-coordinate for the next circle
    start_y += circle_radius * 2 + circle_gap

# Display the canvas
show()
```

## **4.6.6 Caterpillar**
```
NUM_CIRCLES = 15

# This graphics program should draw a caterpillar. 
# A caterpillar is made up of NUM_CIRCLES circles.
# The circles should alternate red - green - red - green, etc
# Use a for loop to draw the worm, 
# centered vertically in the screen. 
# Also, be sure that the worm is still drawn across 
# the whole canvas, even if the value of NUM_CIRCLES is changed.

from codehs import *

# Constants
NUM_CIRCLES = 10
CIRCLE_RADIUS = 30
CIRCLE_GAP = 10

# Set up the canvas
set_canvas_size(400, 400)

# Calculate the vertical center of the canvas
canvas_center = get_height() / 2

# Loop to draw the caterpillar
for i in range(NUM_CIRCLES):
    # Create the circle
    circle = Circle(CIRCLE_RADIUS)
    if i % 2 == 0:
        circle.set_color(Color.red)
    else:
        circle.set_color(Color.green)

    # Calculate the y-coordinate of the circle
    circle_y = canvas_center - ((NUM_CIRCLES * (CIRCLE_RADIUS * 2 + CIRCLE_GAP)) / 2) + (i * (CIRCLE_RADIUS * 2 + CIRCLE_GAP))

    # Set the position of the circle
    circle.set_position(get_width() / 2, circle_y)

    # Add the circle to the screen
    add(circle)

# Display the canvas
show()
```

## **4.7.2 General For Loop Quiz**

Question: 1
> How many times will the following code print "hello"?
```
for i in range(3, 8):
    print("hello")
```
> > ANSWER: 5

## **4.7.5 Count By Sevens**

```
# Enter your code here
for i in range(0, 501, 7):
    print(i)

```

## **4.7.6 Powers of Two**
```
# Enter your code here
for exponent in range(20):
    power_of_2 = 2 ** exponent
    if power_of_2 >= 1000000:
        break
    print(power_of_2)

```

## **4.8.2 For Loop Examples Quiz**

Question: 1
> Why do we use constant variables?
> > ANSWER: All of the above

Question: 2
> What will be the value of sum after this code runs?
> > ANSWER: 10

## **4.8.3 Better Sum**
```
# Enter your code here
first_num = int(input("Enter the first number: "))
second_num = int(input("Enter the second number: "))

sum_of_numbers = 0

for num in range(first_num, second_num + 1):
    sum_of_numbers += num

print("The sum of numbers from", first_num, "to", second_num, "is", sum_of_numbers)

```

## **4.8.5 Factorial**
```
# Enter your code here
num = int(input("Enter a number: "))

factorial = 1

for i in range(1, num + 1):
    factorial *= i

print(num, "! is", factorial)

```

## **4.8.6 All Dice Values**
```
# Put your code here
for i in range(1, 7):
    for j in range(1, 7):
        print(i, ",", j)

```

## **4.9.2 Random Numbers Quiz**

Question: 1
> Which of the following returns a random number between 1 and 10?
> > ANSWER:``` random.randint(1,10) ```


Question: 2
> How many possible values can the following code return random.choice([1,5]) return?
> > 2

## ** 4.9.5 Lots of Dice **
```
import random

# Enter your code here

for i in range(100):
    roll = random.randint(1, 6)
    print(roll)

```

## ** 4.9.6 Random Color Square **
```
import random

set_size(480, 400)

# This graphics program should draw a square. 
# The fill color should be randomly choosen from
# the COLORS list

SIDE_LENGTH = 100
COLORS = [Color.red, Color.orange, Color.yellow, Color.green, Color.blue, 
        Color.purple, Color.black, Color.gray]
        

rect = Rectangle(50, 50)
rect.set_color(random.choice(COLORS))
rect.set_position(0, 0)
add(rect)

```

## **4.10.2 While Loops Quiz**

Question: 1
> How many times will this program print "hello"?
```
i = 50
while i < 100:
    print("hello")
```
<sub> (PYTHON) </sub>
> > ANSWER: This code will loop infinitely

Question: 2
> How many times will this program print "hello"?
```
i = 10
while i > 0:
    print("hello")
    i -= 1
```
> > ANSWER: 10

## **4.10.4 Inventory**
```
STARTING_ITEMS_IN_INVENTORY = 20

inventory = STARTING_ITEMS_IN_INVENTORY

while inventory > 0:
    print("We have", inventory, "items in inventory.")
    purchase = int(input("How many would you like to buy? "))

    if purchase > inventory:
        print("There is not enough in inventory for that purchase.")
    else:
        inventory -= purchase
        if inventory == 0:
            print("All out!")
        else:
            print("Now we have", inventory, "left.")

#print("All out!")

```

## **4.10.5 Fibonacci**
```
MAX = 1000  # Define the maximum number

# Initialize the first two numbers in the sequence
num1, num2 = 1, 1

# Print the first two numbers
print(num1)
print(num2)

# Calculate and print the remaining numbers in the Fibonacci sequence
while True:
    next_num = num1 + num2
    if next_num > MAX:
        break
    print(next_num)
    num1, num2 = num2, next_num

```

## **4.10.6 AP Practice: Iteration**

Question: 1
> The AP Exam does not use for loops and while loops, but rather REPEAT or REPEAT UNTIL commands as shown below.
```
REPEAT n TIMES
{
   <block of statements>
}

REPEAT UNTIL(condition)
{
   <block of statements>
}
```
> The program below uses a robot in a 5x5 grid of squares. The robot is represented as a triangle, which is initially in the bottom-left square of the grid and facing toward the right of the grid.
After running which of the following code segments would the robot end up in the same place facing the same direction as after running the code segment below?
```
REPEAT 2 TIMES
{
    MOVE_FORWARD ()
    MOVE_FORWARD ()
    ROTATE_LEFT ()
}
```
> > ANSWER (below)
```
REPEAT 2 TIMES
{
    MOVE_FORWARD ()
}

ROTATE_LEFT ()

REPEAT 2 TIMES
{
    MOVE_FORWARD ()
}
ROTATE_LEFT ()
```
Question: 2
> Consider the following program, which is intended to print the sum of all the positive integers up to number.
```
sum ← 0

REPEAT number TIMES
{
    sum ← sum + number
}

DISPLAY sum
```
> Which of the following best describes the behavior of this program?
> > ANSWER: The program does not work as intended but rather it displays the number squared.

Question: 3
> Consider the following program, which is intended to print the count of even numbers between 1 and number
```
count ← 0

i ← 1

REPEAT number TIMES
{
    IF (i MOD 2 = 0)
    {
        count ← count + 1
    }

    i ← i + 1
}

DISPLAY count
```
> Which of the following best describes the behavior of this program?
> > ANSWER: The program correctly displays the count of even numbers between 1 and number

Question: 4
> In the procedure Mystery written below, the parameter number is a positive integer.
```
PROCEDURE Mystery (number)
{
    value ← number

    REPEAT UNTIL (number = 0)
    {
        value ← value * -1
        number ← number - 1
    }

    IF (value > 0)
    {
        RETURN (true)
    }
    ELSE
    {
        RETURN (false)
    }
}
```
> Which of the following best describes the result of running the Mystery procedure?
> > ANSWER: The result will be true whenever the initial value of number is even


Question: 5
> In the procedure Mystery written below, the parameter number is a positive integer.
```
PROCEDURE Mystery (number)
{
    value ← 0

    REPEAT UNTIL (number = 0)
    {
        IF (number MOD 2 = 0)
        {
            value ← value + 1
        }
        ELSE
        {
            value ← value - 1
        }

        number ← number - 1
    }

    IF (value = 0)
    {
        RETURN (true)
    }
    ELSE
    {
        return (false)
    }
}
```
> Which of the following best describes the result of running the Mystery procedure?
> > The result will be true whenever the initial value of number is even

Question: 6
> Which initial value of number would cause an infinite loop?
```
REPEAT UNTIL(number = 0)
{
  number ← number - 1
}
```
> > ANSWER: Any negative integer.

Question: 7
> Which initial value of number would cause the loop to be skipped?
```
REPEAT UNTIL(number MOD 2 = 0)
{
  number ← number - 1
}
```
> > ANSWER: Any even integer.

**4.11.2 Loop and a Half Quiz**

Question: 1
> If I am using the following condition in my program:
```
while True:
```
> which keyword should I use to make sure I don’t create an infinite loop?
>  > ANSWER: break


Question: 2
> Which Python keyword skips back to the beginning of a loop?
> > ANSWER: Continue

## **4.11.4 Snake Eyes**
```
import random

rolls = 0

while True:
    dice1 = random.randint(1, 6)
    dice2 = random.randint(1, 6)
    rolls += 1

    print("Rolled:", dice1, dice2)

    if dice1 == 1 and dice2 == 1:
        #print("Snake eyes!")
        print("It took you", rolls, "rolls to get snake eyes.")
        break

```

## **4.11.5 Better Password Prompt**
```
SECRET = "abc123"

while True:
    password = input("Enter password: ")

    if password == SECRET:
        print("You got it!")
        break

    print("Sorry, that did not match. Please try again.")

```

## **4.12.1 Python Control Structures Quiz**

Question: 1
> What is the last thing printed by the following program?
```
start = 30
stop = 10
for  i in range(start,  stop - 1, -5):
    if i % 2 == 0:
        print(i * 2)
    else:
        print(i)
```
> > 20

Question: 2
> We want to simulate constantly flipping a coin until we get 3 heads in a row. What kind of loop should we use?
> > While loop

Question: 3
> How many times will the following program print "hello"?
> > Infinite Loop

Question: 4
> The following code continually asks the user for a password until they guess the correct password, then ends. But there is one problem.
> Which of the following will fix this program?
> > Add a 'break;' statement after line 6 so that the program doesn’t loop infinitely

Question: 5
> What will the following program print when run?
> > ANSWER: (below)
```
6
5
6
5
```

Question: 6
> What is the value of the boolean variable can_vote at the end of this program?
```
age = 17
is_citizen = True
can_vote = age >= 18 and is_citizen
```
> > False

Question 7:
<img width="748" alt="7" src="https://github.com/tseytsud/codehs/assets/134737493/e679bf6c-bf30-470e-bacb-0cba51ecdabf">

Question 8:
<img width="748" alt="8" src="https://github.com/tseytsud/codehs/assets/134737493/1552fcac-d3ef-472b-aef3-1d73a94ade60">


Question 9:
<img width="748" alt="9" src="https://github.com/tseytsud/codehs/assets/134737493/cf937c89-c29d-4777-9703-509c11a3cb69">


Question 10:
<img width="748" alt="10" src="https://github.com/tseytsud/codehs/assets/134737493/21ec73c9-5770-4cdf-a5d9-62a71a3cdb21">


Question 11:
<img width="748" alt="11" src="https://github.com/tseytsud/codehs/assets/134737493/1f539bfa-ed1a-4578-b71a-3f8e79b74c7a">


Question 12:
<img width="748" alt="12" src="https://github.com/tseytsud/codehs/assets/134737493/906fd501-fe5f-4cca-a53c-243687505020">


Question 13 and 14:
<img width="748" alt="13 + 14" src="https://github.com/tseytsud/codehs/assets/134737493/ebc38454-25d7-44d6-8747-0aa69b78f5f1">


Question 15:
<img width="748" alt="15" src="https://github.com/tseytsud/codehs/assets/134737493/2ed173b4-f136-4344-ab70-60912262669e">


Question 16:
<img width="748" alt="16" src="https://github.com/tseytsud/codehs/assets/134737493/019abbd9-2856-45a5-b61a-75badf969a46">


Question 17:
<img width="748" alt="17" src="https://github.com/tseytsud/codehs/assets/134737493/614bef45-5ac9-4f08-9d61-de9a46f6ab78">


Question 18:
<img width="748" alt="18" src="https://github.com/tseytsud/codehs/assets/134737493/4b8dbcc4-ae41-4923-9a9c-84e0fee818f2">


Question 19 and 20:
<img width="748" alt="19 + 20" src="https://github.com/tseytsud/codehs/assets/134737493/ea2f9818-9d80-4d3a-9a2a-88bd08885c80">


Question 21:
<img width="748" alt="21" src="https://github.com/tseytsud/codehs/assets/134737493/ec25bea2-b815-4d3f-baba-6081ad8aef6b">


Question 22:
<img width="748" alt="22" src="https://github.com/tseytsud/codehs/assets/134737493/10164242-69e4-4593-8c12-2ec464ad6f5b">


Question 23:
<img width="748" alt="23" src="https://github.com/tseytsud/codehs/assets/134737493/5d603991-c688-4aa4-b5a1-4759f2a4e44a">

Question 24:
<img width="748" alt="24" src="https://github.com/tseytsud/codehs/assets/134737493/1874a4a7-d7a7-497f-a4f8-69682da418fd">

Question 25:
<img width="748" alt="25" src="https://github.com/tseytsud/codehs/assets/134737493/81d77585-8735-4890-8b65-027531e7dfd7">



