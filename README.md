# WGS Extract Version 3 Beta
a desktop tool for verifying, analyzing and manipulating your **DTC 30x [WGS](https://h600.org/wiki/WGS) test** results

__Current release__ is **Beta v3 (15 Jun 2021)**:
* **WGS Extract** [Manual (Google Doc)](https://bit.ly/35IziTY)
* **WGS Extract** [Download Installer (28 KB)](https://bit.ly/2RTk0JL)  **Installer only**  ([Onedrive backup](https://1drv.ms/u/s!AgorjTSMFYpjfBqqcwdiHPk_g6U?e=P1RESj))
* **WGS Extract** [Download Full Release (265 MB)](https://bit.ly/2Tu2jRk)  **Full Release** (normally grabbed by Installer,  ([Onedrive backup](https://1drv.ms/u/s!AgorjTSMFYpjfYGzVGVuJQeZKOk?e=mauOSR))
```
SHA256: 
fdbdfbd4dc4b2601b63287af3781a772183329f13806038f7d884a2c30f5b7fd *WGSExtract-Betav3_15Jun2021_installer.zip
437bf494b0f89f865e4cf59c966ab8f1c156d8ca298aa0f182d9b803c3b889d6 *WGSExtract-Betav3_15Jun2021_Full.zip
MD5:
ea348682c1b3eb76fa43d2df759aa16d *WGSExtract-Betav3_15Jun2021_installer.zip
02726af1630bc2e5aec83823a356de9e *WGSExtract-Betav3_15Jun2021_Full.zip
```
[More information on hashes used to verify the download release is available](https://www.howtogeek.com/67241/htg-explains-what-are-md5-sha-1-hashes-and-how-do-i-check-them/)

Finally, 16 months after the Beta v2 release, we bring you our Beta v3.  If you have any version installed, you can overlay the Installer scripts in the same directory and they will work to save the large reference genome files for reuse so you can avoid the large download.  See the 00README.txt, Release Notes and [Manual (Google Doc)](https://bit.ly/35IziTY) for more information. The installer grabs locally hosted files from Microsoft Onedrive.  The links above are to  Google Drive. (OneDrive no longer supports Bitly shortened links.)

Still waiting for your WGS test results?  Want to get started today?  See the [International Genome Sample Resource (1K Genome archive)](https://www.internationalgenome.org/data) for BAM files that you can download and play with to learn the tool while waiting for your results.

This tool is geared toward the needs of [genetic genealogy](https://h600.org/wiki/Genetic+Genealogy) but may be helpful for those looking into health-releated uses of WGS tests. The **sub-$500, Direct-to-Consumer (DTC), 30x Whole Genome Sequence (WGS) tests** are delivered with basic data files and reports. This tool serves to bridge the gap between the [WGS files](https://h600.org/wiki/Sequencing+File+Formats) delivered and the present day [genetic genealogy community tools](https://h600.org/wiki/Third+Party+Analysis+Tools). Many health analysis sites accept the microarray and VCF files generated here as well.

This tool is designed to be a simple, push-button manipulation of [WGS files](https://h600.org/wiki/Sequencing+File+Formats) from any source. It hides the scripting of complex bioinformatic tools and automatically determines needed parameters and variances for the data supplied it.  For more control over your pipeline, either learn to use the underlying tools directly in a command shell or seek a Galaxy server (such as [UseGalaxy](https://usegalaxy.org/)).

We use the Facebook group [Dante Labs and Nebula Genomics Customers](https://www.facebook.com/groups/373644229897409/) for discussions on how to make use of your **sub-$500, DTC 30x WGS test** results. Bugs, use cases and announcements about this tool happen there.  As part of that Facebook groups' Files section, you will find a number of useful companion documents and tool references.  In particular, start with [Bioinformatics for Newbies](http://bit.ly/38jnxnK).

User issues, if not brought up in the [Facebook group](https://www.facebook.com/groups/373644229897409/), should be raised in the [user issues section of this site](https://github.com/WGSExtract/WGSExtract.github.io/issues). This local issues section is the preferred location so code bugs, use limitations and suggested improvements can be tracked within the development project.

The tool acronym is **WGSE** and is pronounced as "wig-see". We encourage that use in English language conversation.

Developer's should visit the main GitHub [WGS Extract Developers Code Repository](https://github.com/WGSExtract/WGSExtract-Dev/).  Development issues, code bugs and limitations should be [raised in the development issues section](https://github.com/WGSExtract/WGSExtract-Dev/issues) so they are tracked till resolved in a release.

The original, first 2 years, [historical release is documented here](https://github.com/WGSExtract/WGSExtract-Historical).

This page is located at https://WGSExtract.github.io/ and serves as the new WWW home for the tool. As the need develops, we will create our own Facebook Group for users to raise issues outside of the [User Issues Section](https://github.com/WGSExtract/WGSExtract.github.io/issues) already mentioned.

The tool has the potential to be a simple install in a BioConda environment as it is a Python package. But as a majority of the users are on Microsoft Windows 10 systems, and Bioconda nor the underlying bioinformatic tools are not available there, we currently deliver the tool with our own installers. This may change going forward after we find a Win10 package manager to supply the bioinformatic tool ports we develop here. We do fully test and use the Linux and Apple MaxOS versions; on Intel, AMD and Apple M1 (Arm) architectures. This is the only source of the bioinformatic tools on a Win10 system (that we are aware of).

**Win10 Release Users**
Some have downloaded the tool solely to gain access to the Win10 native executables of the Bioinformatic Tools that we make available.  These are installed as part of the Win10 Installer package.  They rely on locally sourced blobs that you can download and use without installing the whole **WGS Extract** program; if you desire. Note that the licenses are part of the **WGS Extract** program.

* **Win10 [CygWin64 partial](https://drive.google.com/file/d/1lYZbFJ3eyDps7e4I_Yu4zVyZz_vjjVcd/view?usp=sharing)** environment (11 MB); minimal to support the Bioinformatic Tools and WGS Extract installer
* **Win10 [CygWin64 Bioinformatic](https://drive.google.com/file/d/1xf24oYYieU6SuiNFkrHG01qNwyJXZdKE/view?usp=sharing)** tools (43 MB); hstlib, samtools, bcftools, bwa, etc
* **[Merge of the above two](https://bit.ly/3epnGeQ)** tool sets (56 MB); already overlaid and combined as happens during installation)
* **Win10 [CygWin64 full](https://bit.ly/2TtArgn)** environment (46 MB); minimal CygWin64 install but the full, basic CygWin64 release with matching DLL versions for the above Bioinformatic tool release. As of June 2021, the release includes htslib 1.12 from April 2021.
The third will get you everything delivered with **WGS Extract**. The fourth a better, fully working BASH environment to use the bioinformatic tools in.  You will need to merge the two to get both.  These are all provided as a convenience with no support or warranty.
```
$ md5sum *.zip
0898dba22b4d7c074a203e49a12f70ad *win10tools-1.12.zip
6a347e44667eb7320868cb7688b870c6 *win10tools-bioinfo1.12.zip
9ef4829ed8cdccfcbda7139a67fe3c2c *win10tools-cygwin64-full.zip
cf67ef5fe86db0837f71f7847b91db08 *win10tools-cygwin64.zip
$ shasum -a 256 *.zip
f956dc197ad89ccd0ab1345abc89559f492059d26f20a444d7f1ddec31225557 *win10tools-1.12.zip
a160a7930e06b984b547a071cfa742d6538089e2fcc7ae1b1ac3644bc1ae6bdd *win10tools-bioinfo1.12.zip
6c1d743dc6176f96ac0fbb6b5fb39e0a0c5db0bcc10742bdc2756993b36f43aa *win10tools-cygwin64-full.zip
0c72aec08091f3f1bd6fb5154d9b0e69b416cf9b0e8dcd145f558dbaf51ac45c *win10tools-cygwin64.zip
```
