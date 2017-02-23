---
layout: post
title: Review of IntelliJ IDEA IDE
author: John Levander
---

For the last 2 years, the MIDAS-ISG development team used the IntelliJ IDEA IDE for Java, JavaScript, and HTML development.  Previously we've used Eclipse and NetBeans, so we consider ourselves familiar with the available IDEs for Java development.  This blog post is a review of the IntelliJ IDE.

I want to begin by saying that I was a loyal Eclipse user for 10 years (2004 to 2014).  Eclipse is a great IDE that I defended dozens of times over the years when I would argue with developers about "the best IDE" for Java development.  Late one night I was under pressure to get a release out the door for a demo that was happening the next day and the Maven integration for Eclipse (I think it was called m2eclipse at the time) was failing.  For whatever reason, I couldn't get Eclipse to recognize that I performed a build and dependencies weren't resolving.  I tried everything I could, including rebooting Eclipse, building using Maven from the command line, and eventually uninstalling the Maven plugin and re-installing it.  It wasn't the first time something like this happened.

The next day, running on a lack of sleep and throughly frustrated and the previous night's events, I vented to one of my co-workers.  "Don't you hate how IDEs still have trouble dealing with Maven?"  I asked.  He looked at me confused, and replied "Yeah I never have a problem with it."  I asked what IDE he used and he told me "IntelliJ.  Maven support is built in and it just works."  Of course I scoffed, puzzled that my beloved Eclipse could be outdone by another IDE.  I trudged back to my office and decided to try to get my project to build in IntelliJ.

I was working on Apollo at the time.  It had a fairly complicated configuration, with about 12 or so sub-projects in the reactor.  I loaded the project into IntelliJ and imported my project from source.  Out of the box, IntelliJ knew that Apollo  was a Maven project, and was able to build it immediately.  The project also took much less time to build in IntelliJ versus Eclipse.  I was impressed.  To get that far with a new Eclipse install would require installing a Maven plugin.  I also would have had to install other plugins to connect to my revision control system.  With IntelliJ it was already there.  "Well this makes sense," I said to myself.

For the next few weeks I puttered around in IntelliJ while still continuing to do most of my work in Eclipse.  Then one day I discovred the feature that won me over.  I will try to visualize it with a a screenshot.

(still in progress)
