# PowerShell Overview

## What is PowerShell

PowerShell is a cross-platform task automation, scripting language that also consists of a command-line shell. You can use it to run individual commands, create your own commands, or write full functioning scripts and programs.

## Getting Help in PowerShell

One of the best parts of PowerShell is its built in help system. It has help files for most commands and a lot of content for in depth information and programming fundamentals in PowerShell.

### Updating the Help

Before we use the help files, we want to make sure they are all up to date. Just copy and paste the following command into your PowerShell terminal to update the help files.

```powershell
Update-Help *
```

### Using the Help

Now, to use the help, you will use `Get-Help` followed by the command you want to know more about. In our example, we will use `Set-Location`

```powershell
Get-Help Set-Location
```

This will give you a synopsis, a longer description, the syntax.

You can get more information including details about each parameter, examples on how to use the command and more by adding the **Full** paramter.

```powershell
Get-Help Set-Location -Full
```

## Setting up PowerShell

When PowerShell starts, for security purposes, the default behavior is to not allow scripts to run. You have to run a command to change this. Once you run the following command, you should have to run it again. Copy and paste the follwing command to your terminal to change the settings.

```powershell
Set-ExecutionPolicy -ExecutionPolicy Unrestricted
```

## Navigating the File System with PowerShell

Navigating your file system in PowerShell can be useful in multiple ways. It can be faster than navigating the GUI. It can help you understand your file system better. It can allow you to programatically adjust your file system such as automating archiving old folders or creating a new project with a single command. There are many reasons to do so and another one is being able to manage git with a PowerShell terminal.

To start, open a PowerShell terminal. You can search "PowerShell" in your Windows Search box.

By default, the PowerShell terminal will display it's current "**location**" in the command line.

![PowerShell Command Line](/PowerShell/Images/TerminalCommandLine.png)

Let's break down the terminal image above.
 - `PS` - This is a default start for a PowerShell terminal app. Some people prefer to only see this and you can customize your termial to this if you want.
 - `C:\Source` - This is your current file location. This means that if you run a command or script, it will operate out of this location in your file system.
 - `>_` - This is an indicator of the end of the information in your terminal cursor and where you will be typing.

You can navigate to different locations in your file system by typing commands. To change your location you will use the PowerShell command, `Set-Location` or the **alias** (Kind of like a nickname for a command) `cd`. In the code below, I will use both commands to move to the `Fundamentals` folder inside the `Source` folder, and then back to the `Source` folder.

```powershell
PS C:\Source> Set-Location -Path C:/Source/Fundamentals
PS C:\Source\Fundamentals> cd C:/Source
PS C:\Source>
```

You can see that `Set-Location` changes the working location to the `Fundamentals` folder and then `cd` changes the location back.

## Installing a module

One of the great things about PowerShell is that you can install different modules. Modules give you access to commands and scripts that others have written and made available for anyone to use.

### PowerShell Gallery

By default, PowerShell is connected to the [PowerShell Gallery](https://www.powershellgallery.com/). This is the main repository do distribute PowerShell modules and where you can find most published modules. If you ever write your own module, this is most likely where you will want to put it to get it to the most people.

### Install the Az PowerShell module

The Az PowerShell module is the official module to manage Azure resources. It is a good idea to get familiar with it if you plan on working in Azure at all.

Run the following command to install the module.

```powershell
Install-Module -Name Az
```

A message will appear asking you to verify if you want to install. Enter either `A` or `Y`.

> If you haven't installed a module before, there will be two messages. One to install NuGet and the other to install the module. Agree to both.
