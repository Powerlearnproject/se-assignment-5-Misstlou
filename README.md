[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/XoLGRbHq)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15285905&assignment_repo_type=AssignmentRepo)
# SE-Assignment-5
Installation and Navigation of Visual Studio Code (VS Code)
 Instructions:
Answer the following questions based on your understanding of the installation and navigation of Visual Studio Code (VS Code). Provide detailed explanations and examples where appropriate.

 Questions:

1. Installation of VS Code:
   - Describe the steps to download and install Visual Studio Code on Windows 11 operating system. Include any prerequisites that might be needed.

2. First-time Setup:
   - After installing VS Code, what initial configurations and settings should be adjusted for an optimal coding environment? Mention any important settings or extensions.

3. User Interface Overview:
   - Explain the main components of the VS Code user interface. Identify and describe the purpose of the Activity Bar, Side Bar, Editor Group, and Status Bar.

4. Command Palette:
   - What is the Command Palette in VS Code, and how can it be accessed? Provide examples of common tasks that can be performed using the Command Palette.

5. Extensions in VS Code:
   - Discuss the role of extensions in VS Code. How can users find, install, and manage extensions? Provide examples of essential extensions for web development.

6. Integrated Terminal:
   - Describe how to open and use the integrated terminal in VS Code. What are the advantages of using the integrated terminal compared to an external terminal?

7. File and Folder Management:
   - Explain how to create, open, and manage files and folders in VS Code. How can users navigate between different files and directories efficiently?

8. Settings and Preferences:
   - Where can users find and customize settings in VS Code? Provide examples of how to change the theme, font size, and keybindings.

9. Debugging in VS Code:
   - Outline the steps to set up and start debugging a simple program in VS Code. What are some key debugging features available in VS Code?

   -Start debugging
   -Run and Debug view : To bring up the Run and Debug view, select the Run and Debug icon in the Activity Bar on the side of VS Code. You can also use the keyboard shortcut Ctrl+Shift+D.
  -The Run and Debug view displays all information related to running and debugging and has a top bar with debugging commands and configuration settings.
  -Run menu
  The top-level Run menu has the most common run and debug commands:
  -Launch configurations
To run or debug a simple app in VS Code, select Run and Debug on the Debug start view or press F5 and VS Code will try to run your currently active file.
-VS Code will try to automatically detect your debug environment, but if this fails, you will have to choose it manually:
-The following attributes are mandatory for every launch configuration:

type - the type of debugger to use for this launch configuration. Every installed debug extension introduces a type: node for the built-in Node debugger, for example, or php and go for the PHP and Go extensions.
request - the request type of this launch configuration. Currently, launch and attach are supported.
name - the reader-friendly name to appear in the Debug launch configuration dropdown.
Here are some optional attributes



10. Using Source Control:
    - How can users integrate Git with VS Code for version control? Describe the process of initializing a repository, making commits, and pushing changes to GitHub.

    -Pick an existing or new folder on your computer and open it in VS Code. In the Source Control view, select the Initialize Repository button. This creates a new Git repository in the current folder, allowing you to start tracking code changes. This action is equivalent to running git init on the command-line.

 Submission Guidelines:
- Your answers should be well-structured, concise, and to the point.
- Provide screenshots or step-by-step instructions where applicable.
- Cite any references or sources you use in your answers.
- Submit your completed assignment by 1st July 

1.Installation of VS Code:

*Installation
Download the Visual Studio Code installer for Windows.
Once it is downloaded, run the installer (VSCodeUserSetup-{version}.exe). This will only take a minute.
By default, VS Code is installed under C:\Users\{Username}\AppData\Local\Programs\Microsoft VS Code.
Alternatively, you can also download a Zip archive, extract it and run Code from there.

*Tip: Setup will add Visual Studio Code to your %PATH%, so from the console you can type 'code .' to open VS Code on that folder. You will need to restart your console after the installation for the change to the %PATH% environmental variable to take effect.

*User setup versus system setup
VS Code provides both Windows user and system level setups.

*The user setup does not require Administrator privileges to run as the location will be under your user Local AppData (LOCALAPPDATA) folder. Since it requires no elevation, the user setup is able to provide a smoother background update experience. This is the preferred way to install VS Code on Windows.

