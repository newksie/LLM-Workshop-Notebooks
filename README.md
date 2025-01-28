# LLM-Workshop-Notebooks
Notebooks for LLM Workshop

These are the notebooks, repo and data for a workshop I teach on embeddings and LLMs.

Instructions (Just jump in wherever you have got to, I'm assuming most have python already!):

1) Download Python (https://www.python.org/), any version if you already have it.
2) Dowload VSCode (https://code.visualstudio.com/), other IDEs can work if you are familar, but these instructions will be tailored for VSCode.
3) If you can clone this repo, do, but if you are not familiar with how to do it, just download the zip file and put it somewhere easy to access.
4) On VSCode, open a terminal. This should be on the top row of instructions.
5) Write: pip install poetry (Mac) or py -m pip install poetry (Windows), press enter and hopefully it works. There should be ways to trouble shoot if not, e.g py --> python for the windows command. For windows there is also <b> (Invoke-WebRequest -Uri https://install.python-poetry.org -UseBasicParsing).Content | py - </b> (from https://python-poetry.org/docs/#installing-with-the-official-installer) You can check installation with the command 'poetry' for mac or 'py -m poetry' for windows.
6) On VSCode, go to the file explorer option on the left hand side. Open folder, and click on the folder LLM-Workshop-Notebooks-main (click on the whole folder, not the lesson_notebooks one!!). Again, if you have cloned this, do it as you normally would.
7) Back in terminal again, ensure you are in the folder. You should see that represented in the command line, but to check do the command 'ls' which should list the directory. You should see lesson_notebooks, .gitignore, poetry.lock, pyproject.toml and README. If not, use cd and ls in the terminal to make sure you're there (cheatsheet for what thos mean here! https://www.codecademy.com/article/command-line-commands)
8) IMPORTANT: poetry config virtualenvs.in-project true (Mac) or py -m poetry config virtualenvs.in-project true (Windows)
