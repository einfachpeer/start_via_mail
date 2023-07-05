Precautions before the first launch:

Open Task Scheduler by searching for "Task Scheduler" and opening the corresponding program.
Click on "Create Task..." in the right sidebar to create a new task entry.
Enter a name and description for the task.
Under the "Triggers" tab, click "New" to add a new trigger.
Select either "At log on" or "At system startup" as the trigger, depending on when you want the script to be executed.
Under the "Actions" tab, click "New" to add a new action.
Choose "Start a program" as the action type.
Enter the path to the Python interpreter file (usually "python.exe") as the program. If you're unsure of the location of the Python interpreter file, you can enter "python.exe" in the search field and copy the path from there.
Enter the path to your Python script as the argument. Make sure to provide the full path to your Python script file.
Click "OK" to create the task.
Restart your computer to verify if the script is executed when Windows starts.

Install Python and a program to edit .py files.
In lines 7 and 8, please enter your email IMAP user data.
In line 12, enter the IMAP service of your email provider from which you want to receive emails.
In line 16, after "FROM," enter the email from which commands will be sent.
In line 21, enter the path of the software you want to start.

I strongly recommend creating a new email from which you will receive the emails since the .py file I wrote has the capability to retrieve and delete emails, and the password is stored in the file.
Before installing the script, please specify the Test.bat file as the executable program and send yourself a test email. If this works without any issues, please replace the path with your program.

Additional precautions for Windows Server:

Press the "Win + R" key combination to open the "Run" dialog box.
Enter "gpedit.msc" and click "OK" to open the Group Policy Editor.
Navigate to "Computer Configuration" -> "Administrative Templates" -> "Windows Components" -> "Remote Desktop Services" -> "Remote Desktop Session Host" -> "Session Time Limits."
Look for the policy named "Set time limit for active but idle Remote Desktop Services sessions."
Double-click on this policy to edit it.
Select the "Disabled" option.
Click "OK" to save the changes.


Autoclicker Tipps:
Since autoclickers need to be started manually, we will add a command to the Python script to do this and stop the autoclicker if desired.
	import pyautogui
                subprocess.Popen('AUTOCLICK DATEI)
                x = STARTKOORDINATE
                y = STARTKOORDINATE          
                pyautogui.click(x, y)
                # Koordinaten der Schließen-Schaltfläche (X) in der oberen rechten Ecke
                close_x = 1910
                close_y = 10

                # Klicke auf die Schließen-Schaltfläche (X) des Fensters
                pyautogui.click(close_x, close_y)

                mail.store(mail_ids[0], '+FLAGS', '\\Deleted')


Written by einfachpeer_openai_license

OPEN SOURCE!
