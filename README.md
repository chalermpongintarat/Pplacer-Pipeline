# Pplacer-Pipeline
Adapted by Chalermpong Intarat

NBT, NSTDA

chalermpong.int@biotec.ot.th

Nov 20, 2019

Installation Software:
1. Do a command line introductory course, if needed. For Mac, I did Macheads101 on Youtube. This will help you to figure out how to install the software. For a more advance writing scripts etc:
http://mywiki.wooledge.org/BashGuide
optional: do a python intro course, f.e. 'learn python the hard way' or 'python­Code academy'
2. Install anaconda (Python) https://docs.continuum.io/anaconda/install
3. Install a texteditor to work your code. I am using textwrangler. I installed the command line tools. You can run .py code directly from here. For new text file just type "edit
terminal, or .py for python. To run python script type "python namefile.py"
4. Install alignment program MAFFT http://mafft.cbrc.jp/alignment/software/macstandard.html
You can also run alignments through guidance2.0 online. Will help you identify unconserved regions.
5. Install homebrew. To do so, type in your terminal:
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
6. Install GSL1.16 through homebrew (needed for PPLACER to run)
brew install gsl
7. Download and unzip pplacer­Darwin­v1.1.alpha17 from https://github.com/matsen/pplacer/releases/tag/v1.1.alpha17 place PPLACER, GUPPY and rppr binaries in $PATH. I just copied them into
usr/local/bin
8. Install raxML (slow) and fasttree (fast) for building of trees and log files
9. Install taxtastic to build and maintain reference packages
https://github.com/fhcrc/taxtastic
This will also automatically also install biopython 1.66
10. Install Jalview to look at alignments (you need to have java installed, go to apple to download). Open Jalview from website
javaws http://www.jalview.org/webstart/jalview.jnlp -open yourFileName
11. Install HMMER 3.1b on computer (http://hmmer.org/). The manual has a tutorial. To run HMMbuild, your alignment has to be transformed from fasta format to Stockholm HMMofFasta. You can use little package called bioscripts converter to do this job. You can also run HMMbuild on MSF file, see http://bioinf.ibun.unal.edu.co/cursos/Course0 Jalview can convert alignment in MSF format
12. Install seqmagick to remove duplicate sequences, quickly change between sto and fasta files, etc. http://seqmagick.readthedocs.org/en/latest/
13. Install Guidance2.01 http://guidance.tau.ac.il/ver2/source.php. Lots of warning messages when compiling, not yet curated for Mac...
14. Install R and biostrings. In R, type:
source("https://bioconductor.org/biocLite.R") biocLite("Biostrings")
15. Install guidance2.0: need to install bioperl first, is a bit complex... still needs to be done
16. Install prottest and make RaxML tree
17. Install NCBI edirect to fetch and search NCBI from the command line. http://www.ncbi.nlm.nih.gov/books/NBK179288/
cd ~
perl -MNet::FTP -e \
'$ftp = new Net::FTP("ftp.ncbi.nlm.nih.gov", Passive => 1); $ftp->login; $ftp->binary; $ftp->get("/entrez/entrezdirect/edirect.zip");'
unzip -u -q edirect.zip
rm edirect.zip
export PATH=$PATH:$HOME/edirect ./edirect/setup.sh
efetch -help

References:
  1. https://github.com/matsen/pplacer
  2. http://armbrustlab.ocean.washington.edu/node/346
