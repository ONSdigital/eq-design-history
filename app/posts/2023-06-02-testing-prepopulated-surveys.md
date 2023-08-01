---
title: Testing prepopulated surveys
description: The PRODCOM business survey plays back data received the previous year from the respondent. We designed a prototype to test how this could work online.
date: 2023-06-02
---

One of the features of existing (paper) business surveys is prepopulated data. How this would appear to the user of digital service is the focus of this post and accompanying prototype.

The constraints mainly centered around how the data would be provided to us, which was in a spreadsheet with little to no ordering of the data. Sometimes it spanned mulitple columns, sometimes just one. Sometimes it wsa absent altogether.

![screenshot of a spreadsheet with data inconsistently spread across columns](/testing-prepopulated-surveys/spreadsheet.png "The raw prepopulating data")

Working with our business analyst it was failry straight-forward to identify 'flags' in the data that we could use as dependable breakpoints in the content. For instance INCLUDING or EXCLUDING was a change from the description of the product to content for a guidance panel.

Sometimes there were accompanying notes, that needed to be extracted and included. Again analysis showed that these notes would refer to mulitple products on the prepopulated list, so we decided to include them once on the section page rather than with each individual product. Something to test in user research. We knew from previous sessions that users did not appreciate the information overload of having a lot of content on one page when being asked to complete a task.

## What we prototyped

As well as prepopulated data, we wanted to take the opportunity with this prototype to get feedback on a new service start page that our content designer was working on, and a section after submission for attracting further research participants - something we as a team struggle with.

As always, a version of [the prototype we tested](https://eq-runner-prototypes.netlify.app/prototypes/prodcom/) is maintained on netlify.


![screenshot of the prodcom page showing the prepopulated data in place](/testing-prepopulated-surveys/prodcom.png "Example prepopulated product page")


Here you can see the product name integrated into the main question, the "CN" numbers added in the questino description area, two inputs (there would either be 1,2 or 3 inputs - again defined in the spreadsheet), and unit type from volume. All prepopulated data that we have on file from the last time this survey was completed.

## What we found from research

Aside from finding that it was realy hard to recruit participants (the business could only find us one), we found out that the previewing questions section of the start page was useful. The participant would use it to send questions to other people in the organisation that would be best-placed to answer.

They had no problem completing the survey, and the usability constraints we were aware of due to technical limitations did not impact them. They had however no assistive digital needs.

Those constraints are the need to go back to the list of products after each question (looping, list collector), and grand calculated summary section appearing and disappearing (grand summary).

The user also did not notice/need the codes associated with each input. On the paper form, each response has a unique cocde (e.g. 581309501) that is used by telephone support when someone rings in with an issue. The participant instead said they would just use the titla of the page to define the area they were having a problem with.

## Next steps

A second research session was planned, but no participant was provided by the business. Therefore we will monitor the prepopulted data design and functionality as part of broader EQ product portfolio.