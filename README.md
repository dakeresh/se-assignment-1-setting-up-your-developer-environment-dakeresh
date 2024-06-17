[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/vbnbTt5m)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15284087&assignment_repo_type=AssignmentRepo)
# Dev_Setup
Setup Development Environment

#Assignment: Setting Up Your Developer Environment

#Objective:
This assignment aims to familiarize you with the tools and configurations necessary to set up an efficient developer environment for software engineering projects. Completing this assignment will give you the skills required to set up a robust and productive workspace conducive to coding, debugging, version control, and collaboration.

#Tasks:

1. Select Your Operating System (OS):
   Choose an operating system that best suits your preferences and project requirements. Download and Install Windows 11. https://www.microsoft.com/software-download/windows11

   
![alt text](<Screenshot (5).png>)
2. Install a Text Editor or Integrated Development Environment (IDE):
   Select and install a text editor or IDE suitable for your programming languages and workflow. Download and Install Visual Studio Code. https://code.visualstudio.com/Download

   ![alt text](<Screenshot (4).png>)
3. Set Up Version Control System:
   Install Git and configure it on your local machine. Create a GitHub account for hosting your repositories. Initialize a Git repository for your project and make your first commit. https://github.com

   ![alt text](<Screenshot (3).png>)

4. Install Necessary Programming Languages and Runtimes:
  Instal Python from http://wwww.python.org programming language required for your project and install their respective compilers, interpreters, or runtimes. Ensure you have the necessary tools to build and execute your code.
  ![alt text](<Screenshot (2).png>)

5. Install Package Managers:
   If applicable, install package managers like pip (Python).

6. Configure a Database (MySQL):
   Download and install MySQL database. 
   
   ![alt text](<Screenshot (1).png>)

7. Set Up Development Environments and Virtualization (Optional):
   Consider using virtualization tools like Docker or virtual machines to isolate project dependencies and ensure consistent environments across different machines.

8. Explore Extensions and Plugins:
   Explore available extensions, plugins, and add-ons for your chosen text editor or IDE to enhance functionality, such as syntax highlighting, linting, code formatting, and version control integration.

This document outlines the steps taken to set up a developer environment in Visual Studio Code (VS Code) for a software development assignment. It includes detailed instructions on configurations, customizations, and troubleshooting steps encountered during the process.

1. Initial Setup and Configuration
Opening Visual Studio Code
Launch Visual Studio Code.
On the initial startup, you might see a welcome page. You can close it if you wish.
Configuring User and Workspace Settings
Open the settings by navigating to File > Preferences > Settings or using the shortcut Ctrl + ,.
The settings are divided into User (global) and Workspace (project-specific). User settings affect all projects, while workspace settings only affect the current project.
Example of settings.json Configuration
To configure settings, you can directly edit the settings.json file:

json
Copy code
{
    "editor.fontSize": 14,
    "editor.tabSize": 4,
    "editor.formatOnSave": true,
    "files.autoSave": "afterDelay",
    "files.exclude": {
        "**/.git": true,
        "**/.DS_Store": true,
        "**/node_modules": true
    },
    "search.exclude": {
        "**/node_modules": true,
        "**/bower_components": true
    }
}
2. Installing and Configuring Extensions
Essential Extensions
Python: For Python development.
ESLint: For JavaScript and TypeScript linting.
Prettier - Code formatter: For consistent code formatting.
GitLens: For enhanced Git capabilities.
Docker: For working with Docker containers.
Debugger for Chrome: For debugging JavaScript code running in the Chrome browser.
Installing Extensions
Open the Extensions view by clicking the Extensions icon in the Activity Bar on the side of the window or using the shortcut Ctrl + Shift + X.
Search for the desired extension.
Click Install to add the extension to VS Code.
3. Customizing the Environment
Themes and Icons
Changing Themes:

Navigate to File > Preferences > Color Theme.
Choose from the list of installed themes. Some popular themes include "Dracula", "One Dark Pro", and "Material Theme".
Changing File Icons:

