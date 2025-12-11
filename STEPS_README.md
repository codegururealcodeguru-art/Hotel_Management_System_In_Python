**steps to create hotel management system in python**
**Step 1: Setup Your Environment**
Install Python (if not already installed):
👉 Download Python

Open any Python IDE or editor:

IDLE (comes with Python)

VS Code

PyCharm

Or even a simple text editor + terminal

**Step 2: Create a New Python File**
Create a file named:
hotel_management.py

**Step 3: Import Tkinter Modules**
import tkinter as tk
from tkinter import messagebox
tkinter = Main GUI library

messagebox = Pop-up alerts for info or warnings

**Step 4: Define the HotelManagement Class**
class HotelManagement:
    def __init__(self, root):
        # GUI layout and initialization here
This will hold all buttons, text boxes, and logic.

**Step 5: Create Input Fields**
Use Entry, Label, and OptionMenu to create fields:

Guest Name

Phone Number

Room Type (dropdown: Single, Double, Deluxe, Suite)

**Step 6: Add Buttons**
Add the following buttons:

Check-In – adds guest to the list

Show All Guests – displays all current guests

Check-Out – removes guest by name

**Example:**

tk.Button(root, text="Check-In", command=self.check_in)
**Step 7: Add Output Display**
Use a Text widget to show guest list:

self.output = tk.Text(root, height=12, width=60)
**Step 8: Define the Logic Methods**
check_in() – adds guest to self.guests

show_guests() – displays all guests in Text box

check_out() – removes a guest from list

**Step 9: Launch the App**
At the end of the file, write:

root = tk.Tk()
app = HotelManagement(root)
root.mainloop()
This starts the GUI loop.

**Step 10: Run and Test**
Run the script:

python hotel_management.py
Try check-in, view list, and check-out.

 Final GUI Preview:
Input fields: Name, Phone, Room Type

Buttons: Check-In, Show All Guests, Check-Out

Guest list area (multi-line text box)

 

code explanation
Purpose of the App
It simulates a simple hotel check-in/check-out system that:

Accepts guest details (name, phone, room type)

Adds them to a list

Shows all checked-in guests

**Allows check-out by guest name
**
**1. Imports and Class Setup**
import tkinter as tk
from tkinter import messagebox
tkinter: Python’s standard GUI library

messagebox: Provides pop-up alerts for success or errors

**2. HotelManagement Class**
class HotelManagement:
    def __init__(self, root):
Initializes the GUI app.

root: The main window.

 Window Setup:
self.root.title(" Hotel Management System")
self.root.geometry("500x600")
self.root.config(bg="lightblue")
Sets title, window size, and background color.

 Guest List
self.guests = []
Stores guest records as a list of dictionaries.

**GUI Widgets and Input Fields
 1.Guest Name**
self.name_var = tk.StringVar()
tk.Entry(root, textvariable=self.name_var)
Entry box to input guest name.

 2.Phone Number
self.phone_var = tk.StringVar()
tk.Entry(root, textvariable=self.phone_var)
Entry box for phone number.

 Room Type Dropdown
self.room_var = tk.StringVar()
self.room_menu = tk.OptionMenu(root, self.room_var, "Single", "Double", "Deluxe", "Suite")
Drop-down menu for room types.

Buttons
 1.Check-In
tk.Button(root, text="Check-In", command=self.check_in)
Calls check_in() to register the guest.

 2.Show All Guests
tk.Button(root, text="Show All Guests", command=self.show_guests)
Displays all current guests in a text area.

 3.Check-Out
tk.Button(root, text="Check-Out Guest", command=self.check_out)
Calls check_out() to remove a guest by name.

4.Output Display
self.output = tk.Text(root, height=12, width=60)
Multi-line text box to display guest list.

Methods Functionality
1. check_in()
def check_in(self):
    name = self.name_var.get()
    phone = self.phone_var.get()
    room = self.room_var.get()
Gets values from the input fields.

Checks if name and phone are not empty.

Adds a dictionary of guest info to self.guests.

Shows success message or warning.

2. show_guests()
def show_guests(self):
    self.output.delete(1.0, tk.END)
Clears the text area.

Lists all guests with serial number, name, phone, and room type.

3. check_out()
def check_out(self):
    name = self.name_var.get()
Searches the guest list by name (case insensitive).

Removes the matching guest.

Shows a messagebox for success or “not found”.

Running the Application
root = tk.Tk()
app = HotelManagement(root)
root.mainloop()
Creates a tkinter window.

Launches the app by instantiating the HotelManagement class.

Starts the GUI event loop.

Example Use Case
User enters: Name = “John”, Phone = “9876543210”, Room = “Deluxe”

Clicks  Check-In

Guest added to the list

Clicks  Show All Guests to see list

To remove: enter “John” again and click  Check-Out

 
