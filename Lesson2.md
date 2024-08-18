## Turtle Graphics
- Turtle Graphics provides a representation of a physical “turtle” (a little robot with a pen) that draws on a sheet of paper on the floor.
- It’s an effective and well-proven way for learners to encounter programming concepts and interaction with software, as it provides instant, visible feedback.

## Starting a turtle environment
- In a Python shell, import all the objects of the turtle module:
```
import turtle
```
- If you run into a No module named '_tkinter' error, you’ll have to install the Tk interface package on your system.
```
import tkinter
```

## Turtle Fundamentals
- To create a turtle screen
```
ts = turtle.getscreen()
```
- To create a turtle instance
```
t = turtle.Turtle()
```
- To move the turtle forward by 100 steps
```
t.forward(100)
```
- To move the turtle backward by 100 steps
```
t.backward(100)
```
- To change the turtle direction to the left/right by 120 degrees angle
```
t.left(120)
```
``` 
t.right(120)
```
- To change the position of the turtle
```
t.goto(100, 100)
```
- To change the position of the turtle without drawing in the canvas
```
t.penup()
```
- To start drawing in the canvas again after moving position
```
t.pendown()
```
- To go back to the initial position
```
t.home()
```
- To change the turtle's pen color
```
t.color("red")
```
- To create a circle with a diameter of 100
```
t.circle(100)
```
- To fill the circle with a yellow color
```
t.fillcolor("yellow")
t.begin_fill()
t.circle(100)
t.end_fill()
```



