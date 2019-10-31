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