# OSX installation

To set up your own computer for today's session, follow these instructions.
Copying and pasting the given code may be the easiest way to make sure everything works.

1. Open a Terminal `Applications -> Utilities -> Terminal`.
2. If you don't have `homebrew` installed, type the following to your terminal. If you *do* have `homebrew` installed, please skip to the next step

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

3. If you haven't installed the commands `sed` and `wget` in the `Bash` workshop last week, then install them now:

```
brew install gnu-sed --default-names
brew install wget
echo "export PATH=\${PATH}:/usr/local/Cellar/gnu-sed/4.4/bin:/usr/local/Cellar/wget/1.19.1_1/bin" >> ~/.bash_profile
```

4. Install NGS tools: `fastqc`, `cutadapt`, `bwa`, `samtools`, `bcftools`, `freebayes`, `sabre`, `IGV`, `picard`

```
brew install fastqc
brew install cutadapt
brew install bwa
brew install samtools
brew install bcftools
brew install freebayes
```

5. Install `sabre`

```
brew install git
git clone https://github.com/najoshi/sabre
cd sabre
make
SABRE_HOME=`pwd`
echo "export PATH=\${PATH}:${SABRE_HOME}" >> ~/.bash_profile
```

6. Download IGV

```
wget http://data.broadinstitute.org/igv/projects/downloads/2.4/IGV_2.4.0.app.zip
```

7. Download `picard`

```
wget https://github.com/broadinstitute/picard/releases/download/2.12.1/picard.jar
```

After completing the above steps, close the terminal then open it again to start.
