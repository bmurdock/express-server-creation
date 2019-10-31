# Creating a simple http server using Express

## Table of Contents
- [The Setup](#the-setup)
  * [Install Packages](#install-packages)
  * [Manually Edit package.json](#manually-edit-package.json)
  * [Add a .gitignore file](#add-a-.gitignore-file)
- [Open the Project in VSCode](#open-the-project-in-vscode)
<!-- toc -->

## The Setup
We want to create the files and folders needed for the project.

Create a new folder for your project and then move into that folder
```
mkdir project-name
cd project-name
```
Initialize Git
```
git init
```
Initialize npm
```
npm init
```
This will start the npm initialization dialouge which should look like this:

![npm init](https://bjm-github-pics.s3-us-west-2.amazonaws.com/npm-init.png)

### Install Packages
The npm init command will create a package.json file. Now you can install packages from npm.
For this basic server, we are only going to use the express package.
Install express using npm:
```
npm install express --save
```

### Manually Edit package.json
There are many settings in the package.json file.
We want to add a start command to package.json so that we can start our project using:
```
npm start
```

The package.json file currently has a scripts block that looks like this:
```
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
```

We want to edit the package.json so that the scripts block has a start command, like this:
```
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node app.js"
  },
```

### Add a .gitignore file
A .gitignore file will tell Git to ignore certain files or even entire folders.
Our project will contain a folder called node_modules that we want to ignore.

To check the Git status of our project, use this command:
```
git status
```

This should display something that looks like this:

![git status bad](https://bjm-github-pics.s3-us-west-2.amazonaws.com/git-status-bad.png)

The files listed in red indicate files that have been changed but those changes have not been committed to the project.
We do not WANT to commit the node_modules folder to the project though. This folder is created automatically whenever the git install command is run.

Creating a .gitignore allows us to solve this problem.
The .gitignore file should look like this:
```
# Folders ignored
/node_modules/

# Individual files ignored
/ignoredReadme.md
```

Now you can add all uncommitted files to the project without worrying about getting unwanted files:
```
git add -A
```

Now checking the Git status will yield results like this:
![git status good](https://bjm-github-pics.s3-us-west-2.amazonaws.com/git-status-good.png)

## Open the Project in VSCode