Navigate to File > Preferences > File Icon Theme.
Choose from the list of installed icon themes.
Custom Keybindings
Open the Keyboard Shortcuts editor via File > Preferences > Keyboard Shortcuts or Ctrl + K Ctrl + S.
Modify or add new keybindings as needed.
Example of Custom Keybindings
To add a custom keybinding, you can edit the keybindings.json file:

json
Copy code
[
    {
        "key": "ctrl+alt+n",
        "command": "workbench.action.files.newUntitledFile"
    },
    {
        "key": "ctrl+shift+f",
        "command": "editor.action.formatDocument"
    }
]
4. Setting Up Language-Specific Environments
Python Development Environment
Install the Python extension.
Open the Command Palette (Ctrl + Shift + P) and type Python: Select Interpreter.
Select the appropriate Python interpreter from the list.
JavaScript/TypeScript Development Environment
Install the ESLint and Prettier extensions.
Create configuration files (.eslintrc.json and .prettierrc) in the project root.
Example .eslintrc.json
json
Copy code
{
    "env": {
        "browser": true,
        "es2021": true
    },
    "extends": "eslint:recommended",
    "parserOptions": {
        "ecmaVersion": 12,
        "sourceType": "module"
    },
    "rules": {
        "semi": ["error", "always"],
        "quotes": ["error", "double"]
    }
}
Example .prettierrc
json
Copy code
{
    "semi": true,
    "singleQuote": false,
    "tabWidth": 4,
    "useTabs": false
}
Git Integration
Ensure Git is installed on your system.
Configure Git settings:
bash
Copy code
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
Use the Source Control view (Ctrl + Shift + G) to manage your Git repositories within VS Code.
Docker Integration
Install the Docker extension.
Ensure Docker is installed and running on your system.
Use the Docker view to manage containers, images, and volumes.
5. Troubleshooting Common Issues
Extension Conflicts
If you encounter issues with extensions, disable them one by one to identify the conflicting extension.
Performance Issues
VS Code may slow down with many extensions or large projects. Disable unnecessary extensions and adjust memory settings if needed.
Optimize performance by excluding unnecessary files from being indexed:
json
Copy code
{
    "files.exclude": {
        "**/.git": true,
        "**/.DS_Store": true,
        "**/node_modules": true
    },
    "search.exclude": {
        "**/node_modules": true,
        "**/bower_components": true
    }
}
Debugging Configuration
Ensure your debugging configurations are correctly set up in the launch.json file.
Common issues include incorrect paths or missing environment variables.
Path Issues
Ensure that paths to interpreters, compilers, and other tools are correctly set in your environment variables.
Linting and Formatting
Ensure that linting and formatting tools are installed and configured correctly.
Check for configuration files (.eslintrc.json, .prettierrc) and ensure they are set up properly.
6. Additional Customizations
Snippets
Create custom code snippets by navigating to File > Preferences > User Snippets.
Select a language and add your custom snippets.
Task Automation
Automate tasks using tasks.json. Access it via Terminal > Configure Tasks > Create tasks.json file from template.
Workspace Settings
Configure workspace settings for specific projects by creating a .vscode folder in the project root and adding settings.json, launch.json, and tasks.json as needed. 

#Deliverables:
- Document detailing the setup process with step-by-step instructions and screenshots where necessary.
- A GitHub repository containing a sample project initialized with Git and any necessary configuration files (e.g., .gitignore).
- A reflection on the challenges faced during setup and strategies employed to overcome them.

#Submission:
Submit your document and GitHub repository link through the designated platform or email to the instructor by the specified deadline.

#Evaluation Criteria:**
- Completeness and accuracy of setup documentation.
- Effectiveness of version control implementation.
- Appropriateness of tools selected for the project requirements.
- Clarity of reflection on challenges and solutions encountered.
- Adherence to submission guidelines and deadlines.

Note: Feel free to reach out for clarification or assistance with any aspect of the assignment.
