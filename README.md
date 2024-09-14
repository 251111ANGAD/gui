from tkinter import *
import calendar
def show_calender():
    abc = Tk()
    abc.title("CALENDER")
    abc.geometry("550x500")
    abc.config(background = "lightyellow")
    txt_CALENDER = int(txt_YEAR.get())
    cnt_CALENDER = calendar.calendar(txt_CALENDER)
    #CREATED A TEXT WIDGET FOR SHOWNING THE CALENDAR
    txt_WIDGET_CALENDER = Text(abc,font = "Handwriting",wrap = "none",height = 100,width = 100)
    #INSERT THE CALENDER CONTENT INTO THE TEXT WIDGET
    txt_WIDGET_CALENDER.insert("1.0",cnt_CALENDER)
    txt_WIDGET_CALENDER.config(state="disabled")
    txt_WIDGET_CALENDER.grid(row = 5,column = 1) 

    abc.mainloop()
l2 = Tk()
l2.title("CALENDER")
l2.geometry("600x700")
l2.config(background = "lightyellow")
lbl_CALENDER = Label(l2, text = "CALENDAR", font = ("helvetica", 80, "bold"),
                                bg = "lightblue", fg = "grey", relief = "raised",
                                borderwidth = 5)
lbl_ENTER_YEAR = Label(l2, text = "Enter Year", font = ("helvetica", 40, "bold"),
                                bg = "lightgrey", fg = "black", relief = "raised",
                                borderwidth = 5)
txt_YEAR = Entry(l2, font = ("impact", 40), width = 10)
btn_SHOW_CALENDER = Button(l2, text = "SHOW", padx = 25, pady = 10, bd = "25", background = "skyblue",
                                command = show_calender)
lbl_CALENDER.grid(row = 1,column = 1)
lbl_ENTER_YEAR.grid(row = 2,column = 1)
txt_YEAR.grid(row = 3,column = 1)
btn_SHOW_CALENDER.grid(row = 4,column = 1)
l2.mainloop()