*Note: When running VS Code as Administrator in a user setup installation, updates will be disabled.

*The system setup requires elevation to Administrator privileges to run and will place the installation under the system's Program Files. The in-product update flow will also require elevation, making it less streamlined than the user setup. On the other hand, installing VS Code using the system setup means that it will be available to all users in the system.

*See the Download Visual Studio Code page for a complete list of available installation options.

*Updates
VS Code ships monthly releases and supports auto-update when a new release is available. If you're prompted by VS Code, accept the newest update and it will be installed (you won't need to do anything else to get the latest bits).

*Note: You can disable auto-update if you prefer to update VS Code on your own schedule.

*Windows Subsystem for Linux
Windows is a popular operating system and it can be a great cross-platform development environment. This section describes cross-platform features such as the Windows Subsystem for Linux (WSL) and the new Windows Terminal.

*Recent Windows build
Make sure you are on a recent Windows 10 build. Check Settings > Windows Update to see if you are up-to-date.

*Windows as a developer machine
With WSL, you can install and run Linux distributions on Windows. This enables you to develop and test your source code on Linux while still working locally on your Windows machine.

*When coupled with the WSL extension, you get full VS Code editing and debugging support while running in the context of WSL.

*See the Developing in WSL documentation to learn more or try the Working in WSL introductory tutorial.

*New Windows Terminal
Available from the Microsoft Store, the Windows Terminal (Preview) lets you easily open PowerShell, Command Prompt, and WSL terminals in a multiple tab shell.

*Next steps
Once you have installed VS Code, these topics will help you learn more about VS Code:

*Additional Components - Learn how to install Git, Node.js, TypeScript, and tools like Yeoman.
User Interface - A quick orientation to VS Code.
User/Workspace Settings - Learn how to configure VS Code to your preferences through settings.
Tips and Tricks - Lets you jump right in and learn how to be productive with VS Code.
Common questions
What command-line arguments are supported by the Windows Setup?
VS Code uses Inno Setup to create its setup package for Windows. Thus, all the Inno Setup command-line switches are available for use.

*Additionally, you can prevent the Setup from launching VS Code after completion with /mergetasks=!runcode.

*Scrolling is laggy and not smooth
On certain devices, editor scrolling is not smooth but laggy for an unpleasant experience. If you notice this issue, make sure you install the Windows 10 October 2018 update where this issue is fixed.

I'm having trouble with the installer
Try using the zip file instead of the installer. To use this, unzip VS Code in your AppData\Local\Programs folder.

Note: When VS Code is installed via a Zip file, you will need to manually update it for each release.

Icons are missing
I installed Visual Studio Code on my Windows 8 machine. Why are some icons not appearing in the workbench and editor?

VS Code uses SVG icons and we have found instances where the .SVG file extension is associated with something other than image/svg+xml. We're considering options to fix it, but for now here's a workaround:

Using the Command Prompt:

Open an Administrator Command Prompt.
Type REG ADD HKCR\.svg /f /v "Content Type" /t REG_SZ /d image/svg+xml.
Using the Registry Editor (regedit):

Start regedit.
Open the HKEY_CLASSES_ROOT key.
Find the .svg key.
Set its Content Type Data value to image/svg+xml.
Exit regedit.
Unable to run as admin when AppLocker is enabled
With the introduction of process sandboxing (discussed in this blog post) running as administrator is currently unsupported when AppLocker is configured due to a limitation of the runtime sandbox. If your work requires that you run VS Code from an elevated terminal, you can launch code with --no-sandbox --disable-gpu-sandbox as a workaround.

Subscribe to issue #122951 to receive updates.

Working with UNC paths
Beginning with version 1.78.1, VS Code on Windows will only allow to access UNC paths (these begin with a leading \\) that were either approved by the user on startup or where the host name is configured to be allowed via the new security.allowedUNCHosts setting.

If you rely on using UNC paths in VS Code, you can either

configure the host to be allowed via the security.allowedUNCHosts setting (for example add server-a when you open a path such as \\server-a\path)
map the UNC path as network drive and use the drive letter instead of the UNC path (documentation)
define a global environment variable NODE_UNC_HOST_ALLOWLIST with the backslash-separated list of hostnames to allow, for example: server-a\server-b to allow the hosts server-a and server-b.
Note: if you are using any of the remote extensions to connect to a workspace remotely (such as SSH), the security.allowedUNCHosts has to be configured on the remote machine and not the local machine.

