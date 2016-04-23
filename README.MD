
PhpStorm Bug 

This is a workaround to fix the UNICODE character display bug outlined here:
https://youtrack.jetbrains.com/issue/IDEA-81911

I can confirm that this bug is still present  as of 24 Apr 2016 in the following versions:
 
 * PhpStorm 2016.1 Build #PS-145.258, built on March 16, 2016 (JRE: 1.8.0_60-b27 x86)
 * PhpStorm 9.0.2

About:
===
In a nutshell, PhpStorm has issues when zooming in on multi-lingual unicode text. The 
unicode characters will display fine when you initially open the document. But then, when 
you zoom in on the document, the unicode text display turns into boxes. 


Steps to recreate this bug:
===

* Load this gist: https://gist.github.com/ashbeats/ed812ed2dffb3e4cdb7fce1bb60700ad

* Once it loads in phpStorm, zoom in with the scroll wheel at least 3 notches and it should turn into squares.  ( On Windows hold CTRL and turn the scrollwheel )


Current workaround:
===

1 . Install Code2000 - (See : Code2000\CODE2000.TTF)

2. Open phpStorm's settings. (CTRL+ALT+S)

3. Uncheck "Show Only Monospaced Fonts"

4. Configure phpStorm to use "Code2000" as the *secondary fallback font.*

5. Restart phpStorm and test. 

Notes:
===
Code2000 is a shareware font. (See : Code2000\CODE2000.HTM)





