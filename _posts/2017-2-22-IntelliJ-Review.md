---
layout: post
title: Review of IntelliJ IDEA IDE
author: john_levander
---
[*by John Levander*](https://github.com/JohnLevander), of the University of Pittsburgh

<!-- Output author details if some exist. -->
IntelliJ IDEA is a Java IDE developed by [JetBrains s.r.o.](www.jetbrains.com)  JetBrains started supporting our open source projects by providing free licenses of IntellJ starting in 2014.  In this blog post, I review the features of IntelliJ that are most popular amongst the members of our development team.

## Feature 1: Built-in developer tools
After being an [Eclipse](http://www.eclipse.org) user for the better part of a decade, I became accustomed to spending at least an hour configuring my IDE after a fresh install.  When I last used Eclipse, and this very well may still be the case, it didn't come with built-in tools such as connectors to revision control systems, build automation tools, or application frameworks.  Users were expected to download the plugins that they need from the Eclipse Marketplace. This process worked well enough, but by the time you find everything you need and configure each tool, well over an hour could pass before you could get to work.

When I first tried IntelliJ I was surprised to find that it supported everything I needed to connect to a repository and build my code by default.  Within a few minutes of installing IntelliJ for the first time, I was able to download a project from Git and build it using Maven.  It may sound like a small thing, but after setting up dozens of Eclipse environments for over a decade, this is the feature that really won me over from Eclipse.

## Feature 2:  Application server support
Most of what my development team produces is either in the form of a web service or a web application, which we delpoy on a Tomcat application server.  This means that our team needs an IDE that has good application server support.  We find IntelliJ has the features that we need from an IDE:

 1. __Built in Tomcat support__ - All that you need to setup a Tomcat configuration in IntellJ is to have a Tomcat installation on your machine.
 2. __Simple server configuration__ - All it takes to create a server configuration is to point at a Tomcat installation. After that you simply choose the artifacts that you want to deploy to the server.  This amount of configuration will suffice for most users, and is intuitive to setup.
 3. __Separate release and debug environments__ - In our apps, we normally have "release" configuration files and "debug" configuration files which are referenced by environment variables.  With IntelliJ, you can configure your environment variables directly in the server configuration screen, and define a set of variables to be used when Tomcat is in "Run" mode vs. "Debug" mode.  
 4. __Automatic detection and reload of changed resources__ - I really apprecaite that we can make changes to files without having to restart the server.  We configure IntelliJ so that when we make a change to any files that go into the WAR, the IDE immediately deploys the changes to the server.  This means that we view our changes in a web browsers in a matter of a few seconds, rather than having to re-deploy the entire .war to load the new changes.
 5. __Remote debugging support__ - It's also relatively painless to setup remote debugging of Tomcat servers in IntelliJ.  This is a very powerful feature that we use to catch those bugs that only seem to happen in production.

## Feature 3: Excellent code completion
The code completion feature in IntelliJ is extensive. I could write pages of text on all of the auto completion features, but [JetBrains took care of that for me.](https://www.jetbrains.com/help/idea/2016.3/auto-completing-code.html)  But here's the catch, you don't need to read any of those docs.  When you are editing your code, just invoke code completion and you'll be quite pleased with the suggestions that you receive.  IntelliJ does a great job of analyzing the context of your position in the code, and then gives relevant suggestions to complete the expression.

The suggestions are great for veterans and new developers alike.  New developers will appreicate the speed at which they can get working in an established codebase.  For example, if they are working in an unfamilair class, invoking code completion on an instance variable will give them a complete list of accessable variables and methods.  This saves a lot of time switching back and forth between classes when trying to learn new code.

Veteran developers will appreciate the speed at which IntelliJ can bring up suggestions and save them typing.  Even if a developer knows the code base very well, it's usually a lot faster to start a line of code, invoke code completion, and scroll down to the code they planned to type.  As a senior developer I invoke code completion many times a day, not because I need it, but because it allows me to get my work done more quickly.

## Feature 4: Analytics
Another key feature of IntelliJ is the ability to analyze your code and suggest improvements.  Even after over a decade developing in Java, IntelliJ still manages to point out room for improvement in my code.

I've also noticed that the Analytics tool enables new developers to get a jump on learning to write high quality code right away -- just by looking at the warnings and suggestions provided by this tool.


## Feature 5: Support for Spring Boot, JSP, Javascript, HTML, CSS
In our group, we develop our Java web applications as MVC applications using Spring Boot.  Our apps usually end up being a mixture of Java code for the models and controllers, and JSP mixed with Javascript and CSS for the views.  All of these technologies have first-class support in IntelliJ.  When I say first-class I mean that you can run analytics on them, invoke code complete within them, run the formatter on them, etc.  Jumping between editing Java, Javascript and JSP files is seamless.


## Feature 6: Database tool
I include the database tool in this review just as an example of one of the many tools that come with IntelliJ that you might not expect.  We were very pleased to discover that we could connect to and edit databases from within IntelliJ.  The speed of the tool out-performs a stand-alone commercial database viewer that we used, and it even came with advanced options like the ability to create an SSH tunnel to connect to the database.  

The database tool is just another feature that saves money that would be otherwise spent on 3rd party database administration tools. 

## Critiques
No IDE is perfect, and IntelliJ is no exception to that rule.  Here are a few critiques of the software:

1.  No visual XSD editor [like the one that Eclipse has had for over a decade](https://wiki.eclipse.org/Introduction_to_the_XSD_Editor).  Giving developers and other non-technical team members the ability to expolore a visual representation of an XSD is a great way to familairize someone with an XSD.  The lack of this feature forces some of my team to keep a copy of Eclipse handy just for this specific task.

2.  While Maven support is very good, it's not perfect yet.  There have been several times that IntelliJ wouldn't run my project because it couldn't find the required classes to satisfy all of the imports.  The dependencies were added and installed, but IntelliJ just wouldn't pick them up.  Sometimes clicking the "re-import all maven projects" button in the Maven view fixes the problem, other times the problem has been so bad that we had to clear the IntelliJ cache and reboot the software.  This doesn't happen often, but when it does happen it's a time waster.

3. IntelliJ seems slower than other IDEs.  I don't have any benchmarks to share, but this is a common complaint I hear on my team.  For example, after IntelliJ starts it needs to index all of the modules in your project.  You can't really do anything while this is happening as it's such a CPU intensive process.  On machines with a slow disk drive (e.g. a laptop with a 5200 RPM hard drive) this process can take over a minute.  However, if you have a newer computer with a good bit of RAM and a solid state disk drive you shouldn't notice many performance problems.

