<img width="819" height="107" alt="image" src="https://github.com/user-attachments/assets/83d2dced-7803-4c42-8c2d-ef0be8595c4a" /># Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT
<img width="887" height="111" alt="image" src="https://github.com/user-attachments/assets/6224e6f9-228b-4bb9-a689-1cd5db7f8ed5" />

Remove the directory "my-folder"

## COMMAND AND OUTPUT
<img width="911" height="55" alt="image" src="https://github.com/user-attachments/assets/b48fb196-e921-4355-814d-48df4c100c4d" />


Create the file Rose.txt

## COMMAND AND OUTPUT

<img width="767" height="107" alt="image" src="https://github.com/user-attachments/assets/eb0451bf-29e8-4ab9-a8c3-f4ea94a967db" />

Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT

<img width="819" height="107" alt="image" src="https://github.com/user-attachments/assets/d819f0c2-6813-48d2-9f64-8106cc7a4e79" />


Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
<img width="671" height="62" alt="image" src="https://github.com/user-attachments/assets/63d77aac-cd76-402a-a168-05ba228e156e" />


Remove the file hello1.txt

## COMMAND AND OUTPUT
<img width="658" height="171" alt="image" src="https://github.com/user-attachments/assets/dbb713e9-7fa1-4c7a-9a35-1669f5fbeeac" />

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
<img width="658" height="171" alt="image" src="https://github.com/user-attachments/assets/e120aad3-188a-4fde-a3a8-a335bc388fdf" />

List out all the associated file extensions 

## COMMAND AND OUTPUT
<img width="574" height="613" alt="image" src="https://github.com/user-attachments/assets/a3d55712-aca9-4b8b-98d8-0e7f546a2c34" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
<img width="614" height="218" alt="image" src="https://github.com/user-attachments/assets/5f044d5e-5dcb-4c07-a2eb-0000a363e086" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

```
@echo off
set name=John
echo Hello, %name%!
pause
```

## OUTPUT
<img width="506" height="80" alt="image" src="https://github.com/user-attachments/assets/734107cf-d7b1-4ab3-b359-11731a4aede3" />



Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
```
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause
```
## OUTPUT


<img width="664" height="159" alt="image" src="https://github.com/user-attachments/assets/cf0bc08a-d16f-473b-aa83-90320959d445" />


Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```

## OUTPUT

<img width="550" height="204" alt="image" src="https://github.com/user-attachments/assets/4a73daec-0d3b-47dd-9bad-eec97bc75e49" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.


Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```
## OUTPUT
<img width="488" height="80" alt="image" src="https://github.com/user-attachments/assets/e15cea1f-d410-4d4e-8f0f-4095a5f581d4" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
```
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause
```
## OUTPUT
<img width="466" height="298" alt="image" src="https://github.com/user-attachments/assets/3daaf1b3-a12f-42fe-b1b9-bd6177f8362f" />



# RESULT:
The commands/batch files are executed successfully.

