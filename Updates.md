Updates to the current release that were made since the Beta v3 release of 15 June 2021.  These notes here along with the Release Notes should give you a more comprehensive list of changes since v2.

Your v3 release is dated and posted in the header when you start the program.  If your date is before the latest shown on the home page here, then you likely want to update your release.  To update, simply delete the **program/** folder in your installation directory.  Download the new release installer and place in your same installation folder. Then run the appropriate **Upgrade_yourOS** script file.  That will upgrade you to the latest release.

Release Notes since the initial v3 15 June 2021 release (newest first):
**30 June 2021**:
* Align and Unalign button added to **Analysis** tab in DEBUG_MODE.  Actually, was there internally as the Realign called them both. Simply completed the GUI to call them by buttons.  This included adding new request windows for missing data in the stand-alone Align button.  Align works off any fastq file(s) specified and allows any of the 10 reference genomes to be chosen.
* Reference Genome selector expanded; Build number added to description string; mainly for the Unknown Reference Genome.
* Oxford Nanopore BAM / CRAM / FASTQ processing polished off.  Mainly, added the minimap2 alignment command instead of BWA for those FASTQs. Minimap2 already part of Win10tools; added to Ubuntu Upgrade script.  Not available as package in MacOS (and not trying to compile locally so not available)
* Added individual get_and_process scripts for each of the 10 reference genomes in the reference/genomes folder. For when you do not want to run option (1) to download all ten files. Can run the individual script for when the tool reports it is missing a specific reference genome on a command you wish to run. Eventually this will all be moved into Python code and be done dynamically on demand.
* Refined memory calculator for samtools sort command to use 10% less of the available memory; then divided by the number of OS CPU processors available. Required adding psutil to the Python PIP library.

**15 June 2021**:
* Initial Beta v3 release.  See the release notes in the install directory for major changes from Beta v2 (18 Feb 2020).
