---
title: Stacking errors
description: How we present more than one error for a form input
date: 2023-07-21
---


The pattern already exists for showing multiple errors on a single page - you have to hunt around a bit for it as it's not a listed component - but you can [find it under panel](https://service-manual.ons.gov.uk/design-system/components/panel#error).

There is more documentation on the pattern page for [helping users to correct errors](https://service-manual.ons.gov.uk/design-system/patterns/correct-errors).

Anyway, once you find it - it's fine. The issue we had was what if the errors are both on the same input?

 ![screenshot of an example error screen with mulitple issues on one input](/stacking-errors/screenshot.png "One input, two errors")

The [guidance only shows one error](https://service-manual.ons.gov.uk/design-system/components/error).

And the code would not support a semantic list of errors associated with one input.

    ```<p class="ons-panel__error">```
    ```<strong>Enter a number that is less than 60</strong>```
    ```</p>```

So we needed to make a simple tweak there...

## What we prototyped

	```<ol class="ons-list ons-list--bare">```
      ```<li class="ons-list__item ons-panel__error">```
        ```<strong id="error-1">Enter a number more than or equal to -1000</strong>```
      ```</li>```
      ```<li class="ons-list__item ons-panel__error">```
        ```<strong id="error-2">Enter a number rounded to 2 decimal places</strong>```
      ```</li>```
    ```</ol>```

Making it an ordered list instead of paragraphs, or a paragraph of line-broken sentances, makes this much more semantic HTML.

## Next steps

Needs some more accesibility testing and then should be discussed with the design system team - shold we replace all error inputs with the new code - even if there is only one error, or stick with a paragraph?