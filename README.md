# hello_world.py

import PySimpleGUI as sg

sg.Window(title="Hello World", layout=[[]], margins=(100, 50)).read()

layout = [[sg.Text("Hello World python GUI ")], [sg.Button("ok")]]

# Create the window
window = sg.Window("Dome", layout)


# Create an event loop

while True:
    event, values = window.read()
    # End program if user closese window or
    # presses the OK button
    if event == "OK" or event == sg.WIN_CLOSED:
        break

window.close()
