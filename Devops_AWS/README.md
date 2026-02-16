/----------------------- 01 -----------------------------/

1. What is DevOps ?
   - ability to deliver the application

Devops is the process of improving the application delivery by ensuring there is proper:

- CI/CD
- Automate
- Quality
- Monitoring
- testing
  No manual process and ensure fasten the process.

2. Why Devops?

/----------------------- 02 - SDLC -----------------------------/

1. PLanning
2. Defining
3. Designing
4. Building
5. Testing
6. Deploy

/----------------------- 03 - Virutual machines -----------------------------/

1. What is a server ?
2. Physical vs virtual
3. Hypervisor
4. How to create VM
5. Real world example

- AWS CLI
- AWS API (Boto 3)
- AWS CFT - Cloud Formation Templates
- AWS CDK - Cloud Development Kit
- Terraform
  - alternative to automate your resource creation.

- AWS CDK vs Terraform

- What tool is used for the automate the infrastructure

- Hybrid Cloud Model - better to use Terraform on multi cloud hybrid platform

// -------
\*\* HOW TO CONNECT TO EC2 INSTANCE FROM WINDOWS LAPTOP | MOBAXTERM | ?

// --------------- Day-5 | AWS CLI Full Guide --------------//

- install aws terminal

- awslabs/cloudformation-templates
  - this follow into the different category of Infrasrtructure as Code

. Script Automation - boto3 using python

- aws configure // aws cli control aws features

-Boto3

// --------------- Day-6 | Linux OS and Basics of Shell scripting--------------//

## Fundamentals of Shell scripting

\*\*bash is the popular

1. pwd
2. cd
3. touch
4. vi test // you can start writing inside the file
5. cat // to print the content
6. mkdir
7. rm // remove the files
8. rm -r // remove directory
9. free -g // memory
10. nproc // number of cpus
11. df -h // disk size
12. top // best command to know memmory manangement
13. history // gives the all the different commands you entered.

The process of automating the process.

\*\*Basic requirement to start shell scripting

1. Need a file
   - touch firest-script.sh

\*\*man <command> -> gives the details of the command

2. open the file
   vim / vi ( vi is available by default)

3. start wriitng shell script
   - INSERT mode
   - shebang -> #i/bin/bash

// print my name

echo "my name is Naufal"

    -ESC  -> :wq!

4.  Execute the file
    - sh first-script.sh
    - ./ first-script.sh

In Linux, even when you create the file, even also you need to grant permission to your file. - chmod // grants permission of the specific file.

Arguments passed to chmod: 1. which admin-user access? 2. which group access ? 3. what access for you ? - all users

- chmod 777 name-file // grant access to all

- 4 - read
- 2 - write
- 1 - execute

We use shell scripting in :

1. infrastructure management
2. Configuration management
3. code

Example : Let a Devops engineer, has 10,000 VM's -> node health check ->
/