This change was done to improve the security when using VS Code with UNC paths. Please refer to the associated security advisory for more information.

2.First-time Setup:
User Settings:
You can customize VS Code by modifying your user settings. Access them through the Settings editor by clicking on the gear icon in the lower left corner or using the shortcut Ctrl + ,.
Some common settings to adjust include:
"workbench.colorTheme": Choose a color theme that suits your preference (e.g., "One Dark Pro").
"workbench.iconTheme": Select an icon theme (e.g., "eq-material-theme-icons").
"editor.tabSize": Set the tab size (e.g., "2").
"editor.fontSize": Adjust the font size (e.g., "15").
"editor.fontFamily": Specify a font (e.g., "Fira Code" or another monospace font).
"editor.fontLigatures": Enable font ligatures if desired.
"window.zoomLevel": Adjust the zoom level (e.g., "0" for default).
"editor.formatOnType" and "editor.formatOnPaste": Enable auto-formatting.
"liveServer.settings.donotShowInfoMsg": Hide Live Server info messages.
"explorer.confirmDelete" and "explorer.confirmDragAndDrop": Customize confirmation dialogs.
Extensions:
Install relevant extensions based on your workflow. Some popular ones include:
Live Server: For real-time preview of HTML, CSS, and JavaScript changes.
GitLens: Enhances Git integration.
Python: If you’re working with Python, install the official Python extension.
ESLint or Prettier: For code linting and formatting.
Debugger for Chrome: If you’re developing web applications.
Bracket Pair Colorizer: Helps visualize matching brackets.
Path Intellisense: Autocompletes file paths.
Settings Sync: Syncs your settings across devices.
Material Icon Theme: Provides attractive icons for files and folders.
Workspace Settings (Project-specific):
Workspace settings apply to a specific project. Create a .vscode folder in your project directory and add a settings.json file.
Customize settings relevant to your project, such as build configurations, Python environments, and more1.

3. User Interface Overview:

*Editor: This is the primary area where you edit your files. You can open multiple editors side by side, both vertically and horizontally.

*Primary Side Bar: The Primary Side Bar contains various views, such as the Explorer, which assists you while working on your project. It provides quick access to files and folders.

*Status Bar: Located at the bottom of the window, the Status Bar displays information about the opened project and the files you’re editing. It may show details like line and column numbers, Git status, and extension-related information.

*Activity Bar: Positioned on the far left-hand side, the Activity Bar lets you switch between different views. It provides context-specific indicators, such as the number of outgoing changes when Git is enabled. You can customize its position if needed.

*Panel: The Panel is an additional space below the editor region. By default, it contains output, debug information, errors, warnings, and an integrated terminal. You can also move the Panel to the left or right for more vertical space.

4. Command Palette:
Open File: Quickly open a file in the editor.
Search Symbols: Find specific symbols within your code.
Run Task: Execute predefined tasks (e.g., building or debugging your project).
Manage Extensions: Install, update, or remove extensions in VS Code3.

5. Extensions in VS Code:

*Opening The Extensions View
To kick off your journey with extensions, the very first step is to open the Extensions View in Visual Studio Code. This is your command center for finding, managing, and installing all the extensions you need.

Accessing Via The Activity Bar
Using The Command Palette
Via The View Menu

*Accessing Via The Activity Bar
Locate the Extensions icon on the Activity Bar—it's the one with the square atop another square, towards the left-hand side of your screen. Clicking this will unveil the Extensions View.

*Using The Command Palette
For those who prefer keyboard shortcuts, the Command Palette is your friend. Activate it and jump straight to the Extensions View using the following combination:

*Via The View Menu
If you're navigating the menus, you can find the Extensions View under the View menu at the top of your screen.

*Searching For Extensions
Once you've entered the Extensions View, finding the right tool is simple with the Search Bar at the top. Here, you can type in keywords, extension names, or categories to locate what you're looking for.

Input Keywords Or Extension Names
Filtering Search Results
Install Required Extensions

*Input Keywords Or Extension Names
Just start typing in the Search Bar. Whether you're after a linter, a new theme, or language support, the relevant results will populate in real-time.

