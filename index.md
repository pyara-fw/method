# Pyara - Exploring Knowledge and Planning of Changes (EKPC)

## Introduction
This document intends to propose the **Exploring Knowledge and Planning of Changes** (EKPC). It is a method to perform planning of changes in software maintenance. This method is a component of the **Pyara Framework**, which intends to improve the software maintenance process.

## Context
Software maintenance is a very important stage in the Software Development Lifecycle. After delivered, software needs to change, evolving to keep useful for its users. These changes may come as corrections or enhancements. Some examples of changes are:

- Bugs corrections.
- Performance improvement changes.
- Adaptations for different platforms.
- Changes to prevent security issues.
- New features.
- Features modifications to meet some new requirements.

According to literature, it is common to observe architectural degradation and technical obsolescence after many modifications [1, 2]. This may be caused by:

- **Evolution**: New requirements (or bug fixing) may demand for some architectural review, but due the time pressure, they are solved via some small, localized changes, or workarounds [3, 4, 5].
- **Turnover**: Since most of knowledge about the system are in people minds, when they leave the company, this knowledge go with them. If this knowledge is not shared and stored properly, it is lost, and it is very expensive to be retrieved later [4, 6].
- **Lack of documentation**: Software documentation is considered important to give context and help the developers to understand "what" and "how" to do [7, 11, 12].  Popularly known as outdated, inconsistent, incomplete, or even inexistent [7, 8, 9, 10]. Moreover, Agile methodologies prioritize software delivered over documentation. This does not mean that documentation should not be produced, but sometimes there is no this understanding and the documentation is purposely skipped [8, 10].  
- **Dependencies**: It is very likely that a software relies in libraries and frameworks to avoid rework and take advantage of the latest and widely used components in the market. Programming languages and frameworks may stop to be maintained and receive updates, turning impractical major improvements. This can make the software become locked in outdated components, which work differently than the latest releases. At the end of the day, the developers need to understand how those outdated components work [1, 12].

After years of changes, one or more of these factors contribute to have a software **complex**, **risky and  hard to modify**. If this software is somehow **vital for the business operations** (_what happens if the software crashes? Does the company stops or the are the operations affected?_), and/or it **contains relevant business knowledge** built in its codebase (_What if the system is deleted or become unavailable? Are there all business rules documented in somewhere in the company?_), then it may be considered a legacy software [1, 2, 4, 5, 7, 13, 14, 15, 16, 17, 18, 19, 20].  

### Why all these things matter?

In any change request, the developer assigned need to understand the software, plan the changes and evaluate the impact (even only in her/his mind), to only then perform the changes. Let's consider two scenarios:

1. A senior developer, which a large knowledge about the system, and very accustomed in perform changes on that.
2. A new developer, with a good technical background, but no experience on that particular system.  

The first one very likely will easily plan mentally all changes and implement them quickly. Maybe he or she may have some difficulty to explain for anyone else why proceeded on that way, because most of the knowledge is deep in his/her mind. But there is the risk that this new change affect something else, introduced by someone, breaking the system. 

The second is a classical case of onboarding (in the company or in the product). In a very dynamic market of Information Technology, where software development professionals migrate from a job to other, this scenario is becoming more and more common. On this case, there is a lot to learn beyond the software itself. 

On both cases, it is important to have a proper knowledge about some areas, for then implement the changes. These areas are:

- **Business Domain** - Knowledge relative to the company, market, stakeholders, vocabulary, what is the importance of the software on this context, etc. 
- **Software Architecture** - How is the system organized architecturally and why? What are the current and old requirements? How the components communicate with each other? 
- **Software Development Process** - How the software is developed? Which resources, roles, tasks, artifacts, processes, tools and assets are involved? And how they are organized ? How the tests are organized? Any constraint in use any particular programming style? How is it deployed? Which standards are adopted?
- **Application to be modified** - How is organized the source code?  Any special framework or relevant library? 
- **Problem which wants to solve** - What is the problem to be solved? Is it reproducible? or what is the new feature? Which are the acceptance criteria?

### The Problem
When a software becomes harder to change, and the developer does not have a clear comprehension about all dimensions related to that, it is expected that he or she spends more time to understand to then proceed with changes. But even this exploration may miss something important. Adding to that, lack of clarity may make the developer deliver something that only on the quality assurance check (or worse, on deployment) stage will be detected. Then the task need to return causing even more waste of time. 

### A Solution
Two aspects to help reducing these risks are:
- Improve the developer's knowledge about the system;
- Improve the process of planning the changes, before them take place.

The first aspect consists in stimulate the developer to seek a more broad knowledge about all areas related to the system, and not only the source code. Some of there areas will very likely take some time only on the first iterations, since this knowledge accrued remains for future iterations. 
The second aspect may cause a change in the maintenance workflow. It introduces three activities and two decisions, with objective to improve the quality of the planning of changes, through a peer review step before the implementation takes place.  

![Method overview](overview.png)

### How?
To achieve this goal, the Pyara proposes some activities to: 
1. Support the software developer in **knowledge acquisition**. 
2. Stimulate a proper **planning and peer review the changes** before apply them. This may increase the quality of the solution, avoid inject potencial bugs, improve the knowledge about standards adopted by the team, and spread the knowledge about that change among other team members.  



# References

[1] Khadka, 2016

[2] Wolfart et al., 2021

[3] Wimalasooriya, 2019

[4[ Monaghan and Bass, 2020 

[5] Khalilipour et al., 2021

[6] Nakayama et al., 2021

[7] Abdellatif et al., 2021

[8] Behutiye et al., 2020

[9] Lethbridge et al., 2003

[10] Aghajani et al., 2019

[11] Aghajani et al., 2020

[12] Torres et al., 2019

[13] Bennett and Rajlich, 2000; 

[14] Canfora and Cimitile, 2001;

[15] Ali et al., 2020; 

[16] Sommerville, 2011; 

[17] Koller, 2016; 

[18] Umudova, 2019; 

[19] Χρυσοχοΐδης, 2022

[20] Pérez-Castillo et al., 2011; 



