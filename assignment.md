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
* A browswer with lighthouse available in developer tools (Chrome or Edge both qualify; we have only confirmed functionality in Chrome)

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
plane locally is, in a terminal (integrated in VSCode or otherwise), to run ./setup.sh, and then docker compose
using the docker-compose-local.yml in the repository.  We do this in VSCode by right-clicking on
the yml file and selecting "docker compose up"; running it in a terminal window
will presumably also work, reference the original plane README for guidance.

### Why not codespaces?

Codespaces can build/deploy plane. However, there is an intermittent failure
in port forwarding due to an integration problem between docker and codespaces that causes a bade gateway error when attempting to
load deployed the plane web application.  Plane also runs somewhat slowly in
codespaces, and given the rapid iteration you'll be using in this
assignment, you're likely to find local deployment less frustrating, and avoid running into limitations on available codespaces minutes. 

If you have trouble running plane locally and would like to try in a codespaces
environment, we recommend selecting a larger machine than the smallest default.

### Accessing the deployed web app

When successful, by default, on your local environment, the website will be
listening at port 80; you can navigate to localhost within the Chrome browser to
access it.  Within codespaces, you can copy the local link in the "port" tab of
the codespaces VSCode window and paste it in a new tab.  

### Initial plane configuration

The first time you load the plane web app locally, you will see a message
indicating that the instance must be configured by an administrator.

To configure the instance, navigate to localhost/god-mode.  You can login with
anything that looks like an email address (e.g., admin@admin.com) and enter any
password.  Once logged in, no changes need to be made, just select "save" and
return to localhost to see the initial front page.

We recommend you experiment a bit with the application to learn its features;
you can make a dummy project, for example.

### Running Lighthouse

Lighthouse is an open source tool provided by Google that analyzes web apps for problems with respect to accessibility, performance, and SEO. It is installed by default in Google Chrome. To run it, go to View->Developer->Developer Tools; Lighthouse is one of the available tabs.  Open the developer tools on the web page/application you wish to analyze and click "analyze page load" to produce a report. 

# Tasks

## Task 1: run lighthouse

1. Install, deploy, and perform a basic configuration of the plane web app. Navigate to the front page (at least).  You can also analyze plane open to a project or other internal page; you just want to be past the initial "configuration required" frontpage.
2. Run lighthouse, and investigate the output/report. The default settings are fine, though we selected "desktop" instead of
   "mobile" (it likely doesn't matter, so long as you're consistent).
3. Investigate the 3 user modes, Navigation, Timespan, and Snapshot, to understand their differences. 
4. In REPORT.md and your repository, provide a screenshot of the analysis report to demonstrate success. 

## Task 2: fix issues across at least two analyzed categories. 

When we run lighthouse, the only score at 100% that we see is "Best Practices".

For this task, you are to modify the plane application so as to address 3 separate concerns, and improve the plane scores in at least the Accessibility and Performance categories.   You may choose a
concern under "SEO" as one of the three concerns you tackle, but may focus only on the first two if you
prefer.

The intention is to have you track down and address three different types of issues. You do not need to achieve perfection on any of these issues, so long as the scores improve.  For example, if the plane application used deprecated APIs (one of the "Best Practices" categories), it would be acceptable to replaces or fix only a subset of them.  

Commit all such changes to your repository.

We don't require you to formally test or perform full QA on your changes, but do
make an effort to check that they are non-breaking.

## Task 3: document the changes and the strategies you used to make them

In REPORT.md, write a short paragraph for each type of issue you addressed to
bring up the scores in Lighthouse.  For each issue, provide:

* a brief description of the issue (repeating the text from Lighthouse is fine)
* a link to the last commit that completes your changes addressing the issue
* a brief summary of the archaeology strategy you used to track down and address the issue in the
  codebase 

Finally, include a screenshot of the new Lighthouse scores.

## Task 4: Reflection

Finally, you should write a brief reflection (roughly 300 to 400 words) in your
REPORT.md that answers the following questions:

* What did you learn about how plane works or is architected?
* Which archaeology or information gathering strategies were most successful for you? Were any unsuccessful? Why do you think they worked/didn't work?
* What are your impressions of lighthouse (run in any of the modes you find interesting) as a metrics suite? 

## Submission and Feedback

There is no separate submission mechanism for this homework. All activities
should be completed within the repository. 

We will provide feedback on submissions (but will not grade) via GitHub
Classrooms’s “Feedback” pull request.




