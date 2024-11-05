**BlutoRS**
-----
**This project is a fork of [Bluto](https://github.com/darryllane/Bluto) by Darryl Lane. The original project appears unmaintained, so this fork named BlutoRS by [ProjectResurrect](https://github.com/ProjectResurrect) aims to continue improving and maintaining it.**
-----
**DNS Recon | Brute Forcer | DNS Zone Transfer | DNS Wild Card Checks | DNS Wild Card Brute Forcer | Email Enumeration | Staff Enumeration | Compromised Account Enumeration | MetaData Harvesting**
 
>Maintainer: ProjectResurrect  |  Email:'contact@boukhrisssaber.tn'

>https://github.com/ProjectResurrect/BlutoRS


## About ProjectResurrect

**ProjectResurrect**  revives and updates powerful, forgotten open-source security tools, helping teams defend against modern threats with proven, trusted resources.


## Versioning

This fork continues from version `v2.4.17` of the original repository. The latest version is `v2.5.0` (details in the changelog).


## Usage

BlutoRS now takes command line arguments at launch, the new options are as follows;

	-e		This uses a very large subdomain list for bruting.
	-api	You can supply your email hunter api key here to gather a considerably larger amount of email addresses.
	-d		Used to specify the target domain on the commandline.
	-t		Used to set a timeout value in seconds. Default is 10

**Examples:** (check the **Running BlutoRS** section below)

	bluto -api 2b0ab19df982a783877a6b59b982fdba4b6c3669
	bluto -e
	bluto -api 2b0ab19df982a783877a6b59b982fdba4b6c3669 -e
	bluto -d example.com -api 2b0ab19df982a783877a6b59b982fdba4b6c3669 -e


## Installation Instructions

**Clone the Repository**

To get started, clone this repository to your local machine:

```bash
git clone https://github.com/ProjectResurrect/BlutoRS.git
cd BlutoRS
```

**Set Up Virtual Environment (Optional)**

It's recommended to use a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```
**Install Dependencies**

Install the required Python packages:

```bash
pip install -r requirements.txt
```

**Running BlutoRS**

Ensure the main bluto script has execute permissions:
```bash
chmod +x bluto

```

Run BlutoRS directly from the cloned directory:

```bash
./bluto --domain example.com
```

**Optional: Create a Symbolic Link for Easier Access**

To use bluto from any directory, create a symbolic link:

```bash
sudo ln -s $(pwd)/bluto /usr/local/bin/bluto
```
Now, you can run bluto directly from anywhere.

## Upgrade Instructions

To get the latest version of BlutoRS, pull the latest changes from the repository:

```bash
git pull origin main
```

Changelog
====
* Version __2.5.0__ (__05/11/2024__):
  * Added Python 3 compatibility
  * fixed regular expressions and packages related issues
  * improved README
  * Changed License to MIT

Legacy Versions
====
* Version __2.4.7__ (__20/07/2018__):
  * Last release by the original author
  * GeoIP lookup refactor
  
* Version __2.3.10__ (__13/01/2017__):
  * BugFixes
  
* Version __2.3.6__ (__14/08/2016__):
  * BugFixes
  * Timeout value can be parsed as argument (-t 5)
  
* Version __2.3.2__ (__02/08/2016__):
  * MetaData Scraping From Document Hunt On Target Domain
  * Target Domain Parsed As Argument
  
* Version __2.0.1__ (__22/07/2016__):
  * Compromised Account Data Prensented In Terminal And HTML Report

* Version __2.0.0__ (__19/07/2016__):
  * Pushed Live 2.0
 
* Version __1.9.9__ (__09/07/2016__):
  * Email Hunter API Support Added.
  * Haveibeenpwned API Support Added.
  * HTML Evidence Report Added.
  * Modulated Code Base.
  * Local Error Logging.
