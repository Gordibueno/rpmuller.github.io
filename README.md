Projects
========
* [PyQuante](http://pyquante.sf.net)/[PyQuante2](https://github.com/rpmuller/pyquante2)
* [Sympy for Quantum Circuits](https://github.com/rpmuller/sympy/tree/sympy_qcircuit/sympy/physics/quantum)
* Python bindings for Libxc
* Python bindings for Libint
* Python2.7 bindings for Libquantum

IPython Notebooks
=================
* Crash Course in Python for Scientists: Coming Soon!
* [PyQuante2 Overview](http://nbviewer.ipython.org/5745404)
* [Sympy Quantum Circuit Plotting](http://nbviewer.ipython.org/5843312)
* [SVG graphics in IPython notebooks](http://nbviewer.ipython.org/5666810)

Progress
========
* 29 Jun 2013
  - Updated [Sympy Circuit Notebook](http://nbviewer.ipython.org/5843312) and got a few more examples to work.
  - Reviewed priorities.
* 28 Jun 2013
  - Removed old iterators: no more simple, usimple, averaging
* 27 Jun 2013
  - Killed the stuff I did with RuntimeErrors in the iterators, and wrote a non-generator-based
    SCFIterator that properly exits, and can keep track of whether or not it is converged. Haven't
    wired this in to much of the code yet.   
  - Making a little progress updating the pyqu bindings for Py27
* 26 Jun 2013
  - Added RuntimeErrors to PyQuante2 iterators when maxiters reached. Am not doing anything to catch
    these at this point, but could do so later on.
* 25 Jun 2013
  - Poor man's scratcher: find . -size +100M -mtime +28 (yes, I need to clean my scratch directories).
    Can also use with -exec rm {} \;
  - Had trouble getting the nosetests to run quickly in pyquante2. Worked around this by doing a 
    setup.py build_ext --inplace to get the cython libraries in the appropriate places, after which
    the nosetest went from taking 74 sec to run to taking < 2 sec!
  - Also moved test_cython into the tests directory, since now nose can run these tests.

* 24 Jun 2013
  - Profiling of unit tests in PyQuante2: Weird results. Looks as if the python versions of the integral routines
    are being called when running tests through nose, but the cython version are called when running from the
    command line.
  - Spent a little bit of time doing some more with the sympy circuit plotter. Updated the notebook. 
    Can now do arbitrarily labelled 1Q gates, as well as controlled versions of these. Block multi-Q
    gates don't work, nor do gates with matrices as their labels.
* 23 Jun 2013
  - libquantum wrappers: Extending python with C is very frustrating. Can't seem to get anything but segfaults! 
    Cython makes things much nicer, but I'm having trouble getting it to recognize _Complex
  - When MacPorts won't download files for you, you can manually download them and stick them in 
    [Macports root]/var/macports/distfiles. But why does MacPorts fail to fetch so often? 
    EDIT: proxy problems, of course.
  - Sticking this here since I forget it so often. To change the default (python or whatever) version in macports, do

    port select --list python

* 22 Jun 2013
  - Fixed pyquante2 orbital symmetry bug, which wasn't a bug but arose from my missing a transpose.
  - Prettified the pyquante2 plotting routines, and added to IPython notebook.
  - Got proper X, CNOT, and CPHASE gates to work in Sympy

Links
=====
* [My Sandia Homepage](http://www.cs.sandia.gov/~rmuller).
* [Citations on Google Scholar](http://scholar.google.com/citations?user=ihGf4wgAAAAJ&hl=en).

