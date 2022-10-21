[Home](README.md)

# Required Block of Code

```python
import math
print(math.pi)
do_calc = True
while(do_calc == True):
    while (True):
        try:
            print("-----------------------")
            print("Shape Volume Calculator")
            print("-----------------------")
            print("1. Calculate volume of a cone")
            print("2. Calculate volume of a cube")
            print("3. Calculate volume of a cylinder")
            shape = input("Choose 1, 2, or 3:")
        except ValueError:
            print("The input you typed was invalid. please type 1, 2, or 3 to make selection.")
        else:
            if (shape == "1" or shape == "2" or shape == "3"):
                break
            else:
                print("The input you typed was invalid. please type 1, 2, or 3 to make selection.")
    if (shape == "1" or shape == "3"):
        while(True):
            try:
                r=float(input("Enter radius:"))
            except ValueError:
                print("The value you entered was invalid. Only type numbers please.")
            else:
                break
    while (True):
        try:
            h=float(input("Enter height:"))
        except ValueError:
            print("The value you entered was invalid. Only type numbers please.")
        else:
            break
    if (shape == "1"):
        volume = math.pi*r*r*(h/3)
        name = "cone"
    if (shape == "2"):
        volume = h*h*h
        name = "cube"
    if (shape == "3"):
        volume = math.pi*r*r*h
        name = "cylinder"
    print("Volume of the " + name +" is",volume)
    while (True):
        try:
            another_calc = input("Do you want to perform another calculation? (y/n):")
        except ValueError:
            print("The value you entered was invalid. Only type y for yes and n for no please.")
        else:
            if (another_calc == "y" or another_calc == "n"):
                break
            else:
                print("The value you entered was invalid. Only type y for yes and n for no please.")
    if (another_calc != "y"):
        do_calc = False
        
```
