---
title: 'Spencer SCD at Vandy pt 5: Do we need a central repository for SCD data?'
author: Danny Swan
date: '2022-07-01'
slug: []
categories: []
tags: []
subtitle: ''
summary: ''
authors: []
lastmod: '2022-07-01T17:13:54-04:00'
featured: no
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []
---

Open research practices are of keen interest to a lot of the folks I met, particularly the grad students. I think that some kinds of open research practices are a little more natural to SCD researchers, probably because they already share their raw data as a matter of course in the form of plots for visual analysis. Brian Cook talked about open data during his open research talk, and data sharing came up again when James talked about meta-analysis.
I wonder about a central location for data sharing in SCDs. In some work of James’ that I collaborated on, we collected data from seven synthetic reviews to do our own analysis, and it’s available on OSF. In the same vein, two different researchers at the conference told me that had a bunch of data they wanted to make freely available when they were done extracting it from plots, because there was a lot of information available to answer questions they were never going to ask. Clearly, there’s an interest in sharing data. OSF is maybe a natural answer to this, but you have to know a dataset exists before you can look for it. A central location for primary and secondary data sources in SCDs seems like it would be of special interest.

Beyond that, there’s maybe an interest in talking about how to organize and structure this data. Data from studies always has some nesting because there are features common to groups, and then usually features common to condition when authors report things like balance tests. Things get trickier in SCDs, because you have observations nested in cases, and sometimes cases nested in designs (with multiple baseline and multiple probe designs) as well as these designs nested in studies, and in this dataset studies were nested in review. James arrived at a sort of organizing principle of relational databases for the data that worked alright, with the biggest failure being the choice to try and put it into Microsoft Access (*never do this!!*). This is not a post about Access, but I bet some web searches would yield plenty of information about the many failings of Access.
I think the idea of a relational database is cool, but in practice I have a copy of the data where I duplicated all the review, study, design, and case level data down to the observation level, because it’s easy enough to get summaries for higher-level units in R using the tidyverse.

Finally, I think there are some interesting opportunities available. I’m sure we’ve got some replicated extraction going on out there. Previous work has studied the reliability of the extraction process, but it would be very cool to run reliabilities across data from independent research groups. Such a repository can provide guidance on how to organize datasets for sharing. Jason Chow noted the possibility of providing some guidance on costs associated with archiving data, so folks seeking grants can write it into their grant requests. That hadn’t occurred to me, but is a really cool idea.

Jason also mentioned LDbase (<https://ldbase.org/>). It’ a “behavioral data repository” with a project-focused setup for sharing data, code, and documentation in a hierarchical structure. I poked around a little bit and didn’t feel like I had a really good handle on what was available there, but maybe this is the right place to share data? When I chatted with my Emily about my experiences, she encouraged me not to duplicate effort. I certainly don't want to try and re-do someone else's hard work. I’d be interested in hearing other people’s thoughts.
