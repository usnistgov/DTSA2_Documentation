### Documentation

This web site provides some basic documentation. Additional documentation can be found at the following links.

### DTSA-II Video Tuturials on YouTube

*   [Introduction to NIST DTSA-II](https://www.youtube.com/watch?v=K7w9WOIdVyY)
*   [Introduction to Quantitative Analysis using NIST DTSA-II](https://www.youtube.com/watch?v=MoW5w0RFdrI)
*   [Introduction to Simulation using NIST DTSA-II](https://www.youtube.com/watch?v=1703Y24tOtc)
*   [Using the Material Editor in NIST DTSA-II](https://www.youtube.com/watch?v=ZWUHM2SEyMU)
*   [Understanding Peak Shape References](https://www.youtube.com/watch?v=nFQdpwL0d5Q)
*   [Advanced Quantitative Analysis using NIST DTSA-II](https://www.youtube.com/watch?v=Roq1xd0CZdc)

### Download the demo K240 data

* [K240 Demo Data](K240example.zip)

### Introductions to DTSA-II

*   [Introduction to DTSA-II](IntroductionToDTSA-II.pdf) from the Lehigh Microscopy School
*   [Dale Newbury's NIST DTSA-II ("Son of DTSA"): Step-by-Step](DalesDTSA2Presentation.pdf) Presentation introducing DTSA-II and most of the basic functionality.
*   [Examples of high quality quantifications performed with DTSA-II](Examples_of_high_quality_standards_based_analysis.pdf) You too can make similar robust, reliable measurements

### Basic information

*   [Configuring instruments and detectors](DTSA-II_Configuration.pdf):Basic information on setting up instrument and detector definitions.
*   [Calibrating a detector](DTSA-II_Calibration.pdf): Discusses the hows and whys of calibrating a detector in DTSA-II.
*   [Planning a measurement](DTSA-II_Optimization.pdf): Optimizing a measurement using the Optimization Alien.
*   [Simple quant example](DTSA-II_An_example_of_a_simple_quant.pdf): Quantifying K458, a simple glass containing Si, Ba, Zn and O.
*   [DTSA-II Publication Quality Output](DTSA-II_Publication_quality_spectra.pdf): Generating publication quality spectrum plots using DTSA-II
*   [DTSA-II Utility Functions](DTSA-II_Utility_functions.pdf): Documentation for various spectrum manipulation utility functions
*   [Introduction to Spectrum Simulation](DTSA2_Intro_to_simulation.pdf)
*   [Using the material editor](DTSA2_The_Material_Editor.pdf) The material editor is your friend (if you'll get to know it.)

### Quality Control - Proving your instrument is working correctly

*   [The Faults and Foibles of EDS Detectors - 2016 edition](FaultsFoiblesEDS.pdf) How do SDDs work and what are the consequences. Also covers procedures to ensure that your detector is working optimally.
*   [Introduction to QC](DTSA2_QC.pdf) How to ensure your measurements are reliable
*   [Adding a QC spectrum](DTSA2_Quality_Control_Adding_a_QC_spectrum.pdf)
*   [Generating a QC control chart](DTSA2_Quality_Control_Generating_a_report.pdf)

### Intermediate topics

*   [Using Standard Bundles to simplify standards-based quantification](Standard_Bundles.pdf)
*   [Using ζ-factors to quantify STEM unsupported thin film samples](Zeta-Factors.pdf)
*   [Strategies for high quality standards](Strategies_for_high_quality_standards.pdf)
*   [What is a standard? What is a reference?](DTSA2_Standards_vs_References.pdf) An attempt to explain this complicated (but important) subject
*   [How spectra are quantified?](DTSA2_Mechanics_of_Quant.pdf) A little bit of insight into what DTSA-II does to convert spectra into measures of composition.
*   [How to rename spectra](Renaming_spectra.pdf)

### Advanced: Scripting

*   [Scripting quantification](DTSA-II_Scripting_quantification.pdf):Advanced scripting of spectrum quantification using DTSA-II and Python
*   [Basic scripting in DTSA-II](Basic_scripting_in_DTSA-II.pdf): Introduces some basic concepts to get you started with the most powerful part of DTSA-II

### Other advanced topics

*   [Moving DTSA-II from one computer to another](https://www.cstl.nist.gov/div837/837.02/epq/dtsa2/Moving%20DTSA-II.pdf): Move DTSA-II to another computer without losing important data
*   [Customizing Line Colors in the Spectrum Display](https://www.cstl.nist.gov/div837/837.02/epq/dtsa2/SettingCustomSpectrumLineColors.pdf)

### The Microscopy Today Tutorial Series

*   [Getting Started with NIST DTSA-II](MT1_GettingStartedWithNIST_DTSA_II.pdf)
*   [Manipulating Spectra Using DTSA-II](MT2_ManipulatingSpectraUsingDTSA_II.pdf)
*   [Standards-base Quantification Using DTSA-II - Part 1](MT3_Standards_based_Quantication_Part1.pdf)
*   [Standards-base Quantification Using DTSA-II - Part 2](MT4_Standards_based_Quantication_Part2.pdf)

### Jeff Davis' 1 Minute Tutorials

*   [Tutorial 1](DTSA-II_Tutorial_1.pdf): Creating a Detector
*   [Tutorial 2](DTSA-II_Tutorial_2.pdf): Calibrating a Detector

### Quant Examples

[This zip file](DemoSpectra.zip) contains two sets of spectra. The first demonstrates quantifying Benitoite (BaTiSi3O9). Benitoite is interesting because of the overlap between Ba and Ti. The second set contains K411/K412 - two NIST-made glasses. These are interesting because you can quantify K412 using pure elements/simple compounds as standards or using K411 and Al2O3. The later is more accurate than the former.

The zip file also contains the information necessary to configure a detector (in Preferences) to match the one on which the spectra were collected. You need to configure this detector before attempting to quantify the spectra and then select this detector from the "Default Detector" lists on the main window. Now when you load the spectra they will be associated with this configuration.

### Qual Examples

[This zip file](QualSpectra.zip) contains many different spectra for practicing qualitative analysis. 'Qual' is one of those skills which requires practice to develop but is a critical skill for reliable microanalysis. In our experience, the auto-qual routines in the vendors software almost work. If they never worked, we'd never trust them and that would be fine. If they always worked, we could trust them and that would be fine. Since they almost work, many people close their eyes and pretend that they are reliable. That is a problem. As a result, there are many unfortunate errors in internal corporate reports and the literature. If you are content with being correct 80% of the time, use auto-qual. If you expect better, you'll have to perform qual yourself. These spectra can help you to practice. The spectra are labeled by level of difficulty and the correct answers are available in a text file.
