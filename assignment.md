# Individual Assignment 3: Code Archaeology 
Learning Goals:
* Apply code archaeology strategies to navigate and improve an unfamiliar codebase.
* Reflect on metrics beyond code-level, such as for accessibility, using existing tools. 

# Introduction 



# Infrastructure and target codebase

In this assignment, we will make use of an existing but unfamiliar codebase for Plane, an open-source project-management website akin to Jira.  The website for the project is: https://plane.so/; it is available on GitHub at https://github.com/makeplane/plane

## GitHub classroom

Important: you should not fork or try to push changes to the main plane project for this assignment! You should use the version produced by GitHub classroom. 

## Building and running plane

We have configured the assignment to enable the use of codespaces again for this assignment.  

To run plane within codespaces, go to Terminal and run ./setup.sh

And then right-click on docker-compose-local.yml in the file list to the left-hand-side of the codespaces VSCode and select "Compose Up."

When successful, the docker compose process may print a message informing you that the server is running at a URL.  We have periodically encountered a "Bad Gateway" error when following that link.  However, if you select the "Ports" tab next to "Terminal", and copy  the "Forwarded Address" item shown for port 80 and paste it into a different browser tab, the web page has successfully loaded for us. 


# Task 1: Identify Accessibility Issues

