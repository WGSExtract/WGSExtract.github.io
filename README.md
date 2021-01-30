# WGS Extract
a desktop tool for verifying, analyzing and manipulating your **DTC 30x [WGS](https://h600.org/wiki/WGS) test** results

__Current release__ is Beta v2b (18 Feb 2020):
* **WGS Extract** [Manual (Google Doc)](http://bit.ly/36Jdpnq)
* **WGS Extract** [Download Release (5 GB)](http://bit.ly/3afRl6O)
```
SHA256: 41D68ED9ABEAAD0AA6BB68F3043294DC02F5DD17E28F86BB776C56704148F76C
MD5: 690C3C6D5CFBF745114D1690C4C00065
```
[More information on hashes used to verify the download release is available](https://www.howtogeek.com/67241/htg-explains-what-are-md5-sha-1-hashes-and-how-do-i-check-them/)

**`IMPORTANT`**: [MacOSX Release Patch](https://github.com/WGSExtract/WGSExtract-Dev/blob/master/Docs/Betav2b_MacOSX_patch.md) is available for Version Beta v2b.  Fixes the install and start scripts of the program. Adds an Unintall as well. (v1 on 25 April 2020, v3 on 20 Jun 2020, v5 on 31 Oct 2020)

**`Note`**: [Français Language Patch](https://github.com/WGSExtract/WGSExtract-Dev/blob/master/Docs/Betav2b_Francais_Patch.md) is available for Version Beta v2b.  Adds Français language support to the existing English and Deutsch language support. (1 May 2020)

**`Note`**: If working with a Nebula Genomics CRAM file, please [check the CRAM to BAM conversion document](https://bit.ly/31TeqYH). The next release will handle CRAMs and BAMs interchangeably.

This tool is geared toward the needs of [genetic genealogy](https://h600.org/wiki/Genetic+Genealogy) but may be helpful for this looking into health-releated uses of WGS tests. The **sub-$500, Direct-to-Consumer (DTC), 30x Whole Genome Sequence (WGS) tests** are delivered with basic data files and often some health-related reports. This tool serves to bridge the gap between the [WGS files](https://h600.org/wiki/Sequencing+File+Formats) delivered and the present day [genetic genealogy community tools](https://h600.org/wiki/Third+Party+Analysis+Tools). 

This tool is designed to be a simple, push-button manipulation of [WGS files](https://h600.org/wiki/Sequencing+File+Formats) from any source. It hides the scripting of complex bioinformatic tools in the background and automatically determines needed parameters and variances for the data supplied it.  For more control over your pipeline, either learn to use the underlying tools directly in a command shell or seek a Galaxy server (such as [UseGalaxy](https://usegalaxy.org/)).

The tool has the potential to be a simple install in a BioConda environment or even as a simple Python package. But as a majority of the users are on Microsoft Windows 10 systems, and the underlying tools are often not available there, we currently deliver the tool as a more complex, install everything approach. This may change going forward after we find a Win10 package manager to supply the bioinformatic tool ports from. We do fully test and use the Linux and Apple MaxOS versions. This is the only source of the bioinformatic tools on a Win10 system (that we are aware of).

We use the Facebook group [Dante Labs and Nebula Genomics Customers](https://www.facebook.com/groups/373644229897409/) for discussions on how to make use of your **sub-$500, DTC 30x WGS test** results. Bugs, use cases and announcements about this tool happen there.  As part of that Facebook groups' Files section, you will find a number of useful companion documents and tool references.  In particular, start with [Bioinformatics for Newbies](http://bit.ly/38jnxnK). 

User issues, if not brought up in the [Facebook group](https://www.facebook.com/groups/373644229897409/), should be raised in the [user issues section of this site](https://github.com/WGSExtract/WGSExtract.github.io/issues). This issues section is the preferred location so code bugs, use limitations and suggested improvements can be tracked within the development project.

The tool acronym is **WGSE** and is pronounced as "wig-see". We encourage this use in English language conversation.

Further documentation beyond the manual link above is available in our [WGS Extract Developer's Documentation Repository](https://github.com/WGSExtract/WGSExtract-Dev/tree/master/Docs).

Developer's should visit the main GitHub [WGS Extract Developers Code Repository](https://github.com/WGSExtract/WGSExtract-Dev/).  Development issues, code bugs and limitations should be [raised in the development issues section](https://github.com/WGSExtract/WGSExtract-Dev/issues) so they are tracked till resolved in a release.

The original, first year, [historical release is documented here](https://github.com/WGSExtract/WGSExtract-Historical).

This page is located at https://WGSExtract.github.io/ and serves as the new WWW home for the tool. Once the new version without the reference models is released for distribution here, the historical IP-number site link given above will go away. The current manual link of http://bit.ly/36Jdpnq will be redirected to this page as a more permanent link as well. As the need develops, we will create our own Facebook Group for users to raise issues outside of the [User Issues Section](https://github.com/WGSExtract/WGSExtract.github.io/issues) already mentioned.
