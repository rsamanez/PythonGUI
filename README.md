
## How to create a GUI Application with Python Tkinter
Basic Program

```
import tkinter

window = tkinter.Tk()
window.title("GUI")

# creating 2 text labels and input labels

tkinter.Label(window, text = "Username").grid(row = 0) # this is placed in 0 0
# 'Entry' is used to display the input-field
tkinter.Entry(window).grid(row = 0, column = 1) # this is placed in 0 1

tkinter.Label(window, text = "Password").grid(row = 1) # this is placed in 1 0
tkinter.Entry(window).grid(row = 1, column = 1) # this is placed in 1 1

# 'Checkbutton' is used to create the check buttons
tkinter.Checkbutton(window, text = "Keep Me Logged In").grid(columnspan = 2) # 'columnspan' tells to take the width of 2 columns
                                                                             # you can also use 'rowspan' in the similar manner

window.mainloop()

```
## Creating the Installer
We need PyInstaller to create the binary file
```
pip install pyinstaller
``` 
command to create the application on Windows
```
pyinstaller --onefile --noconsole --icon=some_icon_file.ico ApplicationName
```
command to create the application on Mac
```
pyinstaller --onefile --noconsole --icon=some_icon_file.icns ApplicationName
```
This sample command ( Mac OS Application )
```
pyinstaller --onefile --icon=python.icns --noconsole Sample1.py
```

