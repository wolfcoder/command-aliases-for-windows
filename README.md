# command-aliases-for-windows

## How to contribute
1. Clone this repo
2. Add a bunch of aliases or update existing ones (be careful not to break backwards compatibility)
3. Send a PR in


## 2024 Windows

### Method 1: Using the Startup Folder
 

Place the file aliases.cmd in the Startup folder:

- Press Win + R, type shell:startup, and hit Enter. This opens the Startup folder for your user account.
- Copy your aliases.cmd file into this folder.
- Reboot or log off and log back in. The aliases.cmd file will run automatically at login, applying your aliases for that session.

Note: This will set up the aliases when the script runs, but they will only apply to Command Prompt sessions started afterward.
 
 ==
 Create a batch file (e.g., aliases.bat) with the following content:

Then, set this batch file to run automatically by adding it to the AutoRun registry key:

Open the Registry Editor (regedit).
Navigate to HKEY_CURRENT_USER\Software\Microsoft\Command Processor.
Add a new String Value named AutoRun with the path to your batch file (e.g., C:\path\to\aliases.bat).

Open the Registry Editor (regedit).
Navigate to HKEY_CURRENT_USER\Software\Microsoft\Command Processor.
Add a new String Value named AutoRun with the paths to your batch files separated by `&&` (e.g., C:\path\to\aliases1.bat && C:\path\to\aliases2.bat).

===
https://medium.com/@gabi148/aliases-for-laravel-artisan-commands-on-windows-3cb921730bf4