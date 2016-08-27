# WordPressSSG (Standing on the Shoulders of Giants)
Coding For WordPress? Let's build better WordPress themes &amp; plugins by "Standing on the Shoulders of Giants".

## Why WP SSG?
Remember how we are solving some issues which might have been solved by some other great developer in his/her popular plugin or theme with all source code for us to inspect and learn from.

You might know how when we add short-codes and have to return the output instead of echo/printing as otherwise it will be displayed on the top of the content. I was having hard time to manage complex output of a short-code to save into a variable to return at the end of the function, then thanks to a plugin, I learned this simple techquie built-in to PHP which I could have easiy used and fix this issue.

I promised myself to document those edge cases with the code and reference to plugins/themes and authors to help me keep reference for me and for other WordPress Developers.

## Table of Contents

### ShortCodes

#### Returning Short-Code functions' output where there is lot of stuff to output, use ob_start i.e. 
```php
$ob_start();
//then all your echo calls or raw html here
//then end with these three calls to properly return output
$content = ob_get_contents();
ob_end_clean();

return $content;

```
