# Spiro_graph
#the given python code generates a beautiful spiro graph using python turtle library 

from turtle import Turtle, Screen
import random

def random_color():
    r = random.randint(0, 255)
    g = random.randint(0, 255)
    b = random.randint(0, 255)
    tuple_color = (r, g, b)
    return tuple_color


gullu = Turtle()
gullu.shape('turtle')


def spiro_graph(gap):
    for _ in range(int(360/gap)):
        gullu.color(random_color())
        gullu.circle(100)
        gullu.setheading(gullu.heading() + gap)

spiro_graph(2)

screen = Screen()
screen.exitonclick()
