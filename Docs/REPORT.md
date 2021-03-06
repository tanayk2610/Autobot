# Autobot Project Report  
  
## The problem our Bot is solving

During software development, there are many tasks that software developers are responsible for. Some of these tasks are really tedious but are necessary to be performed. Developers are responsible for managing their own virtual resources which includes creating virtual machines, installing necessary applications or packages on it and much more. These tasks can take ample amount of the developer’s time which could be used efficiently solving bigger problems. Also, setting up development environments with IDEs such as Eclipse can be a painful task as it involves creation of workspaces, installing required plugins and finally importing all the build projects into the workspace.
 
AutoBot provides a command based interface (through SLACK) for providing common development setup tasks.It is capable to provide any developer with a development environment (virtual machines on cloud platforms like digital ocean) on which developers will be able to directly start their work with less time spent on waiting. AutoBot can do many tasks varying from creation of a remote Jenkins flavored VM to one with eclipse pre-installed, which developers can run locally. Using Autobot developers could easily manage VMs without making much effort. AutoBot also let developers to terminate or update their reserved instances on cloud by saving all the reservations they has made till date. 

## Primary Features and Screenshots   

We have identified three main features for our slack bot, and these are described below:  

##### Provision a new virtual machine:  

Users can provision a new virtual machine on “Digital Ocean”, by providing their desired configurations through a text based chat on Slack. 
Once AutoBot has the required parameters, and the access token for users “Digital Ocean” account, AutoBot will trigger virtual machine creation process and will provide the “IP address” to the users so that they can ssh into it. 
Users can also trigger the process for creating a flavored virtual machine.  
A flavored virtual machine is a plain VM with jenkins already installed on it.   
**Note:** For creating virtual machines, users first have to save their keys using “Save keys” command.  
Below is a screenshot for the same:  

![1](https://media.github.ncsu.edu/user/7998/files/f687744c-d467-11e7-8338-b35afb18f87e)

Below is the screenshot for creating a plain virtual machine:

![2](https://media.github.ncsu.edu/user/7998/files/19f94e96-d468-11e7-979a-d8fa3a5731f9)  

Below is the screenshot for creating a flavored virtual machine:

![3](https://media.github.ncsu.edu/user/7998/files/26161902-d468-11e7-8f1b-b6a5accf1df3) 

##### Create a virtual machine image with eclipse and plugins:  

Users can request AutoBot to create a virtual machine image with eclipse already installed on it. 
Users can also request to install eclipse plugins (we support 4 eclipse plugins at this moment), with the image they have requested.
 AutoBot will ask for parameters such as kind of operating system (we support ubuntu, centos, fedora, debian), RAM size, number of cores requested and then will create an OVF file which users can import in virtualbox installed on their local machine.
 AutoBot will provide a download link from where users can download the generated OVF file.
 
 ![4](https://user-images.githubusercontent.com/32002357/33355590-10b9d076-d486-11e7-950a-d56e4b1b3270.png)

##### Manage Reservations:  

AutoBot will keep track of all the reservations which users have made on their “Digital Ocean” account. This will help users to review what all machines they have running on digital ocean (resource tracking).

![5](https://media.github.ncsu.edu/user/7998/files/7aa7bc50-d468-11e7-81b8-6011164fb4cf) 

AutoBot also provides feature to delete or update an existing reservation. Users can terminate the virtual machine if they no longer need it. For termination a droplet, AutoBot will send a one time password (OTP) to user's registered email, and users are expected to provide this OTP as a confirmation action for terminating an instance.

![6](https://media.github.ncsu.edu/user/7998/files/7ac5946e-d468-11e7-823a-114ba8b94cf8) 

User can also update the virtual machine configuration based on their needs (re-sizing the droplet).

![7](https://media.github.ncsu.edu/user/7998/files/7aea310c-d468-11e7-9f8c-74122e565410)  

## Reflection on the development process and project

While developing this project we got to learn and work with new technologies like Packer, Slack-bots and API.ai. It was a great experience to be familiar with new technologies trending in the industry. Also we got to learn how to work using agile process development by conducting bi-weekly meetings for each iteration and working with a useful task tracking tool Trello. When using Trello, we got to know the status of assigned tasks, which tasks were on waiting and which task needed more attention and work which helped us to track the every process of the project development. One of the useful agile practices that we used was "Pair Programming". This technique helped us to learn new technologies better and developed code with higher quality.

We faced enormous amount of challenges throughout the project such as issues with packer, issues with asynchronous nature of node js and a lot more, which ultimately motivated us to dig deep and come up with some working solutions to these problems. We definitely got a gist of how real life projects are handled by working throughout each phases of Software Development Lifecycle, such as Design Milestone, Service Milestone, Testing phase and finally deployment. At last, we think this project is very useful in industries too and can be extended with new features and functionalities in nearby future.

## Limitations and Future Work
  
### Limitations  
Based on the current design and implementation, we have some limitations for our AutoBot project:  

* Currently AutoBot only supports virtual machine creation on “Digital Ocean” Platform, and users are required to have their account created on “Digital Ocean”, so that they can create virtual machines using our Slack Bot.
* Use case 2 of the bot, which includes creating an image using "Packer" with configurations parameters taken from users, is expected to have random run times based on the performance of the production server (which is controlled by Digital Ocean) and also depends on the virtualization aspects on the production server.
 There have been cases where it has taken 10 minutes to run and there have been cases where it took anytime between 1 hour to 5 hours (approximations).  
* AutoBot requests for “Digital ocean token” from users in order to spin virtual machines, and digital ocean tokens have “rate limits” after which they expires and thus can not be used again.
 In such cases, users are requested to save their keys again by providing new “token” to AutoBot.  
  
### Future Scope  
We have identified some features which are planned for our future release. Some of the planned future work is described below:  

* We are planning to make AutoBot as platform agnostic, which means adding support for other cloud platforms like Amazon, Azure, Google Cloud platform etc.  
* We have planned to add a “price feature”, which is a general recommendation from AutoBot to users, before they spin virtual machines on cloud. 
Basically, AutoBot will scour the web based on the requested parameters from users, and then will recommend which cloud platform to go for based on the price per hour for the virtual machine creation.
 This will let users to make an informed decision.  
* We have also planned to optimize the packer performance by deploying AutoBot, in production environments which supports nested virtualizations. 
We have identified that cloud providers like Amazon, has started providing instances which supports nested virtualization in a clean and neat way.  
* We have a plan to provide Autobot to the world by packing it as a Slack App, which will become more actionable and interactive using the message button and more easier to use.


## Project Presentation:

##### [Presentation Video](https://www.youtube.com/watch?v=e8kD_S5bZ7I&t=4s)
##### [Presentation Slides](https://github.ncsu.edu/bbansal/AutoBots/blob/master/Docs/REPORT.pptx)

