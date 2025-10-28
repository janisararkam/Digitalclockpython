# Digitalclockpython
"PROJECT DESCRIPTION" 
This project is a Digital Clock built using Python and its Tkinter library.
It displays the current time and date, updating automatically every second.
Through this project, we learn how to build a Graphical User Interface (GUI) in Python and how to use the time module to fetch and format current time and date.
1️⃣ import tkinter as tk
Purpose: Imports the Tkinter module and gives it a short alias tk.
Why Tkinter?
Tkinter is a built-in Python library used to create Graphical User Interfaces (GUI).
It allows you to design windows, buttons, labels, and other visual elements in Python.
Why alias tk?
Instead of writing tkinter every time, we use tk for simplicity (e.g., tk.Label, tk.Tk()).
2️⃣ from time import strftime
   Purpose: Imports the strftime() function directly from the time module.
Why time module?
The time module provides various time-related functions.
Here, strftime() helps us format the current time and date into a readable string.
Why strftime()?
strftime() means string format time — it converts the current system time into a string according to the format you define (like hours, minutes, seconds, etc.).
3️⃣ root = tk.Tk()
Purpose: Creates the main window (root window) of the GUI application.
  In every Tkinter application, this is the first step — it initializes the window where all widgets (buttons, labels, etc.) will appear.
Think of root as the canvas on which your digital clock will be drawn.
4️⃣ root.title("Digital Clock")
   Purpose: Sets the title of the main window.
Whatever string you provide here will appear at the top bar of the window.
Example: If you run the program, you’ll see “Digital Clock” written on the window’s title bar.
5️⃣ def time():
   Purpose: Defines a function named time which updates the current time and date on the label.
   This function will be called repeatedly to refresh the time every second so that the clock keeps ticking.
6️⃣ string = strftime('%H:%M:%S %p\n%D')
   Purpose: Fetches the current system time and date, and stores it in the variable string.
   Explanation of the format:
   %H → Hour (24-hour format)
   %M → Minute
   %S → Second
   %p → AM or PM
  \n → New line (moves the date to the next line)
  %D → Date in MM/DD/YY format
  Example output:
  15:25:40 PM
  10/28/25
7️⃣ label.config(text=string)
    Purpose: Updates the label widget with the new time and date value stored in string.
The .config() method is used to modify existing properties of a widget.
Every second, this line ensures the displayed time changes to the new one.
8️⃣ label.after(1000, time)
   Purpose: Tells Tkinter to call the time() function again after 1000 milliseconds (1 second).
   This creates a loop — after every second, the time is updated automatically.
   Without this, the clock would only show the time once and stop updating.
9️⃣ label = tk.Label(root, font=('calibri', 50, 'bold'), background='yellow', foreground='black')
   Purpose: Creates a Label widget to display the time and date.
   Parameters explained:
    root → The label will appear inside the main window (root).

font=('calibri', 50, 'bold') → Sets the font family, size, and style.

background='yellow' → Sets the background color of the label.

foreground='black' → Sets the text color to black.

Labels are used in Tkinter to display text or images — here, we display the clock output.
🔟 label.pack(anchor='center')
   Purpose: Adds the label to the window and centers it.
   pack() is a geometry manager in Tkinter — it arranges widgets on the window.
   anchor='center' keeps the clock aligned at the center of the window.
  1️⃣1️⃣ time()
       Purpose: Calls the time() function once when the program starts.
      This triggers the first display of the current time and also starts the automatic update loop (because of after(1000, time) inside the function).
1️⃣2️⃣ root.mainloop()
    Purpose: Keeps the window open and responsive until the user closes it.
    This is the main event loop of any Tkinter program — it listens for user actions (like closing the window) and updates the display continuously.









    

Without mainloop(), the window would open and close immediately.

