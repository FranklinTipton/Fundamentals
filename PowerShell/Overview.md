# PowerShell Fundamentals

## What is PowerShell

PowerShell is a cross-platform task automation, scripting language that also consists of a command-line shell. You can use it to run individual commands, create your own commands, or write full functioning scripts and programs.

## Navigating the File System with PowerShell

Navigating your file system in PowerShell can be useful in multiple ways. It can be faster than navigating the GUI. It can help you understand your file system better. It can allow you to programatically adjust your file system such as automating archiving old folders or creating a new project with a single command. There are many reasons to do so and another one is being able to manage git with a PowerShell terminal.

To start, open a PowerShell terminal. You can search "PowerShell" in your Windows Search box.

By default, the PowerShell terminal will display it's current "**location**" in the command line.

![PowerShell Command Line](/PowerShell/Images/TerminalCommandLine.png)

Let's break down the terminal image above.
 - `PS` - This is a default start for a PowerShell terminal app. Some people prefer to only see this and you can customize your termial to this if you want.
 - `C:\Source` - This is your current file location. This means that if you run a command or script, it will operate out of this location in your file system.
 - `>_` - This is an indicator of the end of the information in your terminal cusor and where you will be typing.

You can navigate to different locations in your file system by typing commands. To change your location you will use the PowerShell command, `Set-Location` or the **alias** (Kind of like a nickname for a command) `cd`. In the code below, I will use both commands to move to the `Fundamentals` folder inside the `Source` folder, and then back to the `Source` folder.

```powershell
PS C:\Source> Set-Location -Path C:/Source/Fundamentals
PS C:\Source\Fundamentals> cd C:/Source
PS C:\Source>
```

You can see that `Set-Location` changes the working location to the `Fundamentals` folder and then `cd` changes the location back.


