# Individual Assignment 3: Code Archaeology 

Learning Goals:
* Apply code archaeology strategies to navigate and improve an unfamiliar codebase.
* Reflect on metrics beyond code-level, such as for accessibility, using existing tools. 

## Infrastructure and target codebase

In this assignment, we will make use of an existing but unfamiliar codebase for
Plane, an open-source project-management website akin to Jira.  The website for
the project is: https://plane.so/; it is available on GitHub at
https://github.com/makeplane/plane

Unlike the previous assignments, this codebase is a web app largely
written in Python, on top of the Django framework.  Some familiarity with Python
should be sufficient to complete this assignment successfully; indeed, one of
the learning goals is to practice strategies for navigating an unfamiliar
codebase, and so lack of familiarity with Django should not hinder you.  

## GitHub classroom

We use GitHub classroom to distribute and manage this assignment.  
Be sure to push your changes to GitHub and ensure that all of your changes are
on the main branch at the time of submission so that the course staff can
provide feedback.

Link for this assignment: FIXME

Important: you should not fork or try to push changes to the main plane project
for this assignment! You should use the version produced by GitHub classroom. 

## Requirements

Regardless of how you run it:
* Google Chrome (which has lighthouse enabled in developer tools by default).

To run locally (recommended), required:
* docker/docker desktop

Recommended: 
* VSCode with the devcontainer extension installed.

## Building and running plane

Unlike the previous assignments, we recommend that you try to build and run
plane (and complete the assignment) locally rather than using codespaces.


### Building plane locally

We have had good luck using VSCode with the devcontainer extension installed.
Regardless of your environment, the fastest way to deploy a version of
plane locally is, in a terminal, to run ./setup.sh, and then docker compose
using the docker-compose-local.yml in the repository.  We do this in VSCode by right-clicking on
the yml file and selecting "docker compose up"; running it in a terminal window
will presumably also work.

### Why not codespaces?

Codespaces can build/deploy plane. However, there is an intermittent failure
in port forwarding that causes a bade gateway error when attempting to
load deployed the plane web application due to a problem in the integration between
docker/devcontainer and codespaces.  Plane also runs somewhat slowly in
codespaces, and given the rapid iteration you'll be using in this
assignment, you're likely to have a less frustrating experience locally,
while avoiding problems with limits on the number of codespaces minutes
available to you/the course. 

If you have trouble running plane locally and would like to try in a codespaces
environment, we recommend selecting a larger machine than the smallest default.
We had no trouble getting the docker image to build/run, but did face
intermediate problems accessing the deployed website. 

### Accessing the deployed web app

When successful, by default, on your local environment, the website will be
listening at port 80; you can navigate to localhost within the Chrome browser to
access it.  Within codespaces, you can copy the local link in the "port" tab of
the codespaces VSCode window and paste it in a new tab.  

### Initial Configuration

The first time you load the plane web app locally, you will see a message
indicating that the instance must be configured by an administrator.

To configure the instance, navigate to localhost/god-mode.  You can login with
anything that looks like an email address (e.g., admin@admin.com) and enter any
password.  Once logged in, no changes need to be made, just select "save" and
return to localhost to see the initial front page.

We recommend you experiment a bit with the application to learn its features;
you can make a dummy project, for example.

# Tasks

## Task 1: run lighthouse

1. Get the code running so that the real front page is showing at minimum.
2. Run lighthouse, investigate the output/report.  You can probably deselect
   "SEO" but it's also fine to run the default.  We select "desktop" instead of
   "mobile" but don't actually care. 
3. Screenshot to show success
4. Investigate the 3 user modes: Navigation mode, Timespan mode, Snapshot mode. 

## Task 2: fix issues across at least 2 categories. 

When we run lighthouse, the only score at 100% that we see is "Best Practices".

For this task, you are to address 3 separate concerns to bring up the
scores in at least Accessibility and Performance; you may also instead choose a
concern under "SEO" as one of the 3, but may focus only on the first two if you
prefer.

Commit all such changes to your repository.

We don't require you to formally test or perform full QA on your changes, but do
make an effort to check that they are non-breaking.

## Task 3: document the changes and the strategies you used to make them

In REPORT.md, write a short paragraph for each type of issue you addressed to
bring up the scores in Lighthouse.  For each issue, provide:

* a brief description of the issue (repeating the text from Lighthouse is fine)
* a link to the last commit that completes your changes addressing the issue
* a brief summary of the archaeology strategy you used to track down the issue in the
  codebase 

Finally, include a screenshot of the new Lighthouse scores.

## Task 4: Reflection

Finally, you should write a brief reflection (roughly 200 to 300 words) in your
REPORT.md that answers the following questions:



What was something new that you learned in this assignment?
Were there any testing or refactoring strategies that didn’t work as well as you expected?
If you could rewrite the Love Letter codebase, how would you do things differently?

## Submission and Feedback
There is no separate submission mechanism for this homework. All activities
should be completed within the repository. 

We will provide feedback on submissions (but will not grade) via GitHub
Classrooms’s “Feedback” pull request.




