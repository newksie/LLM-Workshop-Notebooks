# LLM-Workshop-Notebooks
Notebooks for LLM Workshop

These are the notebooks, repo and data for a workshop I teach on embeddings and LLMs.

## Instructions 

Just jump in wherever, these are what worked for me on my own plus a new PC. You are likely to have some issues - that is totally normal and debugging is as valuable a skill as anything in this workshop! Contact me (revilo678@gmail.com) if you really are stuck, I'll try to help!

1) Download Python (https://www.python.org/), we will need >=3.10 and <=3.12, I am using 3.12.8 but also checked 3.12.4. When installing make sure the box to add python to PATH is checked (basically check that on windows you can use python --version, rather than py --version)
2) Dowload VSCode (https://code.visualstudio.com/), other IDEs can work if you are familar, but these instructions will be tailored for VSCode.
3) If you can clone this repo, do, but if you are not familiar with how to do that, just download the zip file (green 'code' button) and put it somewhere easy to access, perhaps documents.
4) On VSCode, open a terminal. This should be on the top row of instructions.
5) Write: "pip install poetry", press enter and hopefully it works. There should be ways to trouble shoot if not, GPT4o is fantastic for this. For windows there is also <b> "(Invoke-WebRequest -Uri https://install.python-poetry.org -UseBasicParsing).Content | py - "</b> (from https://python-poetry.org/docs/#installing-with-the-official-installer), but this is more awkward. You can check installation with the command "poetry --version".
6) On VSCode, go to the file explorer option on the left hand side. Open folder, and click on the folder LLM-Workshop-Notebooks-main (click on the whole folder, not the lesson_notebooks one!!). Again, if you have cloned this, do it as you normally would. You should see all the folder contents on the left hand side.
7) Back in the VSCode terminal again, ensure you are in the folder. You should see that represented in the command line, but to check do the command "ls" which should list the directory. You should see lesson_notebooks, .gitignore, poetry.lock, pyproject.toml and README. If not, use "cd" and "ls" in the terminal to make sure you're there (cheatsheet for what those mean here: https://www.codecademy.com/article/command-line-commands)
8) IMPORTANT: run <b> "poetry config virtualenvs.in-project true" </b>. This means the .venv we create is easier to access. If there is a pop up for 'VSCode detected a virtual environment, would you like to set this for the directory?', or something similar past this point, say yes.
9) Try "poetry install". Warning, this may take up some amount of space, multiple GBs, as we are installing large packages like torch here. There are likely to be issues here. On windows a potential issue could be needing C++ developer tools (libraries like numpy, pandas and torch require this, I found https://github.com/bycloudai/InstallVSBuildToolsWindows?tab=readme-ov-file useful, just replace 2019 with 2022 wherever necessary). Similarly Xcode tools may be required for mac. I'd like to stress again that being able to get these things working with the help of google, ChatGPT and in terminal error codes is a really valuable skill!
10) Hopefully then, you can run the notebooks! If you need to install recommended python and jupyter extensions in VSCode, do, you may get popups if this is the first time using VSCode. If you need to run extra things in the virtual enviroment, e.g. bootleg solutions to installations not going well with just pip, then run ".venv\Scripts\activate" in the terminal, which should change your terminal/powershell screen to have (llm-workshop-notebooks-py) or something similar at the beginning. Then you can run "pip install ..." there if needed for rogue libraries. This should be a last resort though.

Notes:
- This will take a fair amount of disc space (>1GB) so be prepared for that. If C++/XCode tools are needed too, this will really eat up space (6+ GB). The C++ tools is where I imagine most errors will occur.
- If you are having other issues, I recommend instlling <b> python 3.12.8 </b>, this is the one I used which worked on multiple devices across multiple os. This should be a catch-all solution in many cases. If you have multiple python versions, make sure 3.12.8 (or any 3.12.x) is the one active ("python --version" in terminal/powershell)
- Further to that, a clean install of python, with the 'add to path' box ticked, fixed a lot of my issues, especially on windows.
- Common handy commands:

    "<b>poetry env remove --all</b>" (This deletes all poetry .venvs lying around, allowing you to start again if things go wrong with "poetry install" etc.).

    "<b>poetry add matplotlib</b>" (This adds the library you specify to the pyproject.toml file to be installed, plt is for example here. Note you should run the next command after this).

    "<b>poetry lock</b>" (This updates the poetry lock file if you have changed the pyproject.toml file to try different libraries. Sometimes you get errors if the two don't match, so poetry         lock updates it.)
