# WGS Extract
is a desktop tool for verifying, analyzing and manipulating your **Personal 30x [WGS](https://h600.org/wiki/WGS) test** result. It can also be used with any human genome based [BAM or CRAM](https://h600.org/wiki/Sequencing+File+Formats) file. Including [WES](https://h600.org/wiki/WES) test results; albeit with a more limited benefit.

**WGS Extract** **User Manual**: [v4 Alpha](https://bit.ly/3JCyZNa) (Google Doc)

__Latest Releases__ you can install on the [supported platforms](#supported-platforms) are:
* **[BETA v4 Installer (Aug 2022 and later)](https://bit.ly/3Ow0GJG)** (note: installs the latest stable ALPHA v4 until BETA v4 is truly available).
* **[ALPHA v4 (1 Apr 2022 and later) Installer](https://bit.ly/3B8MK5s)**
* **[Dev(eloper) v4+ (Aug 2021 and later) Installer](https://bit.ly/3z7nGZQ)**

See the **v4 Release Notes** in the installation directory and the **Installation Section** in the [v4 Alpha](https://bit.ly/3JCyZNa) manual for more details about the v4 release and your platform.

>As of the 31 July 2022 release, the program will now auto-update if you run the installer again. Not just the environment the tool depends on.

This tool is geared toward the needs of [genetic genealogy](https://h600.org/wiki/Genetic+Genealogy) and [Ancient DNA](https://h600.org/wiki/Deep+Ancestry) (aDNA) studies but may be helpful for those looking into health-releated uses of [WGS](https://h600.org/wiki/WGS) tests. The **personal, sub-$500, Direct-to-Consumer (DTC), 30x Whole Genome Sequence ([WGS](https://h600.org/wiki/WGS)) tests** are delivered with basic data files and reports. This tool serves to bridge the gap between the [WGS data files](https://h600.org/wiki/Sequencing+File+Formats) delivered and the present day [genetic genealogy community tools](https://h600.org/wiki/Third+Party+Analysis+Tools). Many health analysis sites accept the microarray and VCF files generated from your WGS test by this tool.

>Still waiting for your [WGS](https://h600.org/wiki/WGS) test results?  Want to get started today?  See the [International Genome Sample Resource (1K Genome archive)](https://www.internationalgenome.org/data) for [BAM or CRAM](https://h600.org/wiki/Sequencing+File+Formats) files that you can download and play with to learn the tool while waiting for your results.

This tool is designed to be a simple, push-button manipulation of [WGS files](https://h600.org/wiki/Sequencing+File+Formats) from any source. It hides the installation and scripting of complex bioinformatic tools and automatically determines the needed parameters based on the data within your files.  For more control over your pipeline, either learn to use the underlying tools directly or seek out a Galaxy server (such as [UseGalaxy](https://usegalaxy.org/)).

[Dante Labs](https://genome.dantelabs.com), [Nebula Genomics](https://nebula.org/), [Sequencing](https://sequencing.com/), and [ySeq](https://yseq.net/) are test results most commonly used with this tool. [Full Genomes Corp](https://fullgenomes.com/]), [GeneDX](https://www.genedx.com/), [Sano Genetics](https://sanogenetics.com) and [Veritas (historical)](https://veritasgenetics.com) are other test providers whose output is processed here. These are all results from [Illumina](https://illumina.com) or [MGI](https://en.mgi-tech.com/) next generation sequencers.  Results from [Oxford Nanopore](https://nanoporetech.com/) and [PacBio HiFi](https://www.pacb.com/smrt-science/smrt-sequencing/hifi-reads-for-highly-accurate-long-read-sequencing/) and [Revio](https://www.pacb.com/revio/) third generation sequencers can also be used; as can [FamilyTreeDNA](https://familytreedna.com/)'s BigY output. (This is not an endorsement of any company or service; simply reporting what is commonly used with the tool.)

>The tool acronym is **WGSE** and pronounced as "wig-see". We encourage that use in conversation.

We use the Facebook group [Consumer WGS Testing](https://www.facebook.com/groups/ConsumerWGS/) for discussions on how to make use of your **personal, sub-$500, DTC 30x WGS test** results. Bugs, use cases and announcements about the Beta release tool happen there.  As part of that Facebook groups' Files section, you will find a number of useful companion documents and tool references.  In particular, start with [Bioinformatics for Newbies](http://bit.ly/38jnxnK).

User issues, if not brought up in the before-mentioned [Facebook group](https://www.facebook.com/groups/ConsumerWGS/), should be raised in the local [user issues section of this GitHub site](https://github.com/WGSExtract/WGSExtract.github.io/issues). The issues section is preferred so code bugs, use limitations and suggested improvements can be tracked within the development project.

There is a separate [Facebook group for Developers and Alpha testers](https://www.facebook.com/groups/wgsedev) where bleeding edge issues are discussed and tested before wider availability.  Developer's should visit the main GitHub [WGS Extract Developers Code Repository](https://github.com/WGSExtract/WGSExtract-Dev/) as well.  Development issues, code bugs and limitations should be [raised in the development issues section](https://github.com/WGSExtract/WGSExtract-Dev/issues) so they are tracked till resolved in a release. The manual contains many suggested improvements if you want to take a stab at modifying and improving the code. If the latest release is not checked in to GitHub, simply download the latest release and start from there. Look in the **Program** folder for the **Python** source files.

With v4, we have opened the following three release tracks to all: Beta, Alpha and Dev(eloper).  Chose the installer for the track you wish to be on. Then simply rerun the installer when you are ready for an update to get the latest available release for that track. Developer releases are every few weeks and minimally tested. Alpha releases every one to few months and tested on each release platform with some key, new features not yet complete.  Beta releases are every quarter to year and extensively regression tested and self consistent in their feature set.

If you want to change release tracks at anytime, simply edit the release.json file in the installation directory to change to the desired release track and then rerun the installer. Or overlay the new installer downloaded from above onto your existing installation. The only difference in each installer is the release.json file and its track setting inside. Your current, installed version is displayed at the top of the program when run.

We bring you v4 some 13 months after v3.  The original, first 2 years [v1 and v2 historical release](https://github.com/WGSExtract/WGSExtract-Historical) from Marko is documented there. v3 went into Alpha on the 18th June 2020 and was finally released as Beta on the 15th June 2021. v4 entered Alpha on 1 April 2022 and has yet to be formally Beta released.

This page is located at [https://WGSExtract.github.io/](https://WGSExtract.github.io/) and serves as the WWW home for the tool. As the need develops, we will create our own Facebook Group for users to raise issues outside of the local [User Issues Section](https://github.com/WGSExtract/WGSExtract.github.io/issues) already mentioned.

# Supported Platforms
64 bit OS and processor platforms tested as part of the release process are:
* Microsoft Windows 10 and 11 on Intel and AMD 64 bit processors; WSLG in Win11 looks promising but is not fully supported yet.
* Apple MacOS 10.15 (Catalina), 11 (Big Sur), 12 (Monterrey) and 13 (Ventura) on Intel and Apple M1/M2 processors. (note: We rely on Macports which has dropped support for Mojave and earlier already)
* Ubuntu Linux LTS 18.04, 20.04, and 22.04. We recommend 22.04 to get the latest Samtools release. (note: 18.04 is deprecated by many bioinformatic tool ports already.)

The tool has the potential to be a simple install in a [BioConda environment](https://anaconda.org/bioconda) as it is mostly just a [Python package](https://www.python.org/). But a majority of our users are on Microsoft Windows 10/11 systems. Bioconda nor the bioinformatic tools are supported there. So we currently deliver the tool with our own installer and Windows executables. This may change going forward after we find a Windows package manager to separately supply the bioinformatic tool ports we currently create. This is the only source of recent bioinformatic tool releases on a Windows system (that we are aware of). Docker packages are either not usable across all the platforms or too ineffecient for these large file and program needs. But could play a role in the future.

# Thanks
* To the [JetBrains / PyCharm community](https://www.jetbrains.com/pycharm/) for the support of a Pro developers license to this and other open-source projects
* To the [Github community](https://github.com/) for their free support to open source projects like this one

# Windows Release Users
Some have downloaded the **WGSE** tool solely to gain access to the Win10 native executables of the Bioinformatic Tools that we make available.  These are installed on Windows systems.  You can use these Bioinformatic tools independently after installing the **WGS Extract** program on Windows.  Look in the cygwin64/usr/local folder for all the bioinformatic tools. Just add cygwin/bin and cygwin/usr/local/bin to your PATH to make the programs available in the command line of CMD, Powershell or the native BASH there. 

In v4, this is a full, BASE environment of Cygwin64 captured as of the stated release date.  The bioinformatic tools are compiled to this same versions on that release date. So do not update the cygwin64 libraries direftly else the bioinformatic tools may break.

The CygWin64 tools natively compiled to a Windows platform can be slower than native Linux binaries on the same platform.  The Windows **WSLG** environment with Ubuntu Linux using the Linux versions of the bioinformatic tools can be installed and used also.  Once **WSLG** becomes more complete and supported in Windows 11, we will likely avoid delivering Windows executables all together and simply ask Windows users to install and use **WSLG** for running **WGS Extract**. At which time we can consider becoming a Bioconda package as well.  We do not provide support for the use of **WSGE** on **WSLG** at this time. Recent changes in the **WSL2** file system in the last year finally made **WGSE** possible and generally faster than the Cygwin64 native binaries. This occurs because the Windows kernel cannot support some fundamental features from Unix / Linux that the bioinformatic tools rely on (e.g. memory mapped files).

```
SHA256:   TBD
 *WGSExtract-Alphav35_31Jul2022_installer.zip (may not be same version available above)
MD5:      TBD
 *WGSExtract-Alphav35_31Jul2022_installer.zip  (may not be same version available above)
```
[More information is available on using hashes to verify the download](https://www.howtogeek.com/67241/htg-explains-what-are-md5-sha-1-hashes-and-how-do-i-check-them/)
