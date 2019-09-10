This version of jemdoc+MathJax uses flex for layout instead of tables; basically, I wanted the menu position to be fixed on tall pages.

Readme of jemdoc+MathJax
------------------------

jemdoc+MathJax
==============
*jemdoc* is a light text-based markup language designed for creating websites.  See http://jemdoc.jaboc.net/ for more information and the detailed usage of jemdoc.

*jemdoc+MathJax* adds the MathJax support to jemdoc.  You can use the same jemdoc syntax (and therefore no need to make any changes in your jemdoc scripts if you are an original jemdoc user), but the equations will be beautifully rendered by MathJax.  See http://web.stanford.edu/~wsshin/jemdoc+mathjax.html for more information and examples. 

System requirements
-------------------
Python 2 or Python 3

(Many thanks to [Ganesh Ajjanagadde](http://www.mit.edu/~gajjanag/), who made most of the changes for Python 3 compatibility.)

What's new in jemdoc+MathJax
----------------------------
- MathJax support
- Underscore
- Control of the behavior of links: open in the current web broswer tab or in a new tab
- Works on both Python 2 and 3

How to use jemdoc+MathJax
-------------------------
The only major difference from the original jemdoc in usage is the mechanism to fetch the javascript engine for MathJax.  The recommended way of doing this is to specify the URL of the javascript engine inside a configuration file (`mysite.conf` in the following example) and to provide the file to the jemdoc executable as

	jemdoc -c mysite.conf YOUR_JEMDOC_SCRIPT.jemdoc

An example `mysite.conf` can be found in the `example/` directory.  

The `example/` directory also contains jemdoc script files that demonstrate the usage of the additional features implemented in jemdoc+MathJax.  You can build a website out of these jemdoc scripts by executing the following command inside the `example/` directory:

	../jemdoc -c mysite.conf *.jemdoc
	
To see the resulting website, open any HTML files generated by the above command inside a web browser.

Except for the MathJax support and the few additional features mentioned previously, jemdoc+MathJax is almost exactly the same as the original jemdoc.  To learn the usage of the original jemdoc, see the [jemdoc user guide](http://jemdoc.jaboc.net/using.html), expecially the [example page](http://jemdoc.jaboc.net/example.html).

Disclaimer
----------
The focus of the implementation of the additional features was to "make them just work," so the implementation is suboptimal, both in terms of performance and style.  

Still, several users and I find jemdoc+MathJax is quite stable and does the job correctly :-)

Wonseok Shin

README of the original jemdoc
-----------------------------
> jemdoc is a light text-based markup language designed for creating websites. It
> takes a text file written with jemdoc markup, an optional configuration file and
> an optional menu file, and makes static websites that look something like
> http://jemdoc.jaboc.net/.
> 
> It was written by me, Jacob Mattingley, in 2007, and definitely isn't the type
> of code I would put on my CV. Lots of people use jemdoc, especially in academia.
> 
> Much more info at http://jemdoc.jaboc.net/.

