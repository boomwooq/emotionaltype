# Emotional Type #

This project is part of Master thesis in Visual Communication, Master of Design, HGK-UIC FHNW, Basel School of Design (2017). The project is seeking for an alternative way of emotional expression in text message which could be applied in semi-formal situation, e.g., work place communication between co-worker, supervisor and subordinate, providing the tone of voice control. The result of this project not only encourage the user to express either positive or negative emotion but also provide the clear sarcastic sense which is usually considered ambiguous in the pure text. For more about the project, please visit www.emotionaltype.org

(Screenshot- all master with weight)

The exploration of this project take place in Apple device as an initial case to explore, therefore, the default type face is SF San Francisco and also sharing the same metrics with others. 



## How to view/use the fonts ## 

* [Mac preview](https://github.com/googlei18n/fontview/releases) , by Google

* [Axis Praxis](http://www.axis-praxis.org/)  by Laurence Penney. An easy browser interface for previewing and testing 

  * Requires a [browser that supports Variable Fonts](http://www.axis-praxis.org/blog/2017-04-05/17/how-to-get-variable-fonts-working-in-safari-chrome-and-firefox-macos)

    e.g. [Google Chrome Canary](https://www.google.com/chrome/browser/canary.html)

Credit: [i-can-variable-font](https://github.com/scribbletone/i-can-variable-font) 

## How to make ## 

* Please, check out [i-can-variable-font](https://github.com/scribbletone/i-can-variable-font) for the clear instructions and additional informtion of how to generate variable font. 

* More in my case, the problem I found: 

  It caused me this conversion error line in Terminal:

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

   while generating variable fonts. It is because my font contains different curve segments from a straight line to curve.

  ​

  To solve the problem, I have to change those straight line (zero-length controls point) to co-linear controls point.

  (screenshot1)(screenshot2)

## Build with ##

* [Robofont](http://doc.robofont.com)
* [Superpolator](http://superpolator.com)
* [Prepolator](http://tools.typesupply.com)

## Note ##

I'm a newbie to this whole things: 

* Type Design
* Generate variable font
* Github

If there any mistakes or there is any other corrections you would like to add, you're more than welcome! Or If you have questions regarding the project idea, please do not hesitate to ask either by email (boom.promphans@gmail.com) or create an issue here. 



What I shared here might be just the basic information which cannot be compared to those professional, however, I believe that it might be useful, may be, for other newbies out there. 

— 