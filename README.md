- 👋 Hi, I’m @Aleksey2929
- 👀 I’m interested in something without languages
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: Mask kills yourself when he see me😂
from turtle import *
from time import sleep
from random import randint, choice
def bonus():
    global k
    k = 2
lt = []
n = int(numinput('Choise', 'Choise your fighter (1, 6)', minval=1, maxval=6))
colors = ['red', 'blue', 'green', 'purple', "orange", 'lime', 'grey', 'lightgrey', ]
for i in range(6):
    t = Turtle()
    t.shape('turtle')
    t.up()
    t.color(choice(colors), choice(colors))
    #t.screen.colormode(241)
    #t.color((randint(0, 240), randint(0, 240),randint(0, 240)), (randint(0, 240), randint(0, 240),randint(0, 240)))
    t.teleport(-400,i*100-200)
    t.pensize(10)
    t.down()
    lt.append(t)
is_active = 1

example = Turtle()
example.hideturtle()
example.pensize(4)
example.teleport(400, 7*100-200)
example.right(90)
example.fd(8*100)
example.left(90)
example.pensize(1)
k = 1
lt[n-1].screen.onkey(bonus, "Up")
lt[n-1].screen.listen()
shootl = []
while is_active:
    a = choice(lt)
    if lt.index(a) == n-1:
        a.forward(randint(1, 5)*k)
        if k > 1:
            k -= 0.1
    else:
        a.forward(randint(1, 5))
    '''if a.xcor()%50 in [0, 1, 2, 3, 4]:
        a.pencolor(choice(colors))'''
    if randint(1, 100) == 10:
        a.fd(5)
    if randint(1, 100) == 10:
        example.teleport(a.xcor(), a.ycor())
        example.showturtle()
        
    if a.xcor() > 400:
        is_active = 0
#$ exitonclick()
<!---
Aleksey2929/Aleksey2929 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
