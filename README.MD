PhpStorm Bug
===

This is a workaround to fix the UNICODE character display bug outlined here:  
https://youtrack.jetbrains.com/issue/IDEA-81911


I can confirm that this bug is still present  as of 24 Apr 2016 in the following versions:
 
 * PhpStorm 2016.1 Build #PS-145.258, built on March 16, 2016 (JRE: 1.8.0_60-b27 x86)
 * PhpStorm 9.0.2

About:
---
In a nutshell, PhpStorm has issues when zooming in on multi-lingual unicode text. The 
unicode characters will display fine when you initially open the document. But then, when 
you zoom in on the document, the unicode text display turns into funky boxes. 


Steps to recreate this bug:
---
* Load [unicode-tests.php](unicode-tests.php)  in phpStorm

* Zoom in with the scroll wheel at least 3 notches and some characters should turn into squares.  
( On Windows hold CTRL and turn the scroll-wheel )


Current workaround:
===
1. Install Code2000 - (See : [Code2000\CODE2000.TTF](Code2000/CODE2000.TTF))
2. Open phpStorm's settings. (CTRL+ALT+S)
3. Uncheck "Show Only Monospaced Fonts"
4. Configure phpStorm to use "Code2000" as the *secondary fallback font.*
5. Restart phpStorm and test. 

**Notes:**
---
Code2000 is a shareware font. 
(See : [Code2000\CODE2000.HTM](Code2000/CODE2000.HTM))

** There is still a kerning bug with phpStorm 2016.1 in the phpDoc comments. (check out the comments in [unicode-tests.php](unicode-tests.php))
