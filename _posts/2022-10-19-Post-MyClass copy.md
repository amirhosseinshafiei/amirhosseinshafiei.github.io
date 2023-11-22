---
layout: posts
title: jungle
---

import turtle <br>
import random <br>

color_list = ["green4","chartreuse4","forestgreen","darkgreen","darkgreen"] <br>

def leaf(x): <br>
    turtle.fillcolor(random.choice(color_list)) <br>
    turtle.begin_fill() <br>
    turtle.right(20) <br>
    for _ in range(9): <br>
        turtle.forward(x) <br>
        turtle.left(5) <br>
    turtle.end_fill() <br>    
    turtle.left(135) <br>
    turtle.fillcolor(random.choice(color_list)) <br>
    turtle.begin_fill() <br>
    for _ in range(9): <br>
        turtle.forward(x) <br>
        turtle.left(5) <br>
    turtle.left(155) <br>
    turtle.end_fill() <br>

def tree(d,r,n): <br>
    if d<20: <br>
        return <br>
    turtle.pensize(n) <br>
    turtle.pencolor("chocolate4") <br>
    turtle.forward(d) <br>
    turtle.left(r) <br>
    tree(d * (random.random()/2+0.5), r * (random.random()/2+0.7), n * (random.random()/2+0.5)) <br>
    turtle.pencolor(random.choice(color_list)) <br>
    turtle.pensize(3) <br>
    if d<80: <br>
        turtle.left(45) <br>
        leaf(d/20) <br>
        turtle.right(90) <br>
        leaf(d/20) <br>
        turtle.left(45) <br>
    turtle.pencolor("chocolate4") <br>
    turtle.right(2*r) <br>
    tree(d * (random.random()/2+0.5), r * (random.random()/2+0.7), n * (random.random()/2+0.5)) <br>
    turtle.pencolor(random.choice(color_list)) <br>
    turtle.pensize(1) <br>
    if d<80: <br>
        turtle.left(45) <br>
        leaf(d/20) <br>
        turtle.right(90) <br>
        leaf(d/20) <br>
        turtle.left(45) <br>
    turtle.pencolor("chocolate4") <br>
    turtle.left(r) <br>
    turtle.backward(d) <br>
    
def setup_screen(width, heigh): <br>
    turtle.left(90) <br>
    turtle.pencolor("chocolate4") <br>
    turtle.tracer(0) <br>
    turtle.hideturtle() <br>
    turtle.screensize(width, heigh) <br>


turtle.pencolor("darkolivegreen") <br>
turtle.penup() <br>
turtle.right(90) <br>
turtle.forward(300) <br>
turtle.left(90) <br>
turtle.pendown() <br>
turtle.pensize(400) <br>
turtle.forward(1000) <br>
turtle.backward(2000) <br>
turtle.left(90) <br>
turtle.penup() <br>
turtle.forward(500) <br>
turtle.right(90) <br>
turtle.pendown() <br>
turtle.pencolor("khaki3") <br>
turtle.pensize(600) <br>
turtle.forward(2000) <br>
width, height =1600, 200 <br>
x=-width/2 <br>
y=-height/2 <br>
setup_screen(width, height) <br>
tree_count = 15 <br>

for ـ in range(tree_count): <br>
    x += random.randint(90, 110) <br>
    y = random.randint(-400, -100) <br>
    turtle.penup() <br>
    turtle.setpos(x, y) <br>
    turtle.pendown() <br>
    tree(random.randint(100, 120), random.randint(20, 30), random.randint(15, 25)) <br>
    turtle.update() <br>   

turtle.mainloop() <br>

