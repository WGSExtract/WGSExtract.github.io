# WGS Extract  (WGSE.bio)
is a desktop tool for verifying, analyzing and manipulating your **Personal 30x [WGS](https://h600.org/wiki/WGS) test** result. It can also be used with any human genome based [BAM or CRAM](https://h600.org/wiki/Sequencing+File+Formats) file including [WES](https://h600.org/wiki/WES) and Y-only test results.

**WGS Extract** **User Manual**: [v4 User Manual](https://get.wgse.io/WGSExtract_v4_User_Manual) (Google Doc)

__Latest Releases__ you can install on the [supported platforms](#supported-platforms) are:

| Track | Version | Date | md5 hash signature |
| :--- | :---: | :---: | :---: |
| **[BETA v4](https://get.wgse.io/WGSExtract-Beta_latest_installer.zip)** | 44.2 | 28 Feb 2023 | ab2abb496432d7810f98f6df53ea30bc |
| **[ALPHA v4](https://get.wgse.io/WGSExtract-Alpha_latest_installer.zip)** | 44.3 | 30 Oct 2023 | 1a15c0eeddea162605c4f52f3e76254d |
| **[Dev(eloper) v4+](https://get.wgse.io/WGSExtract-Dev_latest_installer.zip)** | 44.4 | 30 Mar 2024 | 1df34162f0c49c345d744e8fc883b078 |

These are just the installer scripts.  You need to download, unpack and run the installer for your OS. See the **Installation Section** in the [user manual](https://get.wgse.io/WGSExtract_v4_User_Manual) for details about installing on your platform.  See the **v4 Release Notes** in the installation directory for more information about the updates in the current release. You should periodically re-run the installer to update to the latest release in the track you select. There is information available on how to use [hashes to verify the Installer you download](https://www.howtogeek.com/67241/htg-explains-what-are-md5-sha-1-hashes-and-how-do-i-check-them/).
>* (Beta only) Ubuntu 24.04 is not available in this release.  Use the Alpha track to get a working installation for that OS. 18.04 is not available in Alpha and later releases due to the removal of needed libraries. Try the Linux Conda installer available in Alpha and later instead.
>* (Beta only) If you are on MacOS Sonoma (14.xx), then you need to overlay this updated [Install_macos.command](https://raw.githubusercontent.com/WGSExtract/WGSExtract-Dev/master/Installer/Install_macos.command) file onto your current installation (or installer files).  MacPorts cannot gracefully handle the update of the Operating System in their package. And Macports names their packages with the MacOS code name and version (which is not known before hand). The update fixes the new OS issue.
>* (Beta only) When installing or updating, you may see the message "44.2: syntax error: invalid arithmetic operator" when checking for the latest program package.  No worry. When we next update the installer package, it will fix this error and allow the program package to update. We will not update the program package before the installer is fixed for this error.

This tool is geared toward the needs of [genetic genealogy](https://h600.org/wiki/Genetic+Genealogy) and [Ancient DNA](https://h600.org/wiki/Deep+Ancestry) (aDNA) studies but can be helpful for those looking into health-releated uses of [WGS](https://h600.org/wiki/WGS) tests. The **personal, sub-$500, Direct-to-Consumer (DTC), 30x Whole Genome Sequence ([WGS](https://h600.org/wiki/WGS)) tests** are delivered with basic data files and reports. This tool serves to bridge the gap between the [WGS data files](https://h600.org/wiki/Sequencing+File+Formats) delivered and the present day [genetic genealogy community tools](https://h600.org/wiki/Third+Party+Analysis+Tools). Many health analysis sites accept the microarray and VCF files generated by this tool.

>Still waiting for your [WGS](https://h600.org/wiki/WGS) test results?  Want to get started today?  See the [International Genome Sample Resource (1K Genome archive)](https://www.internationalgenome.org/data) for [BAM or CRAM](https://h600.org/wiki/Sequencing+File+Formats) files that you can download and play with to learn the tool while waiting for your results.

This tool is designed to be a simple, push-button manipulation of [WGS files](https://h600.org/wiki/Sequencing+File+Formats) from any source. It hides the installation and scripting of complex bioinformatic tools and automatically adapts based on the data within your files.  For more control over your pipeline, either learn to use the underlying tools or seek out a Galaxy server (such as [UseGalaxy](https://usegalaxy.org/)).

[Dante Labs](https://genome.dantelabs.com), [Nebula Genomics](https://nebula.org/), [Sequencing](https://sequencing.com/), and [YSEQ](https://yseq.net/) are test results most commonly used with this tool. [Full Genomes Corp](https://fullgenomes.com/]), [GeneDX](https://www.genedx.com/), [Sano Genetics](https://sanogenetics.com) and [Veritas (historical)](https://veritasgenetics.com) are other test providers whose output is processed here. These are all results from [Illumina](https://illumina.com) and [MGI](https://en.mgi-tech.com/) next generation sequencers ([NGS](https://h600.org/wiki/ngs)).  Results from [Oxford Nanopore](https://nanoporetech.com/) and [PacBio HiFi CCS](https://www.pacb.com/smrt-science/smrt-sequencing/hifi-reads-for-highly-accurate-long-read-sequencing/) third generation, long-read sequencers can also be used; as can [FamilyTreeDNA](https://familytreedna.com/)'s BigY output. (This is not an endorsement of any company or service; simply reporting what is commonly used with the tool.)

>The tool acronym is **WGSE** and pronounced as "wig-see". We encourage that use in conversation.

We encourage the use of the Facebook group [Personal WGS](https://www.facebook.com/groups/PersonalWGS/) for discussions on how to make use of your **personal, sub-$500, DTC 30x WGS test** results. Bugs, use cases and announcements about the Beta release tool happen there.  As part of that groups' Files section, you will find a number of useful companion documents and tool references.  In particular, see [Bioinformatics for Newbies](http://bit.ly/38jnxnK). We also maintain a number of [corrollary documents](https://h600.org/wiki/Bioinformatics+Documents).

User issues, if not brought up in the  [Personal WGS](https://www.facebook.com/groups/PersonalWGS/) Facebook group, should be raised in the local [user issues section of this GitHub site](https://github.com/WGSExtract/WGSExtract.github.io/issues). The issues section is preferred so code bugs, use limitations and suggested improvements can be tracked within the development project.

There is a separate Facebook group for [WGSE Developers and Alpha testers](https://www.facebook.com/groups/wgsedev) where bleeding edge issues are discussed and tested before wider availability.  Developer's should visit the main GitHub [WGS Extract Developers Code Repository](https://github.com/WGSExtract/WGSExtract-Dev/) as well.  Development issues, Alpha code bugs and limitations should be raised in the [development issues section](https://github.com/WGSExtract/WGSExtract-Dev/issues) so they are tracked till resolved in a release. If you want to take a stab at modifying and improving the code, then the manual contains many suggested improvements. If the latest release is not checked in to GitHub, simply download and install the latest DEVelopers release and start from there. Look in the **Program** folder for the **Python** source files.

There is a separate Reference Genome Library manager that can be run to check and update the library.  The **WGSE** program will check and determine when it needs a genome and prompt you to install any missing file then.  The tool now verifies checksums of all library downloads and final, installed versions. This along with installer and startup activites to check the latest versions of files (and possibly update them), are the only network access requirements to run the tool. Otherwise the tool is standalone. There is an uninstaller to unwind all the changes made by the installer. You should never locate your data files within the installation folder.

v4 entered Alpha on 1 April 2022 and was formally Beta released on 6th November 2022. v5 entered pre-Developer mode release on 10 March 2023 and had a first real release in July then Nov 2023. Old releases are documented in the [historical release section](https://github.com/WGSExtract/WGSExtract-Historical). (v5's release in Dev has been delayed.) 

The tool home page is [WGSE.bio](https://wgse.bio/). With the developers and delivery platform using [WGSE.io](https://wgse.io/) (note the slight difference; they will cross reference each other). Currently, both point to this page located at [https://WGSExtract.github.io/](https://WGSExtract.github.io/). 

# Supported Platforms
64 bit OS and processor platforms tested as part of the release process are:
* Microsoft Windows 10 and 11 on Intel and AMD 64 bit processors using Cygwin64 and soon Msys2 packages for the bioinformatic tools. WSLG in Win11 with a Linux Desktop (not server) can be used to install the Ubuntu or Linux release of this tool.
* Apple MacOS 10.15 (Catalina), 11 (Big Sur), 12 (Monterrey), 13 (Ventura) and 14 (Sonoma) on Intel and Apple M1/M2 processors. (note: We rely on Macports which has dropped support for Mojave and earlier already)
* Ubuntu Linux LTS 20.04, 22.04 and 24.04. We recommend 22.04 to get the latest Samtools release. (note: 18.04 is deprecated by many bioinformatic tool ports and being phased out.)
* Any Linux by using Conda (actually micromamba and bioconda). This will soon deprecate the Ubuntu only installer and is the preferred Linux install method.

The tool has the potential to be a simple install in a [BioConda environment](https://anaconda.org/bioconda) as it is mostly just a [Python package](https://www.python.org/). But a majority of our users are on Microsoft Windows 10/11 systems. Bioconda nor the bioinformatic tools are supported there. So we currently deliver the tool with our own installer everywhere and Windows executables. This may change going forward after we find a Windows package manager (pacman) to separately supply the bioinformatic tool ports we currently create. This is the only source of recent bioinformatic tool releases on a Windows system (that we are aware of). Docker packages are either not usable across all the platforms or too ineffecient for these large file needs. But could play a role in the future.

# Thanks
* To the [JetBrains / PyCharm community](https://www.jetbrains.com/pycharm/) for the support of a Pro developers license for this and other open-source projects
* To the [Github community](https://github.com/) for their free support to open source projects like this one

# Windows Release Users
Some have downloaded the **WGS Extract** tool solely to gain access to the MS Windows native executables of the Bioinformatic Tools we include.  You can use these Bioinformatic tools independent of the **WGS Extract** program.  Look in the cygwin64/usr/local folder for the bioinformatic tools. Just add cygwin64/bin and cygwin64/usr/local/bin to your PATH to make the programs available from the Terminal command line of CMD, Powershell or BASH. If you do not wish to use the rest of the **WGSE** release, just delete everything except the cygwin64 folder and adjust your path for wherever you move the folder. For those using the new Msys2 release, it is the msys2/usr/bin and msys2/ucrt64/bin folders; respectively.

Since v4, this is a full, BASE environment of Cygwin64 that is captured as of the stated release date.  The bioinformatic tools are compiled to this same version on that release date. So do not update the cygwin64 libraries else the bioinformatic tools will break. Msys2 is just a minimal set of tools to operate **WGSE**.

Windows 11 **WSLG** with Ubuntu Linux Desktop (not server) can be used to install and run **WGS Extract**. You have to tune **WSLG** parameters to get effective use of your disk space, CPU cores and memory under WSLG.  This is rarely better than the native Windows executables. The Windows kernel cannot support some fundamental features from Unix / Linux that the bioinformatic tools rely on (e.g. memory mapped files). The WSL I/O performance for files outside its VMDK file space does make the tool slower in WSL than native Windows; in most cases. And will greatly expand your VHDK virtual disk (if you keep your files local) by .5 to 1 TB or larger. This space cannot generally be recovered.
