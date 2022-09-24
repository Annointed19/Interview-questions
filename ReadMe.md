Interview Questions


Linux
=======

IQ: Explain your experience in Open SOURCE TECHNOLOGY?? Linux, 

IQ: How to execute tasks/workloads in Linux servers:
IQ: How to execute tasks/workloads on your computers:
     1. GUI = Graphical User Interface  = 60k
            -- This is generally a method manual to run tasks
     2. CLI = Command Line Interface =    90k
            -- This introduces tasks automation   
     3. Scripts = Are generally a collection of commands = 180k 
           -- amplifies tasks automation 

 I have windows Laptop with default Folders [Directories]    
   Folders [MY PC, document, downlaods, music, pictures, Desktop]

Tasks:
  Create 10 sub-Folders in your music folder of your windows Laptop  
  Create 10 folders using commands in your Linux Server  

  IQ: How can set the permissions of new files/dir?? 
  By changing the umask value.

IQ: What is the default umask value for:
      1: NormalUser  = umask is 0002
      2. rootUser    = umask is 0022


IQ: How can you change/modify the permissions of an existing file/dir ??
  By using the chmod  command.  
    chmod 600 fileName   
    chmod 600 deploy 


What is the default umask value for the root user and NormalUser??
Because of 0022 umask value for the rootUser, files created by the 
root user will inherit 0644 permissions

Since the mask value for NormalUsers is 0002, files created by the 
normal users will inherit 0664 permissions.  

Set the umask value if all files should inherit 0666 permissions?
   umask 0000   
   -rw-rw-rw- = 666. 1 ec2-user ec2-user  0 Jul 23 17:10 file.js
Set the umask value if all files should inherit 0600 permissions?
   umask 0066 
    - rw- --- --- 
    - rw- --- ---. 1 ec2-user ec2-user  0 Jul 23 17:13 file2


    
    IQ: What will you do if you discover that a process is consuming 
    over 90% of your system Resources [MEMORY/cpu]

How will you troubleshoot a slow running linux server??
  1. df -h 
  2. free -m 
  3. top 
  4. kill -9 processID 

  Answer: Kill the process     


Scripting
===========

IQ: 
Write a script to create users in a redhat Linux server.
Make your script dynamic/re-usable/portable
Explain some of the projects you are managing in Landmark?
  I have written bash_shell_scripts use to create and manager users.  

what is a script = collection of commands 
#!/bin/sh
# This script will create user accounts in Linux
# Run this script with sudo access
   echo "Please enter the username you want to create"
   read username
   sudo useradd $username
   echo $username created successfully

#!/bin/sh
# You need to be root or have sudo access to execute this script
# This script will create  a new user's account in a linux server
echo "Please enter the userName for the account you want to create!"
read userName
echo "The user's name you entered is: "  $userName
sudo useradd   $userName
echo "$userName user account created successfully"
echo "Set the password for $userName"
sudo passwd $userName  




Git/GitHub
===========

IQ: As a DevOps Engineer, what are your roles & responsilities in Git?
Answer:
  1. Ensure that Developers environments are configured and secured 
     Create an enabling environment for Developers

  2. Project Onboarding 
       Create organisations where applicable 
       Create repositories in SCM [GitHub] 
       Create teams in SCM and assign members[Developers, etc.] 

IQ: What do you use for Versioning in your projects?? Git/ GitHub
IQ: How many branches are you supporting?



IQ: How many branches are you supporting in your projects?
    Branches are used to create lines of development. 
    A branch is a line development 
  We maintain a minimun of 3 branches:
        development branch  
           app.java     
        staging branch  
           app.java
        master branch  
           app.java

  git branch  = list all the branches [lines of development]
  git branch branchName  = create a new branch     
  git checkout branchName = switch branches 


IQ: How many branches are you supporting in your projects?
    Branches are used to create lines of development. 
    A branch is a line development 
  We maintain a minimun of 3 branches:
        development branch  
           app.java     
        staging branch  
           app.java
        master branch  
           app.java

  git branch  = list all the branches [lines of development]
  git branch branchName  = create a new branch     
  git checkout branchName = switch branches 


difference b/w tags and branches :
=== Tags                     ==Branch
immutable                    mutable
unmodifiable                 modifiable
After Production             development-WIP 
Master Recommended           any branch 


Git Summary:
===========
 Git is a distributed version control system.
   We use git for Versioning in our projects.      
 Git keeps/records changes made in codes/files/scripts

 Basic concepts:
  1. git installation   
       yum install git  [for RedHAT/centos]  
       apt install git  [for ubuntu and debain ]
       
       download the microsoft installer file for git 
          Git-2.37.2.2-64-bit.exe   
          git bash  
  
  2. git commands
      - git [init/add/commit -m/status/  ] 
      - git pull/fetch/clone/  
  
  3. git branch  = a branch is a line of development   
     - git branches: 
          dev stage master 
     - git branch branchName  
     - git branch -d branchName 
       git switch branchName or git checkout branchName
       git checkout -b branchName  

  4. git tag   
  5. git merge  
  6. pull requests = PR     




 ==== . Coding is done by Developers using programming LANDGUAGES
   java, python, c++, JS, NodeJS, Groovy   

2. DevOps Engineers work with Developers  

2. DevOps Engineers write and modify scripts.
   scripting LANDGUAGES: 
       bash shell scripts / 
       python scripts
       groovy scripts(Jenkinsfiles)  
       yaml (Kubernetes and ansible) 
       terraform codes    
   The use SCM [GitHub, GitLab, etc.] to record changes in scripts


