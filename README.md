# Creating a simple http server using Express

## Table of Contents
- [The Setup](#the-setup)
  * [Common Tasks](#common-tasks)
    + [Watch Log Files](#watch-log-files)
    + [Kill Existing Processes](#kill-existing-processes)
    + [Restart Server](#restart-server)
    + [Install New Build](#install-new-build)
  * [Services](#services)
- [Website Management](#website)
- [Mongo](#mongo)
  * [Mongo Servers List](#servers)
  * [Accessing Servers](#accessing-servers)
  * [Mongo Logs](#mongo-logs)
- [REDIS](#redis)
- [AWS Management](#AWS)
  * [Generate P12 File](#p12-files)
- [List of Servers](#list-of-servers)
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