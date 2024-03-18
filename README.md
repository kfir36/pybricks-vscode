# PyBricks VS Code setup
i will explain how to use the [pybricks](https://pybricks.com/) spike prime with the [pybricksdev](https://github.com/pybricks/pybricksdev) python module.
**important!!** only use [python 3.9](https://www.python.org/downloads/release/python-3913/)

 1. installations:
	### software:
	  - VS Code [https://code.visualstudio.com/](https://code.visualstudio.com/)  
	Editing python programs. Use the "System Installer".

	 - Python 3 [https://www.python.org/](https://www.python.org/)  
		It's python.

	 - pybricks [https://beta.pybricks.com/](https://beta.pybricks.com/)  
		you will need to install it on your robot.
	### VS Code extensions:
	 -   [Error Lens](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)
	 -    [Pylance](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance)
	-   [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
	-   [Black Formatter](https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter)
	### python modules:
	- `pip install pybricks`
	- `pip install pipx`
	It is possible (even most likely) the above finishes with a WARNING looking similar to this:
		
		```
		WARNING: The script pipx.exe is installed in `<USER folder>\AppData\Roaming\Python\Python3x\Scripts` which is not on PATH

		```

		If so, go to the mentioned folder, allowing you to run the pipx executable directly. Enter the following line (even if you did not get the warning):

		~~~
		.\pipx.exe ensurepath

		~~~

		This will add both the above mentioned path and the `%USERPROFILE%\.local\bin` folder to your search path. Restart your terminal session and verify `pipx` does run.
	- `pipx install pybricksdev`
	- `pip install black`
2. -   Add a keyboard shortcut to run the programs that we write. `Ctrl-Shift-P` > `Preferences: Open Keyboard Shortcuts (JSON)`. Edit the JSON to add the keyboard shortcut to run the task. Paste in the code below at the bottom of keybindings.json.

	-   **RUN OUR PROGRAM!** Turn the robot on and ensure the keyboard shortcut `ctrl-shift-L` runs the command, which should also run their program. Also, `Ctrl-Shift-P` > `Tasks: Run task` should pop up a menu with the correct entry. Watch the terminal and make sure the robot name is correct. If not, recheck that you completed step 11 correctly.

keybindings.json
~~~json
[
    {
        "key" : "ctrl+shift+l",
        "command" : "workbench.action.tasks.runTask",
        "args": "Run on robot"
    }
]
~~~
