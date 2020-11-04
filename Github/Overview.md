# GitHub Fundamentals

GitHub is a way for you to start storing code and begin to build best practices utilizing version control and git. The benefits of this are:

  - Ability to contribute to same source code in a team setting.
  - Reliable storage and access (not computer specific).
  - Version control allowing you modify code, test neww features, and easily correct breaks.
  - Open source contributions (if public repository, the limit does not exist for contributors).

## Getting started

### Installing Git

Git is a free version control system designed to handle small and large projects. It allows you to work on multiple features simultaneously and keep a history of your work.

> When you are installing git, make sure to select the option to "Add to path." This will make sure that git is accessable when you try and use it in your terminal.

You will need to download git to work in github and any other major code sharing platform.

Go [here](https://git-scm.com/downloads) to download git for your OS.

### Signing up to Github

Getting started with GitHub is a simple process by signing up with an email, creating a username and password.

Go to [GitHub](https://github.com/). The front page is set up to add your email, username, and password and sign up very easily.

![GitHubSignUp](/Github/Images/GitHubSignup.png)

## Creating your first repository

### Repository Overview

A repository contains all folders, files, and revision history for a project. This is the code, documentation, pipeline definitions, etc...

### Choosing a name

Your repository name should be short and memorable. It should give people an idea of what the repo (repository) is about and also get them interested in the project.

### Choosing Public or Private

This decision is based on if you want others to be able to access or not.

  - Public - Anoyone on the internet can see the repository but you can choose who can contribute.
  - Private - You choose who can see and contribute.

### Initializing the Repository with extras

This allows you to create the repository with some options.

  - README - A file where you can write a long description for your project with information.
  - .gitignore - You don't need to worry about this one right off the bat. However, later on, this file allows you to define files, or types of files to exclude from being committed to your repository.
  - Licenses - You can choose to initiate the repository with different licenses. The most common for open source projects is the [MIT License](https://mit-license.org/). This allows users to copy and use or change your code for any scenario they see fit. There are more licenses you you can find more info on all of them [here](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/licensing-a-repository).

### Finishing the repository.

To finish creating the repository, simply click the"Create repository" button at the bottom of the page.

![Create Repository Button](/Github/Images/CreateRepositoryButton.png)

## Cloning the repository to your local machine

Cloning a repository down to your local machine will create a copy of the repository to a location on your computer you specify. It allows you to work on the code locally without changing the code in GitHub unless you want to. This is useful when working with a team to develop something or working in someone elses open source project.

### Choosing a location

> **Best Practice Tip**
> I generally try and keep all projects in a single location so I don't have to go looking all over for different projects. I suggest creating a **Source** folder (literally a folder named Source) to keep all projects there.

### Clone the repository

Go to your GitHub repository. Select the **Code** dropdown box and select the clipboard icon to copy the URL to your clipboard.

![GitHub Clone URL](/VSCode/Images/githubcloneurl.png)

Copy and paste the following code into a [PowerShell](/PowerShell/Overview.md) terminal window to create the source folder, navigate to that location, and clone the repository. replace `<your repository here>` with the url to your GitHub repository you . Example command: `git clone https://github.com/FranklinTipton/Fundamentals.git`

> This is for Windows only.

```powershell
# Windows only
New-Item -Path 'C:\Source' -ItemType Directory -Force
Set-Location -Path 'C:\Source'
git clone <your repository here>
```

Your repository should be cloned and linked to your GitHub Repository
