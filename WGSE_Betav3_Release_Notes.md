# Release notes Beta v3 10 Jul 2021.
These notes here are in the `WGSE_Betav3_Release_Notes.txt` file installed with the software. They should give you a more comprehensive list of changes since Beta v2.

Your installed v3 release version is dated and displayed in the banner when you start the program.  If your date is before the latest shown above, then you likely want to update your software.  To update, simply delete the **program/** folder in your installation directory.  Download the new release installer, unzip and copy it over files in your old installation folder. Then run the appropriate **Upgrade_yourOS** script file.  This will update you to the latest release.

Releases are shown newest first and back to the initial **Beta v3 release of 15 June 2021**.

# **10 Jul 2021**:
* Reworked Upgrade_UbuntuLinux.sh (all platforms) and reference/genomes/get*sh to create single new script (get_and_process_refgenomes.sh) with 17 choices instead of just yes/no in old Upgrade*sh script. Removed all the individual get_ref*sh scripts introduced in the 30 Jun 2021 release.
* Restructured install of WGS Extractv3 to create, from scratch, the win10tools/tmp and temp/ folders (even though in release .zip) so bad ACLs on previous installs do not propagate.
* Fixed minor bug in process_reference_genomes.sh that prevented handling multiple file parameters correctly
* Added -y option to win10 python self-extracting archive command in Upgrade_UbuntuLinux.sh so it does not give the user an option of changing the download location
* Minor refactoring of some internal names

# **30 June 2021**:
* Align and Unalign button added to GUI **Analysis** tab in new FASTQ frame.  This adds new request pop-ups for needed parameters and generalizes the sub-functions of the BAM Realign button.  Align works off if any FASTQ file(s) specified and allows any of the 10 reference genomes to be chosen to make the target BAM or CRAM.
* Reference Genome selector window expanded and cleaned-up; Build number added to description string; mainly for the Unknown Reference Genome.
* Oxford Nanopore BAM / CRAM / FASTQ processing finished.  Mainly, added the minimap2 alignment command for the Align FASTQs button. Minimap2 is already part of Win10tools; added to the Ubuntu Upgrade script.  Minimap2 is not available in MacOS (not in any package manager we have found)
* Added individual get_and_process scripts for each of the 10 reference genomes in the reference/genomes folder. For when you do not want to run option (1) to download all ten files. Can run the individual script for a particular reference gebine for when the tool reports the file is missing. Eventually this will all be moved into Python code and be done dynamically on demand. Also added -EBI versiobs of scripts for the 4 1K Genome models located on NIH servers.  The EBI scripts uses the EBI copy.  NIH servers seem to give problems to some in the EU.  EBI servers tend to be problematic for most others.  Gives one the option to try one or the other now.
* Refined the memory calculator for the samtools sort command to use 10% less of the available memory; then divided by the number of OS CPU processors available. Required adding psutil to the Python PIP library and as part of the install / upgrade.
* Reduced valid CombinedKit (zip'ped) metric from 5 MB to 500 KB (to better support Teemu doing ad-mixture analysis on aDNA samples)
* Numerous minor refactoring (e.g. in mainwindow names) and latent introduced bugs (e.g. in DEBUG_MODE unsort command) completed.

# **15 June 2021**:
Initial Beta v3 release.  List major changes from Beta v2 (18 Feb 2020).

A key new feature is the tool can take in a BAM or CRAM and all functionality works with either specification.  Also, you can use the tool to convert from one file format to the other. By any BAM, we include subset ones.  Not just WGS. FamilyTreeDNA BigY-500 and -700 BAMs.  Like Y- or mtDNA-only BAMs you create with the tool. All are accepted and used.

Another key feature is the ability to re-align your BAM to a new reference model.  Results may not be as robust and complete as delivered by your WGS test vendor.  But is a start at offering comparable files with more options. Key is, it allows you to convert from Build 37 to 38 or back. Microarray file generation works best from Build 37. Y Haplogroup work from Build 38. Now you can do both in the tool.

The stats area has been dramatically reworked and added to.  Measures are made without including the 'N' values in the reference model.  This represents around 5% in both Build 37 and 38; and is over 50% of the Y chromosome itself.  So the values are now more accurate to what is really possible from the reference model.  Y now appears more accurate for the read depth actually available.  Additionally, the initial stats are delayed if not taking just a second to run (for an un-indexed BAM or any CRAM). And two new additional stats buttons are in the stats page itself. One to calculate the breadth of coverage and one to calculate stats for the WES (Exome) portion of the BAM / CRAM.  The latter important for WGZ testers from Dante Labs.

There are many performance improvements.  For example, where possible, we look to see if a key intermediate file is available.  And if so, reuse it so significant time can be saved from having to regenerate it.  The CombinedKit with the microarray file generator is one key place this occurs.  We have also added functionality to determine the number of processor cores and specify the use of them if a benefit can be gained. Another area is creating the FASTQ from the BAM for realignment. Or the reference model index needed for alignment.

A save button has been added to all results screens (copy-paste of text still not possible).  And they are all labeled with the BAM / CRAM file used to generate them as well as tool version used to create them.

Settings are now saved and restored when restarting the tool. Saving time in operating the tool after a break.

Proper, more complete and robust installers have been built for the three platforms.  It is a constant catch-up with Apple as they keep changing what tools like this from outside their Apple Store are allowed to do.  So much so it becomes near impossible to have a single program / script that works on multple OS versions. Please be patient if you discover one of these changes before we have a chance to diagnose and fix it. We removed the use of pre-compiled Applescripts and added .command "single click" files for MacOS.

The previous release was a 5 GB download. The actual Python and Bash shell script source code is only a little over a megabyte.  With reference data files for the Microarray generator and yleaf needing another 80 megabytes (compressed).  The vast majority of that download was the human genome reference models (5 at just over 1 gigabyte each).  And the Win10 bioinformatic and python tool release.  We now download as much of this as possible either during install or only on demand.  We also have a script to take your old installation and transfer any of these large files that may be needed so they do not have to be downloaded again. The initial download is simply the installer scripts.

Here is a mapping of the basic, standard reference genomes between the v2 and v3 releases:
| Beta v2b (18 Feb 2020) | Beta v3 (15 Jun 2021)           | Notes
| ---------------------- | ------------------------------- | --------------------------------------------
|hs37d5.fa.gz            | `*`                             | (no change)
|human_f1k_v37.fasta.gz  | `-`                             | (no change) ; not ever used
|GCA_000...set.fna.gz    | `*` hs38.fa.gz                  | renamed
|`-`                     | `-` hs38dh.fa.gz                | added, aka GRCh38_full_analysis...hla.fa.gz
|hg19.fa.gz              | `-` hg19_wgse.fa.gz             | renamed, in error and should not be used
|`-`                     | `*` hg19_yseq.fa.gz             | added, replaces earlier hg19.fa.gz
|`-`                     | `*` hg19.fa.gz                  | added, only true Yoruba hg19 model
|hg38.fa.gz              | `*`                             | (no change)
|`-`                     | `**` Homo_sapiens.GRCh37...fa.gz| added, only true EBI numeric-SN / GRCh models
|`-`                     | `**` Homo_sapiens.GRCh38...fa.gz| added, only true EBI numerc-SN  / GRCh models

`*` marked v3 models are the core, base ones that should be used most often.  `-` dash marked ones are there but likely not needed unless dealing with some ancientDNA that used them.  `**` marked models are new and the only numeric-Sequence-named models that some historically called 'GRCh'.

This adds 5 new models and nearly 5 GB more of space.  Two of the old models should not be useed. They need only be saved if you used them outside of the WGS Extract v2 program (your own tool runs with samtools directly).

Although the UI appears very similar, the tool has, for the most part, been rewritten underneath. This to dramatically improve performance, remove spurious bugs throughout, and is more robust with an expansion of functionality.  We hope to improve the UI in the next release. The program went from 1600 Source Lines of Code (SLoC) to well over 6500 now. All the old code was refactored or rewritten.

This release started the day the old Beta v2 release was delivered on 18 February 2020.  And includes the patches made to that release over the next few months.  While we had hoped for a v3 release in June 2020 (and we did make an internal one), inevitable delays made us take another 12 months.  The largest issue was working to expand the code to handle any BAM (or CRAM) thrown at it. Many have started processing AncientDNA samples; which come in all varieties of formats and reference models.  We scoured the Internet and found well over 150 different reference models that BAMs have been aligned too.  We had to work to catalogue and characterize them. This is still a work in progress.

More detailed bullet notes on changes in this Beta v3 15 June 2021 release since Beta v2 18 Feb 2020:
(Taken from the Beta v3 manual forked on 15 June 2020 with ~~strike-through~~ suggested changes listed at the end. Removed from there once added here.)
* Added programs/tmp folder to Win10tools release to resolve BASH not finding /tmp error.
* Downloaded yleaf original .py's and undid many unneeded changes.  Also incorporated yleaf v2.2 upgrade to handle CRAMs. We still have many changes; some of which can be back ported into the yleaf master.
* Modified MacOS install to not check for dot, not install graphviz, and auto install python3 and macports
* Heavily modifed MacOSX and Ubuntu Linux start scripts; renamed to Install_xxxxx.sh
* All files and paths are quoted everywhere. So embedded spaces are now allowed everywhere.
* The tool incorrectly identified BAMs based on the GCA*fna.gz reference model (aka hs38.fa.gz) as being GRCh38 (meaning, EBI Numeric naming) when it in fact is HG "chrN" naming.
* Pop-up warning on non-hs37d5 based models in microarray generation adjusted for clarity
* Stats adjusted for the N's in the reference model.(note: N's in the BAM stream are not yet analyzed and reported on)
* As part of generalization for CRAM use, determine and specify the CRAM reference model where needed.  Also know about and create the CRAM Index file (.crai). Note that the .crai is not the same as a .bai. In particular, samtools idxstats cannot operate off the .crai and so takes scanning the full CRAM to generate results.
* Added a BAM to CRAM and CRAM to BAM button
* Generalized and fixed BAM to FASTQ unaligner. No longer using deprecated samtools bam2fq feature and instead samtools fastq one.
* Changed use of samtools mpileup (deprecated) to bcftools mpileup.
* Moved haplogrep jar file from standalone folder to new jartools folder (similar to parallel win10tools folder for Windows 10 executables). For future expansion to add GATK, etc. Updated to v2.2 as well.
* Updated yleaf v2.1 to 2.2 and back ported many changes and fixes added here
* Generalized all result windows to use common form. Added a Save and Close button to all.  Added a BAM file name, WGS extract tool version and current time/date stamp to all.
* Major cleanup of Y Haplogroup output page.  Added ISOGG tree button.  Cleaned up pop-up for more than 3 SNPs to more compactly present long lists of SNPs.
* Major cleanup on stats pages.  Added LOCALE numeric printing, scale factors on values (K, M).  Added Other to capture rest of sequences.  Fixed many bugs; especially when subsetted BAMs supplie. Added more newly determined stats like number of sequences, reference model refinement, size of file, content of file (Auto, X, Y, Mito, unmapped). Clarified RAW versus MAPped values.
* Added tool version and release date to main banner at top. Added button to get to WGS Extract manual.  Moved exit button there instead of at bottom of screen.
* Cleaned up and created Class for handling temp directory. Fixed deletion of entries; especially for directories like the yleaf one. 
* Added DEBUG feature to provide more robust reporting, prevent deletion of TEMP directory entries when on, etc. 
* All windows have explicit close / exit buttons and handle cleanup in such cases consistently
* Tried to clarify and reduce amount of text, in general, to be more precise
* Added, more explicitely, the recommended files in the Microarray tool (Renamed from Autosomal to Microarray tool also.)  Added "select recommended" button and explicit close button.
* added -B option to mpileup calls to support Nanopore Long read files
* French language translation / form added (thanks François Boucher for translation). Portugese and Finnish also in process.
* Major rewrite and expansion to create new install scripts.  Simplified start scripts to just tool invocation
* Detect and indicate when BAM is not sorted nor indexed.  Add buttons to sort and/or index the BAM. Removed required to automatically invoke or do before stats call. Do give pop-up warning if not there.
* Cleaned up settings tab (first, main tab) to bifurcate settings BAM file support into separate frames.  Expanded data reported on BAM.  Added many BAM-specific buttons such as STATS (moved from last tab Analysis), Sort, Index, To/From CRAM, realign and show header.
* Settings now saved and restored with each run.  So language remembered and restored without asking.  Added language button to settings frame of main tab to change language once set.  Added Reference Library and Temporary Files buttons to change from default installation location; if user wishes to move to more optimum location.  Last used BAM file and Output directory saved and restored; including any stats on the BAM.
* Added button to generate Yonly VCF file (from BAM; not the simpler subset from existing VCF). Add annotation although not required for feeding Cladefinder or yFull.
* Upgraded to newer 3.7.7 Python (from 3.7.3). Still using standalone WinPython "zero" release that does not require Windows installer. Removed from general release and handled directly by Win10 installer. Still retained 32 bit version (found issue with 64 bit portability still). Also found issues with 3.8 and 3.9 on Win10 (partly with PIP libraries) and so stayed with 3.7 Issues during Alpha testing with 3.7.7 and some libraries that were since upgraded force a Win10 upgrade to 3.8.9.
* Re-ported HTSLib tools (at first 1.10, then 1.11 and now) 1.12. All are 64bit now (new requirement for handling CRAMs).  Was v1.6 and v1.4 on Cygwin32 and MinGW64 before (using htslib 1.9 though).
* PIP upgrades to all packages relied on (Pillow 6.0.0 to 7.2.0, Pip from 19.x.x to 20.1.x, numpy and pandas used by yleaf (versions?), and removed items not needed that were left over in release (python-dateutil, pytz, setuptools, six).
* Added a generalized Please Wait to all calls of subprocesses. Gives tool running and estimated time. (Need to add a cancel button. Need to modify time based on # procs, speed of CPU and size of BAM)
* inlined "extract23" script variant used and greatly simplified.
* improved generated file names to remove extraneous text.  Some had over 25 characters added to a file name.
* Code refactored in major ways through out. More robust in handling of file names to clearly demarcate native OS versus generic path.  Also quoting all paths.  Use "with open ... in" block instead of f.open, f.close, conditional expressions, f-strings instead of formats, lines limited in character length, used multiline string auto concatenation instead of multiple assignments with +=. Code modularized and many modules placed into classes that get initialized. Setup single global variable (settings.py) file that all can share in a common way (wgse.xxxxx)
* greatly simplified and pulled into python code the processing of a bam header, bam body and idxstats run.
