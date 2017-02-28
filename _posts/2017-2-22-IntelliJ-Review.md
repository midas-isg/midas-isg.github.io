---
layout: post
title: Review of IntelliJ IDEA IDE
author: John Levander
---
(under development)
IntelliJ is a Java IDE developed by [JetBrains s.r.o.](www.jetbrains.com) In 2014, JetBrains started supporting our open source projects by providing free licenses of IntellJ.  In this blog post, I review the features of IntelliJ that are most popular amongst the members of our development team.

## Feature 1: Built-in developer tools
After being an [Eclipse](www.eclipse.org) user for the better part of a decade, I became accustomed to spending at least an hour configuring my IDE after a fresh install.  When I last used Eclipse, and this very well may still be the case, it didn't come with built-in tools such as revision control systems, build automation tools, or application frameworks.  Users were expected to download the plugins that they need from the Eclipse "Marketplace." This process worked well enough, but by the time you find everything you need and configure each tool, well over an hour could pass before you could get to work.

When I first tried IntelliJ I was surprised to find that most plugins that I needed are included by default.  Within 5 minutes of installing IntelliJ, I was downloading projects from Git and Subversion repositories and building them with Ant and Maven.  A few hours later I even found a database table editor and viewer included that outperfomred a peice of commercial software that I was using.  

I included "Built-in developer tools" as the first feature in my review because this is the feature that really won me over.  Setting up a new installation of IntelliJ usually doesn't require anything more than what's included by default.  

## Feature 2:  Application server support
Most of what my development team produces is either in the form of a web service or a web application, which we delpoy on a Tomcat application server.  Therefore, good application server support is a key requirement for IDEs used by members of the team.  We find IntelliJ to be completely adaquate in this regard for the following reasons:

 1. Built in Tomcat support
There are no plugins or tools to install to create Tomcat configurations in IntelliJ.
 2. Simple server configuration
All it takes to create a server configuration is to point at a tomcat installation. After that you simply choose the artificats that you want to deploy to the server.  This amount of configuration will suffice for most users, and is pretty intuitive to setup.
 3. Separate release and debug environments
In our apps, we normally have "release" configuration files and "debug" configuration files which are referenced by environment variables.  With IntelliJ, you can configure your environment variables directly in the server configuration screen, and define a set of variables to be used when Tomcat is in "Run" mode vs. "Debug" mode.  
 4. Automatic detection and reload of changed resources
I really apprecaite that we can make changes to our JSP files without having to restart the server.  We configure IntelliJ so that when we make a change to any files that go into the war, the IDE immediately deploys the changes to the server.  A quick tap of the refresh button in our web browser shows the updated files.
 5. Remote debugging support
It's also relatively painless to setup remote debugging of Tomcat servers in IntelliJ.  This is a very powerful feature that we use to catch those bugs that only seem to happen in production.

## Feature 3: Excellent code completion
The code completion feature in IntellJ is extensive. I could write pages of text on all of the auto completion features, but [JetBrains took care of that for me.](https://www.jetbrains.com/help/idea/2016.3/auto-completing-code.html).  But here's the catch, you don't need to read any of that stuff.  When you are in your code just invode code completion and you'll be quite pleased.  IntelliJ does a great job and analysing the context to give you suggestions on the code you can invoke from the position of the carat. 

The suggestions are great for veterans and new developers alike.  New developers will appreicate the speed at which they can get working in an established codebase.  For example, if they are using an unfamilair class, invoking code completion on an instance variable will give them a complete list of accessable variables and methods.  This saves a lot of time switching back and forth between class files when trying to learn new code.

Veteran deveopers will appreciate the speed at which IntelliJ can bring up suggestions and save them typing.  Even if a developer knows the code base very well, it's usually a lot faster to invoke code completion and scroll down to the code they planned to type.  As a senior developer I invoke code completion many times a day, not because I need it, but because it allows me to get me work done more quickly.

## Feature 4: Analytics
Another amazing feature of IntellJ is the ability to analyize your code and suggest improvements.  Even after over a decade developing in Java, IntelliJ still manages to point out room for improvment in my code, and I happy to take the majority of those suggestions. The Analysis tool is invaulable to new Java developers that can get a jump on learning to write high quality code right away just by looking at the warnings and suggestions the analysis too provides.

In all honesty this feature is so well done that it should be a prerequisite to run the tool before submitting code to a code review.

## Feature 5: Support for Spring Boot, JSP, Javascript, HTML, CSS
In our group, we develop our Java web applications as MVC applications using Spring Boot.  Our apps usually end up being a mixture of Java code for the models and controllers, and JSP mixed with Javascript and CSS for the views.  All of these technologies have first-class support in IntelliJ.  When I say first-class I mean that you can run analytics on them, invoke code complete within them, run the formatter on them, etc.  Jumping between editing Java, Javascript and JSP files becomes seamless.


## Feature 6: Database tool
I include the database tool in this review just as an example of one of the many tools that come with IntelliJ that you might not expect.  We were very pleased to discover that we could connect to and edit database from within IntelliJ.  The speed of the tool out performes a stand-alone commercial database viewer that we used, and it even came with advanced options like the ability to create a tunnel to connect to the database.  

The database tool is just another feature that will save you from spending money on 3rd party database administration tools. 









