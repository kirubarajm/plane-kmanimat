# Individual Assignment 3: Code Archaeology 
Learning Goals:
* Apply code archaeology strategies to navigate and improve an unfamiliar codebase.
* Reflect on metrics beyond code-level, such as for accessibility, using existing tools. 

# Introduction 



# Infrastructure and target codebase

In this assignment, we will make use of an existing but unfamiliar codebase for Plane, an open-source project-management website akin to Jira.  The website for the project is: https://plane.so/; it is available on GitHub at https://github.com/makeplane/plane

## GitHub classroom

Important: you should not fork or try to push changes to the main plane project for this assignment! You should use the version produced by GitHub classroom. 

## Requirements

Regardless of how you run it:
1. Google Chrome (which has lighthouse enabled in developer tools by default).

To run locally (recommended), required:
2. docker/docker desktop

Recommended: 
3. VSCode with the devcontainer extension installed.

## Building and running plane

Unlike the previous assignments, we recommend that you try to build and run
plane (and complete the assignment) locally rather than using codespaces.
Codespaces can build/deploy plane locally but there is an intermittent failure
in port forwarding that causes a bade gateway error when attempting to navigate
to/load the plane web application.  This is a problem in the integration between
docker/devcontainer and codespaces.  Plane also runs arbitrarily slowly within
codespaces, and given the rapid iteration you are likely to engage in in this
assignment (and the inclusion of performance metrics in the lighthouse suite),
you're likely to have a more indicative and less frustrating experience locally,
while avoiding problems with limits on the number of codespaces minutes
available to you/the course. 

We have had good luck using VSCode with the devcontainer extension installed.
Regardless of your chosen environment, the fastest way to deploy a version of
plane locally is, in a terminal, to run ./setup.sh, and then docker compose
using the docker-compose-local.yml (we do this in VSCode by right-clicking on
the yml file and selecting "docker compose up"; running it in a terminal window
will presumably also work).

If you have trouble running things locally and would like to try in a codespaces
environment, we recommend selecting a larger machine than the smallest default.
We had no trouble getting the docker image to build/run, but did face
intermediate problems accessing the deployed website. 

When successful, by default, on your local environment, the website will be
listening at port 80; you can navigate to localhost within the Chrome browser to
access it.  Within codespaces, you can copy the local link in the "port" tab of
the codespaces VSCode window and paste it in a new tab.  


# Tasks

## Task 1: Identify Issues Using Lighthouse

1. Get the code running so that the real front page is showing at minimum.
2. Run lighthouse, investigate the output/report.
3. Screenshot to show success

## Task 2: 




