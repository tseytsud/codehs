# codehs

# UNIT 3


----------------------
# UNIT 4

**4.6.2 For Loops Quiz**

Question: 1
> How many times will the following program print "hello"
> > ANSWER: 5

Question: 2
> In the following code, what will be the last number to print to the screen before the program finishes?
> > ANSWER: 18

**4.6.4 Meme Text Generator**
```
# Enter your code here
for i in range(50):
    print("Takes one political science class. Knows how to solve the world's problems.")
```

**4.6.5 The Worm**
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

**4.6.6 Caterpillar**
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

**4.7.2 General For Loop Quiz**

Question: 1
> How many times will the following code print "hello"?
```
for i in range(3, 8):
    print("hello")
```
> > ANSWER: 5




