from tkinter import *


# importing strftime function to capturing system's time

from time import strftime

# creating tkinter window
digital_clock = Tk()
digital_clock.geometry("600x300")
digital_clock.title('Digital Clock')

# Display time on the label using this function
def time():
    string = strftime('%H:%M:%S %p')  # %h=hour ,%M=Minute ,%S=second ,p%=am or pm according to the given time value
    lable.config(text = string)
    lable.after(1000, time)

#Increase the user experience designning the label widget

lable = Label(digital_clock, font = ('calibri', 40, 'bold'),
            background = '#AA0000',
            foreground = 'white')


# clock at the centre of the tkinter window

lable.pack(anchor = 'center')
time()  #function calling

mainloop()
