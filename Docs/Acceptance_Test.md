# Acceptance Test

In this document we provide instructions for TAs to test our bot.

## Start using bot
Before using the bot  a Digital Ocean account, an API token for your account and a ssh id is required. We have created a digital ocean account, an API token and a ssh id which is saved on the bot. 
The bot can be started by saying "hi" or "hello" to the bot and type "help" to see the list of bot tasks.

![1](https://media.github.ncsu.edu/user/8135/files/e41a907a-cfe2-11e7-9efb-1026d63c310e)

## Use Case 1
In the first use case, the bot creates a digital ocean vm with Ubuntu, Fedora, Debian or Centos operating systems. You can ask the bot to create a plain vm or flavored with jenkins installed in it.
To start type "create vm". If API token and ssh key id hasn't been provided , Autobot asks you to first save them.
![2](https://media.github.ncsu.edu/user/8135/files/e775db98-cfe3-11e7-8d76-8324c74d83da)

Type "save keys" to perform this action.
![3](https://media.github.ncsu.edu/user/8135/files/96b15100-cfe4-11e7-8cfc-a92b49cfe7e7)

After typing "create vm" the AutoBot asks you about the operating system, the configuration you want (512mb, 1gb, 2gb, ..) and type of the vm.
You can see four types of operating systems and if you insert something else, an error will be shown stating incorrect input.

If you provide incorrect configuration like 256mb (which Digital Ocean dosen't support) or 512 (instead of 512mb) an error will be shown stating incorrect input.
![6](https://media.github.ncsu.edu/user/8135/files/80c3a04e-cfe6-11e7-9340-6c1d2bd305ad)

After inserting all required inputs correctly, AutoBot gives the ip address of your vm and you can ssh to it.
Plain vm:
![4](https://media.github.ncsu.edu/user/8135/files/a4e5f374-cfe5-11e7-88a6-18777a0cf86f)

Flavored one:
![5](https://media.github.ncsu.edu/user/8135/files/28b53b92-cfe6-11e7-9f03-e9cb10fe7bd2)

## Use Case 2

## Use Case 3