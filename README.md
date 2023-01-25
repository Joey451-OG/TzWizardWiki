# TzWizard
A tool for converting time zones and displaying mod time zones.

# How To Use TzWizard
1. Open a terminal window on your computer.
 
2. Navigate to the directory where the TzWizard script is stored using the `cd` command. For example, if the script is stored in your "Documents" folder, you        would enter `cd Documents` in the terminal.

3. Once you are in the correct directory, enter `python TzWizard.py` to run the script.
   You will be greeted with the message `Welcome to TzWizard! What would you like to do? (Type "help" for a list of commands)`

4. To display a list of commands and their explanations, type `help` and press enter.

5. To convert a time from your time zone to the time zones of other mods, type `convert` and press enter. You will be prompted to enter your name, and then the            desired time in 24 hour format. The script will then display a list of all known mods and the equivalent time in their time zones.

6. To convert a time from AM/PM format to 24 hour format, type `24hr` and press enter. You will be prompted to enter a time in AM/PM format, and the script will          display the equivalent time in 24 hour format.

7. To display a list of all known mods, type `modlist` and press enter. 

8. To clear the terminal screen, type `clear` and press enter.

9. To exit the script, type `exit` and press enter.

Please note that the script is only able to convert times for the mods that are in the `modlist` dictionary, if you want to add another mod you need to add the mod name and the corresponding time zone offset to the dictionary.

# How TzWizard Works

1. The first line `import os` imports the `os` module, which provides a way for the script to interact with the operating system.

2. The next lines, describe the time zones of different mods and they are stored in a dictionary called `modlist` with mod name as key and time offset as value.

3. There are several functions defined in the script:
  - `HELP()`: This function displays a list of commands and their explanations when the `help` command is entered by the user.
  - `MODCONV(greenwichHour, m)`: This function takes in the Greenwich Hour and mod name as input and returns the equivalent time in the mod's time zone. It does this       by subtracting the mod's time offset from the Greenwich Hour, and if the resulting hour is less than 0 or greater than 24, it adjusts the hour accordingly.
  - `CONVERT(name)`: This function takes in the user's name as input and prompts the user to enter a desired time in 24 hour format. It then uses the `MODCONV`             function to convert the input time to the time zones of all known mods and displays the results in a list.
  - `CLEAR()`: This function clears the terminal screen. It uses the `platform` attribute of the `sys` module to determine the operating system and then calls the         appropriate command to clear the screen.
  - `24CONV(ls)`: This function takes in a list of input (time in AM/PM format) as input and converts it to 24 hour format.

4. The variable `run` is set to `True` to indicate that the script should continue running until the `exit` command is entered.

5. The `print` statement at the beginning of the script welcomes the user to the TzWizard tool and prompts them to enter a command.

6. The script then enters a while loop that continues running as long as the value of `run` is `True`. Inside the while loop, the script waits for the user to enter a    command.

7. When a command is entered, the script checks if the command is `help`, `convert`, `24hr`, `modlist`, `clear`, or `exit`. If the command is `help`, the `HELP`          function is called, if it's `convert`, the `CONVERT` function is called, if it's `24hr` the `24CONV` function is called, if it's `modlist` the mod list is printed,    if it's `clear` the `CLEAR` function is called. If the command is `exit`, the value of `run` is set to `False` which causes the while loop to exit and the script to    end.

8. If the command entered is not recognized, the script will print an error message and prompt the user to enter another command.

In summary, this script provides a command-line interface for converting time zones and displaying mod time zones, and also includes functions for converting AM/PM time to 24-hour format, clearing the terminal screen, and displaying a list of commands.


This README.md file was writen my ChatGPT 3 and formated by It'sJoeyG
