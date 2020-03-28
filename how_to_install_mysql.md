# How to Install MySQL, MySQL Workbench, and MySQL CLI on Windows 10

## Roadmap

1. Install Chocolatey Package Manager
2. Install MySQL, MySQL Workbench, and MySQL Command Line Tools
3. Log into MySQL and set root password
4. Test connection in MySQL workbench

## STEP ONE: Install Chocolatey Package Manager

Chocolatey is the package manager for Windows, much like apt-get for Ubuntu or Homebrew for macOS.

It is an absolutely essential application for Windows 10... so of course Windows 10 does not include it out of the box. You'll need to install it.

#### How to Install Chocolatey

1. Open Powershell as an administrator (right-click, 'run as administrator')
2. Enter or copy/paste the following command:

```text

Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

```

#### TEST CHOCOLATEY

Enter the following command in Powershell:

```
choco --version

```

You should see something like 0.10.15 depending on your version.

## STEP TWO: Install MySQL, MySQL Workbench, and MySQL Command Line Tools

1. Open Powershell as administrator
2. Use Chocolatey to install all three packages with the following command

```
choco install -y mysql mysql.workbench mysql-cli

```

3. Watch the magic happen. THe install should take a few minutes.
4. Enter the following command in Powershell to verify installation

```
mysqld --version

```

Output should be something like

```
C:\tools\mysql\current\bin\mysqld.exe  Ver 8.0.19 for Win64 on x86_64 (MySQL Community Server - GPL)
PS C:\Windows\system32>
```

This verifies both your installation of MySQL and MySQL Command Line Tools.

Enter MySQL Workbench into Windows search. You should see it installed as an application. Save it to your start menu or taskbar if you'd like.

## STEP THREE: Log in to MySQL and Set Root Password

1. Open Powershell as Administrator
2. Enter the following MySQL-CLI command:

```
mysql -u root password <whatever you want your password to be>
```

You should see a whole bunch of text scroll by. If you scroll up to the top you'll see these are all possible MySQL CLI Commands. Go ahead and memorize them, I'll wait.

Done? Okay, moving on.

3. Verify your login

Enter the following command in Powershell:

```
mysql -u root -p
```

You should be prompted for a password. Enter the password you selected earlier. You should see a message welcoming you to MySQL Monitor and you'll notice your command prompt has changed.

You are now in the MySQL CLI. you can exit by pressing ctrl-c.

## STEP FOUR: Test Connection in MySQL Workbench

MySQL Workbench is an awesome graphical tool for working with MySQL databases. If you are using MySQL in a project, you'll use Workbench _way_ more than you'll ever use the CLI tools.

1. In Windows, find the MySQL Workbench application using search or by clicking on the icon if you saved it to start or the taskbar earlier.

2. Click on the button that says "Local Instance MySQL"

3. You should be prompted for a password. Enter the password you set earlier and save it in the vault if you'd like (recommended)

4. Entering your password will connect you to your local MySQL Server. What you're looking at is a GUI for the MySQL Server itself, not any particular database. Unless you added databases during Hack Reactor, you won't see any here.

Congrats! You're now ready to use MySQL Server in your development projects and as a tool for learning SQL. We'll get to that in the next session!

## What to do next

Start learning SQL syntax. It is an absolutely essential skill for developers.

Codecademy is a good place to start learning the basics:
https://www.codecademy.com/learn/learn-sql
