---
title: New products - making data more specific
description: Due to a technical constraint we needed an in input instead of a text field. This serendipitously meant the data become clearer and more digestible downstream 🙌.
date: 2023-06-22
---

As we work through each paper-based form that we have been task to recreate online, there is on occasion something very analogue that doesn't translate directly.

This is one of those times.

The Index Numbers of Imports Prices survey (informally called Prices) used the paper format to allow users to add amendments to product information directly as they were completing the form. There was a checkbox to indicate a change, which would raise a flag on the scanning system and require a person to read the amendments and manually add them in. This should then go back upstream to update our source data. The updates were written into a single comments box on the back of the form.


## What we prototyped
First pass was to take the format of the paper survey and lift and shift online. With the exception of adding a comments box for each product, rather than just the single generic one at the end. There is still one generic one, we'll test if there is a user need for this. We thought about incorporating the summary card pattern into this from the gov.uk design system, but were warned off showcasing new functionality due to build time.

![Example of a product screen, with prepopulated content at the top](/defining-new-products/1-before.png "Example of a product screen, with prepopulated content at the top")

## What we found from research
We did not test with users, but feedback from the business was that moving the accuracy of details, and the question about price, onto 2 screens would allow for more accurate data collection. So rather than having everything on one screen, we have moved to initially showing the products details and asking if they are correct (with the ability to update if not), and then asking about the price separately.

![Screenshot of the details screen](/defining-new-products/2-after-1.png "Asking about the details of a product")

![Screenshot of the price screen](/defining-new-products/3-after-2.png "Asking the price for the product")


## Next steps
Need to conduct user research to establish whether this interaction works for users.
We also need to consider the current suitability of the question page template, as having a list of product details is hard to accommodate - especially if we want to use the summary card design pattern in future.

![Screenshot of the pattern page from the ONS design system](/defining-new-products/4-question-page.png "The question page pattern from the ONS design system")