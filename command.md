# Scripting with the Command Window

It is hard to overstate the power of scripting within the command window. Anything you can do with the DTSA-II and the Electron Probe Quantification library you can do from the command window. Many functions from EPQ that are not otherwise available through DTSA-II are available through the command window. Furthermore, the command window is a complete programming language - the Python language implemented in Java. You could write an home accounting package in DTSA-II or more realistically maybe a web server serving up quantitative algorithms. Let's just says it's powerful!

Using the command window to its full capabilities is a challenge to which you could devote years of study. For one, you will have to learn the syntax of the Python language (CPython 2.2). However, in addition to providing a full Python programming environment for using EPQ algorithms, the command window also provides some very basic functionality in a manner that is more natural than a graphical user interface. Probably the best example is **spectrum mathematics**.

### Accessing spectra

All the spectra available on the **Spectrum** tab in the spectrum list are available through the command line. Typing the command

```py
ls()
```

will display a two column list. The first column contains an abbreviated name for the spectrum "s?". The second column contains the full name as displayed in the spectrum list. You will refer to the spectra using the abbreviated name in the first column but you will be operating on exactly the same spectrum as is listed on the spectrum tab in the spectrum list. Changes made through the command line will propagate to the spectra in the spectrum list. Change the name of spectrum "s2" and the associated spectrum in the spectrum list will change name.

### Manipulating spectra

It is often desirable to compute the sum or take the difference of the channel data in two or more spectra. The command line provides a very simple way to accomplish this. For example, you can create a new spectrum "a1" that is the difference of spectrum s1 and s2 by typing

```py
a1=s1-s2
```

"a1" now contains a spectrum object in which each channel of s1 had the equivalent channel in s2 subtracted off. You don't immediately see a1 because it resides only in memory. But adding the spectrum "a1" to the spectrum list is as simple as typing

```py
a1.display()
```

Spectrum "a1" will be added to the spectrum list and displayed on the spectrum display. "a1" will also be assigned a new name in the "s?" series which you can access through `listSpectra()`. You could have combined the two operations without creating an intermediate object "a1" by typing

```py
(s1-s2).display()
```

You can add two spectra by typing `(s1+s2).display()` or add/subtract fractional spectra by typing `(s1-0.5*s2).display()` or `(s1+0.99*s2).display()`. Once you get used to working with spectra, this mechanism is very quick and efficient.

There are many other common spectrum manipulation tasks that are simple from the command line.

```py
print s1.peakIntegral(2500,4000)
```

will compute and display a background-corrected peak integral from E=2500 to 4000 eV.

```py
print s1.duaneHunt()
```

will compute and display the Duane-Hunt limit in keV.

### Other functions

Other important information is accessible through the command line.

```py
listData("Si")
```


will list important microanalytical data about the element Si including the atomic number, atomic weight, edge energies and the x-ray transition energies.

```py
fileOpen()
toolsQuantificationAlien()
toolsEditSpectrumProperties()
```

are exactly equivalent to the menu items of the same name.

### Script files

Script files can be developed with a standard text editor and run within the command environment. The following imports have been predefined for your convenience. They facilitate access to the classes in the EPQ library and the DTSA-II application. You may learn more about the EPQ library from the JavaDoc programmers documentation. The JavaDoc is packaged with the executable may be installed at the user's preference.

```py
import gov.nist.microanalysis.EPQLibrary as epq
import gov.nist.microanalysis.EPQTools as ept
import gov.nist.microanalysis.Utility as epu
import gov.nist.microanalysis.NISTMonte as nm
import gov.nist.microanalysis.dtsa2 as d2
import java.lang as jl
```

There is a lot more to the command line but this should give you a flavor and a feel for whether you are interested in pursuing this method of working with spectra further. The _Scripts_ page gives some examples of more sophisticated scripts.
