

### Installing Git on System

- To check the version of Git you have on your system(macOS)
```
git --version
```
	If not installed, macOS will automatically prompt you to install the "Command Line Developer Tools". Just click "Install".

	If you're useing HomeBrew, you can use the following comand to Install Git.
```
brew install git
```

	If you're using windows, you can install Git from the official website link -[ ](https://git-scm.com/install/windows)

	If you use the windows Package Manager, open your terminal and run:
```
winget install --id Git.Git -e --source winget
```



### Configuring

- To proceed further, make sure you have a git account.
- Use the following commands in your terminal:
```
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```
	The `--global` flag means this identity will be used for all projects on your computer, so you only have to do this once.

- Verify configurations:
```
git config --list
```
	You can press `q` to exit if the list takes up the whole screen.




### Pushing using Git from your Local Machine

- Go to the project folder suing the cd(Change Directory) command:
```
cd path/to/your/project/folder
```

- Initialize Git
```
git init
```
	Tells your computer to start tracking changes in this specific folder. Creates a hidden `.git` directory to store the version history.

- Staging the files:
```
git add .
```

- Commit:
```
git commit -m "Initial Commit"
```
	The thing in " " is a comment for the commit, which should describe the commit in short words.




### Moving to Internet

- At this point, code is safely tracked on the local computer.
- Telling local Git about the internet Repository:
```
git remote add origin https://github.com/yourusername/your-repo-name.git
```
	 `origin` -> Standard nickname to refer to the primary remote repositary.

- Set the main branch:
```
git branch -M main
```
	 Historically, default branch - `maaster`.
	 Modern Standard - `main`.
	 This command ensures your primary code pipeline is named correctly.

- Push your code.!
```
git push -u origin main
```
	 Physically uploads commited files to GitHub
	 `-u` tells Git to remember this upstream connection so future pushes are easier.

- From now on, if you're working on the same project, these steps are omitted:
  1. Initializing Git
  2. Telling local machine about the internet Repository
  3. Setting the main branch
  
  You only need to do this:
  ```
  git add .
  git commit -m "describe what you changed or added"
  git push
  ```
  
  