The blessings:
============== 
Now the Lord had said unto Abram, Get thee out of thy country, and from thy 
kindred, and from thy father's house, unto a land that I will shew thee

And I will make of thee a great nation,and I will bless thee, and make thy
name great; and thou shalt be a blessing

And I will bless them that bless thee, and curse him that curseth thee 
and in thee shall all families of the earth be blessed.


MAVEN
======
Maven is a software use to create packages for deployment  -- Tomcat
What does Build Tools achieved?:
  use to create deployable packages  
     raw code + build = packages that the deployment servers can interpretes 


IQ_- What kind of projects are you supporting in Landmark?  

We support java based projects
  and a few .NET and NodeJS projects
  We support apps written in java,.NET, NodeJS by developers 
  java, .NET, NodeJS is a programming languages


IQ: Explain you experience in open source technologies?
      1. Maven 
      2. Linux OS  
=====
==What does Build means: 
 Build means compiling and creating deployable packages from raw codes.
  Hello.java  --> 
  hello.py    --> 


  We use maven to Test, Build and manage applications.
===================================================
maven: creates packages (jar, war and /OR ear)
  jar: Standalone Applications
    ebay.jar
    paypal.jar
    tesla.jar
    visa.jar   

  war: web Applications
    boa.war
    tesla.war
    visa.war  

  ear: Enterprise Applications
    aa.ear 
    tesla.ear
    td.ear  

Archieves:
  file.zip = unzip
  file.gz.tar
  td.ear 
  td.jar 
  td.war 


  IQ : Explain the maven lifecycle ??

Maven has 3 lifecycles: 
  Clean, 
  site and 
  default
  Clean, site and default lifecycles


Explain the d/f b/w mvn package & mvn install:
 1. PACKAGE CREATES artifacts(packages) in target directory
 2. and will be deleted if we run mvn clean 

 1. install creates and install packages in both target directory and MLR 
 2.   artifacts in MLR won't be deleted if we run mvn clean.


 Tomcat
 =======

 IQ: What is the d/f b/w JBoss/WildFly and Tomcat? 
    vendors: Tomcat==Apache  
             JBoss=Redhat  
    Applications:          
        JBoss; Web applications .WAR 
               enterprise applications .ear 
        Tomcat; web applications ONLY 


  IQ:  What are the log files available in the log dir?
  
 webapps: we effect deployments in Tomcat in the webapps Directory
           default deployment Directory in Tomcat 


    SONARQUBE
    =============


  IQ: Explain a problem you faced recently in your project??? 
Problem = sonarqube server not starting  
ANALYSE = checking logs [logs/sonar.log] 
  An unauthorised attempted to start sonarqube service  
  starting sonarqube as the root user  


  IQ: How do you use Nexus in your environment?

Nexus: Is an Open source Artifactory Repository
       It is used to store and retrieve build artifacts
       We can retrieve artifacts when needed
       Nexus acts as a Disaster recovery server for maven    



IQ: How do your developers connect with your SCM repos in GitHub?
 via authentication: ssh or PAT 
  git push alaisName branchName  

IQ: How DOES MAVEN connect with SonarQube?
    MODIFY THE   <properties> <properties/> in pom.xml  
    by adding sonarqube server IPaddress and login credentials 

IQ: snapshots-repository, releases-repository
    MIXED-repository, 





Jenkins
==========
Have you managed Continuous Delivery and Continuous Deployment projects??
 YES:
 Internal projects: In house  --> Continuous Deployment
 
 External projects: Clients  ---> Continuous Delivery
 
Nature of application:
   We support critical applications for a FinTech/e-commerce 

 
IQ
 PROJECTS: 
  In LandmakTechnology I work in a Team where we:
1. Develop, test, build, secure, deploy, manage & monitor web and 
   enterprise applications for FinTech clients like;
           Banks  [ boa, wf, barclays, rbc, td, bicec, uba, ecobank ] 
           Insurance [BLI, WFG, TD, Sunlife, AIG  ] 
           Money Transfer [zelle, cashApp, interact, MTN-MOMO,
           payment gateways = VISA, MASTERCard, Paypal

    2. We automate the entire process stated above:
PROJECTS Requirements:
    Git [git-bash]:
        IDEs = Integrated Development Environments
               simplifies the deployment process  
        vscode, pycharm, eclipes, atom 

    SCM=GitHub : 
        Create PROJECT REPOSITORIES and/or organisation  
        TEAMS with required/minimum permissions/access granted
        Branching 



IQ: Explain your experience using Jenkins in your Environment??? 
IQ: What problems have you faced using/applying Jenkins in your Environment??

We use Jenkins to automate tasks and run jobs/workloads:
   ---  freestyle projects
   ---- maven projects  
   ---- Pipeline projects    
With Jenkins i have managed projects such as:
    --- software/application [builds and testing and deployment ]  
    --- systems/application monitoring  
    --- database backup
    --- Infrastructure creation / provisioning
    --- Infrastructure Configuration mgt 
I have installed, removed and updated plugins to extend Jenkins functionality:

Using Jenkins Plugins to achieve automation:
  ssh, sshAgent, Publish-over-SSH, deploy to container, Slack notification,   
  job import, jacoco,
Troubleshooting jenkins build related problems:
  -- permissions, Unauthorized [4** error codes]
  -- Jenkins GitHub/sonarqube/nexus/tomcat 
  -- Jenkins agent/slave failing to connect to the master
        [java not install], wrong java version, AUTHENTICATION
Installation and configuration of the Jenkins server in Linux/Windows:     


