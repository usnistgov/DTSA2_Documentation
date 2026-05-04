## Latest News:

### [NIST DTSA-II Polaris](dtsa2_polaris.jar) released on 30-Jan-2026
  *   A bug-fix release of [NIST DTSA-II Oberon](dtsa2_Oberon.jar) released on 22-Nov-2024

### An update [NIST DTSA-II Oberon](dtsa2_Oberon.jar) released on 11-Jun-2024
  *   Implemented a dynamic width filter-fit to improve low energy line resolving power
  *   Add documentation for changing spectrum line color: [Documentation](SettingCustomSpectrumLineColors.pdf) [Example](specColors.csv)
  *   Improved uncertainty calculation when normalizing compositions
  *   Bug fix: Correct calculation of detector efficiency at negative energies
  *   Update atomic weights with IUPAC 2021 values
  *   Bug fix: Fix spectrum similarity metric calculation for peaks above the beam energy
  *   Toned down the colors of images in the GUI
  *   Resize keV buttons on spectrum display panel on Mac
  *   Add BadgerFilm export option
  *   Add backscatter angle histogram class for MC simulations (scriptable-only)
  *   Other small improvements and fixes

### An update [NIST DTSA-II Neptune](dtsa2_neptune.jar) release on 10-Mar-2023
  *   Added STEM-in-SEM quantification using bulk standards
  *   Added the [multi-spectrum metric](https://doi.org/10.1017/S143192762200263X) to the Standard Bundler dialog
  *   Read and write image files written with spectra
  *   Improved low-energy fitting residuals
  *   Updated support for recent Java Runtime Environments (comes with JRE19)
  *   Added a "buried layer" model to the Monte Carlo GUI
  *   User-selectable look-and-feels (under File->Preferences)
  *   Improved command memory on the command line (Ctrl-Space searches for matches)
  *   Many other small improvements

## Videos
We've added DTSA-II Video Tuturials on YouTube
  *   [Introduction to NIST DTSA-II](https://www.youtube.com/watch?v=K7w9WOIdVyY)
  *   [Introduction to Quantitative Analysis using NIST DTSA-II](https://www.youtube.com/watch?v=MoW5w0RFdrI)
  *   [Introduction to Simulation using NIST DTSA-II](https://www.youtube.com/watch?v=1703Y24tOtc)
  *   [Using the Material Editor in NIST DTSA-II](https://www.youtube.com/watch?v=ZWUHM2SEyMU)
  *   [Understanding Peak Shape References](https://www.youtube.com/watch?v=nFQdpwL0d5Q)
  *   [Advanced Quantitative Analysis using NIST DTSA-II](https://www.youtube.com/watch?v=Roq1xd0CZdc)

## Demo Data
*   Download the demo K240 data from [here](K240example.zip)

## Journal Articles
*   Read Newbury and Ritchie (Open Access/Free Download!!) [Performing elemental microanalysis with high accuracy and high precision by scanning electron microscopy/silicon drift detector energy-dispersive X-ray spectrometry (SEM/SDD-EDS)](https://link.springer.com/article/10.1007/s10853-014-8685-2)
*   Read Newbury and Ritchie [Measurements of Trace Consistuents by Electron-Excited X-ray Microanalysis with Energy-Dispersive Spectrometry](https://journals.cambridge.org/action/displayAbstract?aid=10314582)
*   Read Newbury and Ritchie [Performing elemental microanalysis with high accuracy and high precision by scanning electron microscopy/silicon drift detector energy-dispersive X-ray spectrometry (SEM/SDD-EDS)](https://link.springer.com/article/10.1007/s10853-014-8685-2)
*   Read Newbury and Ritchie [Quantitative Electron-Excited X-Ray Microanalysis of Borides, Carbides, Nitrides, Oxides, and Fluorides with Scanning Electron Microscopy/Silicon Drift Detector Energy-Dispersive Spectrometry (SEM/SDD-EDS) and NIST DTSA-II](https://journals.cambridge.org/action/displayAbstract?aid=9989340)
*   Read Newbury and Ritchie [EDS Measurements of X-Ray Intensity at WDS Precision and Accuracy Using a Silicon Drift Detector](https://journals.cambridge.org/action/displayAbstract?aid=8653733)

## Overview

DTSA-II is a multi-platform software package for quantitative x-ray microanalysis. DTSA-II was inspired by the popular Desktop Spectrum Analyzer (DTSA) package developed by Chuck Fiori, Carol Swyt-Thomas, and Bob Myklebust at NIST and NIH in the '80's and early '90's.

DTSA-II has being designed with the goal of making standards-based microanalysis more accessible for the novice microanalyst. _We want to encourage standards-based analysis by making it as easy as possible to get reliable results._ Many operations which had previously required user intervention under DTSA now are performed entirely by the software. Furthermore, the software attempts to guide the user step-by-step through common processes while performing quality control sanity checks. While this might not provide the flexibility that some sophisticated users may desire, we feel that this philosophy is more consistent with the way laboratories are moving towards technicians responsible for multiple techniques and away from experts in single techiques. We encourage users who desire the additional power and flexibility available in the EPQ library to learn to script using Jython or to create their own alternative user interface. EPQ is much more capable than the fraction exposed via DTSA-II.

DTSA-II is based on an entirely new code base written by Nicholas W. M. Ritchie. The codebase has been carefully divided into a shared algorithm library which forms the basis for a handful of software products and a user interface shell. DTSA-II is the user interface shell and the EPQ library is the algorithm library.

DTSA-II remains under active development. Many features - some fairly basic - remain unimplemented. Other features have not been tested as much as the developer might like. The program made available to the public via this web site represents the current best available version in the judgement of the developer. DTSA-II remains experimental software and no representations are made regarding the suitability of the product for any particular application.

## Major features:

### Basic IO and Display

*   Read energy dispersive x-ray spectra in a variety of different commercial and non-commercial formats including the industry standard EMSA format
*   Display and overlay spectra with various scaling options on linear/log/sqrt axes
*   Copy/save/print the spectrum display as a bitmap/PNG file
*   Output the spectra as a GNUPlot file for publication quality output
*   Overlay labeled x-ray emission lines and x-ray absorption edges
*   Define and integrate regions-of-interest
*   View spectrum contextual information
*   Archive spectra to a searchable database
*   Sub-sampling of spectral data to simulate shorter acquisition times
*   Basic spectrum math functions
*   Background modeling or background stripping
*   Energy axis linearization
*   Spectrum smoothing
*   Peak removal (trimming)
*   Peak search / identification

###   Spectrum Simulation
*   Analytical (φ(ρz)) simulations of energy dispersive x-ray spectra
*   Normal or oblique incidence angle
*   Variable beam energies, beam fluxes, materials
*   Monte carlo simulations of energy dispersive x-ray spectra
*   Spectra from bulk samples
*   Mounted or unmounted thin films
*   Cubical or spherical particles with or without a substrate
*   Simulated spectra may be manipulated as experimental spectra
*   Variety of detector options including Si(Li), SDD and microcalorimeter

### Standards-based Quantification
*   Standards-based quantification of EDS spectra
*   Filter-fit linear-least squares fitting of reference spectra
*   Quantification based on references or like-standards
*   φ(ρz) correction of the k-ratios
*   ζ-factor correction of thin-film samples
*   Results reported as HTML with estimates of uncertainty

### Reporting
*   Actions are recorded in a daily HTML activity report
*   Report may be opened in an alternative HTML viewer

### Platforms and Source Code
*   DTSA-II is based on the EPQ library - a full-featured library of electron probe quantification algorithms
*   DTSA-II only exposes a fraction of the power within the EPQ library. The remainder may be accessed via custom Java applications or via Jython scripting.
*   The EPQ library includes the full NISTMonte for Monte Carlo simulation of electron/x-ray transport
*   DTSA-II / EPQ library are available as source code
*   DTSA-II / EPQ library are written in Java SE 6 compatible source
*   DTSA-II / EPQ library can execute on any platform supporting Java SE 6 or later
*   DTSA-II / EPQ library is regularly tested on Windows XP, Ubuntu Linux & Apple OS X

## Disclaimer
This software was developed at the National Institute of Standards and Technology by employees of the Federal Government in the course of their official duties. Pursuant to title 17 Section 105 of the United States Code this software is not subject to copyright protection and is in the public domain. DTSA and the EPQ library are experimental systems. NIST assumes no responsibility whatsoever for its use by other parties, and makes no guarantees, expressed or implied, about its quality, reliability, or any other characteristic. We would appreciate acknowledgement if the software is used. This software can be redistributed and/or modified freely. The author requests that any derivative works bear some notice that they are derived from it, and any modified versions bear some notice that they have been modified.

Any mention of commercial products is for information only; it does not imply recommendation or endorsement by NIST nor does it imply that the products mentioned are necessarily the best available for the purpose.