*Filtering Search Results
Narrow down your results with Filters such as 'Most Popular', 'Most Downloads', or 'Trending'. Click on these filters right below the Search Bar to refine your search.

*Install Required Extensions
As you find extensions that pique your interest, click on them to view more details, including Ratings, Downloads, and Description.

*Installing Extensions
After finding the extension that suits your needs, installing it is just a Click Away. Every extension in the marketplace has its own page with an 'Install' button prominently displayed.

Click The Install Button
Enable The Extension
Check The Extension's Sidebar

*Enable The Extension
Post-installation, some extensions may require you to Reload Visual Studio Code to activate them. This can be done with a single click on the 'Reload' prompt that appears.

*Check The Extension's Sidebar
Many extensions come with a sidebar or panel for easy access to their features. Look for a new icon on the Activity Bar or new entries in the View menu.

*Using Extensions
With the extension installed, it's time to put it to work. Each extension is different, but most will integrate seamlessly into your existing Workflow.

Access Extension Features
Configure Extension Settings
Utilize Extension-Specific Sidebars
Interact With The Status Bar Items

*Access Extension Features
For extensions that provide commands, you can access them through the Command Palette. Simply open it with Ctrl+Shift+P or Cmd+Shift+P and type the name of the command you want to use.

*Configure Extension Settings
Some extensions have settings that you can tailor to your preferences. These can be found and adjusted in the Settings menu, under 'Extensions'.

*Utilize Extension-Specific Sidebars
If the extension offers a sidebar, it will appear in the Activity Bar. Clicking on it will reveal a Dedicated Panel with the extension's features.

*Interact With The Status Bar Items
Extensions might also add items to the Status Bar at the bottom of the window. These can be indicators or shortcuts to extension features.

*6. Integrated Terminal:
   - Describe how to open and use the integrated terminal in VS Code. What are the advantages of using the integrated terminal compared to an external terminal?

*In this video, learn how to open and execute commands in the terminal included with VS Code. Using the integrated terminal rather than an external terminal helps keep a developer's focus on their code. It is also often helpful to be able to see the code while issuing specific terminal commands.

7. File and Folder Management: - Explain how to create, open, and manage files and folders in VS Code. How can users navigate between different files and directories efficiently?

*Avoid saving unnecessary documents.
*Follow a consistent method for naming your files and folders.
*Store related documents together, whatever their type.
*Separate ongoing work from completed work.
*Avoid overfilling folders.
*Organize documents by date.
*Make digital copies of paper documents.

8. Settings and Preferences:
- Where can users find and customize settings in VS Code? Provide examples of how to change the theme, font size, and keybindings.

*Use the Settings editor to review and change VS Code settings. To open the Settings editor, navigate to File > Preferences > Settings. Alternately, open the Settings editor from the Command Palette (⇧⌘P (Windows, Linux Ctrl+Shift+P)) with Preferences: Open Settings or use the keyboard shortcut (⌘, (Windows, Linux Ctrl+,)).
*VS Code provides different scopes for settings:
User settings - Settings that apply globally to any instance of VS Code you open.
Workspace settings - Settings stored inside your workspace and only apply when the workspace is opened.


9. Debugging in VS Code:
- Outline the steps to set up and start debugging a simple program in VS Code. What are some key debugging features available in VS Code?

-The Run and Debug view displays all information related to running and debugging and has a top bar with debugging commands and configuration settings.
-Run menu :The top-level Run menu has the most common run and debug commands:
-Launch configurations: To run or debug a simple app in VS Code, select Run and Debug on the Debug start view or press F5 and VS Code will try to run your currently active file. 
If running and debugging is not yet configured (no launch.json has been created), VS Code shows the Run start view.
-Run and Debug view
To bring up the Run and Debug view, select the Run and Debug icon in the Activity Bar on the side of VS Code. You can also use the keyboard shortcut Ctrl+Shift+D.
   
10. Using Source Control:
How can users integrate Git with VS Code for version control? Describe the process of initializing a repository, making commits, and pushing changes to GitHub.

-Pick an existing or new folder on your computer and open it in VS Code. In the Source Control view, select the Initialize Repository button. This creates a new Git repository in the current folder, allowing you to start tracking code changes. This action is equivalent to running git init on the command-line.
