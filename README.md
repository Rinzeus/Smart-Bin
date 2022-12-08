equation = ""

def show(value):
    global equation
    equation+=value
    label_result.config(text=equation)

def clear():
    global equation
    equation = ""
    label_result.config(text=equation)

def calculate():
    global equation
    result =""
    if equation !="":
        try:
            result=eval(equation)
        except:
            result="ERROR"
            equation=""
    label_result.config(text=result)
    
label_result= Label(root,width=25,height=2,text="",font=("arial",30))
label_result.pack()
