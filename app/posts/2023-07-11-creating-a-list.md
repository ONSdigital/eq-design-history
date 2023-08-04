---
title: Working with long lists
description: Designing a better way than radios or select to loop through a list of products.
date: 2023-07-11
---

This originally came about as a challenge from our internal users to reduce the lower limit on a select dropdown from 25 items to 24. When we invetigated the reason for this, it transpired that the initial limit was set very high to disuade survey creators from overusing the component. Government-wide research has shown the select component to perform badly in accessibility, and [current guidance](https://design-system.service.gov.uk/components/select/) is to only use as a last resort.

When asked what to use instead, our recommendation was to use radio buttons. Either one long list, or a series of radio lists becoming more specific each time, e.g. select continent, select country, select town.

We were shown that the survey gives a long list to the user, who then has to work through and answer the same question (around pricing) for each product they sell.

As our original recommendation of radios was based on the assumption of picking just one answer from a series of options, we had to quickly rethink as the pattern here suggests more than one option would be the normal user experience.

Enter the checkboxes.

![screenshot of a long list of checkboxes](/creating-a-list/checkboxes.png "")

Because we now understood the business need to be for the user to report the prices of only the relevent products on a list, we could make this a better interaction by:
1. Allowing the user to create a 'short list' of only the relevant products by checking off each relvant one from a longer list
2. Looping through that short list with exising EQ functionality to ask the follow-up question

Instead of using 40+ radios or a select dropdown, and relying on a user remembering which one they had already completed, we had a slightly longer interaction but a much lower cognitive burden. It was also much more accessibile.

![screenshot of user-created short list](/creating-a-list/created-list.png "")

![screenshot of repeating question applied ot one item from short list](/creating-a-list/looping-question.png "")

## What we found from research
Users had no problem working with the long list. Some expressed a preference for having the list ordered alphabetically, or to separate into sub-categories.

We had feedback that the looping part was frustrating, users would prefer not to go back to the list each time, and instead just progress onto the next question. This functionality is not currently possible in EQ.

## Next steps
This has worked as a proof of concept, work now needs to be prioritised to develop the checkbox component to drive List Collector functionality. 

There also needs to be clearer guidance around usage of radios and select components to ensure best practice and optimal user experience.