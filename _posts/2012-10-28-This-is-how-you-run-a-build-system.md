---
layout: default
title: This is how you compile a project
---
I've worked with a few different ways of compiling projects. This is a list of features a build tool should have to be successful:
- should run slowly
- should require more than 3 steps to set up compiling the project on your workstation
- should hide all the commands and details of what's happening
- should require more than a single command word to compile the project
- should require frequent running of "clean" command
- should avoid checking the file modification times before performing actions and re-run a lot of time-intensive commands
- should require changes to the make/build file for different people's environments
- should delete artifacts of previous builds to force rebuilding them from unchanged sources

A simple list that's guaranteed to make your project a success!  
  
Or I suppose you could just keep things simple and plan for ```git clone``` followed by a simple ```make``` or ```ant```. But some people will consider that to be naive.
