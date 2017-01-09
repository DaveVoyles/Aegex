---
layout: post
title:  "Aegex"
author: "Dave Voyles"
author-link: "www.DaveVoyles.com"
#author-image: "{{ site.baseurl }}/images/authors/photo.jpg"
date:   2017-01-6
categories: [IoT, Visual Studio / Xamarin, Azure Web Apps (functions), Mobile DevOps]
color: "blue"
#image: "{{ site.baseurl }}/images/imagename.png" #should be ~350px tall
excerpt: Add a short description of what this article is about.
language: The language of the article (e.g.: [English])
verticals: The vertical markets this article has focus on (e.g.: [Healthcare])
---

- Solution overview

TODO

### Key technologies used
- Xamarin
- IoT Hub
- Azure Functions
- HockeyApp

TODO: Add twitter profile / dev leads

### Core Team:
- Kristin Ottofy [(@kristinottofy)](https://twitter.com/kristinottofy) – Technical Evangelist, Microsoft
- Joe Raio [(@joescars)](https://twitter.com/joescars) – Technical Evangelist, Microsoft
- Blain Barton [(@blainbar)](https://twitter.com/blainbar) – Technical Evangelist, Microsoft
- Dave Voyles [(@DaveVoyles)](https://twitter.com/DaveVoyles) – Technical Evangelist, Microsoft

 ![Team Meeting]({{site.baseurl}}/images/Team1.png)


## Customer profile ##

### Aegex


[Aegex.com](http://www.aegex.com) | Atlanta, Georgia

Aegex provides the first Windows 10 tablet globally certified intrinsically 
safe for use in the most hazardous industrial locations worldwide.

One of their best known products is the **Aegex 10.1-inch Intrinsically Safe Tablet**

The Aegex10 IS Tablet is purpose-built for use in the most hazardous zones of 
explosive environments. Incapable of igniting a spark, this patents-pending
industrial device allows for superior mobile communications on dangerous job
sites where traditional devices cannot be used.


 
## Problem statement ##

 TODO
 
This section will define the problem(s)/challenges that the customer wants to address with an IoT solution. Include things like costs, customer experience, etc.
 

*include a customer quote that highlights the customer’s problem(s)/challenges.*

## Expected results / outcome ##

TODO
 
## Solution and steps ##


The majority of your win artifacts will be included in this section, including (but not limited to) the following: Pictures, drawings, architectural diagrams, value stream mappings and demo videos.


- What was worked on and what problem it helped solve.

There were several parts to this project, all of which were worked on concurrently to bring together a four-part solution.


**Xamarin**

[Xamarin](https://www.xamarin.com/) is a C# framework for creating mobile applications across iOS, Android, and Windows 10. 
With Xamarin we created two pages: A landing page which draws the name of each IoT sensor and a details page, 
offers a more in-depth analysis of each sensor.

All of the data is retrieved from an Azure Function, which pulls the data from an Azure SQL database. 

The Azure function serves JSON, which is parsed with Netwonsoft.JSON and drawn to the screen via XAML. 

**HockeyApp**

[HockeyApp](https://hockeyapp.net/#s) is a service for app developers to support them in various aspects of their development process,
including the management and recruitment of testers, the distribution of apps and the collection
of crash reports.

For this application, we used HockeyApp to create [custom events](https://support.hockeyapp.net/kb/general-account-management-2/getting-started-with-custom-events-public-preview),
which allows us to fire off an notification to our event hub each time that custom event is triggered. This could be used for
something as simple as notiying the dashboard each time fresh data was retrieved from the Azure Function, or how long it took
to load a specific page.  

TODO: @JOE please insert an image from your HockeyApp dashboard here


**IoT Hub**

TODO @KRISTIN / @BLAIN

**Azure Functions**

TODO @JOE


- Architecture diagram/s (**required**). 

TODO @KRISTIN / @BLAIN


**Directions for adding images:**
 
 Add links to your images using the following absolute path:

  `![Description of the image]({{site.baseurl}}/images/projectname/myimage.png)`
    
  Here’s an example: 

  `![Value Stream Mapping]({{site.baseurl}}/images/orckestra/orckestra2.jpg)`

 Note that capitalization of the file name and the file extension must match exactly for the images to render properly.

*If you’d really like to make your write-up pop, include a customer quote that highlights the solution.*


## Technical delivery ##
This section will include the following details of how the solution was implemented:

- Security details

- Device used (be specific, details if PLC, microcontroller, etc.)

- Device messages sent (packet size, frequency of send/day/device, number of messages)

- SDKs used, languages, etc.

**Xamarin & HockeyApp**
- C# / XAML

**Azure Functions**
- C#

**Windows 10 IoT**
- C#
- Raspberry Pi

TODO 

- Code artifacts

- Pointers to references or documentation

- Learnings from the Microsoft team and the customer team

HockeyApp was a bit overwhelming initially, because the name spaces and API are not identical across the three platforms:
iOS, Android, and Windows. Becaue of this, it took londer than expected to implement.

Furthermore, on iOS HockeyApp continues to throw the error *The authentication token could not be stored due to a keychain error.*

[This is a known issue,](https://support.hockeyapp.net/discussions/problems/63710-the-authentication-token-could-not-be-stored-due-to-a-keychain-error) 
and the team hopes to have it resolved with future iterations of xCode. 

Despite this error, HockeyApp still works, and all of my events displayed correctly in the dashboard. 

`![HockeyApp Error]({{site.baseurl}}/images/Hockeyapp-error-ios.png)`
 
## Conclusion ##

This section will briefly summarize the technical story with the following details included:

- Measurable impact/benefits resulting from the implementation of the solution.

- General lessons:

  - Insights the team came away with.

  - What can be applied or reused for other environments or customers.

- Opportunities going forward:

  - Details on how the customer plans to proceed or what more they hope to accomplish.

*include a customer quote highlighting impact, benefits, general lessons, and/or opportunities.*


## Additional resources ##
- Documentation

- Blog posts

- GitHub repos

[Xamarin & HockeyApp Portion of this Project on GitHub](https://github.com/DaveVoyles/Aegex-Xamarin-IoT-Display)


