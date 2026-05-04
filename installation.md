## READ THIS - Prerequisites

*   You will need to have Java 8 installed to run the DTSA-II installer. The running the installer will copy all the necessary files to an appropriate location and create Start Menu links for Windows. The DTSA-II installer only works with Java JRE or JDK version 8 (or earlier.) JRE8 is available through [Oracle](https://www.oracle.com/java/technologies/downloads/#java8) or through [AdoptOpenJDK](https://adoptium.net/temurin/releases/?version=8). You will only need JRE 8 for the installation process. You can uninstall it after you have successfully installed DTSA-II.
*   If you use 64-bit MS Windows, the DTSA-II installer comes with a suitable JRE and will "just work" once installed. The installer will make links to the applications on the start menu.
*   If you use Linux, Apple OS X or 32-bit Windows, you will also have to install a more recent Java JRE or JDK. Here, again Java is making our life more difficult. The most recent versions of the JRE/JDK won't work. I recommend going [here](https://adoptium.net/temurin/releases/?version=25) and installing OpenJDK 25.

DTSA-II is regularly tested on a well-patched 64-bit Windows 10 and 11 systems. Until recently, I also occasionally ran it on Windows 7. When it was tested on OS X and Linux, it was observed to work and produce identical results. However, this was years ago and your mileage may differ. DTSA-II should work on any Java-supported platform and produce identical numeric results.

## Download

Please review the [release notes](releaseNotes.md) before installing DTSA-II.

### Current Release

*   [DTSA-II Polaris (includes Java Runtime Environment 24 for Windows) - the "groovy release"](dtsa2_Polaris.jar)
*   [DTSA-II Polaris (without a Java Runtime Environment for Apple or Linux)](dtsa2_Polaris_nojre.jar)

### Older Versions

*   [DTSA-II Oberon (includes Java Runtime Environment 24 for Windows)](dtsa2_Oberon.jar)
*   [DTSA-II Neptune (includes Java Runtime Environment 21 for Windows)](dtsa2_neptune.jar)
*   [DTSA-II Neptune (without a Java Runtime Environment for Apple or Linux)](dtsa2_neptune_nojre.jar)
*   [DTSA-II Microscopium (multiplatform Java installer)](dtsa2_microscopium.jar)
*   [DTSA-II Lorentz (previous version)](dtsa2_lorentz.jar)
*   [Release Notes](releaseNotes.md)
*   The source code for [DTSA-II](https://github.com/NicholasWMRitchie/DTSA-II) and the [EPQ Library](https://github.com/NicholasWMRitchie/EPQ) are available through GitHub

### Pre-Release

DTSA-II undergoes frequent small modifications to improve the program by adding features or fixing bugs. I often make these updates available through a "pre-release channel." Prereleases are not tested as carefully as releases but may be worth a look if you want the latest features or bug fixes.

*   [DTSA-II Prerelease (includes Java Runtime Environment 19 for Windows)](https://drive.google.com/file/d/17YAXRYkQ9vAQ509AwP5eZagdGfShX-dE/view?usp=share_link)
*   [DTSA-II Prerelease (without a Java Runtime Environment for Apple or Linux)](https://drive.google.com/file/d/1O5ZhYX34ByxeuD6ocVbqp8xIljq9FEc0/view?usp=share_link)

## Microscopy Today Downloads

[This archive](mt4_example.zip) contains the files described in the article in the January 2012 Microscopy Today article _Standards-Based Quantification in DTSA-II - Part II_.

## Installation

### All Platforms

1.  The installer is a regular Java JAR file. Other than requiring a version 8 or earlier JRE, it will probably run just by "double-clicking" the dtsa2\_XXX.jar file.
2.  If this doesn't work, you can also execute the JAR file from the command line.

1.  Open a command line. You can use the Windows-key+R to open the "run dialog" and then enter "cmd" to run the command line.
2.  Use the "cd" command to change the working directory to the directory in which "dtsa2\_microscopium.jar" has been stored.
3.  Enter the command "java -jar dtsa2\_microscopium.jar". This will run the installer.

### Apple OS-X

1.  The 'DTSA-II latest' installer will copy all the necessary files into a folder in your Application directory.
2.  OS X comes with a Java JRE 8.0 but DTSA-II requires version 21.0.
3.  You can get a more recent JDK/JRE from [AdoptOpenJDK](https://adoptopenjdk.net/releases.html/). However OS X will continue to default to the system 8.0 version. To resolve this you will need to create a small batch file to force use of the AdoptOpenJDK.
*   One user reports that this batch file works for him
    
```bash
#!/bin/bash
export JAVA\_HOME=\`/usr/libexec/java\_home -v 21.0.4\`  # Change the version number to the locally installed version
cd "/Applications/NIST DTSA-II Polaris 202?-??-??" # where the "?" reflect the revision you have installed.
$JAVA\_HOME/bin/java -jar dtsa2.jar
``` 
    
where he used

```bash    
/usr/libexec/java\_home -V
```    

to determine the versions of the installed JREs.

*   You can create a link to this batch file on your desktop and use that link to start the application as though it were native.

### Linux etc.

1.  The installer will copy the files to /usr/local/NIST/...
2.  You will need to ensure that version 21 of the OpenJDK or later has been installed using your distribution's package manager.

## Uninstallation

### All Platforms

1.  A program called "uninstaller.jar" is created in the "Uninstaller" directory within the program install directory.
2.  Double-click or "java -jar uninstaller.jar" to uninstall the program.
