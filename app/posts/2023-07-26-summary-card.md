---
title: Prototyping with Gov Design System components
description: Not reinventing the wheel
date: 2023-07-26
---

Something that was ruled out of scope in an ealier look at presenting pre-populated data back to users was the summary card pattern used in the GOV.UK Design System.

As we unexpectedly had some time due to re-priorisation of work, we had a chance to look at how we could use this component for ONS. As it doesn't currently exist in our prototype kit / design system we'd either need to recreate it, or include it by including govuk-frontend as a node module.

This surfaced a bigger discussion within the community about the value of maintaining our own design system when the GOV.UK one has 85% percent of the patterns and components we have, plus some we don't. It also benefits from wider research and accessibility testing.

Speaking with interaction designers and front-end devs it was felt that the pros of using the GOV.UK Design System were outweighed by the cons. Namely that we needed to be our own identity as an arms-length organisation, and that we'd be "at the mercy of the gov.uk designs and if they were to change that could cause some issues for us".


![screenshot of the summary card pattern](/summary-card/screenshot.png "GOV.UK design pattern, in the ONS prototype kit")

So this could only be a proof-of-concept. If it proves effective in user research then an ONS version of the component would need to be built and maintained by our own design system team.


In order to use the component, we ahd to make changes to the ONS prototype kit to add govuk-frontend into the list of node modules it referenced.

We also needed to update the helper file `create-nunjucks-environment` to add govuk-frontend into the source list alongside the ons one:
```const templatePaths = ['src', 'src/prototypes', `node_modules/@ons/design-system${dsVersionDirectory}`];```


One final thing to note is that the GOV.UK Design System prototype kit now has [documentation for using plugins](https://prototype-kit.service.gov.uk/docs/install-and-use-plugins) - essentially adding the functionality from other organisations into the main system.


This could be an avenue to explore, where we could use the GOV.UK system for basic components and then have a plugin for all the ONS-specific ones layerd on top.