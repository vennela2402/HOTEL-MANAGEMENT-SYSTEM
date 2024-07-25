# import tkinter module
from tkinter import *
import random
# import font
from tkinter import font
# import image
from PIL import Image, ImageTk
# import time
import time
# import messege box
import tkinter.messagebox


window = Tk()

window.title('wines management system by vennela')
window.geometry("1270x700")
window.colormapwindows = 'white'


'''
bg= PhotoImage(file='C:\\Users\\divya\\Desktop\\vennela.gif') 
label7 =Label (window, image=bg) 
label7.place(x=0, y=0)
'''

label8 = Label(window, text="BREAKING BOUNDARIES WINES",
               font="times 28 bold italic", bg="white")
label8.place(x=600, y=40, anchor="center")


localtime = time.asctime(time.localtime(time. time()))
label3 = Label(window, text=localtime, font='times 18', bg="white")
label3.place(x=950, y=80)


E_Red_Wine = StringVar()
E_White_Wine = StringVar()

E_Rose_Wine = StringVar()
E_Sparkling_Wine = StringVar()

E_Dessert_Wine = StringVar()
E_Fortified_Wine = StringVar()

PaidTax = StringVar()

SubTotal = StringVar()
YourTotalBill = StringVar()

Nameofcustomer = StringVar()
MobileNo = StringVar()

E_Red_Wine.set("")

E_White_Wine.set("")

E_Rose_Wine.set("")

E_Sparkling_Wine.set("")

E_Dessert_Wine.set("")
E_Fortified_Wine.set("")

PaidTax.set("0")

SubTotal.set("0")

YourTotalBill.set("0")

Nameofcustomer.set("")
MobileNo.set("")


label2 = Label(window, text="Name of Customer:",
               font="times 15 bold", bg="white")
label2.place(x=20, y=110)
e10 = Entry(window, bd=2, textvariable=Nameofcustomer, font="times 15",)
e10.place(x=200, y=115)

labe13 = Label(window, text="Mobile.No : ", font="times 15 bold", bg="white")
label3.place(x=450, y=110)
e11 = Entry(window, bd=2, textvariable=MobileNo, font="times 15",)
e11.place(x=560, y=115)


label1 = Label(window, text=("Menu"), font="times 20 bold", bg="white")
label1.place(x=70, y=170)

labe19 = Label(window, text="Select the items",
               font="times 20 bold", bg="white")
labe19.place(x=370, y=180)


label10 = Label(window, text="Red Wine-RS 1999", font="times 18", bg="white")
label10.place(x=20, y=230)
e1 = Entry(window, bd=2, textvariable=E_Red_Wine)
e1.place(x=400, y=240)

label11 = Label(window, text="White Wine-RS 1599", font="times 18", bg="white")
label11.place(x=20, y=280)
e2 = Entry(window, bd=2, textvariable=E_White_Wine)
e2.place(x=400, y=290)

label12 = Label(window, text="Rose Wine-RS 2099", font="times 18", bg="white")
label12.place(x=20, y=330)
e3 = Entry(window, bd=2, textvariable=E_Rose_Wine)
e3.place(x=400, y=340)


label13 = Label(window, text="Sparkling Wine-RS 3449",
                font="times 18", bg="white")
label13.place(x=20, y=380)
e4 = Entry(window, bd=2, textvariable=E_Sparkling_Wine)
e4.place(x=400, y=390)

label14 = Label(window, text="Dessert Wine-RS 999",
                font="times 18", bg="white")
e5 = Entry(window, bd=2, textvariable=E_Dessert_Wine)
label14.place(x=20, y=430)
e5.place(x=400, y=440)

label15 = Label(window, text="Fortified Wine-RS 5571",
                font="times 18", bg="white")
label15.place(x=20, y=480)
e6 = Entry(window, bd=2, textvariable=E_Fortified_Wine)
e6.place(x=400, y=490)


f1 = Frame(window, bg="white", relief=SUNKEN)

f1.place(x=600, y=300)

text_input = StringVar()

operator = ""


def btnclick(numbers):
    global operator
    operator = operator + str(numbers)
    text_input.set(operator)


def btnClearDisplay():
    global operator
    operator = ""
    text_input.set("")


def btnEqualsInput():
    global operator
    sumup = str(eval(operator))
    text_input.set(sumup)
    operator = ""


txtdisplay = Entry(f1, font=('arial 13'), textvariable=text_input, bd=2, insertwidth=1,
                   bg="white", justify='center')
txtdisplay.grid(columnspan=4)


'''

btn7 = Button(f1, bd=0, font=('arial 15'), text="7",bg="white", command=lambda: btnclick(7)) 
btn7.grid(row=2, column=0)

btn8 = Button(f1, bd=0, fg="black", font=('arail 15'),text="8", bg="white", command=lambda: btnclick(8))
btn8.grid(row=2, column=1)

btn9 = Button(f1, bd=0, fg="black", font=('arail 15'), text="9", bg="white", command=lambda: btnclick (9))
btn9.grid(row=2, column=2)

Addition = Button (f1, bd=0, fg="black", font=('arail 15'), text="+", bg="white", command=lambda: btnclick("+"))
Addition.grid(row=2, column=3)

btn4 = Button(f1, bd=0, fg="black", font=('arail 15'), text="4", bg="white", command=lambda: btnclick(4))

btn4.grid(row=3, column=0)

btn5 Button(f1, bd-0, fg="black", font-('arail 15'),

text="5", bg="white", command-lambda: btnclick(5))

btn5.grid(row=3, column=1)

btn6 - Button(f1, bd-0, fg="black", font=("arail 15'), text="6", bg="white", command-lambda: btnclick(6))

btn6.grid(row=3, column=2)

Subtraction = Button(f1, bd-0, fg="black", font=( 'arail 15'), text="-", bg="white", command-lambda: btnclick("-"))

Subtraction.grid(row=3, column=3)








'''


window.mainloop()

