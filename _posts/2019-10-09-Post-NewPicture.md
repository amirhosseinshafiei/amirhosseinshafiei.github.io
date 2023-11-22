---
layout: posts
title: tree 
---


import turtle <br>

def leaf(x): <br>
    turtle.fillcolor("green") <br>
    turtle.begin_fill() <br>
    turtle.right(20) <br>
    for _ in range(9): <br>
        turtle.forward(x) <br>
        turtle.left(5) <br>
    turtle.end_fill() <br>    
    turtle.left(135) <br>
    turtle.fillcolor("lightgreen") <br>
    turtle.begin_fill() <br>
    for _ in range(9): <br>
        turtle.forward(x) <br>
        turtle.left(5) <br>
    turtle.left(155) <br>
    turtle.end_fill() <br>

def tree(d,r,n): <br>
    if d<20 or r<5: <br>
        return <br>
    turtle.pensize(n) <br>
    turtle.pencolor("brown") <br>
    turtle.forward(d) <br>
    turtle.left(r) <br>
    tree(d*0.8,r*0.8,n*0.6) <br>
    turtle.pencolor("darkgreen") <br>
    if d<80: <br>
        turtle.left(45) <br>
        leaf(d/10) <br>
        turtle.right(90) <br>
        leaf(d/10) <br>
        turtle.left(45) <br>
    turtle.pencolor("brown") <br>
    turtle.right(2*r) <br>
    tree(d*0.8,r*0.8,n*0.6) <br>
    turtle.pencolor("darkgreen") <br>
    if d<80: <br>
        turtle.left(45) <br>
        leaf(d/10) <br>
        turtle.right(90) <br>
        leaf(d/10) <br>
        turtle.left(45) <br>
    turtle.pencolor("brown") <br>
    turtle.left(r) <br>
    turtle.backward(d) <br>
    
   
turtle.tracer(0) <br>
turtle.hideturtle() <br>  
turtle.penup() <br>
turtle.left(90) <br> 
turtle.backward(200) <br>
turtle.pendown() <br>
turtle.pensize(20) <br>
turtle.pencolor("brown") <br>
turtle.forward(100) <br>
tree(100,40,20) <br>
turtle.update() <br>
turtle.mainloop() <br>
