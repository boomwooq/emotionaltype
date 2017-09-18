# Emotional Type #

This project is part of a Master's thesis in Visual Communication, HGK-UIC FHNW, Basel School of Design (2017). The project is seeking an alternative way of emotional expression in text messages. Not to be compared with emojis or emoticons, it was aimed to be used in semi-formal levels e.g., communication in workplace between co-workers, supervisors and subordinates, or the situation when you would like to express emotion but not in a personal level. 



The letterforms were manipulated by applying angularity and curvature idea to express negativity and positivity respectively. It was positioned between expressive handwriting and typography, for more explaination about how the typeface was designed, please check out [process documentation](https://www.dropbox.com/s/juh1nblepx19gpw/emotionaltype_processdocumentation.pdf?dl=0). And on page 144-145 and 190-191 also gave a shortly explaination about how the manipulation system was made. However, Emotional font is not complete; The typeface itself has not yet been fully developed, and the font, here, contains only nine latin letters— a, e, i, l, m, n, o and t.   



By using OpenType (1.8) variable font format, Emotionaltype gives users ability to customize their tone of voice by providing the various range of steps in between negative to default and defualt to positive. Ideally, this project encourage the user to express both positive and negative emotions in text, and also allow one to express sarcasm. For more about the project, please visit www.emotionaltype.org  



![image of all weights](https://github.com/boomwooq/emotionaltype/blob/master/screenshot/all_weights.png)

Note that this project focused on Apple devices as an initial example to explore and therefore the default typeface is SF San Francisco, which also been set as a metric model for Emotionaltype since it was designed to be used along with the default typeface of that device. 

![image of screenshot_2](https://github.com/boomwooq/emotionaltype/blob/master/screenshot/screenshot_2.png)



## How to view/use the fonts ## 

* [Mac preview](https://github.com/googlei18n/fontview/releases) , by Google

* [Axis Praxis](http://www.axis-praxis.org/)  by Laurence Penney. An easy browser interface for previewing and testing 

  * Requires a [browser that supports Variable Fonts](http://www.axis-praxis.org/blog/2017-04-05/17/how-to-get-variable-fonts-working-in-safari-chrome-and-firefox-macos)

    e.g. [Google Chrome Canary](https://www.google.com/chrome/browser/canary.html)

Credit: [i-can-variable-font](https://github.com/scribbletone/i-can-variable-font) 

## How to make this variable font ## 

* Please, check out [i-can-variable-font](https://github.com/scribbletone/i-can-variable-font) for the clear instructions and additional informtion of how to generate variable font. 

* More in my case, the problem I found: 

  At first, It caused me this conversion error line in Terminal while I was trying to generate variable fonts:

  ```terminal
  .
  .
  .
      interpolate_layout_from=interpolate_layout_from, **kwargs)
    File "/Library/Python/2.7/site-packages/fontmake/font_project.py", line 488, in run_from_ufos
      ufos, reverse_direction, conversion_error, **kwargs)
    File "/Library/Python/2.7/site-packages/fontmake/font_project.py", line 204, in build_interpolatable_ttfs
      conversion_error=conversion_error)
    File "/Library/Python/2.7/site-packages/fontTools/misc/loggingTools.py", line 372, in wrapper
      return func(*args, **kwds)
    File "/Library/Python/2.7/site-packages/fontmake/font_project.py", line 159, in convert_curves
      reverse_direction=reverse_direction, dump_stats=True)
    File "/Library/Python/2.7/site-packages/cu2qu/ufo.py", line 260, in fonts_to_quadratic
      glyphs, cur_max_errors, reverse_direction, stats)
    File "/Library/Python/2.7/site-packages/cu2qu/ufo.py", line 165, in _glyphs_to_quadratic
      raise IncompatibleGlyphsError(*glyphs)
  cu2qu.ufo.IncompatibleGlyphsError: 'u'
  ```

  Later, I fould that because I bring in more curved segments and total number of points increases throughout the different masters. To solve the problem, I have to change from zero-length control points (straight line) to co-linear control points.

  ![image of point](https://github.com/boomwooq/emotionaltype/blob/master/screenshot/colinearcontrolpoint-01.png)

  Thanks to Erik van Blokland for responding my email with the clear and helpful explanation. 

  ​

## Built with ##

* [Robofont](http://doc.robofont.com)
* [Superpolator](http://superpolator.com)
* [Prepolator](http://tools.typesupply.com)

## Note ##

I'm a newbie to all of this:

* Type Design
* Variable Fonts
* Github

If there are any mistakes or there any other corrections you would like to add, you're more than welcome! Or if you have questions regarding the project, please do not hesitate to ask either by email (boom.promphans@gmail.com) or create an issue here. 



What I have shared here might be just the basic information, which cannot be compared to issues discussed by professionals, but I believe that what I have shared might be useful, maybe, for other newbies out there. 

— 